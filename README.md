# Snake Console Game Documentation
This documentation provides an overview of the "Snake" console game.
The game is a simple implementation of the classic Snake game, where the player controls a snake that moves around the screen to eat fruits and grow longer.
The objective is to eat as many fruits as possible without colliding with the walls or the snake's body.

## Program Class
### Fields
* int Height: The height of the game board (number of rows).

* int Wide: The width of the game board (number of columns).

* int[] x: An array to store the x-coordinates of the snake's body parts.

* int[] y: An array to store the y-coordinates of the snake's body parts.

* int fruitX: The x-coordinate of the fruit on the game board.

* int fruitY: The y-coordinate of the fruit on the game board.

* int parts: The current length of the snake (number of body parts).

* ConsoleKeyInfo keyInfo: Stores the latest key press information.

* char key: Stores the direction in which the snake should move (W: Up, S: Down, D: Right, A: Left).

* Random rnd: A random number generator used to place the fruit on the game board.

### Constructor
* The constructor initializes the game board's dimensions (Height and Wide).

* It sets the initial position of the snake's head.

* It hides the cursor to provide a cleaner user experience.

* The initial position of the fruit is randomly generated.

### WriteBoard Method
The WriteBoard method clears the console and draws the game board by drawing the borders with - characters and | characters.

### Input Method
The Input method checks if a key is available in the console input.

If a key is available, it stores the information in keyInfo and extracts the key character to update the key variable.

## WritePoint Method
The WritePoint method writes a single character (#) to the console at the specified position (x, y) to represent a part of the snake or a fruit.
## Logic Method
* The Logic method updates the game's logic by moving the snake, checking for fruit collisions, and handling the snake's growth.

* If the snake's head collides with the fruit, the snake grows, and a new fruit is randomly placed.

* The snake's body is updated by shifting each part's position to the previous part's position.

* The key variable determines the snake's direction of movement.

* The method updates the positions of the snake's body parts and the fruit, then redraws them on the game board.

* A delay of 100 milliseconds is introduced using Thread.Sleep(100) to control the speed of the game.

## Main Method
* The Main method creates an instance of the Program class (snake).

* It enters an infinite loop where the game board is drawn, user input is processed, and the game logic is updated repeatedly.

* The game continues until the user exits the program by pressing any key.

This concludes the documentation for the "Snake" console game. The game provides a simple and fun Snake experience,
allowing the player to control the snake to eat fruits and grow in length. However, it lacks collision detection with the walls,
which could be added to enhance the game's challenge.
