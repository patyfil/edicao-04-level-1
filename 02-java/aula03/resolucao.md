# Aula 03 - Resolução do exercício

A ideia aqui é receber algum parâmetro ao executar o programa e exibir o valor deste parâmetro dentro do nosso texto.

`AlunoResetComParametro.java`
```java
class AlunoResetComParametro {

    public static void main(String[] args) {
        System.out.println("Sou aluno do Level 1 do CWI Reset! Me chamo "+ args[0]);
    }

}
```

```sh
javac AlunoResetComParametro.java
java AlunoResetComParametro Alexandre
Sou aluno do Level 1 do CWI Reset! Me chamo Alexandre
```

---
👈 [Voltar para aula](aula.md)