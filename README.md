import java.util.ArrayList;
import java.util.Scanner;

public class CadastroUsuarios {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        ArrayList<String> usuarios = new ArrayList<>();
        int opcao;

        do {
            System.out.println("\n=== MENU ===");
            System.out.println("1 - Cadastrar usuário");
            System.out.println("2 - Listar usuários");
            System.out.println("0 - Sair");
            System.out.print("Escolha uma opção: ");
            opcao = scanner.nextInt();
            scanner.nextLine();

            switch (opcao) {
                case 1:
                    System.out.print("Digite o nome do usuário: ");
                    String nome = scanner.nextLine();
                    usuarios.add(nome);
                    System.out.println("Usuário cadastrado com sucesso!");
                    break;
                case 2:
                    System.out.println("\nUsuários cadastrados:");
                    for (String u : usuarios) {
                        System.out.println("- " + u);
                    }
                    break;
                case 0:
                    System.out.println("Encerrando o sistema...");
                    break;
                default:
                    System.out.println("Opção inválida.");
            }
        } while (opcao != 0);

        scanner.close();
    }
}
