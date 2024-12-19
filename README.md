# Guess The Number Game - README

## Project Overview

**Guess The Number** is a simple number-guessing game developed in Java. The goal of the game is for the player to guess a randomly generated number between 1 and 100 in the fewest attempts possible. The game provides feedback after each guess, indicating whether the player's guess is too high, too low, or correct.

## Features
- **Random Number Generation**: The game generates a random number between 1 and 100 for the player to guess.
- **User Input**: Players can input guesses and receive feedback on whether the guess is too high or too low.
- **Attempt Counter**: The game tracks the number of attempts the player makes before guessing correctly.
- **Game Feedback**: After each guess, the player is informed whether their guess is too high, too low, or correct.

## Technologies Used
- **Programming Language**: Java
- **Random Number Generation**: `Random` class in Java
- **User Input**: `Scanner` class for reading player input

## Installation

### Prerequisites
- Java 8 or later installed on your system.

### Steps to Set Up
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/DeepakPanneerselvam1455/Guess-The-Number.git
   ```

2. **Install Java**:
   - Download and install [Java JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) if it's not already installed.

3. **Run the Application**:
   - Open the project folder in your IDE or run the game directly from the terminal.
   - To run the game via terminal:
     ```bash
     javac GuessTheNumber.java
     java GuessTheNumber
     ```

## Gameplay

1. The game will generate a random number between 1 and 100.
2. The player will be prompted to guess the number by entering a value between 1 and 100.
3. The game will provide feedback on whether the guess is too high, too low, or correct.
4. The game continues until the player guesses the correct number.
5. Once the correct number is guessed, the game will display the number of attempts taken to find the correct answer.

### Example Gameplay:
```
Welcome to 'Guess the Number'!
I've selected a number between 1 and 100.
Try to guess it!

Enter your guess: 50
Too low! Try again.

Enter your guess: 75
Too high! Try again.

Enter your guess: 63
Congratulations! You guessed the correct number 63 in 3 attempts.
Thank you for playing 'Guess the Number'!
```

## Code Structure

- **GuessTheNumber.java**: The main file that contains the logic for generating a random number, receiving user input, and providing feedback on the guess.

### Example of `GuessTheNumber.java`

```java
import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        // Generate a random number between 1 and 100
        int targetNumber = random.nextInt(100) + 1;
        int guess = 0;
        int attempts = 0;

        System.out.println("Welcome to 'Guess the Number'!");
        System.out.println("I've selected a number between 1 and 100.");
        System.out.println("Try to guess it!");

        // Loop until the user guesses the correct number
        while (guess != targetNumber) {
            System.out.print("Enter your guess: ");
            guess = scanner.nextInt();
            attempts++;

            if (guess < targetNumber) {
                System.out.println("Too low! Try again.");
            } else if (guess > targetNumber) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You guessed the correct number " + targetNumber + " in " + attempts + " attempts.");
            }
        }

        scanner.close();
        System.out.println("Thank you for playing 'Guess the Number'!");
    }
}
```

## Author

- **Author**: [Deepak P](https://github.com/DeepakPanneerselvam1455)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or contributions, feel free to open an issue or contact the project maintainer.

- **Contact**: [Deepak P](https://github.com/DeepakPanneerselvam1455)
