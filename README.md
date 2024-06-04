# Scratch Tutorial

This tutorial will walk you through how to build a game using Scratch.

The game we will be creating can be played here: https://scratch.mit.edu/projects/1024206125/

## 1. Setup and Adding Sprites
### Accounts

You can work on a project without an account, but you cannot save your projects. So, personally I advise signing up for an account.

If you chose to sign up, cick on the file shapped button.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/8db08655-a743-4b47-971e-a2a3b42afdc6)

Then click to create a new project.
![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/7f9e99f3-2ca6-4ce0-a8ee-14d85ace3246)


### The First Project
![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/d3e03eca-d16c-464f-a655-bb89551cecc8)

The far left are the list of code blocks that can be put together to cause actions in the game.

The center area is where you place the code blocks.

The top far right is the game screen.

The bottom far left contains the list of objects in the game (sprites) and the details about the sprite that is currently selected.

At the top left of the game screen there is a green flag and a red stop sign. Clicking on the green flag starts the game and clicking on the red stop sign stops it.

Blocks can be taken out of the list and placed into the center. Clicking on a block will activate it and cause it to perform its action. When activated, blocks finish what they are doing and then activate the block below them.

The code block area is associated with whichever sprite you have selected. Changing the selected sprite will change the code block area to display whatever code blocks you have given to that sprite.

In the bottom right corner of the sprites area there is a cat's head with a plus sign next to it. Click on this (or hover over it and then click on one of the options) to add a new sprite into the game.


## 2. Character Movement
### The START block:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/d12b0ba7-1c13-4b18-a838-363c074e9c06)

The start button triggers the code attached to it when the game starts. Note that it has a puzzle peice shape (bump) on the bottom. Every block that has a shape like this on the bottom can have another block attacked to it if that other block has a puzzle peice shaped dent in its top. Any block that does not cannot.

### The DIRECTION blocks:

We want the ship to follow around the mouse. Or in other words, we want the ship to face the mouse and then move forward.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/7d840843-daf3-4f19-a125-baf31244e8af)

The first block makes the sprite point in a specific direction.

The second block makes the sprite point towards a specific object (another sprite or the mouse).

90 degrees is right, -90 degrees is left, 0 degress is up, and 180 degrees is down:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/4f0257a5-32d5-4ad3-9713-08bf50c96a2f)

### The FOREVER block:

We want the rocketship to always be looking towards the mouse, so we surround the direction block with a forever block.

The forever block activates what is inside it over and over in a loop.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/6b8487b3-32ac-4a52-904e-9135974cb616)

Now it will always point toward the user's mouse.

### The MOVE block:

This block will cause the sprite to move in the direction it is pointing. How much it moves depends how many steps it is told to take each time it moves.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/b412a6d7-76b5-4e62-bb16-027c017f5ae1)

Putting everything we have done so far together, we get this code. It make the roketship move towards the user's mouse.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/97eac183-84b7-4a7b-8743-5ed6fe742806)

### Troubleshooting:

But there are two problems. One, the rocketship flys sideways and two, the rocketship freaks out when it gets to the mouse.

To fix the rocketship flying sideways, we can simply turn it after it moves. If you turn it before it moves, then it will fly circles around the mouse. This is because it is now looking at the mouse, then looking to the side, and then moving.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/6ac82bef-def8-4286-9323-6297e58c17c7)

The rocketship is freaking out when it hits the mouse because it is overshooting the mouse and then flipping around to go back over and over. This causes it to look like it is flickering. To fix this, we simply prevent it from moving on top of the mouse. To do this, we only have it move when it is a certain distance away from the mouse.

### The DISTANCE DETECTION block

To code this, we must detect how far away the mouse is and only run the code we have written so far when the distance is greater than the distance we want it to be away.

To determine the distance between two objects, we use the distance to block and set the target to the mouse.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/f795655a-47dc-4c17-ab63-ea47771c69a1)

### The GREATHER THAN block

To check to see if it is greater than the distance we decided on (25), we use the > block (operator). If what you put in the left side is greater than what you put in the right side, then it says true. If it is smaller it says false. (Click the > block when it has two values to see what it says.)

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/b4483bd6-ae1e-4064-93be-8e66165edcdc)

### The IF block:

