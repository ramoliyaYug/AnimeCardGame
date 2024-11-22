# Anime Cards Match 🎴

Anime Cards Match is an interactive memory game featuring anime-themed cards. This project demonstrates advanced web development skills, including DOM manipulation, event handling, and responsive design, making it perfect for showcasing technical expertise.

---

## 🚀 Features

- **Interactive Gameplay:** Match pairs of anime cards while keeping track of errors.
- **Dynamic Board:** A 4x5 grid generated dynamically, ensuring a unique experience every time.
- **Error Counter:** Real-time tracking of mistakes to challenge the player.
- **Celebratory Video:** Displays a reward video upon game completion.
- **Responsive Design:** Fully adaptable to various screen sizes and devices.

---
## 🔧 How It Works

#### 1. Game Initialization
- On load, `script.js` shuffles the cards and sets up a 4x5 grid dynamically.

#### 2. Gameplay
- Players click on cards to reveal them. Two cards can be selected at a time.
- If the cards match, they stay revealed; otherwise, they are flipped back.

#### 3. Error Tracking
- Each mismatch increments the error counter, displayed on the screen.

#### 4. Victory Celebration
- Once all pairs are matched, a victory video is displayed.
- After 4 seconds, the game resets for replay.

## Functionality Explained

### 1. Global Variable Declaration
- Global variables are always declared at the top of all functions for better organization and accessibility.
- In this project, the global variables are used to store:
  - The number of **errors** made during the game.
  - The list of **cards** and the shuffled **board** layout.
  - The number of **rows** and **columns** defining the game grid.
  - The two **selected cards** during gameplay.
  - The count of **matched cards** to track progress.

### 2. Shuffle Cards Function
- The `shuffleCards` function ensures randomized placement of cards on the board, enhancing the game's unpredictability.
- It duplicates the card list and shuffles it using an algorithm to create randomness.
- The function:
  - First creates duplicates of the cards.
  - Generates a random index using `Math.random`.
  - Performs a simple swapping of cards to achieve a random board configuration every time the page reloads.


### 3. Dynamic Board Setup

- The game board generates dynamically depending on the number of rows and columns, shuffling cards in a grid.
- Brute-force is used for the generation of the game matrix by iterating over rows and columns.
- The outer loop generates each row, while the inner loop populates the row with cards.

#### Inside the Inner Loop:
- An image element is created and assigned a unique ID based on the matrix coordinates.
- A generic CSS class is added for styling, and an event listener is set for clicks, invoking the `selectCard` function.
- The element is appended to the board.

- Finally, after 2 seconds, an asynchronous call is made to the `hideCards` function to hide the cards.

### 4. Choose Card Logic
- It is responsible for the game's logic related to the selection of cards during play.
- Uses simple `if-else` for controlling the flow of card selection.
- Dynamically updates the `src` attribute of a selected card image based on its state.

### 5. Update Card Logic
- Checks if the two selected cards match.
- Makes use of an `if-else` condition for handling the two cases-match or not.
 
### 6. Display Video Logic
- Displays a video on the DOM after all cards are matched.
- This is called inside the `updateCard` function when the game has been won.

## 🖥️ Live Demo

Experience the game live by visiting the following link:  
[Anime Cards Match - Live Demo](https://ramoliyayug.github.io/AnimeCardGame/)
