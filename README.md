Chapter 5 
This is a mouse-controlled game where the player must avoid intelligent AI seekers that pursue them using autonomous agent behavior based on vector math. The game ends when any seeker collides with the player.

Things Being Modeled:
I'm modeling two types of objects: a Player class for the user-controlled entity and a Seeker class representing the AI agents. The seekers use vector-based movement to simulate realistic pursuit behavior.

Data Structures:
I use a player variable for the single player object and a seekers array to store multiple autonomous agents. A gameOver boolean tracks when the player has collided, and a score variable could be added to track survival time.

What Happens in setup():
In setup(), I create the canvas and initialize the Player object at the center. I also create multiple Seeker objects with random starting positions and push them into the seekers array.

How draw() Works:
Each frame, the background is redrawn, the player moves toward the mouse, and each seeker calculates a steering force to pursue the player. After seekers update their positions, the program checks for collisions; if one occurs, the game ends and displays "Game Over".

Descriptions:

Player class

Properties: x, y, radius, color

Actions: update() smoothly follows the mouse, display() draws the player circle.

Seeker class

Properties: pos (position), vel (velocity), acc (acceleration), maxSpeed, maxForce, radius

Actions: seek(target) calculates and applies steering force toward the player, update() updates velocity and position, display() draws the seeker.

