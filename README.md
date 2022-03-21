import java.util.Scanner;

public class cal {
    public static void main(String[] args) throws Exception {
        Scanner in = new Scanner(System.in);
        System.out.print("Input first number: ");
        double firstNumber = in.nextDouble();
        System.out.print("Input sign: ");
        String sign = in.next();
        if ((sign.equals("-") || sign.equals("*") || sign.equals("+") || sign.equals("/"))){
            System.out.print("Input second number: ");
            double secondNumber = in.nextDouble();
            double result;
                if (secondNumber == 0 && sign.equals("/")) {
                    System.out.print("Poshol ****");
                    return;
                }
            if (sign.equals("/"))
                result = firstNumber / secondNumber;
            else if (sign.equals("*"))
                result = firstNumber * secondNumber;
            else if (sign.equals("+"))
                result = firstNumber + secondNumber;
            else
                result = firstNumber - secondNumber;
            System.out.format("%f %s %f = %f", firstNumber, sign, secondNumber, result);

        }
        else {
            System.out.print("Wrong sign");
        }


    }
}
