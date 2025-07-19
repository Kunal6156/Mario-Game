# 🎮 Mario Game
This is a simple 2D game inspired by classic Mario, built using Pygame. The player controls Mario, who must avoid fireballs launched by a dragon. The game features increasing difficulty levels, score tracking, and a high score system.

-----

## ✨ Features

  * **Classic Mario Feel**: Simple mechanics reminiscent of old-school platformers.
  * **Dynamic Obstacles**: A dragon moves vertically and shoots fireballs horizontally.
  * **Score System**: Earn points by dodging fireballs.
  * **High Score Tracking**: Keeps track of your best score across sessions.
  * **Increasing Difficulty**: The level progresses based on your score, affecting the boundaries of the game.
  * **Game Over Screen**: Displays "GAME OVER" along with Mario and the dragon, prompting the player to restart.
  * **Sound Effects**: Plays theme music during the game and a "Mario dies" sound effect on game over.

-----

## 🛠️ Installation

### Prerequisites

  * Python 3.x
  * Pygame library

### Steps

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd SimpleMarioGame
    ```
2.  **Install Pygame:**
    ```bash
    pip install pygame
    ```

-----

## 🚀 How to Play

1.  **Run the game:**
    ```bash
    python mario.py
    ```
2.  **Start Screen:** The game will display a "PRESS ANY KEY TO START" screen. Press any key to begin.
3.  **Controls:**
      * **Up Arrow Key (↑)**: Makes Mario move upwards.
      * **Down Arrow Key (↓)**: Makes Mario move downwards.
4.  **Objective:** Avoid the fireballs coming from the right side of the screen.
5.  **Game Over:**
      * If Mario collides with a fireball, the game ends.
      * If Mario touches the top (cactus bricks) or bottom (fire bricks) boundaries, the game also ends.
      * Upon game over, your score will be displayed, and you can press any key to restart or `ESC` to quit.

-----

## 📁 Project Structure

```
.
├── mario.py            # The main game logic and Pygame implementation
├── dragon.png          # Image asset for the dragon character
├── maryo.png           # Image asset for the Mario character
├── fireball.png        # Image asset for the fireballs
├── bricks.png          # Image asset for generic bricks (though cactus_bricks and fire_bricks are used directly)
├── cactus.png          # Image asset for cactus (background element)
├── cactus_bricks.png   # Image asset for the top boundary (cactus and bricks)
├── fire_bricks.png     # Image asset for the bottom boundary (fire and bricks)
├── end.png             # Image asset for the game over screen
├── start.png           # Image asset for the start screen
├── mario_theme.wav     # Audio file for the game's background music
└── mario_dies.wav      # Audio file for Mario's death sound effect
```

-----

## 💡 How it Works

  * **Pygame Initialization**: Sets up the game window, caption, and initializes fonts and sound mixers.
  * **Game Loop**: The `game_loop` function manages the main execution of the game, including updating game states, drawing elements, and handling events.
  * **Player (`Mario` Class)**: Handles Mario's movement based on keyboard input and checks for collisions with boundaries and fireballs.
  * **Enemy (`Dragon` Class)**: Controls the dragon's vertical movement and its position relative to the window.
  * **Projectile (`Flames` Class)**: Represents the fireballs shot by the dragon, moving from right to left.
  * **Score and Level**: The `SCORE` is incremented for each fireball successfully dodged. The `check_level` function adjusts the top and bottom boundaries based on the `SCORE`, increasing difficulty.
  * **Collision Detection**: Uses `colliderect` method to detect interactions between Mario and fireballs.
  * **Game Over State**: When a collision occurs or Mario hits boundaries, `game_over()` is called, displaying the game over screen and updating the high score.

-----

## 🤝 Contributing

Feel free to fork the repository and contribute to this simple game\! Suggestions for new features, bug fixes, or performance improvements are welcome.

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/your-feature-name`).
3.  Make your changes.
4.  Commit your changes (`git commit -m 'feat: Add new feature'`).
5.  Push to the branch (`git push origin feature/your-feature-name`).
6.  Open a Pull Request.

-----

## 📄 License

This project is open-source and available under the MIT License.

-----

## 📞 Contact

For any questions or inquiries, please open an issue on the GitHub repository.

-----
