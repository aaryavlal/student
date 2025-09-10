---
layout: base
title: Background with Object
description: Use JavaScript to have an in motion background.
sprite: images/platformer/sprites/plane.png
background: images/platformer/backgrounds/airport.png
permalink: /background
---

<canvas id="world"></canvas>

<script>
  // Grab the canvas from the page and set up drawing context
  const canvas = document.getElementById("world");
  const ctx = canvas.getContext('2d');

  // Create image objects for the background and the player sprite
  const backgroundImg = new Image();
  const spriteImg = new Image();
  backgroundImg.src = '{{page.background}}'; // Set background image source
  spriteImg.src = '{{page.sprite}}';         // Set sprite image source

  // Wait for both images to load before starting the game
  let imagesLoaded = 0;
  backgroundImg.onload = function() {
    imagesLoaded++;
    startGameWorld();
  };
  spriteImg.onload = function() {
    imagesLoaded++;
    startGameWorld();
  };

  function startGameWorld() {
    // Only start if both images are loaded
    if (imagesLoaded < 2) return;

    // GameObject is a base class for anything drawn on the canvas
    class GameObject {
      constructor(image, width, height, x = 0, y = 0, speedRatio = 0) {
        this.image = image;      // The image to draw
        this.width = width;      // Width of the object
        this.height = height;    // Height of the object
        this.x = x;              // X position
        this.y = y;              // Y position
        this.speedRatio = speedRatio; // How fast it moves, relative to game speed
        this.speed = GameWorld.gameSpeed * this.speedRatio; // Actual speed
      }
      update() {} // Placeholder for movement logic
      draw(ctx) {
        ctx.drawImage(this.image, this.x, this.y, this.width, this.height); // Draw the image
      }
    }

    // Background scrolls to create a moving effect
    class Background extends GameObject {
      constructor(image, gameWorld) {
        // Fill the whole canvas with the background image
        super(image, gameWorld.width, gameWorld.height, 0, 0, 0.1);
      }
      update() {
        // Move the background to the left, looping it for endless scroll
        this.x = (this.x - this.speed) % this.width;
      }
      draw(ctx) {
        // Draw two backgrounds side by side for seamless scrolling
        ctx.drawImage(this.image, this.x, this.y, this.width, this.height);
        ctx.drawImage(this.image, this.x + this.width, this.y, this.width, this.height);
      }
    }

    // Player is the object you control or animate
    class Player extends GameObject {
      constructor(image, gameWorld) {
        // Shrink the sprite to half size and center it
        const width = image.naturalWidth / 2;
        const height = image.naturalHeight / 2;
        const x = (gameWorld.width - width) / 2;
        const y = (gameWorld.height - height) / 2;
        super(image, width, height, x, y);
        this.baseY = y; // Store the base Y position
        this.frame = 0; // Used for animation
      }
      update() {
        // Make the player float up and down using a sine wave
        this.y = this.baseY + Math.sin(this.frame * 0.05) * 20;
        this.frame++;
      }
    }

    // GameWorld manages everything: canvas, objects, and animation
    class GameWorld {
      static gameSpeed = 200; // Controls how fast things move
      constructor(backgroundImg, spriteImg) {
        // Set up the canvas size and position
        this.canvas = document.getElementById("world");
        this.ctx = this.canvas.getContext('2d');
        this.width = window.innerWidth;
        this.height = window.innerHeight;
        this.canvas.width = this.width;
        this.canvas.height = this.height;
        this.canvas.style.width = `${this.width}px`;
        this.canvas.style.height = `${this.height}px`;
        this.canvas.style.position = 'absolute';
        this.canvas.style.left = `0px`;
        this.canvas.style.top = `${(window.innerHeight - this.height) / 2}px`;

        // Create the background and player objects
        this.objects = [
         new Background(backgroundImg, this),
         new Player(spriteImg, this)
        ];
      }
      // The main animation loop: update and draw all objects
      gameLoop() {
        this.ctx.clearRect(0, 0, this.width, this.height); // Clear the canvas
        for (const obj of this.objects) {
          obj.update(); // Move or animate
          obj.draw(this.ctx); // Draw to canvas
        }
        requestAnimationFrame(this.gameLoop.bind(this)); // Repeat!
      }
      // Start the animation
      start() {
        this.gameLoop();
      }
    }

    // Create the game world and start the animation
    const world = new GameWorld(backgroundImg, spriteImg);
    world.start();
  }
</script>