Then we add the if block. It surrounds other blocks like the forever block, and only runs the code inside it if what you place in the diamond slot is activated.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/35a591c8-5657-4761-8dd2-507cd7d914b7)

Note that some things have diamond slots and some things are diamond shaped. Some things have circular slots and some things have circular sides. Anything with a diamound shape can fit in anything with a diamond shaped slot while anything with circular sides can fit in any slot with circular sides. However, a diamond shape canot fit in a circular sided slot and neither can a circular sided shape fit in a diamon shaped slot.

### Finished movement code:

Putting this together you get the final code that makes the ship follow the mouse around:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/f1f1cef3-f111-46be-8151-efa33bd68529)

### Animation

Currently the ship moves around, but it does not really look like a ship flying through space. To make it look more like one, it needs animation. The rocketship sprite comes with five costumes. A costume is how the sprite looks. The fifth is for when the rocket is landed so we don't need it right now and will delete it by clicking the trash can in the upper right corner.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/c761abeb-07ae-4480-ad48-dd8b8c150418)

The other costumes are of the rocket flying through space. To add animation, we want to have the sprite switch to each of these costumes, one by one.

### The COSTUMES blocks:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/71dac20e-9e32-4ee1-9cf3-80e96fd5687d)

The first block allow us to change a sprite into a specific costume. The second will simply change the sprite into the next costume on the list. If the sprite is wearing the last costume on the list, it will change the sprite into the first costume on the list. We want to always be alternating between all the cosumes on the list, so we will use the START and FOREVER blocks to so.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/8bff28a9-4e15-43dc-9ce8-257a3c77df18)

### Troubleshooting:

The rocket is spinning too fast. To fix this we need to wait a little while after every time we change the sprite's costume.

### The WAIT block:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/5c550877-4ecf-4a00-9b0d-fc828e1d1358)

The WAIT block will stop running the code for however long you tell it to (in seconds). You can give it a decimal if you want it to wait a part of a second. I have found that 0.2 seconds is a good amount of time to wait between changing costumes.

### Finished animation code:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/1e9cbadc-f835-4b10-b78b-17cf8852f8e6)

Now the rocket looks like it is flying through space, instead of just sliding across the ground towards the mouse.


### Extra

If you want the ship to fly faster when the mouse is further away, you can do this:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/42cda58b-d0fc-41d8-9ddf-0c669c7ccf0c)


## 3. Enemy

Now we want an enemy that flies towards the rocketship. Since this is basically the same as the move toward mouse code, we can copy and paste that code and make the limited required alterations.

First create a new sprite by cicking the cat plus button in the bottom right corner of the screen and selecting the search bar.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/a6f8682b-8394-4819-84e5-bbf58f3197da)

I desided to use the dragonfly as my enemy but you can chose whatever you want.

### Enemy movement code:

Grab the code for movement that you already wrote and drag it on top of the new enemy sprite. Then drop it. A copy of the code blocks will appear in the enemy sprite. Now we need to change everywhere the code says "mouse-pointer" to "Rocketship". We also want to make the enemy a little slower than the rockethip so change the number of steps it takes each time to 2.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/e5138b02-5e29-4ff9-bd3a-1b9cc064d298)

### Enemy animation code:

If the enemy sprite you chose has multiple costumes like me, you may want to copy over the animation code from the rocketship to the enemy sprite as well.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/1e9cbadc-f835-4b10-b78b-17cf8852f8e6)

### Troubleshooting:

With the current setup, there will only ever be one enemy. We want there to be a new enemy created every second or so. We could create more enemy sprites manually, but that would not solve our problem if more than the number of sprites we coppied are need to be on the screen at the same time. To fix this, we can use a block to create a copy-paste of the enemy every second.

### The CLONE blocks:

To create a copy of a sprite, we clone it. The new clone is exactly the same as the sprite as it is when the clone is created but afterwards it is entirely independant. Actions the clone takes does not affect the original and vice versa.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/3608a403-881a-4492-9c83-96247ad02ff7)

The second block allows the sprite to create a clone of itself.
The first block works just like the START block but activates when the clone is created instead of when the game starts.
The last block deletes this copy of the sprite.

To make the game spawn new enemies, use the START block, the FOREVER block, and the WAIT block to make the sprite constantly create clones of itself.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/ed42fd73-82d4-48cd-8849-dd5ba06f1209)

