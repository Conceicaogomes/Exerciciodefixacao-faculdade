# Exerciciodefixacao-faculdade
import java.util.Scanner;

public class ReajusteSalario {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        
        // Passo 1: Receber o salário do colaborador
        System.out.print("Informe o salário do colaborador: R$ ");
        double salario = input.nextDouble();
        
        // Passo 2: Calcular o reajuste com base nos critérios
        double percentualAumento = 0;
        double valorAumento = 0;
        
        if (salario <= 280.00) {
            percentualAumento = 20;
        } else if (salario <= 700.00) {
            percentualAumento = 15;
        } else if (salario <= 1500.00) {
            percentualAumento = 10;
        } else {
            percentualAumento = 5;
        }
        
        valorAumento = (salario * percentualAumento) / 100.0;
        
        // Passo 3: Calcular o novo salário
        double novoSalario = salario + valorAumento;
        
        // Passo 4: Exibir os resultados
        System.out.println("Salário antes do reajuste: R$ " + salario);
        System.out.println("Percentual de aumento aplicado: " + percentualAumento + "%");
        System.out.println("Valor do aumento: R$ " + valorAumento);
        System.out.println("Novo salário após o aumento: R$ " + novoSalario);
        
        input.close();
    }
}
