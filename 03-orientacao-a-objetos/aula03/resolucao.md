## Classe Mario

`Mario.java`
```Java
public class Mario {
    public String nome;
    protected double altura;
    private int idade;

    public void imprimeCaracteristicas(){
        System.out.println("Mario{" +
                "nome='" + nome + '\'' +
                ", altura=" + altura +
                ", idade=" + idade +
                "}");
    }

    public void imprimePoderes() {
        System.out.println("Super força, Super salto, super velocidade e outros.");
    }
}
```

## Classe com Método Main

`App.java`
```Java
public class App {
    public static void main(String[] args) {
        Mario mario = new Mario();
        mario.nome = "Mario Bros";
        mario.altura = 1.52;
       // mario.idade = 46; <-- Não é mais possível alterar porque está privado

        mario.imprimeCaracteristicas();
        mario.imprimePoderes();
    }
}
```

## Resultado da Execução no Console
```
Mario: corPele='claro', altura=1.52, idade=46, possuiBigode=true, letraBone=M.
Força sobre-humana, salto sobre-humanos, super velocidade e outros.
```

---
👈 [Voltar para aula](aula.md)