### Troubleshooting
There are currently two problems. Only the original sprite is moving and the original sprite is visible.
Only the original sprite is moving since only the original sprite existed when the game started. Thus, the START block was activaed only for the original sprite. To make all the sprites move, switch the START block out of the WHEN I START AS A CLONE block. Now all the clones will move.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/8eb2194c-18de-49e4-abea-0e80cdc96192)

We want the original sprite to be invisible, copying itelf while the clones are the enemies that are actually going for the player. To make this happen, we use the HIDE block

### The HIDE and SHOW blocks

This block hides (makes invisible) or shows (makes visible) the sprite.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/698abf2e-1fa1-46f6-a22b-f83306e41006)

We want to make the original sprite invisible (hidden) and the clones visible (shown). To do so we should hide the sprite after the START block.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/1eb50933-e8fd-4064-8d59-bf7baf9d1d78)

But now, since the clones are copies of the original sprite, they are hidden too. To fix this, we simply show the sprites after the WHEN I START AS A CLONE block.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/22bf6ca3-d5c4-4365-926c-2e0c1e958aff)

### Troubleshooting
Every clone appears in the same place, but we want them to spawn randomly, anwhere on the screen.

### The GO TO block
To fix this, there is the go to block. This block can teleport the sprite (or clone) to another sprite, the mouse, or a random location on the screen.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/19d87b1e-f127-47ac-999f-71d5f40268dd)

Add this block below the WHEN I START AS A CLONE and before the SHOW block. This way, a new clone is created, it teleports to a random location while still invisible, then becomes visible, and then starts moving towards the rocketship.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/37577070-4214-474b-b736-449be315a1d8)

### Troubleshooting
There is a chance that a clone of the enemy sprite will appear right where the rocketship is located. This would feel unfair to the player who is trying to not touch any enemies. To fix this, we can have the sprite repeatedly teleport to random location and if it is too close to the rocketship, try again.

### The REPEAT UNTIL block

We already know that we can find how far away something is using the DISTANCE TO block and check if that distance is within a certain size using the > block.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/9d52a885-f689-40c8-bfc9-beb31c24bc4b)

The REPEAT UNTIL block activates the blocks within itself over and over just like the FOREVER block. The diference is that once the diamond shaped block in its diamond block says "true". It stops activating its blocks and and allows the block after it to be activated.

In our case, we want to have the new clone keep teleporting until it is at least a certain distance away from the rocketship.

### New clone movement code

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/2bb15292-26c5-4eec-a44b-75921f6b5c0b)


## 3. Enemy has hit the ship

In order to detect if the enemy has touched the rocketship. We can detect when the rocketship has touched an enemy.

### The TOUCHING block

This block says "True" if the current sprite is touching the selected sprite (Dragonfly here).

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/dec99073-d259-4437-bb38-0156b7368f70)

We want the game to stop once the rocketship, so from when the game starts, we can wait until a enemy touches the rocketship and then stop the game.

### The WAIT UNTIL block

This block will wait to activate the block below it until what was put in the diamond shaped slot says "True".

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/8e2293ad-ab00-4629-bcf8-a3ce14ebc20e)

### The STOP block

This block will stop other blocks from activating. This can be done for every block in the game, every block in the sprite, or every vertical line of blocks (called a script) other than the line the STOP block is in. In our case, we want to stop everything when the rocketship is hit, so we will set the block to stop all.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/e998d5ff-271c-4db5-8364-eae040d3aa7e)

### Health

What if we want the rocketship to need to be hit multiple times before the game is over? There are two ways to do this.

We could use the WAIT UNTIL block multiple times. In order to do so, we need to give the player of the game a moment to get away from the enemy that just hit them or the script will complete every WAIT UNTIL block with what looks to a human eye as a single contact with an enemy. To do this, one would use the WAIT block and set a small seconds value. This makes the rocketship invunerable for a little while after getting hit which is generally considered better game design anyway.

Or, what we will do, is use a variable so that we can easily display during the course of the game how many hits the rocket can take before the game is over.

### Variables

To create a variable, select "Make a Variable", type a name, and then click "OK".

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/c236ed0f-8357-4f33-b542-e946f9ffad8c)

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/c57ed4b3-39ed-4764-9938-428209709a4d)

