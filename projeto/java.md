package projeto;

import java.util.Scanner;

public class Chat {
	public static void main(String[] args) {
		//o Scanner principal do codigo onde vai ler a opção escolhida pelo usuario.
		Scanner opcao = new Scanner(System.in);
		
		//nessa parte é onde o usuario inicia a conversa com o chat.
		opcao.nextLine();
		
		//o comando println vai imprimir as informações de orientação para o usuario.(println pula sempre uma linha) 
		System.out.println("===========OLÁ, SEJA BEM VINDO===========");
		System.out.println("----------Ambiente Skate Shop------------");
		System.out.println("=========================================\n");
		System.out.println("Atendimento Virtual\n");
		System.out.println("Ambiente Goiânia\n");
		System.out.println("Loja de Skate\n");
		System.out.println("Desde 2003 a Ambiente é mais que uma loja.\n");
		System.out.println("Somos ponto de encontro, festas, shows, exposições de arte. E loja.\n");
		//Logo abaixo sera mostrado na tela do usuario 5 opções, que podera ser escolhida de maneira aleatoria pelo usuario.
		System.out.println("===============//=================");
		System.out.println("Escolha o numero da opção desejada:");
		System.out.println("1-Loja Virtual Ambiente.");
		System.out.println("2-Eventos Da Ambiente.");
		System.out.println("3-Como Ter Acesso A Pista de Skate.");
		System.out.println("4-Intagram Da Loja.");
		System.out.println("5-Cadastro Virtual.");
		System.out.println("===============//=================");
		System.out.print("->");
		//logo abaixo foi utilizado a estrutura switch case, onde vai receber o numero inteiro digitado pelo usuario e vai retornar uma das opções escolhidas por ele.
		//caso o usuario escolha uma opção que nao seja de 1 até 5, entao havera um retorno padrao onde vai ser exibido na tela uma mensagem de alerta.
		//logo a baixo foi declarada uma variavel que vai receber o numero digitado pelo usuario no comando scanner.
		int escolha = opcao.nextInt();
		//dentro do parametro do switch colocamos a variavel (escolha) que recebeu o valor do scanner.
		switch (escolha) {
		case 1://cada opcão vai retornar uma ação para o usuario.
			System.out.println("===========Loja Virtual==============");
			System.out.println("https://www.ambienteskateshop.com.br/");
			System.out.println("=====================================");
			break;

		case 2:
			System.out.println("===============Eventos==================");
			System.out.println("The Crew Evento de Skate. (em breve)");
			System.out.println("========================================");
			break;

		case 3:
			System.out.println("========================Pista De Skate======================");
			System.out.println("O acesso da Pista de Skate R$ 50,00.");
			System.out.println("Pagamento Apenas No Local!");
			System.out.println("Trabalhamos com: PIX / CARTÃO DE CREDITO E DEBITO / DINHEIRO.");
			System.out.println("============================================================");
			break;

		case 4:
			System.out.println("================Instagram===================");
			System.out.println("https://www.instagram.com/ambienteskateshop/");
			System.out.println("============================================");
			break;
			
		case 5://Se a Opção escolhida pelo cliente for a 5, o codigo ira pedir as informações do Cliente.
			
			System.out.println("==========Cadastro Do Cliente===============");
			//variaveis.
			String nome;
			int idade;
			String aniversario;
			//Outro Scanner foi criado com o objetivo de armazenar as informações pessoais do usuario.
			Scanner scan = new Scanner(System.in);
			//nesse momento o usuario ira informar as informações pessoais dele e ambas serão salvas nas variaveis criadas acima.
			
			System.out.println("Para realizar o cadastramento é necessario algumas informaçoes pessoais:");
			System.out.print("Informe o seu Nome:");
			nome = scan.nextLine();
			System.out.print("Informe a sua Idade:");
			idade = scan.nextInt();
			System.out.println("Informe a data do seu Aniversario:");
			aniversario = scan.next();
			
			System.out.println("\n");//o comando (\n) pula linhas.
			//a partir daqui, o que foi digitado pelo usuario vai ser retornado e exibido na tela dele.
			System.out.println("Confirme As Informações Cadastradas:");
			System.out.println("Nome: " + nome);//No comando Println concatenamos com o simbolo (+) e retornamos a variavel Nome, que armazena o nome do cliente.
			System.out.println("Idade: " + idade);
			System.out.println("Aniversario: " + aniversario);
			
			//o bot vai perguntar se o usuario vai mesmo querer enviar suas informações
			System.out.println("\nDeseja mesmo enviar suas informações?\n");
			System.out.println("(Digite o numero da opção desejada)");
			System.out.println("1-Sim.\n");
			System.out.println("2-Não.\n");
			//caso a respota for 1=Sim. a maquina vai enviar e finalizar o atendimento.
			//casso a respota for 2=Não. o bot nao vai enviar as informações e finalizar o atendimento.
			
			int enviar;
			enviar = scan.nextInt();
			
			if (enviar == 1) {
				System.out.println("");
				System.out.println("Enviado Com Sucesso!");
				System.out.println("");
				System.out.println("Seu Cadastro Esta Finalizado.");
				System.out.println("Em Caso De Eventos, Promoções e Reposição De Novas Peças, Você será Notificado No WhatsApp.");
				System.out.println("");
				break;
			}
			if (enviar == 2) {
				System.out.println("Não enviado!");
				System.out.println("Cadastro Interrompido.");
				break;
			} else {// se o usuario digitou um numero diferente de 1 ou 2 essa mensagem vai ser exibida.
				System.out.println("Numero Invalido");
				System.out.println("Não é possivel proseguir com o seu Cadastro.");
			}
			break;
			
			default://se o usuario digitar qualquer opção que nao seja de 1 a 5, essa mensagem vai ser exibida na tela dele.
			System.out.println("Numero Invalido");
			System.out.println("Opções encerradas!");
			System.out.println("Tente Novamente!");
		}
		opcao.close();//o scanner (Opção) foi fechado.
	}
}
