# Exp.Array
Funções básicas de Array! Prática referente a 2ª atividade da II unid. de LP1 
//O guichê de pedágio de uma rodovia possui um equipamento que registra diariamente a quantidade de carros
// que passaram. Faça um programa para ler cada registro do mês de setembro e informar qual o maior volume de
// carros que passou e em qual dia do mês.

import java.util.Scanner;

public class ExpPedagio {
    public static void main (String [] args){
        Scanner leitor = new Scanner(System.in);

        int[] Setembro = new int[30];
        for(int i = 0; i < Setembro.length; i++) {
            System.out.println("Insira a quantidade de carros do dia: " + (i + 1));
            Setembro[i] = leitor.nextInt();
        }
        int maiorQuantidade = Setembro[0];
        int diaMaiorQuantidade = 0;

        for(int i = 0; i < Setembro.length; i++){
          if(Setembro[i] > maiorQuantidade){
              maiorQuantidade = Setembro [i];
              diaMaiorQuantidade = i;
          }
        }
        System.out.println("A maior quantidade de foi de: " + maiorQuantidade + " carros no dia" + diaMaiorQuantidade);
    }
}
