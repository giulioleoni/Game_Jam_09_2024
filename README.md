# Warm_Up_Game_Jam
 
This project was made for the Warm up Game Jam organised by [A.I.V.](https://www.aiv01.it/) on 23-27 September 2024.

The theme of the jam was "unstable", and the team consisted of five students or former students (including myself) from A.I.V. 

We were 1 game designer, 2 programmers and 2 graphic designers.

The game was made with Enreal Engine 5.3, and is purely UI. It consists of creating various potions by mixing in the cauldron the ingredients that are available on the shelves. There is a time limit within which to finish the game (even without a timer it is made clear through the movement of the moon and other graphic and sound elements).

The full [gameplay](https://www.youtube.com/watch?v=6nqEMh_2uyo) on YT.

I worked on the main HUD and game mechanics.

It was interesting to work on a game project purely in UI, it allowed me to understand and learn more about the functionalities of the UI of unreal and experience new things I didn't know.

All this combined with the context of the jam, which with the little time and people available, forces you to look for alternative solutions.

## Drag and Drop

It was a bit tricky to do the drag and drop system.

On unreal you need to create a specific object the DragdropOperation

![photo_2024-10-03_14-38-39](https://github.com/user-attachments/assets/8723ee71-69bd-4983-ab11-8fc5ee8883d5)

Next I created two widgets, one is the static image of a pot with many ingredients, and the other will be the image that is shown when you drag one of the ingredients to put it in the cauldron.

When I detect a drag on static image, the operation and the widget to be used as a visual are created

![e](https://github.com/user-attachments/assets/82a9f648-132d-4740-8061-e5ab027f22f7)

Then when I drop something I check that I'm hovering over the cauldron image, only then can I add the ingredient to the potion I am making


https://github.com/user-attachments/assets/549c9b7c-0dca-4406-a8eb-22dee7fea968





## Potions

For potions I created a simple enumerate of ingredients, and potions are defined as arrays of ingredients in the game mode

![Screenshot 2024-10-03 151227](https://github.com/user-attachments/assets/ae7eaf79-df54-4d81-b1c9-3901d5423968)

When a new client appears to ask for a potion, the wanted potion will be randomised by choosing from the three combinations A, B or C. So when an ingredient is added, it will be added to the current potion, and then a check will be made with the desired potion

![image](https://github.com/user-attachments/assets/49bd0ff3-24d8-4b22-bb8c-c42f2df151eb)


## Client

Instead of creating many different clients, I thought of using one widget for the client and changing the sprite radomically each time a potion is completed.

I used the UI animations for the fade in/out effects and also for the client's shake (animation executed when he askes for the potion)



https://github.com/user-attachments/assets/fe7a98c0-8b43-4f43-9042-31d1e994742b



The animation of the cloud (and of the cauldron), on the other hand, is created using a material applied to an image that is made visible or not as required.

The material:

![image](https://github.com/user-attachments/assets/64ae57fc-7c0b-4e46-b512-ce6204dfb555)

## Animations

I chose to make extensive use of UI animations, in addition to the client's fade in. 

I used animations for widget movements and fade in/out effects, for exemple at the beginning there is an animation showing customers outside the window queuing up



https://github.com/user-attachments/assets/f6405b67-4860-4b42-bf3e-501c8bcf4c86

The last few seconds of the game to simulate a redness effect in the scene, I used an animation that slowly made a red image (placed above the rest of the HUD) partially visible

https://github.com/user-attachments/assets/118f20f5-e964-4a5b-84b8-352077834727


