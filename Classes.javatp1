package projetotp1;

import java.util.Scanner;

public class Classes {
	
	private static String[] nomes;
	private static Double[] notaav1;
	private static Double[]notaav2;
	private static Double[] media;
	
	
	private static int index;
	
	private static final int QTDE = 100;
	
	
	
	public static void main(String[] args) {
		Scanner in= new Scanner(System.in);
		
		nomes = new String[QTDE];
		notaav1 = new Double[QTDE];
		notaav2 = new Double[QTDE];
		
		String opcao = null;
		
		
		
		do {
			System.out.println("[1] Cadastrar");
			System.out.println("[2] Consultarporaluno");
			System.out.println("[3] Consultartodos");
			System.out.println("[4] Sair");
			
			System.out.print("Informe a opçao desejada:  ");
			opcao = in.next();
			int id=index;
		
			switch(opcao) {
				case "1" :
					if(id < QTDE) {
					System.out.println("Informe o nome: ");
					nomes[id] = in.next();
					
					System.out.println("Informe a nota1: ");
					notaav1[id] = in.nextDouble();
					
					System.out.println("Informe a nota2: ");
					notaav2[id] = in.nextDouble();
					imprimir(id);
					
					System.out.println("Aluno Cadastrado com sucess  na posicao:" + index);
					index++;
					
					}else {
						System.out.println("Não existe mais vaga para o cadastramento!!");
					}
					
					
					break;
			
				case "2" :
					System.out.println(" Informe  a posição: ");
					int pos = in.nextInt();
					
					if(pos >= 0 && pos < index) {
					imprimir(pos);
					
					} else {
						System.out.println("O Aluno é Inexistente!");
					}
					
					break;
				
				case "3":
					if(index!=0) {
					imprimir();
					}else {
						System.out.println("Boletim inexistente");
					}
					break;
					
				
				case "4":
					System.out.println("finalizou!");
					
					break;
				
				
				default:
					System.out.println("OpçaoInvalida!!");
					break;
				}
					
		}while(!opcao.equals("4"));
			
		in.close();
	}
				
	private static double media(int idx) {
		return (notaav1[idx] + notaav2[idx])/2;
		}
		
	private static void imprimir() {
		System.out.println("Boletim dos alunos");
		for (int i = 0; i < index; i++) {
		imprimir(i);
		}
	}
	private static void imprimir(int pos) {		
		double mediaFinal = media(pos);
				
		System.out.printf("[%d] %s %.2f - %.2f - %.2f  %s - %n%n",
		pos +1,
		nomes[pos],
		notaav1[pos],
		notaav2[pos],
		mediaFinal,
		situacao(mediaFinal));
						
					
						
	}		
	private static String situacao(double mma) {
		if(mma<4) {
			return "Reprovado";
		}else if(mma>=7) {
			return "Aprovado";
		}else {
			return "Prova Final";
		}
	}
}
	
		
	
	
