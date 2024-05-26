# library-scratch-tutorial

## 1. Setup and Adding Sprites

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


## 2. Enemy Movement
## 3. enemy touching ship
## 4. shooting
## 5. background
## 6. title screen
## 7. sounds/background music
## 8. pickups
## 9. explosion
## 10. enemy health
