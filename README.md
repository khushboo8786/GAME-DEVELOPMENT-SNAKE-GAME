# GAME-DEVELOPMENT-SNAKE-GAME

*COMPANY*:CODTECH IT SOLUTIONS

*NAME*:KHUSHBOO KUMARI

*INTERN ID*::CT04DN1859

*DOMAIN*:C++

*DURATION*:4 WEEKS

*MENTOR*:NEELA SANTHOSH KUMAR

**This project is a 2D Snake Game developed in C++ using the SFML (Simple and Fast Multimedia Library). The main objective of this implementation was to gain practical experience in working with multimedia libraries, real-time rendering, input handling, sound integration, and game logic structuring using object-oriented programming. The game is interactive, responsive, and features both visual and audio elements to deliver a complete gaming experience.

Project Structure and Game Logic
The game is encapsulated in a class called SnakeGame, which contains all components: the game window, snake logic, apple placement, score tracking, rendering, and audio management. The window is initialized at a resolution of 800x600 pixels, with each grid cell being 20x20 pixels, allowing for consistent alignment of the snake and apple on a tile-based grid.

The snake is modeled as a vector of SnakeSegment structs. Each segment holds an (x, y) coordinate pair corresponding to its position on the grid. Initially, the snake starts with one segment and grows longer every time it eats an apple. Movement is handled using an enumerated Direction type (UP, DOWN, LEFT, RIGHT) and controlled via keyboard input.

Input and Movement Handling
User input is captured in the event loop within the run() method using sf::Event. Arrow keys change the snake’s direction, but direct reversal (e.g., going from RIGHT to LEFT instantly) is disallowed to avoid logical errors. Movement is time-controlled using an sf::Clock, which ensures the snake moves only after a specified delay (speed) has passed. This delay shortens each time the snake eats an apple, gradually increasing the game’s difficulty.

The moveSnake() method handles the snake's logic. Each frame, the body segments follow the head. Depending on the current direction, the head’s position is updated. If the head position matches the apple’s location, a sound is played (eat.wav), the score is increased by 10, the snake grows by one segment, and the apple is randomly repositioned. Additionally, the movement speed is slightly increased (i.e., delay reduced), creating a progressive difficulty curve.

Apple Placement and Collision Detection
Apple placement is randomized using the rand() function within the grid’s bounds and visually represented by a red sf::RectangleShape. Collision detection is twofold:

Wall collision: If the snake's head moves beyond the grid limits, the game ends.

Self-collision: The head’s position is checked against each body segment. If a match is found, the game ends.

Both cases trigger the gameOver() function, which stops the background music and displays a “Game Over” message showing the final score using sf::Text.

Audio Integration and UI
Audio is implemented using SFML’s sound classes. A background music track (bg.wav) loops during gameplay using sf::Music, while the apple consumption event triggers a one-time sound effect (eat.wav) using sf::SoundBuffer and sf::Sound.

The score is dynamically displayed on the screen using a loaded font (arial.ttf) and updated with each apple eaten. The updateScore() function ensures the score label reflects the current score in real time.

Rendering and Game Loop
The game runs inside the run() method, which includes the main loop. This loop handles events, updates the game state (movement and collision), and calls the draw() function. Inside draw(), the screen is cleared and all visual elements (snake, apple, and score text) are rendered onto the window using SFML’s drawing functions.

Conclusion
This project helped me understand core game development principles, such as managing a game loop, real-time input handling, rendering with SFML, sound management, collision detection, and clean code organization through classes and functions. It also strengthened my understanding of C++ STL containers (like vectors), memory-safe graphics handling, and incremental difficulty design. If extended further, I would consider adding pause/resume features, menus, high score saving, and additional game modes for more advanced functionality.

*OUTPUT*:![Image](https://github.com/user-attachments/assets/6fb35a6d-e58e-4450-a16f-a07245bdbe30)



