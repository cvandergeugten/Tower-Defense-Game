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

Currently, the ESC key is bound to bring up the pause menu for the player. Bringing up the pause menu will stop the game momentarily (of course!) and gives the players some options to choose from: continue, retry, or menu.

<b>Continue:</b> Resumes the game where the player left off.

<b>Retry:</b> Starts the current level over, resetting the player's money and number of lives.

<b>Menu:</b> Returns the player to the main menu.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/PauseScreen.gif">
</p>

<h1>Menu Screen</h1>

This simple main menu screen features an animated turret with attached menu buttons: play and quit. I also added a green glow for visual appeal.

<b>Play:</b> Takes the player to the level select screen.

<b>Quit:</b> Exits the program.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/MenuScreenDemo.gif">
</p>

<h1>Game Over Screen</h1>

When the player runs out of lives, the game is over! This will prompt the game over screen to pop up and give the player the option to retry the level or return to the main menu. Information about how many waves the player had survived is also presented on this screen. The game will also continue to run in the background while on this screen so the game still feels alive.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/GameOverScreen.gif">
</p>

<h1>Level Selection Screen</h1>

After selecting the play button from the main menu, the player will be taken to the level select screen where they will be able to choose which level they would like to play! The player can use the scroll bar or click & drag the mouse to navigate the level selection canvas.

<p align="center">
  <img width="460" height="300" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/LevelSelectScreen.gif">
</p>

<h1>Enemies/Waves & Turrets</h1>

In the current state of the game, there are 3 unique enemy types that the player can come across. The basic enemy is colored blue and has a standard amount of health and movement speed. The tough enemy type is red and has a ton of health in comparison, but moves very slow. The last enemy type is a fast enemy which is colored yellow and has very little health but moves very fast. Although there are only these three enemy types so far, the game is developed so that it is easy for designers to add new enemies to the game.

The wavespawner.cs script provides functionality within the Unity editor to choose which enemy type to feature on a particular wave, how many of them to spawn, and the rate at which they will spawn. This makes it easy to design levels and increase the difficulty of each wave as the game progresses.

The game also currently has 3 turret types: Basic, Missile, and Laser. The Basic and Missile turrets utilize projectiles while the Laser turret "locks on" to the enemy with its weapon. New turrets can be easily added to the game by providing a prefab model and customizing the turret properties within the editor.

<p align="center" style="padding:100px;">
  <img width="300" height="200" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/BasicTurretDemo.gif">
  <img width="300" height="200" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/MissileTurretDemo.gif">
  <img width="300" height="200" src="https://github.com/cvandergeugten/Tower-Defense-Game/blob/main/ProjectImages/LaserTurretDemo.gif">
</p>


<h1>Upgrading/Selling Turrets</h1>

<h1>Particle Effects</h1>

<h1>Game Design</h1>
