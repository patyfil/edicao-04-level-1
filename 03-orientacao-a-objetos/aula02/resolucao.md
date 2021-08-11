## Classe Mario

`Mario.java`
```Java
public class Mario {
    String nome;
    double altura;
    int idade;

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
        mario.idade = 46;

        mario.imprimeCaracteristicas();
        mario.imprimePoderes();
    }
}
```

## Resultado da Execução no Console
```
Mario{nome='Mario Bros', altura=1.52, idade=46}
Super força, Super salto, super velocidade e outros.
```

---
👈 [Voltar para aula](aula.md)