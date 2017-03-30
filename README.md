# Deliverable-2

package com.jetbrains;

import java.util.Scanner;

import java.time.LocalDate;

import java.time.Period;

public class Main {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in); // this will allow user to input their own date.

        System.out.print("Enter the oldest date in YYYY-MM-DD: "); // directions for user to input an older date.

        String oldestDateString = scanner.nextLine();

        LocalDate oldestDate = LocalDate.parse(oldestDateString); // this will calculate the oldest userInput date.

        System.out.print("Enter a newer in YYYY-MM-DD: "); // directions for user to input a more recent date.

        String newestDateString = scanner.nextLine();

        LocalDate newestDate = LocalDate.parse(newestDateString); // this will calculate the newer date.


        Period difference = oldestDate.until(newestDate); // this will calculate the difference between the oldest and newest date.

        int days = difference.getDays(); // this will calculate difference in days
        int months = difference.getMonths(); // this will calculate difference in months
        int years = difference.getYears(); // this will calculate difference in years
        scanner.close();

        System.out.println("The time difference between these dates are: " + months + " Months, " + days + " Days, and " + years + " Years."); // this will show the time difference in Months, Days, and Years.
    }
}
