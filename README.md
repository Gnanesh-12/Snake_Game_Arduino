# 🐍 Snake Game for Arduino

A classic Snake game implementation for Arduino using a 16x2 LiquidCrystal Display (LCD). This project features dynamic snake growth, increasing difficulty, and a custom-rendered graphics system using LCD special characters.

![Snake Game](Snake%20Game.png)

## 🚀 Features

- **Classic Gameplay**: Maneuver the snake to eat food and grow longer.
- **Dynamic Difficulty**: The game speed increases as you collect more points.
- **Custom Graphics**: Utilizes 5x8 pixel custom characters to render the snake and food on a standard 16x2 LCD.
- **Score Tracking**: Displays your final score upon game over.
- **Responsive Controls**: Intuitive two-button orientation control.
- **Efficient Memory Management**: Uses a linked-list data structure for the snake's body to optimize memory usage.

## 🛠️ Hardware Requirements

- **Arduino Board** (Uno, Nano, Mega, etc.)
- **16x2 LCD Display** (Hitachi HD44780 compatible)
- **2x Push Buttons**
- **10kΩ Potentiometer** (for LCD contrast)
- **2x 10kΩ Resistors** (for pull-down button configuration)
- **Jumper Wires & Breadboard**

## 🔌 Pin Mapping

| Component | Arduino Pin | Description |
| :--- | :--- | :--- |
| **LCD RS** | 6 | Register Select |
| **LCD Enable**| 7 | Enable Signal |
| **LCD D4** | 8 | Data Pin 4 |
| **LCD D5** | 9 | Data Pin 5 |
| **LCD D6** | 10 | Data Pin 6 |
| **LCD D7** | 11 | Data Pin 7 |
| **Button 1** | 4 | Left Turn / Orientation |
| **Button 2** | 5 | Right Turn / Orientation |

*Note: The LCD R/W pin should be connected to Ground.*

## ⚙️ Installation & Setup

1.  **Wiring**: Connect the components according to the pin mapping table above.
2.  **Library**: Ensure you have the `LiquidCrystal` library installed in your Arduino IDE (included by default).
3.  **Upload**: Open `snake_game1.ino` in the Arduino IDE, select your board and port, and click **Upload**.
4.  **Contrast**: Adjust the 10k potentiometer until the characters on the LCD are clearly visible.

## 🎮 How to Play

1.  **Start**: The game begins with a 3-second countdown.
2.  **Controls**:
    - Press the **Left Button (Pin 4)** to rotate the snake's direction counter-clockwise.
    - Press the **Right Button (Pin 5)** to rotate the snake's direction clockwise.
3.  **Goal**: Eat the "dot" (food) to grow and increase your score.
4.  **Game Over**: The game ends if the snake hits its own body. The snake can pass through walls and reappear on the opposite side (wrap-around).
5.  **Restart**: After a game over, your score is displayed, and the game restarts automatically after a brief delay.

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---
*Developed with ❤️ for the Arduino Community.*