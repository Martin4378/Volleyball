# Volleyball

import java.util.Scanner;

public class P35_Volleyball {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String typeYear = scanner.nextLine();
        int holidaysInYear = Integer.parseInt(scanner.nextLine());
        int daysGoingHome = Integer.parseInt(scanner.nextLine());
        int daysInSofia = 48 - daysGoingHome;

        double daysPlayHoliday = holidaysInYear * 2.0 / 3;
        double daysPlaySofia = daysInSofia * 3.0 / 4;
        double daysOfPlay = daysPlaySofia+ daysGoingHome + daysPlayHoliday;
        double bonusLeapPlay = daysOfPlay * 15 / 100;
        double sumDays = 0;

        if (typeYear.equalsIgnoreCase("leap")){

            sumDays = daysOfPlay + bonusLeapPlay;

        }

        else if (typeYear.equalsIgnoreCase("normal")){

            sumDays = daysOfPlay;

        }


        System.out.println(Math.floor(sumDays));



    }

}
