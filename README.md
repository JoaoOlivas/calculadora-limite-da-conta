import java.util.Scanner;

public class CalculadoraLimiteConta {

    public static void main(String[] args) {
    
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite o saldo médio da conta corrente: ");
        
        double saldoMedio = scanner.nextDouble();

        double limite = calcularLimite(saldoMedio);

        System.out.println("O limite da conta corrente é: R$" + limite);

        scanner.close();
        
    }

    public static double calcularLimite(double saldoMedio) {
    
        double limite;
        
        if (saldoMedio < 500.0) {
        
            limite = 0.0; 
            
        } else if (saldoMedio <= 1000.0) {
        
            limite = saldoMedio * 0.08; 
            
        } else {
        
            limite = saldoMedio * 0.15; 
            
        }

        return limite;
        
    }
  
}
