import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();

        boolean playAgain = true;
        while (playAgain) {
            int targetNumber = random.nextInt(100) + 1;
            int guess = 0;
            
            System.out.println("1부터 100 사이의 숫자를 맞추시오");

            while (guess != targetNumber) {
                System.out.print("숫자를 입력하세요: ");
                
                String input = scanner.next();
                
                try {
                    guess = Integer.parseInt(input);
                    
                    if (guess > targetNumber) {
                        System.out.println("더 낮게");
                    } else if (guess < targetNumber) {
                        System.out.println("더 높게");
                    } else {
                        System.out.println("맞았습니다!");
                    }
                } catch (NumberFormatException e) {
                    System.out.println("올바른 숫자를 입력하세요!");
                }
            }

            System.out.print("게임을 다시 하시겠습니까? (y/n): ");
            char response = scanner.next().charAt(0);
            
            if (response == 'y' || response == 'Y') {
                playAgain = true;
            } else {
                playAgain = false;
            }
        }

        System.out.println("게임을 종료합니다.");
        scanner.close();
    }
}
