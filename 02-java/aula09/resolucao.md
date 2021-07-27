# Aula 09 - Resolução do exercício

## Exercício 1

`Exercicio1Aula9.java`
```java
import java.util.Scanner;

class Exercicio1Aula9 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        System.out.println("Informe uma nota entre zero e dez: ");

        boolean notaValida = false;
        do {
            double notaInformada = scan.nextDouble();
            if (notaInformada >= 0 && notaInformada <= 10) {
                notaValida = true;
                System.out.println("Nota válida: " + notaInformada);
            } else {
                System.out.println("Nota inválida! Informe uma nota entre zero e dez.");
            }

        } while (!notaValida);

    }

}
```

## Exercício 2

`Exercicio2Aula9.java`
```java
import java.util.Scanner;

class Exercicio2Aula9 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        System.out.println("Informe a número inicial: ");
        int valorInicial = scan.nextInt();

        boolean valorFinalMaiorQueInicial = false;
        int valorFinal = 0;
        do {
            System.out.println("Informe a número final: ");
            valorFinal = scan.nextInt();
            if (valorFinal > valorInicial) {
                valorFinalMaiorQueInicial = true;
            } else {
                System.out.println("O número final precisa ser maior que o inicial.");
            }
        } while (!valorFinalMaiorQueInicial);

        for (int i = valorInicial; i <= valorFinal; i++) {
            System.out.println(i);
        }
    }

}
```

## Exercício 3

`Exercicio3Aula9.java`
```java
import java.util.Scanner;

class Exercicio3Aula9 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        int numero;
        int maior = Integer.MIN_VALUE; // Inicia o valor com o menor número possível.

        for (int i = 0; i < 5; i++) {
            System.out.println("Informe um número: ");
            numero = scan.nextInt();

            if (numero > maior) {
                maior = numero;
            }
        }

        System.out.println("O maior número informado foi " + maior);
    }

}
```

## Exercício 4

`Exercicio4Aula9.java`
```java
import java.util.Scanner;

class Exercicio4Aula9 {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        System.out.println("Informe o número que deseja gerar a tabuada:");
        int numero = scan.nextInt();

        System.out.println("Tabuada do " + numero);

        for (int i = 1; i <= 10; i++) {
            System.out.println(numero + " x " + i + " = " + numero*i);
        }
    }
}
```

---
👈 [Voltar para aula](aula.md)