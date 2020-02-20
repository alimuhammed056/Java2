
import java.util.Scanner;

/*

 */
public class NewClass3 {
    boolean b = true;
    public void userInput() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter 1st number");
        int x = sc.nextInt();
        System.out.println("Enter 2nd number");
        int y = sc.nextInt();
        System.out.println("Enter operator");
        String op = sc.next();

        int result = calc(x, y, op);
        if(b)
        System.out.println(result);

    }

    public int calc(int x, int y, String op) {
        int result = 0;
        switch (op) {
            case "+":
                result = x + y;
                break;
            case "-":
                result = x - y;
                break;
            case "*":
                result = x * y;
                break;
            case "/":
                if (y != 0) {
                    result = x / y;
                } else {
                    b = false;
                    System.out.println("Can't divid by zero");
                }
                break;
            default:
                b = false;
                System.out.println("Unknown operator");
        }

        return result;
    }
}
