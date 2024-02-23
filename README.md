# pangrama


import java.util.Scanner;

public class Pangrama {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Solicita ao usuário que insira a palavra
        System.out.println("Digite uma palavra ou frase:");
        String palavra = scanner.nextLine().toLowerCase();
        
        // Verifica se a palavra é um pangrama
        boolean ehPangrama = true;
        for (char letra = 'a'; letra <= 'z'; letra++) {
            if (!palavra.contains(String.valueOf(letra))) {
                ehPangrama = false;
                break;
            }
        }

        // Exibe o resultado
        if (ehPangrama) {
            System.out.println("A palavra/frase é um pangrama.");
        } else {
            System.out.println("A palavra não é um pangrama.");
        }

        // Fecha o scanner
        scanner.close();
    }
}
