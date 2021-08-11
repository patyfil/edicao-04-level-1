## Classe Mario

`Mario.java`
```Java
public class Mario {
    private String nome;
    private double altura;
    private int idade;
    private int estamina;

    public Mario() {
        this.nome = "Mario Bros";
        this.altura = 1.50;
        this.idade = 40;
        this.estamina = 100;
    }

    public Mario(String nome, int idade, double altura) {
        this.nome = nome;
        this.altura = altura;
        this.idade = idade;
        this.estamina = 100;
    }

    public void imprimePoderes() {
        System.out.println("Super força, Super salto, super velocidade e outros.");
    }

    public void imprimeCaracteristicas(){
        System.out.println("Mario{" +
                "nome='" + nome + '\'' +
                ", altura=" + altura +
                ", idade=" + idade +
                ", estamina=" + estamina +
                '}');
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public double getAltura() {
        return altura;
    }

    public void setAltura(double altura) {
        this.altura = altura;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }

    public int getEstamina() {
        return estamina;
    }

    public void setEstamina(int estamina) {
        this.estamina = estamina;
    }
}
```

## Classe com Método Main

`App.java`
```Java
public class App {
    public static void main(String[] args) {
        Mario mario = new Mario();
        mario.imprimeCaracteristicas();
        mario.imprimePoderes();
        System.out.println("---");

        Mario mario2 = new Mario("Super Mario", 32, 1.25);
        mario2.imprimeCaracteristicas();
        mario2.imprimePoderes();
        System.out.println("---");

        Mario mario3 = new Mario("Super Mario Bros", 32, 1.25);
        mario3.imprimeCaracteristicas();
        mario3.setNome("Mariozin");
        mario3.setIdade(53);
        mario3.imprimeCaracteristicas();
        mario3.imprimePoderes();
    }
}
```

## Resultado da Execução no Console
```
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Super força, Super salto, super velocidade e outros.
---
Mario{nome='Super Mario', altura=1.25, idade=32, estamina=100}
Super força, Super salto, super velocidade e outros.
---
Mario{nome='Super Mario Bros', altura=1.25, idade=32, estamina=100}
Mario{nome='Mariozin', altura=1.25, idade=53, estamina=100}
Super força, Super salto, super velocidade e outros.
```

---
👈 [Voltar para aula](aula.md)