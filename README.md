#Calculadora Java
	
	import java.util.Scanner;

	public class Main {
	    public static void limparTela() {
	        System.out.print("\033[H\033[2J");
	        System.out.flush();
	    }
	    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        Calculos calc = new Calculos();

        while (true){
        System.out.println("Digite a operação (+, -, *, /) ou 'sair':");
        String opcao = scanner.nextLine();
        if(opcao.equals("sair")){
            System.out.println("Saindo");
            break;
        }

        System.out.println("Digite num1 e num2:");
        double a = scanner.nextDouble();
        double b = scanner.nextDouble();
        scanner.nextLine();

        switch (opcao) {
                case "+":
                    calc.Soma(a, b);
                    break;
                case "-":
                    calc.Sub(a, b);
                    break;
                case "*":
                    calc.Mut(a, b);
                    break;
                case "/":
                    calc.Div(a, b);
                    break;
                default:
                    System.out.println("Operação inválida!");
           }
            System.out.println("\nPressione ENTER para continuar...");
            scanner.nextLine();
           limparTela();


        }
    }
}




	   public class Calculos {
	    public  void Soma(double a, double b){
	        System.out.println(a + b);
	    }
	    public void Sub(double a, double b){
	        System.out.println(a - b);
	    }
	    public void Mut(double a, double b){
	        System.out.println(a * b);
	    }
	    public void Div(double a, double b){
	        System.out.println(a / b);
	    }
	
	 public Calculos(){

    }
}
