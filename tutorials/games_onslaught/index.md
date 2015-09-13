---
title: Building the Onslaught! Arena game
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/casestudies/onslaught/)'
readiness: 'Ready to Use'
summary: 'Learn how to use the &lt;canvas&gt; element to create an interactive game with retro-looking graphics.'
tags:
  - Tutorials
  - Audio
  - Canvas
  - CSS
  - Design
  - Graphics
  - Performance
  - Webstorage
uri: 'tutorials/games onslaught'

---
**By [Matt Hackett & Geoff Blair](http://www.html5rocks.com/profiles/#matthackett)**
Originally published Februrary 10, 2011

## <span>Summary</span>

Learn how to use the &lt;canvas&gt; element to create an interactive game with retro-looking graphics.

## <span>Introduction</span>

In June of 2010, it came to our attention that local publishing "zine" [Boing Boing](http://boingboing.net/) was having a [game development competition](http://boingboing.net/arcade/). We saw this as a perfectly good excuse to make a quick, simple game in JavaScript and `<canvas>`, so we set to work. After the competition we still had a lot of ideas and wanted to finish what we started. Here's the case study of the result, a little game called [Onslaught! Arena](https://chrome.google.com/webstore/detail/khodnfbkbanejphecblcofbghjdgfaih).

## <span>The retro, pixelated look</span>

It was important that our game look and feel like a retro *Nintendo Entertainment System* game, given the [contest premise](http://www.boingboing.net/2010/06/14/games-inspired-by-mu.html) to develop a game based on a [chiptune](http://en.wikipedia.org/wiki/Chiptune). Most games don't have this requirement, but it's still a common artistic style (especially among indie developers) due to its ease of asset creation and natural appeal to nostalgic gamers.

![Increasing pixel size can decrease graphic design work.](/assets/public/f/ff/pixels.png)

Given how small these sprites are we decided to double-up our pixels, meaning that a 16x16 sprite would now be 32x32 pixels and so forth. From the beginning we had been doubling-up on the asset creation side of things instead of making the browser do the heavy lifting. This was simply easier to implement but also had some definite appearance advantages.

Here's a scenario that we considered:

    <style>
    canvas {
      width: 640px;
      height: 320px;
    }
    </style>
    <canvas width="320" height="240">
      Sorry, your browser is not supported.
    </canvas>

This method would consist of 1x1 sprites instead of doubling them up on the asset creation side. From there, CSS would take over and resize the canvas itself. Our benchmarks revealed that this method can be about twice as fast as rendering larger (doubled-up) images, but unfortunately CSS resizing includes anti-aliasing, something we couldn't find a way to prevent.



This was a deal breaker for our game since individual pixels are so important but if you need to resize your canvas and anti-aliasing is appropriate for your project, you could consider this approach for performance reasons.

## <span>Fun canvas tricks</span>

We all know that `<canvas>` is the new hotness, but sometimes [developers still recommend using DOM](http://paulbakaus.com/2010/07/19/why-canvas-is-not-an-obvious-choice-for-web-games/). If you're on the fence about which to use, here's an example of how `<canvas>` saved us lots of time and energy.

When an enemy gets hit in **Onslaught! Arena**, it flashes red and briefly displays a "pain" animation. To limit the number of graphics we had to create, we only show enemies in "pain" in the downward-facing direction. This looks acceptable in-game and saved tons of time of sprite creation. For the boss monsters however, it was jarring to see a large sprite (at 64x64 pixels or more) snap from facing left or up to suddenly facing down for the pain frame.

An obvious solution would be to draw a pain frame for each boss in each of the eight directions, but this would have been very time-consuming. Thanks to `<canvas>`, we were able to solve this problem in the code:

First we draw the monster to a hidden "buffer" `<canvas>`, overlay it with red, then render the result back to the screen. The code looks something like this:

    // Get the "buffer" canvas (that isn't visible to the user)
    var bufferCanvas = document.getElementById("buffer");
    var buffer = bufferCanvas.getContext("2d");

    // Draw your image on the buffer
    buffer.drawImage(image, 0, 0);

    // Draw a rectangle over the image using a nice translucent overlay
    buffer.save();
    buffer.globalCompositeOperation = "source-in";
    buffer.fillStyle = "rgba(186, 51, 35, 0.6)"; // red
    buffer.fillRect(0, 0, image.width, image.height);
    buffer.restore();

    // Copy the buffer onto the visible canvas
    document.getElementById("stage").getContext("2d").drawImage(bufferCanvas, x, y);

## <span>The Game Loop</span>

Game development has some notable differences from web development. In the web stack, it's common to react to events that happened via event listeners. So initialization code may do nothing other than listen for input events. A game's logic is different, as it's necessary to constantly be updating itself. If, for example, a player hasn't moved, that shouldn't stop goblins from getting him!

Here's an example of a game loop:

    function main () {
      handleInput();
      update();
      render();
    };

    setInterval(main, 1);

The first important difference is that the `handleInput` function doesn't actually *do* anything right away. If a user presses a key in a typical web app, it makes sense to immediately perform the desired action. But in a game, things have to happen in chronological order to flow correctly.

    window.addEventListener("mousedown", function(e) {
      // A mouse click means the players wants to attack.
      // We don't actually do that yet, but instead tell the rest
      // of the program about the request.
      buttonStates[e.button] = true;
    }, false);

    function handleInput() {
      // Here is where we respond to the click
      if (buttonStates[LEFT_BUTTON]) {
        player.attacking = true;
        delete buttonStates[LEFT_BUTTON];
      }
    };

Now we know about the input and can consider it in the `update` function, knowing that it will adhere to the rest of the game rules.

    function update() {
      // Check for collisions, states, whatever else is needed

      // If after that the player can still attack, do it!
      if (player.attacking && player.canAttack()) {
        player.attack();
      }
    };

Lastly, once everything has been computed, it's time to redraw the screen! In DOM-land, the browser handles this heaving lifting. But when using `<canvas>` it's necessary to manually redraw whenever something happens (which is usually every single frame!).

    function render() {
      // First erase everything, something like:
      context.clearRect(0, 0, SCREEN_WIDTH, SCREEN_HEIGHT);

      // Draw the player (and whatever else you need)
      context.drawImage(
        player.getImage(),
        player.x, player.y
      );
    };

## <span>Time-Based Modeling</span>

Time-based modeling is the concept of moving sprites based on the amount of elapsed time since the last frame update. This technique allows your game to run as fast as possible while ensuring that sprites move at consistent speeds.

In order to use time-based modeling we need to capture the elapsed time since the last frame was drawn. We'll need to augment our game loop's `update()` function to track this.

    function update() {

      // NOTE: You'll need to initially seed this.lastUpdate
      // with the current time when your game loop starts
      // this.lastUpdate = Date.now();

      // Calculate elapsed time since last frame
      var now = Date.now();
      var elapsed = (now - this.lastUpdate);
      this.lastUpdate = now;

      // Do stuff with elapsed

    };

Now that we have the elapsed time we can calculate how far a given sprite should move each frame. First, we'll need to keep track of a few things on a sprite object: Current position, speed and direction.

    var Sprite = function() {

      // The sprite's position relative to the top left of the game world
      this.position = {x: 0, y: 0};

      // The sprite's direction. A positive x value indicates moving to the right
      this.direction = {x: 1, y: 0};

      // How many pixels the sprite moves per second
      this.speed = 50;
    };

With these variables in mind here's how we'd move an instance of the above sprite class using time-based modeling:

    // Determine how far this sprite will move this frame
    var distance = (sprite.speed / 1000) * elapsed;

    // Apply the movement distance to the sprite's current position
    // taking into account its direction
    sprite.position.x += (distance * sprite.direction.x);
    sprite.position.y += (distance * sprite.direction.y);

Note that the `direction.x` and `direction.y` values should be *normalized* which means they should always fall between `-1` and `1`.

## <span>Controls</span>

Controls have been possibly the biggest stumbling block while developing **Onslaught! Arena**. The very first demo only supported the keyboard; players moved the main character around the screen with the arrow keys and fired in the direction he was facing with the space bar. While somewhat intuitive and easy to grasp, this made the game almost unplayable at more difficult levels. With dozens of enemies and projectiles flying at the player at any given time, it's imperative to be able to weave between bad guys *while* firing in any which direction.

In order to compare with similar games in its genre we added mouse support to control a targeting reticle, which the character would use to aim his attacks. The character could still be moved with the keyboard, but after this change he could simultaneously fire in any full 360-degree direction. Hardcore players appreciated this feature but it had the unfortunate side effect of frustrating trackpad users.

To accommodate trackpad users, we brought back arrow key controls, this time to allow firing in the pressed direction(s). While we felt that we were catering to all types of players, we were also unknowingly introducing too much complexity to our game. To our surprise, we'd later hear that some players weren't aware of the optional mouse (or keyboard!) controls for attacking, despite tutorial modals, which were largely ignored.

We also are fortunate to have some European fans, but we've heard frustrations from them that they may not have typical QWERTY keyboards and are unable to use the WASD keys for directional movement. Left-handed players have expressed similar complaints.

With this complex control scheme that we've implemented, there's also the problem of playing on mobile devices. Indeed, one of our most common requests is to make **Onslaught! Arena** available on Android, iPad and other touch devices (where there is no keyboard). One of HTML5's core strengths is its portability, so getting the game onto these devices is definitely doable, we just have to solve the many problems (most notably, controls and performance).

To address these many issues, we began playing with a single-input method of gameplay that involves only mouse (or touch) interaction. Players click or touch the screen and the main character walks towards the pressed location, automatically attacking the nearest bad guy. The code looks something like this:

    // Find the nearest hostile target (if any) to the player
    var player = this.getPlayerObject();
    var hostile = this.getNearestHostile(player);
    if (hostile !== null) {
      // Found one! Shoot in its direction
      var shoot = hostile.boundingBox().center().subtract(
        player.boundingBox().center()
      ).normalize();
    }

    // Move towards where the player clicked/touched
    var move = this.targetReticle.position.clone().subtract(
      player.boundingBox().center()
    ).normalize();
    var distance = this.targetReticle.position.clone().subtract(
      player.boundingBox().center()
    ).magnitude();

    // Prevent jittering if the character is close enough
    if (distance < 3) {
      move.zero();
    }

    // Move the player
    if ((move.x !== 0) || (move_y !== 0)) {
      player.setDirection(move);
    }

Removing the additional factor of having to aim at enemies can make the game easier in some situations, but we feel that making things simpler for the player has many advantages. Other strategies emerge, such as having to position the character close to dangerous enemies to target them, and the ability to support touch devices is invaluable.

## <span>Audio</span>

Among controls and performance, one of our biggest issues while developing **Onslaught! Arena** was HTML5's `<audio>` tag. Probably the worst aspect is the latency: in almost all browsers there's a delay between calling `.play()` and the sound actually playing. This can ruin a gamer's experience, especially when playing with a fast-paced game like ours.

Other problems include [the "progress" event failing to fire](http://code.google.com/p/chromium/issues/detail?id=59372), which could cause the game's loading flow to hang indefinitely. For these reasons, we adopted what we call a "fall-forward" method, where if Flash fails to load we switch to HTML5 Audio. The code looks something like this:

     /*
     This example uses the SoundManager 2 library by Scott Schiller:
     http://www.schillmania.com/projects/soundmanager2/
     */

     // Default to sm2 (Flash)
     var api = "sm2";

     function initAudio (callback) {
       switch (api) {
         case "sm2":
           soundManager.onerror = (function (init) {
             return function () {
               api = "html5";
               init(callback);
             };
           }(arguments.callee));
           break;
         case "html5":
           var audio = document.createElement("audio");

           if (
             audio
             && audio.canPlayType
             && audio.canPlayType("audio/mpeg;")
           ) {
             callback();
           } else {
             // No audio support :(
           }
           break;
       }
     };


It may also be important for a game to support browsers that will not play MP3 files (such as Mozilla Firefox). If this is the case, support can be detected and switched to something like [Ogg Vorbis](http://www.vorbis.com/), with code like this:

     /*
     Note: you could instead use "new Audio()" here,
     but the client will throw an error if it doesn't support Audio,
     which makes using "document.createElement" a safer approach.
     */

     var audio = document.createElement("audio");

     if (audio && audio.canPlayType) {
       if (!audio.canPlayType("audio/mpeg;")) {
         // Here you know you CANNOT use .mp3 files
         if (audio.canPlayType("audio/ogg; codecs=vorbis")) {
           // Here you know you CAN use .ogg files
         }
       }
     }


## <span>Saving data</span>

You can't have an arcade-style shoot 'em up without high scores! We knew we'd need some of our game data to persist, and while we could have used something old-hat like cookies, we wanted to dig into the fun new HTML5 technologies. There is certainly no shortage of options, including Local storage, Session storage and Web SQL Databases.

We decided to use `localStorage` since it's new, awesome and easy to use. It supports saving basic key/value pairs which is all our simple game needed. Here's a straightforward example of how to use it:

    if (typeof localStorage == "object") {
      localStorage.setItem("foo", "bar");
      localStorage.getItem("foo"); // Value is "bar"
      localStorage.removeItem("foo");
      localStorage.getItem("foo"); // Value is now null
    }

There are some "gotchas" to be aware of. No matter what you pass in, values are stored as strings, which can lead to some unexpected results:

    localStorage.setItem("foo", false);
    typeof localStorage.getItem("foo"); // Value is "false" (a string literal)
    if (localStorage.getItem("foo")) {
      // It's true!
    }

    // Don't pass objects into setItem
    localStorage.setItem("bar", {"key": "value"});
    localStorage.getItem("bar"); // Value is "[object Object]" (a string literal)

    // JSON stringify and parse when dealing with localStorage
    localStorage.setItem("json", JSON.stringify({"key": "value"}));
    typeof localStorage.getItem("json"); // string
    JSON.parse(localStorage.getItem("json")); // {"key": "value"}

## <span>Summary</span>

HTML5 is amazing to work with. Most implementations handle everything a game developer needs, from graphics to saving the game state. While there are some growing pains (such as `<audio>` tag woes), browser developers are moving quickly and with things already as great as they are, the future looks bright for games built on HTML5.

Except as otherwise [noted](http://code.google.com/policies.html#restrictions), the content of this page is licensed under the [Creative Commons Attribution 3.0 License](http://creativecommons.org/licenses/by/3.0/), and code samples are licensed under the [Apache 2.0 License](http://www.apache.org/licenses/LICENSE-2.0).