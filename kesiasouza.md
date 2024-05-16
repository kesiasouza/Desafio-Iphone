import java.util.Scanner;

import apps.internet.Internet;
import apps.midia.Ipod;
import apps.phone.Phone;

public class IPhone {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.println("Escolha um app: 1: Ipod; 2: Phone; 3: Internet; 0: Sair");
            int app = scanner.nextInt();
            if (app == 1) {
                ipod();
            } else if (app == 2) {
                phone();
            } else if (app == 3) {
                internet();
            } else {
                System.out.println("Você escolheu desligar o seu Iphone");
                System.exit(0);
            }
        }

    }

    static void ipod() {
        Ipod ipod = new Ipod();
        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.println("1: Escolher uma musica, 2: Tocar e 3: Pausar; 0: Sair");
            int app = scanner.nextInt();
            if (app == 1) {
                ipod.selecionarMusica();
            } else if (app == 2) {
                ipod.tocar();
            } else if (app == 3) {
                ipod.pausar();
            } else {
                System.out.println("Fechar aplicativo");
                break;
            }
        }

    }

    static void phone() {
        Phone appPhone = new Phone();
        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.println("1: Ligar; 2: Atender; 3: Inicar correio; 0: Sair");
            int app = scanner.nextInt();
            if (app == 1) {
                appPhone.ligar();
            } else if (app == 2) {
                appPhone.atender();
            } else if (app == 3) {
                appPhone.iniciarCorreioVoz();
            } else {
                System.out.println("Fechar aplicativo");
                break;
            }
        }

    }

    static void internet() {
        Internet net = new Internet();
        Scanner scanner = new Scanner(System.in);
        while (true) {
            System.out.println("1: Exibir pagina; 2: Adicionar nova aba; e 3: Atualizar pagina; 0: Sair");
            int app = scanner.nextInt();
            if (app == 1) {
                net.exibirPagina();
            } else if (app == 2) {
                net.adicionarNovaAba();
            } else if (app == 3) {
                net.atualizarPagina();
            } else {
                System.out.println("Fechar aplicativo");
                break;
            }
        }

    }
}
