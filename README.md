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
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=58e435ad-c2a5-430f-87e8-a5228d4f246b&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzI0MDYifQ.JvOfXUdaPAVXRtfvbFuuhGY_1o64a1lIU_Y3BErJRMHvdwPo6wqdHiYLglzu3cvWg2OUDCAuIJFlHLyt1hoEBBOiLI4rrgV3p5Oj3E7RMEWltNfFUnir-Zl9U1DMmu1e8VEA2fELA_5UG8L_5Hwcdzcz_1a5-cYlfZr5rU1lpy58_oZjPKisLIrfi5y1GVchCRkXDhkZfesezBbn84UBdEXZZg7MzFqVduyLJnwm4Ys17fqgBzrb9wnOb-PzWgECBu6Z-sX-_BT17ttKwOIhJPcSgBQmNAaqRxHjATbRedjFGPcZ2Mc33EA6i4uie_eTZzekJIQqSTeL3uWBkh6NlRFzq7BInvFd4XlXtFOhVmr2xHNGcP06SoK297zEUTpeh4f2pO-snDW1FrGD8i01Uf66uxhL-5SFdPMYnSz7kbs.mbpogwBWCXsMkr4zi_g5cmLYNX7dsmUm62GRGEtH-tU&ApiVersion=2.0" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create the game canvas: <br/>
Here is where we begin to start creating the game. Firstly, start by importing the tkinter module. Then we will be making a class called ‘Game’ and attaching important objects to this class, such as an initialization function and a canvas for the game. Doing this causes the background that was created in the beginning to be implemented using a mainloop function within the newly created class. In addition, we reference the background image that was created earlier using a ‘PhotoImage’ widget. Lastly, we can give the game a title.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YNAENRVQTTSHVFK6DGE5BEZT6VL%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.5S057TrdyoyqjCAhAbYMFEFJFXNaQPbPegRq11gbKbyAIXb0stDSnOGGmnuVxLvpsACd-YapGuDmVKpCLra0ObZ1K6H1Sddhs7Qy6mszNFdMWETXkA0W80JiZcjfs9SO1cVvpmX0UqoLtftE-SCaj__SkclHxpKkoigvqHOc6-hsOKd5olg2lpS3mjK48tcqlxsUi2otUzc9KUerN-flUcNKuv9JRQfxqjmfBWL9cB22dTqBzygcx3FfYT4RFMux7zYD0zVzFN9q-S2ospCvnlRKJV9cfpagWaFr-w4OvAUj-1qMKR89yNnIj4OWRvWy-A-QAOWDJIX2SAbvR5czW7IWMNGCsn4acIZJu1CnWRP4JN1GrC_A0bOb7bqJBKcH.XtiDi-OCGbZ0yZ8klGUpLbMrXMcLTu3-c3iT4VC6ufo%26version%3DPublished&cb=63861625196&encodeFailures=1&width=498&height=495" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create coordinates and collision detection: <br/>
For this step, we create coordinates for the positions of the earlier created sprites.  The necessary components to use are two sets of coordinates, x and y. Next, we utilize a crucial part of any game: collision detection. This is so the game will be able to tell if any of the sprites have collided with one another. Collision detection also allows Mr. Stickman to be able to run around and jump onto platforms which we will delve into more detail in the next step.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YKHDN2G3IV7PVEICASVXDUPNBAC%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.MfISuKI6UnGg3MLjekbPSr0txwo1dOjft__mciznnfEUV-UTdzd_cJT2QksJrtfaqDqfx1AR2qiqnhAxmfBudJ-tswAVLoPvFqqNOKNB-2vHoBnkDjS3usZ-c9YrZw2wPwpqPgOH2d1piGvxb_HeORl0BeMLQb-YzkH1Y2xNPGFxdpdW2fcFFKdiXYBXXJOCYV1_X1uTHdVJNx9O66hBwjDSa9XKQYuXgbohSMKuyKqHXpTMHlCMEUoV193_eXoJVc_zXu1oyo1ZL6vtnIQPT7e_6kJlpA8y8sdxzvYHRIPgjjJjC68yMAXlfGhxaFpY-jPmd4w1GTLfxkMvE7xrLJE98azdqKolQmKXiw0gqy3caojhufWKHFv-2BhSbjH1.Pk5E7RFyp3eq2vsBjU3fJSiThaMRayPhrlSALZz42mQ%26version%3DPublished&cb=63861625211&encodeFailures=1&width=1600&height=814" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add platforms: <br/>
Now we add platforms. Using the steps prior, we are able to add coordinates and collision detection to the platforms while placing them each in different locations. By using another initialization function as well as a ‘PhotoImage’ widget, we are able to tell python to reference the platform images that are placed in the ‘Mr Stickman Game’ folder. This will enable our images to load into the game. Furthermore, through the addition of a new class, we can add moving platforms to raise the difficulty of the game. This addition also grants us the ability to define which platforms move back and forth horizontally and which platforms remain stationary. 
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YOITE5TJTAOPBGIH2E4OMXVD74Q%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.3quS2uW7LGGpqIj9OeFxeo4y5HzydGUSZdaGvS_UjzS3tMtE79sNtfDrpKxMh7Ha7G_4u2pLsS-Nj4Z1_d-XVqLuaZMIMSFfj2NJbgl4-r_VFE1nCuRvziAvyNmpy9A6GJMw-fqmqfTJaU57lr03TO3fLfppcI7UopLinmmwmtV2AO-wzLzcWQVR9xjAMLhoGTwPqlh20bniiOpdMSum5oUhX__KaVPfVe5Asq1idA4rFr9KfnxPqMO2TCiFeiryx88vP3KO6snot1cgWK8RHIernPVcYucSVcKA3KDahuUenlYNXVpGl6SgWZgy_VNMDgWoBJpz7SUzDeu9ogKEQxSTlGB_VCFJFA0JBd_sh4fv-ODXe2YxQI3jMq44xfLC.CjRUAwPK49PBy0EbDZtXsFpXp8r2Eri3EdkK4VJz4Jk%26version%3DPublished&cb=63861625230&encodeFailures=1&width=502&height=532" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Loading & binding Mr. Stickman:  <br/>
In this step, we load Mr. Stickman’s image into our game using the initialization function and a PhotoImage widget. We also use the bind function to create keyboard events that will allow our character to run to the right, left, or jump after a certain key is pressed.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YJCJFUKEK5MTJCJ6O4KVRLL54UN%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.njm5uKaQ0scKrbBmrGQ5tlvxoFAnEeacIqT-gzVc2AY_liY1oeyvIgKcIq4uuPmBEu64DB_-G5FhovRskHt8jPzmfKM7USDYWGC5ZuROzjMn31LwKcKhUSS3iYxpyY-u-qB8zYCpI7ILsv5aCxTuem4Y2N9Kh3XiPf1hMOwV3_ujpCe6FFuyM70qwGch_AI8YnV7zqTLs5zmbLfaD2K_Yx1w9iYnIKDPej9vMWv23scmjZqRVy2GbF7uLPjSI8szfjmbnb8qfJtCwa-rXL7_yyJ5MLY-z9DxFu6ygGHvqZW31nWDtyey7ZHN2h5AmtDAhNyNOkzmIRrDsVha_ZsscpBs-CxNNRfma-LbFFgIAoMbhRfvx500hl3PyW21jQ3B.GsFT_xMeHy7fVXL_HGft96f_y8rMNhsp94Q03k2xKX8%26version%3DPublished&cb=63861625247&encodeFailures=1&width=1131&height=824" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Animate Mr. Stickman: <br/>
Now comes the action. Using a few if statements along with the animate function, we link Mr. Stickman’s movement to the previously created key bindings. This creates the illusion of fluid animation for each frame every time the stick figure moves inside the game. Just like the above steps, we make sure to define coordinates for our stick figure which allows it to be able to move around the screen, and it also adds more collision detection among all the sprites in our game. As a bonus, testing our code during this step helps ensure all sprites are working properly according to our code.
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=4a9603cd-03c0-48ca-99e5-4d3eadf1eedc&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzI0MDYifQ.vTgwjPIqugp0GJpebIaHwS2vYmXNHdS2yrE6VX9XOAF5leGzj1x7l0zOy7BreRcd9AOXp0bouAiBdHmuGKtM4k1-0Ow7ppxkBn4hZlV0Kr59QvGSAiiKl41DqbDYRPbdNW0YqIRcAaq8eNR-nvrIaNx5kKOuBsFsBhGOjqgS16Zs5b1xKzYkhogulA7PgX1NojXod8EwyY6a575kZIc0fFfqK4Vi71kY3zKOIy_k1KIFijjxwjd74v5i_CTw7f4clYF-GFN0145NjWZO_QEmqBLH5GbHYhF_FZbuXtyhlVgWE5entYQHszcQmEbxhgMhMQpof5cd8ftJUUEZPGjKB79V4vevH28_Cj7_9dZFbTHl6GvQaKu-6ZUKvJHDuLuH__vwrwCwtbLfQrTFhFQLI-cAhm2BWOgtIdqux1UAKEw.RWQByCYgFWPHBdcBtic9V5EeB62IDRiDbERjwQ6Uyy4&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add the exit doors and win the game: <br/>
The game needs a win condition. Also, we need to add the door sprites created earlier by creating code that references the door images and also code that detects when our stick figure has arrived at the door. A bit of extra code helps animate the door to open and close as soon as Mr. Stickman arrives. To finish everything we add an endgame function along with a door object so that our door sprites load properly and so the game knows we have reached the exit. Finally, the project has reached completion, and we have just achieved coding a fully animated game! 
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=173821c3-d51e-43c4-a3cd-5b7ee4ccf01d&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzI0MDYifQ.ZJvw4nwdtOHjc8bIpE0Y-QjINFjdA2uawObwSc1Xb2BZ9Ai8mBOXqvGA0gmv4_yBWngMczXqOONUgYBne0o6RieqClqSt5sdoUSutoJmWN8R65qrwPKDSGWEnm0W_sJ6SGZZygvV54So3V8DoURPFHvfFUugcbP4fxJb3WL_XB7QkAHlMLVMH1zG3TK07YzMrk3bnFkl74Sc4fV1mTiQKbBy4ezJuqK9jtJ1mnYeNK99NQ9E8j9jb9JsASE6YblejhOiCMvLYFJPrpW_d_CD2ydpnLSOL-B9vpWuHcPgSe6f9KBDLao-BQWThOhJfMv75qVrWfL8Jcrb7WezkDsnI2Neu6HA2aHBa53IsgEwxqY85MGENr5jjI--fciKFh69EsuHOI-tKZmXOiTPtud8bTC_Dv30e6RBkDdxMZ9Aq2U.s-1i1yTUhY00tV3Z8Q1tBiKZl8E_7Dc_hz6BJUZJpqc&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
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
