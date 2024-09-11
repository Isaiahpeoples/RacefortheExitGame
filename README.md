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
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=58e435ad-c2a5-430f-87e8-a5228d4f246b&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzYzMzcifQ.w94W1Sae-32VLpGk-CuvzN3QYx4wmeDOUpncQmSqiwGlMtyS-3MycKNi6wnnXMmiFDVxYLiyCo1Cw_PPw_ZG_w0FFvNcbs7_SfZ9DQpS-_HDdxiiYjR_kmK1yAwTe0TzXGU4Y56qmBwk-RNsaMbWyJsZJtn8u3yLmqNsFVvxibv5KC_iBmybJcL3qlRWoFmEAa7kJE_1zgqCsNq6Qvh253Ij9C03jf1mbDEEfIetgQaXcIQV1y21I2nnwxAtRZvlk2hoVsaJle2hoVOGGG79qk74fOU-YnQlulevOthHWdUT8twSb0VnTBFqtmfRYL2Xzc3jd_m3BHTL-AUj9oTc2TsPBkUrgd_MeZjyGRIpFvzu9LwA9d91TckYdwrkIMV27lL9deHruQAb8XXpDWZ7IuO423GLHOg3JPbciTUFkPg.UBLtF8j4WFGSpwEQOFXnRwSBXPcYDmgYF4ysjt3V6Tg&ApiVersion=2.0" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create the game canvas: <br/>
Here is where we begin to start creating the game. Firstly, start by importing the tkinter module. Then we will be making a class called ‘Game’ and attaching important objects to this class, such as an initialization function and a canvas for the game. Doing this causes the background that was created in the beginning to be implemented using a mainloop function within the newly created class. In addition, we reference the background image that was created earlier using a ‘PhotoImage’ widget. Lastly, we can give the game a title.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YNAENRVQTTSHVFK6DGE5BEZT6VL%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.eqvilwHlDHsdIzqA0Rvv5gsfqweptPghx2Ihkt0hOPR_4kJNdT8pz5yH-tExrsKc2HiI4Sv1B6eIgfdiL7Om2_Z_JY_qJSFluvznVu1toOgxOqHU-36IPN-JER8Chgwv1CDRRhwyXCPzqizPf-bVJ9VVr6ta4lrLOYNQm7_SGvM1nMIjNMn1JE8zSQ_7wlXmZFHku_xU0fsblvr7MQov2cHzmgNesbT8n4e2zA5Su_LDMVnvAcK7Cj_nfsOZdekrxdH0nemqBrQSsn-M69Yfr9kzoI5UyWxDRu5BJH68KxK6dxXNGF4yDvwrRuh2rvF5UTeqRBW1ekB0BgF_86W4ldDZ9Gyal8hMOfcLPx9bYSLz3n3i-hthxNqRuyunLAur.XtiDi-OCGbZ0yZ8klGUpLbMrXMcLTu3-c3iT4VC6ufo%26version%3DPublished&cb=63861625196&encodeFailures=1&width=498&height=495" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Create coordinates and collision detection: <br/>
For this step, we create coordinates for the positions of the earlier created sprites.  The necessary components to use are two sets of coordinates, x and y. Next, we utilize a crucial part of any game: collision detection. This is so the game will be able to tell if any of the sprites have collided with one another. Collision detection also allows Mr. Stickman to be able to run around and jump onto platforms which we will delve into more detail in the next step.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YKHDN2G3IV7PVEICASVXDUPNBAC%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.xLzcC0DUnch9p-M_hRHZMMncF9qlMGd5woF5gK_t36D3DWXgQ7QLwmZgCitJ9NBOfIyRG2-0AOX05KdID_KznvZRKMBNQGHg4dK9Avt0k8Ti7QhokLfQVN2kHYQqy_ASi0WHUcpLD3jEZHzPoFPtHSQjEMw2Bh4JJBfsorK04lhNabU7Y1Pte5GYY-v2-1GsjvuoByNhngPTcj0D48LephbA8a7I1kVFgOh_65ScRjVseo_4eDX_UxkQ8nECaLqpGUwPlrYiYkn65pyt2hn8cQTYag3eqI6eD_R2Oep5a_SsuDztBomLrnIlUm8wOWfZRpeFRDeKEk9M9yLtHwXOsBDCY7YFgZBip97oubElUeiPwdiD2YwqjOdyyX_HHZuo.Pk5E7RFyp3eq2vsBjU3fJSiThaMRayPhrlSALZz42mQ%26version%3DPublished&cb=63861625211&encodeFailures=1&width=1710&height=871" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add platforms: <br/>
Now we add platforms. Using the steps prior, we are able to add coordinates and collision detection to the platforms while placing them each in different locations. By using another initialization function as well as a ‘PhotoImage’ widget, we are able to tell python to reference the platform images that are placed in the ‘Mr Stickman Game’ folder. This will enable our images to load into the game. Furthermore, through the addition of a new class, we can add moving platforms to raise the difficulty of the game. This addition also grants us the ability to define which platforms move back and forth horizontally and which platforms remain stationary. 
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YOITE5TJTAOPBGIH2E4OMXVD74Q%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.gKrn33fAzmvp_LSZfvrp4aaHy05YtSPQHAtmDGpzI2RLo4HhvD8Nfh__n6uovIbsdeAkpSmyh1DTdMOMoW4SXBb2FM-bwrXgfz2NVtLC3o5B5GHNub_pKzxGVcfQyCjJ1KLJOHU3mP6YIJvLUBH9X7Qz0mT498T7cFRRuXLk7Cy578BW5epgAj36yncsdZxeswTM2kn5AXrpEHKSBT9u55SOjqr1eM8ZLzuD3phfMhh6s6BWffeafhQwFGEpR-Wj21ctcgwzRMggTN5HhLX3nzujzN_DeulM2e9hb2-ud--F35h2WZDxVJstjGGibc_3IFywzhZaTexKGYIdWEjAzNCV4Dj6iy1T3sdUq53MKsgZ6WT4IOTbvPi60S3tvI5k.CjRUAwPK49PBy0EbDZtXsFpXp8r2Eri3EdkK4VJz4Jk%26version%3DPublished&cb=63861625230&encodeFailures=1&width=502&height=532" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Loading & binding Mr. Stickman:  <br/>
In this step, we load Mr. Stickman’s image into our game using the initialization function and a PhotoImage widget. We also use the bind function to create keyboard events that will allow our character to run to the right, left, or jump after a certain key is pressed.
<br />
<br />
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YJCJFUKEK5MTJCJ6O4KVRLL54UN%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUyMDAifQ.utlzNNwbh-cBifNpbdCHtdcK6pqzh6hesHUu613Zzdv7k6afhFX0UpqCeQ779lJbNgAVdajjQWiCwamAU1kW_RFDXrb9AuzZNy90I-VkeLerAmNzyg7kSLrIsFZ90wV5bhJ4Zpi3wgAW9GVcLKtHCDeDqdrf-ah6FAWErCAUrLufdKMst-qGK141HUC0zmWuvvMP87IqBllMh71QdxHk8Ez7SA3URfUfIjlycZbLpGNGlrf9Bkrm1mMc-tSnFFkHyI-sW3_bWvXfrzA-gHC6zYw622cUgDjzHLGUptyfGv2Qb-HELlp0nXq8M6MmuARSFLCh1pUXgVF2bfDGDkw2oTAWGwvbgHTlotL7Rxx7_TDgDRa3mAHjaDwElJdkOjdJ.GsFT_xMeHy7fVXL_HGft96f_y8rMNhsp94Q03k2xKX8%26version%3DPublished&cb=63861625247&encodeFailures=1&width=1131&height=824" height="80%" width="80%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Animate Mr. Stickman: <br/>
Now comes the action. Using a few if statements along with the animate function, we link Mr. Stickman’s movement to the previously created key bindings. This creates the illusion of fluid animation for each frame every time the stick figure moves inside the game. Just like the above steps, we make sure to define coordinates for our stick figure which allows it to be able to move around the screen, and it also adds more collision detection among all the sprites in our game. As a bonus, testing our code during this step helps ensure all sprites are working properly according to our code.
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=4a9603cd-03c0-48ca-99e5-4d3eadf1eedc&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzYzMzgifQ.6AgeLFpyc0KytNTB7NkTpbi1Nfd-VS8AiHUaDHAwORmYhMMk3Zs40P_g0FJGhpk6aqGm7BdqL8L_KiEKbXybK5DZaHuTRdoKfYpkvzX9zqz3RTELsx7rD4eD3PS0EilON2kEKBNg71n6EXnEPFR1cp1C8_GzbsSkg_-8BgqAQuY2wGNBNFC1r7HBtPlWacsbFoxFPsTnUfKp1jaBrb6g1T9wdq0YlXygGk-NkwufWodo07-9-PFurLc0jlLx0wWRgUFm39blRSrBKtmMXE8ZtavYX0bwyp18NDbTVQw94Yy_-z2fy-ar1fJLTIQreZ4QoJKisJEo5k64Oqfr6aehj4tyPOw9klFb_DwYoY0sPIWLUrLi7BqwmYW4kK6NeOF-kSpy8xhvLeOpr5rdv5vrdmErdgGsIL4RkBKJIUijGGI.CsgT3ReB6w-25Iks0JX5CLf3ct-wxAJleb7kKRf7z5I&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
<br />
<br />
Add the exit doors and win the game: <br/>
The game needs a win condition. Also, we need to add the door sprites created earlier by creating code that references the door images and also code that detects when our stick figure has arrived at the door. A bit of extra code helps animate the door to open and close as soon as Mr. Stickman arrives. To finish everything we add an endgame function along with a door object so that our door sprites load properly and so the game knows we have reached the exit. Finally, the project has reached completion, and we have just achieved coding a fully animated game! 
<br />
<br />
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=173821c3-d51e-43c4-a3cd-5b7ee4ccf01d&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzYzMzgifQ.X8ANjnR7_Nixh1la6h0d1U9GgJU9afbWwnEvQg6wwZE9NkLag39p0pKxaShGbQ56iVKqqVCrLVClQDcQaarg3vqOc0Dt2IGeQBAUmq_6EDXqtBoB1u8psrirz01gi7kB7d_vbFVqqm8aBy27_FT35-Vt5UeCCIq0OiEzVPogMpALUYNRKsdVrIRQUI5yqpGmVgw1LFwTdU5ccY7xGUT-IZojiMKCj9W1UKCwhNeSFIzNfAcKkN-fC7zNG0hY4dhS2N2OyiqWCRb-UGyOAE6csQLSC63bFZlMNYXLCBfcY2hf_XnZJDEWk9Q-YfoVl25EdiOWD18jSdSJhzw7_G4hv8_nEfagpq1QQ-Ez2MWLxctb6Otd9IFjf0cDYgm00TdaQmzz3yZfUPxU83HGgcw9xEi8GNAEeeuzQ4XG_6a1K8w.Ztf1BVOhoGWFswoYsy-05Z1I_wBmK6MgJQ6B2X2yNQk&ApiVersion=2.0" height="100%" width="100%" alt="Race for the Exit Game Steps"/>
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
