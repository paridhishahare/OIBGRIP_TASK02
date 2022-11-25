# OIBGRIP_TASK02
//NAME: PARIDHI SHAHARE
*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 * Click nbfs://nbhost/SystemFileSystem/Templates/Project/Maven2/JavaApp/src/main/java/${packagePath}/${mainClassName}.java to edit this template
 */

package com.mycompany.numberguessing;



/**
 *
 * @author paridhi
 */
import java.util.Random;
 import java.util.Scanner;
public class number_guessing
{
    public static void main(String args[])
    {

        int ans, guess, guessNum =0;
        final int maxGuesses = 5;
        String str, playAgain = "y";

        Scanner scan = new Scanner(System.in);
        Random generator = new Random();
        ans = generator.nextInt(101) + 1;

        while 
           (playAgain.equals("y") || playAgain.equals("Y"))
        {
            System.out.println("Hey!! WELCOME TO THE NUMBER GUESSING GAME");
            System.out.println("\nGuess a number from 0 to 100");
            System.out.println("Guess a number (0 to quit):");

            guess = scan.nextInt();
            guessNum = 0;
            while (guess != 0)
            {
                guessNum++;
                if (guess == ans) 
                {
                    System.out.println("CONGRATS! You got it Right!");
                    break;
                } 
                else if (guess < ans)
                    System.out.println("Opss! Your guess was too LOW,Don't loose Hope!! Please try some higher numbers.");
                else if (guess > ans)
                    System.out.println("Opss! Your guess was too HIGH,Don't loose Hope!! Please try some lower numbers");
                if (guessNum == maxGuesses)
                {
                    System.out.println("The number was " + ans +""
                            + "\n Thank you!! Better luck next time");
                    break;
                }
                System.out.println("Enter your guess (0 to quit):");
                guess = scan.nextInt();
            }
            System.out.println(" Hey!! do you Want to Play again?(y/n)");
            playAgain = scan.next();
        }
        System.out.println("Thanks for playing!");
    }
}
