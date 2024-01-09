<h1>Race for the Exit Game</h1>

<h2>Description</h2>
This project is a game that utilizes sprites and animation to produce a fun 2D game using the tkinter module in Python. The goal of the game is to guide the controllable stick figure, Mr. Stickman, to the exit door. To achieve this goal the player will need to navigate Mr. Stickman by running and jumping across platforms until he reaches the exit.
<br />


<h2>Keywords, Functions, & Utilities Used</h2>

- <b>GIMP (GNU Image Manipulation Program)</b> 
- <b>tkinter module</b>
- <b>animate function</b>
- <b>move function</b>
- <b>mainloop function</b>
- <b>collision detection</b>
- <b>key bindings</b>
- <b>photoimage widget</b>
- <b>.gif</b>

<h2>Project Walk-Through:</h2>

<p align="center">
Create game elements: <br/>
Before any coding is done, a few important game elements will need to be created. These game elements include 6 variations of a stick figure, a background, 2 different door images, and 10 different sized platforms. This can be done using GIMP, a free imaging software which allows for the creation of game sprites (moving images in a game). Afterward, we will need to format each image we created into a .gif, so that Python recognizes we would like to use an image along with our code. A critical concept I learned is how important it was to place all the .gifs and code together in the same folder when running any of the code. For simplicity, we can call the folder, ‘Mr Stickman Game’.
<br />
<br />
<img src="https://i.imgur.com/bd99dIe.gif" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create the game canvas: <br/>
Here is where we begin to start creating the game. Firstly, start by importing the tkinter module. Then we will be making a class called ‘Game’ and attaching important objects to this class, such as an initialization function and a canvas for the game. Doing this causes the background that was created in the beginning to be implemented using a mainloop function within the newly created class. In addition, we reference the background image that was created earlier using a ‘PhotoImage’ widget. Lastly, we can give the game a title.
<br />
<br />
<img src="https://i.imgur.com/hEnUZcA.png" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create coordinates and collision detection: <br/>
For this step, we create coordinates for the positions of the earlier created sprites.  The necessary components to use are two sets of coordinates, x and y. Next, we utilize a crucial part of any game: collision detection. This is so the game will be able to tell if any of the sprites have collided with one another. Collision detection also allows Mr. Stickman to be able to run around and jump onto platforms which we will delve into more detail in the next step.
<br />
<br />
<img src="https://i.imgur.com/1DXOFzw.png" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add platforms: <br/>
Now we add platforms. Using the steps prior, we are able to add coordinates and collision detection to the platforms while placing them each in different locations. By using another initialization function as well as a ‘PhotoImage’ widget, we are able to tell python to reference the platform images that are placed in the ‘Mr Stickman Game’ folder. This will enable our images to load into the game. Furthermore, through the addition of a new class, we can add moving platforms to raise the difficulty of the game. This addition also grants us the ability to define which platforms move back and forth horizontally and which platforms remain stationary. 
<br />
<br />
<img src="https://i.imgur.com/Zm38mi5.png" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Loading & binding Mr. Stickman:  <br/>
In this step, we load Mr. Stickman’s image into our game using the initialization function and a PhotoImage widget. We also use the bind function to create keyboard events that will allow our character to run to the right, left, or jump after a certain key is pressed.
<br />
<br />
<img src="https://i.imgur.com/8CaKK2o.png" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Animate Mr. Stickman: <br/>
Now comes the action. Using a few if statements along with the animate function, we link Mr. Stickman’s movement to the previously created key bindings. This creates the illusion of fluid animation for each frame every time the stick figure moves inside the game. Just like the above steps, we make sure to define coordinates for our stick figure which allows it to be able to move around the screen, and it also adds more collision detection among all the sprites in our game. As a bonus, testing our code during this step helps ensure all sprites are working properly according to our code.
<br />
<br />
<img src="https://i.imgur.com/ncWTMeX.gif" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add the exit doors and win the game: <br/>
The game needs a win condition. Also, we need to add the door sprites created earlier by creating code that references the door images and also code that detects when our stick figure has arrived at the door. A bit of extra code helps animate the door to open and close as soon as Mr. Stickman arrives. To finish everything we add an endgame function along with a door object so that our door sprites load properly and so the game knows we have reached the exit. Finally, the project has reached completion, and we have just achieved coding a fully animated game! 
<br />
<br />
<img src="https://i.imgur.com/ZP9vxyr.gif" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
