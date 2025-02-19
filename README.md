import java.util.Scanner;

public class Ac2 {

    public static void main(String[] args) {

        Scanner scn = new Scanner(System.in);

        double pesoAc1, pesoAc2, pesoAg, pesoAf;
        double ac1, ac2, ag, af;
        double notaCorte, media;

        // Entrada dos pesos
        System.out.println("Adicione os pesos das avaliacoes Ac1:");
        pesoAc1 = scn.nextDouble();
        System.out.println("Ac2:");
        pesoAc2 = scn.nextDouble();
        System.out.println("Ag:");
        pesoAg = scn.nextDouble();
        System.out.println("Af:");
        pesoAf = scn.nextDouble();

        // Entrada das notas
        System.out.println("Adicione as notas Ac1:");
        ac1 = scn.nextDouble();
        System.out.println("Ac2 :");
        ac2 = scn.nextDouble();
        System.out.println("Ag :");
        ag = scn.nextDouble();
        System.out.println("Af :");
        af = scn.nextDouble();

        // Entrada da nota de corte
        System.out.println("Adicione a nota de corte:");
        notaCorte = scn.nextDouble();

        // Cálculo da média ponderada
        media = (pesoAc1 / 100 * ac1) + (pesoAc2 / 100 * ac2) + (pesoAg / 100 * ag) + (pesoAf / 100 * af);

        // Verificação se a média é suficiente para aprovação
        if (media >= notaCorte) {
            System.out.println("Passou com média: " + media);
        } else {
            System.out.println("Reprovou com média: " + media);
        }
        boolean repetir;//para repetir ou não 

        do{//faz a ação

        System.out.println("deseja fazer uma nova conta com o mesmo peso e nota de corte? (s/n):");
        char resposta = scn.next().charAt(0);//booleano de falso ou verdadeiro
        repetir = (resposta == 's' || resposta == 'S');

        System.out.println("Adicione as notas ac1:");
        ac1 = scn.nextDouble();
        System.out.println("ac2 :");
        ac2 = scn.nextDouble();
        System.out.println("ag :");
        ag = scn.nextDouble();
        System.out.println("af :");
        af = scn.nextDouble();
        media = (pesoAc1 / 100 * ac1) + (pesoAc2 / 100 * ac2) + (pesoAg / 100 * ag) + (pesoAf / 100 * af);

            if (media >= notaCorte) {
                System.out.println("Passou com média: " + media);
            } else {
            System.out.println("Reprovou com média: " + media);
            }


        }while (repetir);//repetir a ação
        scn.close(); // Fechando o scanner

    }
}
