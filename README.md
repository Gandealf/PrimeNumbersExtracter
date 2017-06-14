# PrimeNumbersExtracter
//A java application to get prime numbers out between two input numbers


package getprimenumbers;

// This is a program designed to get all prime numbers between two input
//numbers.The purpose Of this program is to practice Basic java programming.
// author@Gandealf

import java.util.Scanner;

public class GetPrimeNumbers {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Type in input a:");
        int integer = 0;
        int integer1 = 0;
        if (scan.hasNextInt()) {

            integer = scan.nextInt();
            System.out.println("input a is:" + integer);
            System.out.println("Type in your input b:");
        } else {
            System.out.println("Not a valid number!");
        }
        Scanner scan1 = new Scanner(System.in);
        if (scan1.hasNextInt()) {

            integer1 = scan1.nextInt();
            System.out.println("input numbers are:" + integer + "," + integer1);

        } else {
            System.out.println("Not a valid number!");

        }

        System.out.println("Prime numbers are:");
        int counter = 0;
        for (int i = integer; i <= integer1; i++) {

            if (IsPrime.isprime(i)) {
                counter++;
                System.out.print(i);
                System.out.print(", ");
                if (counter % 5 == 0) {
                    System.out.println(" ");
                }
            }

        }

    }

}
