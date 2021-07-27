# Aula 06 - Resolução do exercício

A ideia aqui é alterar o programa da aula 3 e fazer com que o usuário indique o nome durante a execução do programa. Observe que apresentamos uma descrição "Nome:" antes de solicitar a leitura, para que o usuário perceba que algo está sendo solicitado.

`AlunoResetLeituraTeclado.java`
```java
import java.util.Scanner;

class AlunoResetLeituraTeclado {

	public static void main(String[] args) {
		System.out.println("Nome: ");
		Scanner sc = new Scanner(System.in);
		String nome = sc.nextLine();
		System.out.println("Sou aluno do Level 1 do CWI Reset! Me chamo " + nome);
	}

}
```

```sh
javac AlunoResetLeituraTeclado.java
java AlunoResetLeituraTeclado Alexandre
Sou aluno do Level 1 do CWI Reset! Me chamo Alexandre
```

---
👈 [Voltar para aula](aula.md)