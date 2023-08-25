# THLI-Painball

## Credits
* A Java game created by Mr. Weisswange
* Activity for TeenHacks Long Island 2023 Fall

## Rules
Paintball is a team vs team simulated board game (grid of cells). Each team consists of 10 bots written in Java, that autonomously move without user input. The bots run in sequencial turn (like a boardgame) based on the order they are initialized (random). 

## Tournament Rules
* 10 bots on each team
* 5 minute simulations at max speed
* Only 1 .java file submitted, containing 1 bot
* WHichever team wins more points with a difference >2.5% is considered a win. Difference between scores <= 2.5% are considered ties

### The Following are summarized rules. More in depth explanations are available within the code. 

### Points
The goal of the game is to be the team with the most amount of points. You can gain points through:
* Shooting "paintballs" at the enemy base (+3 points)
* Shooting "paintballs" at the enemy and killing them (+1 point)


Friendly fire is on as well. 
* Shooting "paintballs" at a your own base (+3 points for OPPONENTS)
* Shooting "paintballs" at your own teammates (+1 point for OPPONENTS)

### Game Map
* 33 x 50 cells grid
* Obstacles are randomly generated and are the same on both sides (rotated 180 degrees around the center)
* each bot can call the map (2D array) which contains the location of all objects during the bot's turn
* The base of each team will always be (row, col): (16, 0) or (16, 49). Each base will always have an obstacle 2 blocks away in each of the cardinal & ordinal directions (if those locations are within the bounds)
 
### Game Mechanics
* each bot can shoot/turn/move each turn (only 1)
* each bot can move to any of the 8 adjecent cells (given the cell is in bounds, and not occupied)
* shooting has a cooldown of 2 turns
* bullets move in a straight line (1 of 8 directions) with 2 turns every time bots move 1 turn. Bullets will go on until they hit a bot/obstacle/out of bounds

## Examples
* examples are shown in the "w_brains" folder
* however, make your bots in the "brains" folder. And don't forget to import brains in PaintballMain.java

## Tips & Points
* You do not know if you will be on team 1 or team 2 (spawn on left/right side of the board) so make sure your bot works on both sides
* remove all print statements (or comment them out)
* try to make sure your bot does not throw exceptions or cause an infinite loop (unlike mine...)
* your bots can communicate with each other to know what to do! (ex: keep track of how many bots have been initialized so far so the current bot can decide what role (base charger/defender/killer) it would act as ) (hint: static variables) 
* have fun :D
* KEEP IN MIND, YOU CAN ONLY SUBMIT 1 JAVA FILE. So if you want bots to do multiple roles, you can try using the communicating between your bots to assign roles

## Extra information
Add your bot in the PaintballMain.java file, in the reset function. Make sure to change the array sizes of the teams accordingly <br />

Refer to "Useful methods and their locations.docx" for helpful information to code your bot <br />

Demos link: https://drive.google.com/drive/folders/1WyadDOcEt1OmlF9q73dp1Rdr77CP5jIm?usp=sharing
