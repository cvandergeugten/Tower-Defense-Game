# Tower-Defense-Game

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/MenuScreen_TD.gif">
</p>

<h1>Summary</h1>

This simple tower defense game was developed with Unity and C#. Player's start the game with some money and have to build turrets to prevent enemies from reaching the end goal! Players gain money for defeating each enemy which allows them to continue to grow their defenses. Each turret has its own unique mechanics and price in the turret shop. Players can also upgrade turrets at an additional cost, or sell existing turrets if they are short on funds. In the current version of the game there exists 3 enemy types, but the game was developed to allow for designers to add new enemy and turret types as they see fit. A level system is incorporated to give designers some flexibility and allow for different maps and challenges.

<h1>Game Board</h1>

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/GameBoard.gif">
</p>

Although the project is based in 3D, the game board was created to give more of a 2D feel. The board consists of tiles which can be used to place turrets, as well as a path for enemies to move on. In each level, there is a start and end node which determines where the enemies spawn from and where they will end up if they are able to slip by the player's defenses. The tiles are laid out like a grid which makes is clear to the player where they can and cannot place turrets. Each tile will highlight when the player hovers over it with the mouse so they know which tile is being selected. If no turret has been selected to build, the tiles will not interact with the mouse cursor. Additionally, if the player does not have enough money for a particular turret, the tiles will change color indicating that turret placement is not possible.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/GameBoardTiles.gif">
</p>

<h1>Game Board UI</h1>

When designing the main UI for this game, I had an option of having the UI appear as a heads up display (HUD) which would remain on screen as the player moved the camera around, but I decided to have the UI be static components which have the effect of feeling attached to the game board. The game board UI displays the following for the player: number of lives, money, and time until next enemy wave.

<b>Lives:</b> Displays the player's remaining lives for the current level. When this reaches 0 the game is over!

<b>Money:</b> Displays how much money the player has to purchase turrets and upgrades.

<b>Wave Spawn Timer</b>: Displays how much time (in seconds) the player has left until the next wave of enemies spawn.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/GameBoardUI.gif">
</p>

<h1>Player Shop UI</h1>

Unlike the game board UI, the turret shop exists as a HUD element so that wherever the player moves the camera to, they can always see access the shop items. In the current version of the game there are 3 turrets to choose from, but the canvas element within the UI is designed so that any additions to the shop will integrate smoothly and all of the buttons will be formatted correctly without having to adjust each element one at a time. Each button has an image of the turret and its corresponding price.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/ShopUI.gif">
</p>

<h1>Game Camera</h1>

I gave the player the ability to control the camera using the WASD keys as well as scrolling the mouse the the edges of the screen. The player can also zoom in and out using the mouse wheel. This type of camera control is similar to and RTS styles game's camera and allows the player to focus in on specific parts of the map and see the action up close, or to get a view of their entire defense setup. The movement and zoom functionality has been bound so that the player cannot move too far away from the game board or zoom in under the map.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/GameCamera.gif">
</p>

<h1>Pause Screen</h1>

<h1>Menu Screen</h1>

<h1>Game Over Screen</h1>

<h1>Level Selection Screen</h1>

<h1>Enemies/Waves</h1>

<h1>Upgrading/Selling Turrets</h1>

<h1>Particle Effects</h1>

<h1>Game Design</h1>
