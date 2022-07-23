// Amgstrong-number-in-limit
import java.util.Scanner;

public class amg {

    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int num, digits, result, originalNumber;

        System.out.println("Enter the limit:");
        num = s.nextInt();

        for (int number = 10; number < num; ++number) {
            digits = 0;
            result = 0;
            originalNumber = number;

            for (; originalNumber != 0;) {
                originalNumber = originalNumber / 10;
                ++digits;
            }

            originalNumber = number;

            for (; originalNumber != 0;) {
                int remainder = originalNumber % 10;
                result += Math.pow(remainder, digits);
                originalNumber /= 10;
            }

            if (result == number) {
                System.out.print(number + " ");
            }
        }
    }
}
