import java.util.Scanner;

public class ReajusteSalarial {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        // Solicita o salário do colaborador
        System.out.print("Digite o salário do colaborador: R$ ");
        double salario = input.nextDouble();

        double percentualAumento;
        double novoSalario;

        if (salario <= 280.0) {
            percentualAumento = 20;
        } else if (salario <= 700.0) {
            percentualAumento = 15;
        } else if (salario <= 1500.0) {
            percentualAumento = 10;
        } else {
            percentualAumento = 5;
        }

        double aumento = (salario * percentualAumento) / 100;
        novoSalario = salario + aumento;

        // Exibe os resultados
        System.out.println("Salário antes do reajuste: R$ " + salario);
        System.out.println("Percentual de aumento aplicado: " + percentualAumento + "%");
        System.out.println("Valor do aumento: R$ " + aumento);
        System.out.println("Novo salário após o aumento: R$ " + novoSalario);
    }
}

