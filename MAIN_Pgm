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
