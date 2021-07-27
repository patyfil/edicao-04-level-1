# Aula 07 - Resolução do exercício

## Exercício 1

`Exercicio1Aula7.java`
```java
import java.util.Scanner;

class Exercicio1Aula7 {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		System.out.println("Informe o primeiro número");
		int primeiroNumero = scan.nextInt();
		
		System.out.println("Informe o segundo número");
		int segundoNumero = scan.nextInt();

		int resultado = primeiroNumero + segundoNumero;

		System.out.println("A soma dos números é " + resultado);
	}

}
```

## Exercício 2

`Exercicio2Aula7.java`
```java
import java.util.Scanner;

class Exercicio2Aula7 {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		System.out.println("Informe a primeira nota");
		double primeiraNota = scan.nextDouble();
		
		System.out.println("Informe a segunda nota");
		double segundaNota = scan.nextDouble();

		System.out.println("Informe a terceira nota");
		double terceiraNota = scan.nextDouble();

		System.out.println("Informe a quarta nota");
		double quartaNota = scan.nextDouble();

		double media = (primeiraNota + segundaNota + terceiraNota + quartaNota) / 4;
		System.out.println("A média é " + media);

	}

}
```

## Exercício 3

`Exercicio3Aula7.java`
```java
import java.util.Scanner;

class Exercicio3Aula7 {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		System.out.println("Informe o valor/hora");
		double valorHora = scan.nextDouble();
		
		System.out.println("Informe a quantidade de horas trabalhadas");
		double horasTrabalhadas = scan.nextDouble();

		double salario = valorHora * horasTrabalhadas;

		System.out.println("O salário é " + salario);
	}

}
```

---
👈 [Voltar para aula](aula.md)