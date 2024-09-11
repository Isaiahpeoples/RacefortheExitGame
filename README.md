<div align="center" id="toc">
  <ul style="list-style: none">
    <summary>
      <h1> Race for the Exit Game </h1>
    </summary>
  </ul>
</div>

<h2>Description</h2>
This project is a game that utilizes sprites and animation to produce a fun 2D game using the tkinter module in Python. The goal of the game is to guide the controllable stick figure, Mr. Stickman, to the exit door. To achieve this goal the player will need to navigate Mr. Stickman by running and jumping across platforms until he reaches the exit.
<br />
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
<h3 align="center">Create game elements:</h3> 
<p align="center">
Before any coding is done, a few important game elements will need to be created. These game elements include 6 variations of a stick figure, a background, 2 different door images, and 10 different sized platforms. This can be done using GIMP, a free imaging software which allows for the creation of game sprites (moving images in a game). Afterward, we will need to format each image we created into a .gif, so that Python recognizes we would like to use an image along with our code. A critical concept I learned is how important it was to place all the .gifs and code together in the same folder when running any of the code. For simplicity, we can call the folder, ‘Mr Stickman Game’.
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=58e435ad-c2a5-430f-87e8-a5228d4f246b&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDMzMDUifQ.jzasMfHKdEpFtyG3TNYBHg4ns_fteovd7inxX7zVlh7ma5smAtdeaUhsuXE71tSuvDImaCKfLjhdDxvebubmIHqr94WAAtSJU4t0-35fN1d-MUF6l5tPXcR-ITGXCc7FhG51cxoayviYsjCWpXEiiAnNFFhazFhJopAY8pUWgO710LRI6a56FZKGzu1sPVYSgdlNMawxs8Ix2I9KqhdTBTwsXKy_7tCbMSQwX0BuCyt-16bVKCJwjYUKaV7ds9cwwl7mPPwTYief0bJls_11w9mAMQPhu3AwAeRw85XsurAA_51Wj6Jq0YajP6Kir_VluI16ScxyNxUTzVkf78ousUg2o3oWD11uaZ40EAca7gJ2Uql9bf81cp6wjgGoGHBtTFjZiqsh5YbTgNnKk25AABHOtbaEJA560nOA6EYnKgU._x-RnG7xLG79_6xlwepvdTZkm3Cwhv93z75j9UjyKI0&ApiVersion=2.0" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Create the game canvas:</h3>
<p align="center">
Here is where we begin to start creating the game. Firstly, start by importing the tkinter module. Then we will be making a class called ‘Game’ and attaching important objects to this class, such as an initialization function and a canvas for the game. Doing this causes the background that was created in the beginning to be implemented using a mainloop function within the newly created class. In addition, we reference the background image that was created earlier using a ‘PhotoImage’ widget. Lastly, we can give the game a title.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YNAENRVQTTSHVFK6DGE5BEZT6VL%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.yZrnjXcYL2KwyscAQIe7OVe3o5Kh0MEYvPIkjSBtDl5rnPY6_rbVe0HDcT3xREjlDUm18xJ1EU7r-3UR-1lLLMDABDR0Qiwa7khSx7YTTHVwgpDCqOeyNvTrMWrtWbhPPfVvkgkBYfalpjVGkK2MGLe4-bhMm8iZEq2iTdCeHAhAH68Ecm4QJyKllSAmHuOvcqN0mloH6oWHX45bC8qIu6tDGq89RoWDujgCiQtuPRRNji0NXFDllBUMPFVWpCot5axPpRos6bSi1Zcs7Qj6q-oDfX-GchYP7YUAAW26xGT68ddPrdNXqYELkY1UwJkBvZb0Y4JkwmABv0Y0Tbnx1p9wSCkZ1aw7_gb12Fn-NA6123tYTnaCaC_i80uYy3Cz.CccoyXa_lloNyPlZsJsvjLsqRgi5RlLKUAv_vU-RL5o%26version%3DPublished&cb=63861625196&encodeFailures=1&width=498&height=495" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Create coordinates and collision detection:</h3>
<p align="center">
For this step, we create coordinates for the positions of the earlier created sprites.  The necessary components to use are two sets of coordinates, x and y. Next, we utilize a crucial part of any game: collision detection. This is so the game will be able to tell if any of the sprites have collided with one another. Collision detection also allows Mr. Stickman to be able to run around and jump onto platforms which we will delve into more detail in the next step.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YKHDN2G3IV7PVEICASVXDUPNBAC%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.a0a1g87nl3wlQiFbFLVQZkACa45p92hxYrowWnWxY6uOZPBQdUGSzz2x3m4343ZdIzn9eWnn8nSefR8Y_6kTtOM578GzPxB3-SBXIg_bfWP-LAEj6_gLTPcrHtqVxl6TlIxVtD7hbLDLsvqn0zQZ9E9F_TRLRKyf6ZKy46GlU84NvQ213qWLyDqYqSPe16zhnyU3x3TUOlSXbq-5W7NGjDB45O4QfsB-RIqON6Y7QomThrRORNhBGKJ3IO8fqzMV-PjIfowYZvwQLuPdPTPzqKwRCiSYOECLt29O1oW5q3uyJxn44_3zwuUrcah1_FuLll3XbeC89-_GvjSvfaHYi1US-hrLSoUIZNfHmpvV7WNp8IVMkAcHziwnxUihvPMZ.dTPtnpU1FyUQfDBBsh8wMwE9QDiNpjWzCFybEjQsgyY%26version%3DPublished&cb=63861625211&encodeFailures=1&width=1600&height=814" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add platforms:</h3>
<p align="center">
Now we add platforms. Using the steps prior, we are able to add coordinates and collision detection to the platforms while placing them each in different locations. By using another initialization function as well as a ‘PhotoImage’ widget, we are able to tell python to reference the platform images that are placed in the ‘Mr Stickman Game’ folder. This will enable our images to load into the game. Furthermore, through the addition of a new class, we can add moving platforms to raise the difficulty of the game. This addition also grants us the ability to define which platforms move back and forth horizontally and which platforms remain stationary.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YOITE5TJTAOPBGIH2E4OMXVD74Q%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.mXBmhTFRIZeDqOI3MoYol7O9Z0zEdy0jnLNOM9cxna0hXC28jC34ZpnAwGvF07Ax4vUgB66sCsFj5Fspz5UDZrVHXIFjCiw_AQG_7DanIuwgFUADsEbzQzJ00ZX7xe2IrNJuXc48qbfOjXmIC4sw12ZHog1dapyMeywbYlFgSDOzZUW1YBbXqdfCncFEIp38XaiWyrq39ofLmt8AJQv8L7YzSDsQs0NN1-31W-0-dTVsnJEHl2bJD2y2LrsRv2VKm_Dw0Vp7QAg5MNTfHSiKX_0SOwgadHiERVZ9Z64o1En2VPUOtYEjEqzRqnam-i48j9HiUBh6NrV4CVA8UveyLA5hCuZY1IP8QWgj5CAfrKrbEwdY8xCrQBQ6vyCjQN9I.MkwS570h0uTy4jDAmIIouB3j-8sg3djIJ4-_bC_eqS0%26version%3DPublished&cb=63861625230&encodeFailures=1&width=502&height=532" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Loading & binding Mr. Stickman:</h3>
<p align="center">
In this step, we load Mr. Stickman’s image into our game using the initialization function and a PhotoImage widget. We also use the bind function to create keyboard events that will allow our character to run to the right, left, or jump after a certain key is pressed.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YJCJFUKEK5MTJCJ6O4KVRLL54UN%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ._a8HuWXFE1tMa69bMsBkFF_umccwVLeIgKLOfgHIzVaRfWFEg65hBsoThGqX06K5PJYgrjc2bNcFnku74Kz1o4p5t3vTou0ofmfwHYEMS_GsDym03GXbo7sb9dmXz42dJ4zF4twbDmm-HDTW2gRPbfebuiRGfotMmb89ELvzwZh7UwsYoog8__6DNEe3nm9f6JoYsPZoFGC9wQ8Lode_dsCqrnpm_wBQAV1j5CM9gtzB3eNcAXGR65vLR8r2NQWH3Zsh06ibRClqksotBOPNa2vO2YLEJt0c83XP3zV2m3yHVO62AH1W2ZzEs3EOYYfO2jykjx_c18QRCXogjkiSO1fH729kN-qgOHFqK0FnbKt4cUzUWgn6hu4yIPcXwwBi.n3GxaY2lQMykHY55hFZuRw7XcNeJl_sCceVIua9GA24%26version%3DPublished&cb=63861625247&encodeFailures=1&width=1131&height=824" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Animate Mr. Stickman:</h3>
<p align="center">
Now comes the action. Using a few if statements along with the animate function, we link Mr. Stickman’s movement to the previously created key bindings. This creates the illusion of fluid animation for each frame every time the stick figure moves inside the game. Just like the above steps, we make sure to define coordinates for our stick figure which allows it to be able to move around the screen, and it also adds more collision detection among all the sprites in our game. As a bonus, testing our code during this step helps ensure all sprites are working properly according to our code.
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=4a9603cd-03c0-48ca-99e5-4d3eadf1eedc&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDMzMDUifQ.J4ZsTlCKPs77adq_B116b_jYGe0MH6A7J9PMddKFFbT7bxf08GUbdnV7E2hoiclsXzjiP5qhjmM--23aVVnRP4oa0upsXA4mzfe30AMt30vbzdSQDZWXXEEOaT3E5JC6ajdSJOdnQW6MWaGMY4T6uEQbPiYXUkLkVNy7xWaWm3CBADqMCtefOaH2NB2sA_twncJbgYqLfxPlwFe1v46eaJZOFjgUaStxkk713mPTwMDvP01s0iy2uhW4DbIV-Ins10TC822Jybszh-9zj7d7pVzFLBJdQ3aJDmp0Myfoywq52JZq2Obq1NgbnFOSuwHk79fruoVbtRfH3GiVHypDlL-68k-HVEf0TlYEFq3nrgaDkfJJIUd0dnTfwPR_iur6Ce7dphKKixHYWrcqxL0WCg1hjuwbNKC8jtbTD6M8Gmg.L6VBM1Mcu_MCuTEiRGJKmyA2IEmBE41ctyYZ-4oPWOU&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add the exit doors and win the game:</h3>
<p align="center">
The game needs a win condition. Also, we need to add the door sprites created earlier by creating code that references the door images and also code that detects when our stick figure has arrived at the door. A bit of extra code helps animate the door to open and close as soon as Mr. Stickman arrives. To finish everything we add an endgame function along with a door object so that our door sprites load properly and so the game knows we have reached the exit. Finally, the project has reached completion, and we have just achieved coding a fully animated game! 
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=173821c3-d51e-43c4-a3cd-5b7ee4ccf01d&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDMzMDUifQ.jONT-IL3rhm0G5DLU0TWsQPvRolmBB2UBvyZ2z7D0zhHwkbs7jnl0v1VtxsqcUAhNCcDUH2P2LRTKy6S3S16n225JOKIotJ9piJL5_4M1-CcVRW57wSKpiqK0Lr73cOcnnY3kCyPBsRR5H2s6S2KakkxT3yvi1Nvy9Cm5xLiM6__mtT8V_H-Y37AvtTuUCLE7_zK5pUiaeXuippk19nDZ5Okk-TAJrevAqwMIhlFCn058XyqQKEyRGntNCNTZs3cV8Y1rRLeRJx8mF-KWZWokpiDsAtWwY7QNJLoQP-5hzQ6ajCdFJgm0z6Tmw00Os4NxRgxQ8dFVDCFe7s0rgdgW9ZMEd-yHkB2MzenhSahthM8pnPxiBqxuFKaPQTUUCXCSQblo4pM6ufo0N-KLA5rZGidgto8UEyTzB5sLmJUlxo.UEnkpbTHrYfG09fYVm0xwhQm5n7UhRuHTiFH2dJwnI0&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
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
