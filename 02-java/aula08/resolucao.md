# Aula 08 - Resolução do exercício

## Exercício 1

`Exercicio1Aula8.java`
```java
class Exercicio1Aula8 {

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
		
		if (media == 10) {
			System.out.println("Aluno aprovado com louvores");
		} else if (media >= 7) {
			System.out.println("Aluno aprovado");
		} else {
			System.out.println("Aluno reprovado");
		}
	}

}
```

## Exercício 2

`Exercicio2Aula8.java`
```java
class Exercicio2Aula8 {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);

		System.out.println("Informe um dia da semana [1-7]");

		int diaSemana = scan.nextInt();

		switch(diaSemana) {
			case 1: 
				System.out.println("Domingo"); 
				break;
			case 2: 
				System.out.println("Segunda-Feira"); 
				break;
			case 3: 
				System.out.println("Terça-Feira"); 
				break;
			case 4: 
				System.out.println("Quarta-Feira"); 
				break;
			case 5: 
				System.out.println("Quinta-Feira"); 
				break;
			case 6: 
				System.out.println("Sexta-Feira"); 
				break;
			case 7: 
				System.out.println("Sábado"); 
				break;
			default: 
				System.out.println("Valor inválido"); 
				break;
		}

	}

}
```

---
👈 [Voltar para aula](aula.md)