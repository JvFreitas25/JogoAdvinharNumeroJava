# JogoAdvinharNumeroJava
Olá me chamo João Victor, montei esse código no intuito de ser um mini game que dá pra brincar com seus amigos. O intuito é você declarar o número que deve ser advinhado em uma variável e criar um loop em que o usuário tenha 10 chances, a cada chance que ele errar você deve imprimir se o número secreto é &lt; ou > do que o número que ele digitou.

package ExerciciosDeControle;

import java.util.Scanner;

public class JogoDaAdivinhacao {
	public static void main(String[] args) {
		Scanner entrada = new Scanner(System.in);
		int numero = 37;
		int resposta;
		for(int i = 10; i >= 1; i--) {
			System.out.printf("Voçê tem %d tentativas restantes.\n",i);
			System.out.print("Adivinhe o número: ");
			resposta = entrada.nextInt();
			entrada.nextLine();
			if(resposta != numero) {
				System.out.println("Tente novamente!");
			}
			if(resposta == numero) {
				System.out.println("PARABÉNS, VOCÊ ACERTOU!!!!");
				break;
			} else if(resposta > numero){
				System.out.printf("O número é menor que %d.%n", resposta);
				System.out.println("");
			} else if(resposta < numero) {
				System.out.printf("O número é maior que %d.%n", resposta);
				System.out.println("");
			}
			if(i==1) {
				System.out.println("As suas chances acabaram, o número era "+ numero);
			}
		}
		entrada.close();
	}
}
