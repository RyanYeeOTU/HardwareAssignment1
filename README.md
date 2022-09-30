# Individual Assignment 1

## GDW Role
I am the technical artist in my group: Celbreak. I will mainly be helping my group create 3D assets, as well as concept art and UI menus; however, I will also help where I can with debugging, and designing mechanics and systems of the game with my other group members.

## Week 1
In week 1, we first imported the assets from a shared google drive provided by the TA. We then began to set up the scene in unity with the basic terrain and player character, followed by setting up the input system with basic actions such as move, jump, shoot, etc. Movement was implemented by editing the scripted provided and attaching it to the player character.; additionally, bullet firing was also added by making a new prefab and editing the player controller script to add force to the rigid body when the shoot action is performed. The animator for the player was setup for the walking and idle animations as well.

## Week 2
During Week 2, we covered what are singletons (one instance of an object), and implemented coin pickups; additionally, we added a score manager, where every time you picked up a coin, the game would output back in the console an increase to the score. An editor mode was then added partially, as we ran out of time; however, we were able to add spawning a prefab, and change cameras from the player camera to an editor camera when toggling between either mode. The action map was updated to include key binds for the editor mode.

## My Customizations
Before discussing my additions, I want to make it clear that I used code from the links provided to assist in the creation of moving platforms and attaching the player to the platform to minimize them falling off the platform; additionally, the base project provided by the TA was used to help with fixing of animations and camera.
I added dodging to the left and right by using similar code that was used for jumping, instead of changing the value of Y, the X value was changed instead, using a positive or negative number depending on the key pressed to change directions. The action map was edited to include these 2 new actions, bound to Z and C, Left and right respectively. 

The moving platforms were created by using delta time and both randomized speed and distance limit for the platform. The platform speed multiplied by delta time allowed for the platforms to move back and forth, which was regulated by using the distance limit and a Boolean to determine whether the platform should keep going or change direction. The player is attached to the platform in another script where a box collider is used as a trigger to check if the player is touching it, if it is, the script will offset the player’s position to adjust to the platform. When the player leaves the trigger, the script is supposed to set the target to none and release the player from the attachment.
Additional Coins were added to some platforms, and by using position constraints, are anchored to the platforms allowing them to move together.

Please check the Word Document for details.

https://answers.unity.com/questions/12083/how-to-get-a-character-to-move-with-a-moving-platf.html
https://answers.unity.com/questions/1605810/obstacles-movement-please-help.html
