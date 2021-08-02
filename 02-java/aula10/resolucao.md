# Aula 10 - Resolução dos exercícios

## Exercício 1

`Exercicio1Aula10.java`
```java
import java.util.Scanner;

class Exercicio1Aula10 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        int[] primeiroVetor = new int[5];
        for (int i = 0; i < primeiroVetor.length; i++) {
            System.out.println("Informa o valor da posição " + i);
            primeiroVetor[i] = scan.nextInt();
        }

        int[] segundoVetor = new int[primeiroVetor.length];
        for (int i = 0; i < primeiroVetor.length; i++) {
            segundoVetor[i] = primeiroVetor[i] * 2;
        }

        System.out.println("Primeiro Vetor: ");
        for (int item : primeiroVetor) {
            System.out.println(item);
        }

        System.out.println("Segundo Vetor: ");
        for (int item : segundoVetor) {
            System.out.println(item);
        }

    }

}
```

## Exercício 2

`Exercicio2Aula10.java`
```java
import java.util.Scanner;

class Exercicio2Aula10 {

    public static void main(String[] args) {

        Scanner scan = new Scanner(System.in);

        int[] idades = new int[10];
        for (int i = 0; i < idades.length; i++) {
            System.out.println("Informa a idade da pessoa de número " + i);
            idades[i] = scan.nextInt();
        }

        int quantidadeDeIdadesMaior = 0;
        for (int idade : idades) {
            if (idade >= 18) {
                quantidadeDeIdadesMaior++;
            }
        }

        System.out.println("Idades computadas:");
        for (int idade : idades) {
            System.out.println(idade);
        }
        System.out.println("---");

        System.out.println("Quantidade de pessoas maiores de idade: " + quantidadeDeIdadesMaior);

    }

}

```

---
👈 [Voltar para aula](aula.md)