The variable we will make is called "Health".
Variable means able to change. A variable is like a nickname for an object but you can change that object to be whatever you like. At first we are going to set that object to be the amount of health that the rocketship has at the beginning of the game, and then as players get hit by enemies, we will change that that variable to be their new lower health value. When they are out of health, we end the game.

To do this use a START block and then set the variable "Health" to 5.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/da8db074-d221-4099-8180-7bccdc6dc258)

Now, use the REPEAT UNTIL and WAIT UNTIL blocks to detect when the rocketship has hit an enemy and then change the health by -1. Put a = operator in the REAPEAT UNTIL and have it check to see if "Hearts" is equal to zero. After the REPEAT UNTIL add the STOP block to end the game.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/e64b2667-a8d5-4459-af2a-03f3d293ef3e)

Now, to make the variable visible to the user, click the box next to the variable in the sidebar.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/19cc6aa3-6543-4028-994d-923b0f2fc744)

### Extra:
You can use a similar system to give the enemies health. Just be sure to select "For this sprite only" when creating the variable so that each of the clones has independant health.

# Congratulations
If you have gotten here, you techincally have a complete game. Try to survive as long as you can running away from the enemies. If you would like to stop here, in the pannel on the left side, go to sensing, and check the box near the bottom of the section next to the text "timer". This will give you a high score you can play for.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/7c615d2b-1a3a-4885-8447-1ce00ff7bdd3)

However, there is much more that can be added to improve the game and make it more like the one I showed at the beginning. There are several more sections to come if you would like to keep working on the game.

## 5. Shooting

We want the roketship to be able to fire. It always helps to be overly specific what you want to do when programming, even in scratch. So more specifically, we want to be able to press a button and a projectile fires out the top of the screen, moves forward for some distance, destroying any enemies that the projectile touches, and then after a certain distance the projectile goes away.
Since, just like with the enemies, we don't know how many of them there will be, we will need to use clones again.
First create a new sprite.

### The WHEN KEY IS PRESSED block:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/6ad6a256-41d4-4193-a9a8-abe90b3dbaf0)

This block is like the START block except that it activates when the player presses a specific button.
Choose a button you want to be the fire button and create a clone when the button is pressed. Then have that clone teleport to the rocket, face the same direction it is facing (towards the mouse pointer) and then move forward for the distance you want and then delete the clone. Since the projectile will teleport to where 10 steps ahead would be instead of taking each individual step, you will need to have it move part of the way several times via a REPEAT block.

### The REPEAT block:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/e8d1b349-d85c-45ab-b579-c8d6d319b32a)

This block is just like the forever block except that it repeats its contents the number of times you give it instead of indefinitely.

### Firing projectile code:

The scripts you create should include all of the elements of the examples below.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/98c3c007-f10e-4f12-a3a0-a3fb92dd3d83)

### Destroying enemies:

Now add to the enemy a script that deletes it when it touches a projectile.

The script should look something like this:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/21b2ecf1-d14c-443d-83a9-cafe42bcc589)

## 6. Title screens

To make the game more polished we should add an title screen with the title of the game and a game over screen at allows you to play the game again. To do this we want to change when the game starts from the moment the green flag is pressed to when an on-screen button is pressed. The simplest way to do this is with messages.

### The MESSAGE blocks:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/cef1a1a2-3e7d-4be1-990b-9558e6c65be8)

The first block is like the START block but activates when it receives a message.
The second block sends a message to all sprites.
The third block sends a message to all sprites and then waits until the message is received.

To make the game start when a button is pressed, we can simply have that button send a message and then replace all our START blocks with RECEIVE blocks so that the game starts when the message is received by all the sprites. The same message can be sent on the game over screen to allow the user to restart the game.

Create a new sprite for the title screen. When the START block is activated, show the screen. When the CLICKED block is activated, hide it and broadcast the start game message.

### The CLICKED block:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/431ec697-ea30-4f9f-90ed-c9016e69619e)

The first block is like the START block but activates when this sprite is clicked.

### Game over screen:

Create a new sprite for the game over screen and copy the script with the CLICKED block into it.
Now we need to know when the game is over.
Replace the STOP all block in the rocketship with a BROADCAST block that sends out a "game over" message.

### Stop the game:

Add a RECEIVE block that receives the "game over" message and deletes the clone to everything that creates clones.
Add a RECEIVE block that receives the "game over" message and hides the sprite to everything else.


