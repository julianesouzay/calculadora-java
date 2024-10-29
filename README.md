import java.util.Scanner;

public class Calculadora {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int num1, num2;
        double quociente;
        double potencia;

        System.out.print("Digite o primeiro número inteiro: ");
        num1 = scanner.nextInt();

        System.out.print("Digite o segundo número inteiro: ");
        num2 = scanner.nextInt();

        if (num2 != 0) {
            quociente = (double) num1 / num2;
        } else {
            quociente = Double.NaN; // Definir como NaN se a divisão por zero for tentada
            System.out.println("Erro: Divisão por zero não é permitida.");
        }

        potencia = Math.pow(num1, num2);

        System.out.println("O quociente da divisão de " + num1 + " por " + num2 + " é: " + quociente);
        System.out.println(num1 + " elevado à potência de " + num2 + " é: " + potencia);

        scanner.close();
    }
}
