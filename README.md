# Pong Game: A Classic Arcade Game Built with Python and Turtle

## Overview
This project is a recreation of the classic Pong arcade game, implemented in Python using the Turtle graphics module. It demonstrates key programming concepts such as real-time animation, keyboard event handling, and object-oriented design. The game is designed for two players, with each controlling their paddle to hit the ball and score points.

## Features

### Core Features
1. **Two-Player Gameplay:**
   - Player A controls their paddle with the `W` and `S` keys.
   - Player B controls their paddle with the `Up` and `Down` arrow keys.

2. **Dynamic Ball Movement:**
   - The ball moves smoothly across the screen, bouncing off walls and paddles.

3. **Collision Detection:**
   - The game detects when the ball collides with a paddle or wall and adjusts its direction accordingly.

4. **Score Tracking:**
   - A scoreboard displays the current scores for both players, updating dynamically when a point is scored.

5. **Sound Effects:**
   - Includes sound effects for ball bounces and scoring, enhancing the gameplay experience (requires `afplay` on macOS or equivalent on other systems).

### Enhancements
- **Simple and Intuitive Controls:**
  - Designed for easy two-player interaction.
- **Customizable Gameplay:**
  - Modify ball speed, paddle size, or screen dimensions by adjusting constants in the code.

## How to Play
1. Player A uses the `W` key to move their paddle up and the `S` key to move it down.
2. Player B uses the `Up` and `Down` arrow keys to control their paddle.
3. The goal is to hit the ball with your paddle and score points when your opponent misses.
4. The game runs continuously, tracking scores until stopped.

## Screenshots
*Include screenshots or a GIF demonstrating gameplay.*

## Getting Started

### Prerequisites
- Python 3.9 or 3.11 (confirmed to be compatible)
- Turtle graphics (included by default with Python)
- Optional: Sound files (`bounce.wav` and `Pong.wav`) for enhanced experience

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pong-game.git
   cd pong-game
   ```
2. Ensure the required sound files (`bounce.wav`, `Pong.wav`) are in the project directory.

### Running the Game
Run the `pong_game.py` file:
```bash
python pong_game.py
```

### Note on Sound Effects
The `os.system("afplay <file>&")` command is used for sound playback and works on macOS. For Windows or Linux, replace `afplay` with the appropriate command:
- **Windows:** Use `playsound` or `winsound`
- **Linux:** Use `aplay` or other audio players

## Code Overview

### Key Components

#### 1. **Game Setup**
- The screen is initialized using the `turtle.Screen` class, with a black background and centered layout.
- Paddles and the ball are created as `turtle.Turtle` objects with specified shapes, sizes, and colors.

#### 2. **Paddle Movement**
- Functions (`paddle_a_up`, `paddle_a_down`, etc.) handle the movement of paddles based on keyboard inputs.
- Key bindings are set up using `wn.listen` and `wn.onkeypress` to link keys to paddle movement.

#### 3. **Ball Movement and Collision Detection**
- The ball's position is updated continuously in the game loop.
- Collisions with walls reverse the ball's vertical direction.
- Collisions with paddles reverse the ball's horizontal direction.

#### 4. **Scoring and Resetting**
- When the ball moves past a paddle, a point is scored for the opponent, and the ball resets to the center.
- The scoreboard is updated dynamically using the `pen` object.

#### 5. **Sound Effects**
- Sound effects are played for ball bounces and scoring events using the `os.system` command.

## Future Enhancements
1. **Single-Player Mode:**
   - Implement AI to control one paddle for single-player gameplay.
2. **Power-Ups:**
   - Add special items like speed boosts or ball split mechanics.
3. **Customization Options:**
   - Allow players to set game speed, paddle size, or winning score.
4. **Improved Graphics:**
   - Use modern graphical libraries like Pygame for better visuals.

## Skills Demonstrated

### Core Python Skills
1. **Turtle Graphics Programming:**
   - Leveraging the `turtle` module for creating and animating game elements.
2. **Event-Driven Programming:**
   - Handling user input with key bindings.
3. **Collision Detection:**
   - Using coordinate-based logic to detect collisions and adjust game behavior.
4. **Dynamic UI Updates:**
   - Real-time score updates displayed on the screen.

### Additional Skills
- **Game Loop Implementation:**
  - Continuous updates to the game state in the `while True` loop.
- **Sound Integration:**
  - Using OS-level commands for cross-platform sound playback.

## Acknowledgements
- Sound effects sourced from pixabay.
