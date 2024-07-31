# Hangman Game Project

![Hangman Game Demo](pictures/icons8-hangman-game-64_upscayl_5x_realesrgan-x4plus-anime.png)

## Introduction

Welcome to the Hangman Game! This Python project is an implementation of the classic word-guessing game where players attempt to guess a hidden word one letter at a time. The player has a limited number of incorrect guesses before the game ends. Enjoy playing while sharpening your vocabulary and logic skills!

## Class: Hangman

The `Hangman` class encapsulates the functionality and state of the Hangman game, making it easy to manage the game's logic and state.

### Attributes

- `possible_words`: A list of words from which the game randomly selects the word to guess. By default, it includes the words: `'becode'`, `'learning'`, `'mathematics'`, and `'sessions'`.

- `word_to_find`: The word that the player needs to guess, represented as a list of characters. It is chosen randomly from `possible_words`.

- `lives`: The number of incorrect guesses the player can make. The game starts with 6 lives.

- `correctly_guessed_letters`: A list that shows the current state of guessed letters. Initially, all letters are represented by underscores (`_`), indicating that they are not yet guessed.

- `wrongly_guessed_letters`: A list of letters that have been guessed incorrectly by the player.

- `turn_count`: An integer representing the number of turns taken by the player.

- `error_count`: An integer counting the number of incorrect guesses made by the player.

### Methods

- `__init__(self)`: Initializes the game by setting up the attributes and selecting a random word from `possible_words`.

- `reset_game(self)`: Resets the game state to start a new game with a new word.

- `play(self)`: Prompts the player to enter a letter and updates the game state based on the player's guess.

- `start_game(self)`: Manages the game loop, calling `play()` until the game is over.

- `game_over(self)`: Prints a message when the player runs out of lives, indicating that the game is over.

- `well_played(self)`: Prints a congratulatory message when the player successfully guesses the word.

- `print_game_state(self)`: Displays the current game state, including correctly and incorrectly guessed letters, remaining lives, errors made, and turns played.

## Game Flow

1. **Initialization**: The game initializes and randomly selects a word from `possible_words`.

2. **Gameplay Loop**: The player is prompted to guess a letter. The game updates the state based on whether the guess is correct or incorrect.

3. **State Updates**: 
    - If the guess is correct, the guessed letter is revealed in the word.
    - If the guess is incorrect, the letter is added to `wrongly_guessed_letters`, and the player loses a life.

4. **End Conditions**:
    - **Win**: The player wins if they successfully guess all the letters in the word.
    - **Loss**: The game ends if the player runs out of lives.

5. **Display**: After each guess, the game displays the correctly guessed letters, incorrect guesses, remaining lives, error count, and turn count.

6. **Game Over**: If the player runs out of lives, a game over message is displayed.

7. **Victory**: If the player guesses the word correctly, a congratulatory message is shown.

## How to Run

To play the Hangman game, follow these steps:

1. **Ensure you have Python installed** on your machine. You can download it from [python.org](https://www.python.org/).

2. **Clone or download the project files** to your local machine.

3. **Open a terminal** and navigate to the directory where the game files are located.

4. **Run the game** using the following command:

    ```bash
    python3 hangman.py
    ```

5. **Follow the on-screen instructions** to play the game. Enter one letter at a time when prompted and try to guess the word before you run out of lives.

## Conclusion

This Hangman game offers a fun and interactive experience of the classic word-guessing game. The implementation is flexible and can be easily extended or modified to add new features, such as a graphical user interface or a larger set of possible words.

Enjoy playing Hangman and improve your guessing skills!

## Future Developments

- **Graphical User Interface (GUI)**: Develop a GUI version of the game using libraries like Tkinter or PyQt for a more interactive experience.

- **Custom Word Lists**: Allow users to provide their own list of words for the game.

- **Multiplayer Mode**: Implement a multiplayer mode where players can take turns guessing letters.

- **Difficulty Levels**: Introduce different difficulty levels with varying numbers of lives and word lengths.

## Contributions

Loïc Rouaud (Broma)


---

Thank you for playing Hangman! We hope you enjoy the game and contribute to its development.