## 7. Sounds/Background music

Despite seeming like a small part of a game, music and sound can turn a good game into a great one.

### The SOUND blocks:

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/5285f1cd-02aa-41a2-9906-72d58028a83b)

The first block plays the given sound and then only after the sound has finished playing activates the block below it.
The second block plays the given sound and then imediately activates the block below it.
The third block stops all currently playing sounds for all sprites.

### Sounds tab:

Adding a sound works just like the costumes tab. Click the bottom button and you can choose a sound, record a sound, or upload your own sound.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/9ad4f4d3-24ef-453d-b8ac-5897334844b6)

To add some background music (I chose "Space Ambience" for my music), go to the start screen sprite you created and add a script that once the START button was pressed will play music forever if a variable is set to true. Add a script that sets the variable to true when your "start game" message is received and another that stops all sound and sets the variable to false when the "game over" message is received.

The result should look something like this.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/ee7b4ee9-b11f-4cde-8b86-2c28b49de80c)

### Troubleshooting

Currently the music is very loud.

### The VOLUME blocks

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/aeb49148-9ce0-4f98-bd97-8e81ef75dcce)

These blocks let you change, set, and see the volume. The volume you set only applies to the current sprite. If your music is too loud, you can turn it down by decreasing the percent. And if too loud, you can increase it.


If you want to give the player the option of what volume they want for the music, you can create a variable for it and then constantly set the volume to that variable. Then 
click the check box next to the variable you craeted. A display will pop up on your screen over the game. Double tap that rounded box to change its mode. One of the modes give the player a slider they can use to change the value of that variable and thus the volume of the music.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/f6a70fa9-52c7-4dc2-a16b-b9a25c95ef0b)

## 8. Powerups

Many games like this have powerups. Implementing them is simply a combination of scripts that we have used before. We want to start with a simple collectable that will give the player an extra heart. To do so, we have it randomly spawn clones like the enemies do, go to a random position like the enemies do, increase the player's hearts when it touches the rocketship, and have the clones delete itself when the game is over.

Here is an example of how scripts to do this.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/804316f6-706f-4f47-a98f-944bee8429fb)

## 9. Explosion

I want to have an explosion go off when the player destroyes an enemy or when the rocketship is destroyed by an enemy. To do so, you need to spawn a clone every time an enemy or the rocketship is destroyed and teleport that clone to the location where the enemy was. To do this, we can set a variable to the position of where whe want the explosion to occur whenever we want it to occur. Then when the clone can be spawned, teleported to that position and then set the variable back to "False".

### The GO TO block

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/ffe7bc91-2ac3-41f3-a7eb-f62876c31add)

Teleports the sprite to a specific position. The x value is how far the sprite is from the center horizontally. If the x value is positive, the sprite is right of the center, if the x value is negative it is left of the center. The center has a value of 0. All the way right has a value of 240, all the way left has a value of -240.
The y value is how far the sprite is from the center vertically. If the y value is positive, the sprite is up from the center, if the y value is negative it is down from the center. The center has a value of 0. The top has a value of 180, all the bottom has a value of -180.

### The CURRENT POSIITION blocks

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/d0e03c82-122d-4a5b-9caf-b1559de51c9f)

Says were the sprite currently is.

Since there is no explosion sound effect, I created one by playing two sounds at once and changing the pitch.

### The SOUND EFFECT blocks

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/e1715e2a-eea4-4d6a-bf12-30750f50410d)

These blocks allow changing how sounds sound. You can change their pitch or make them sound like they are coming from the left or the right.

### Example of explosion scripts

Here are the scripts I wrote to make the explosions work. Yours should be similar.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/a09a04c2-f626-434a-8f10-810e5266b9a3)

In the explosion sprite.

![image](https://github.com/JarodSGilliam/library-scratch-tutorial/assets/38574399/fe04635d-8309-4816-8ad4-69e48ffba003)

In the enemy sprite.

## 10. Expanding the game from here

To make the game more interesting, you could add differnent types of enemies or powerups. Both of these can be done by applying what is described above.

I advise just playing around with it. Scratch is ultametely a game in and of itself and the best way to learn programming as a whole is just to mess around with it.
So come up with interesting game ideas and give building them a shot. I can't wait to see what you make!
