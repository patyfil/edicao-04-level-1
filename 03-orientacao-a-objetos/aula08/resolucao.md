## Classe Mario

`Personagem.java`
```Java
public class Personagem {
    private String nome;
    private double altura;
    private int idade;
    private int estamina;
    private int quantidadeMoedas;
    private int quantidadeVidas;

    public Personagem(String nome, int idade, double altura) {
        this.nome = nome;
        this.altura = altura;
        this.idade = idade;
        this.estamina = 100;
        this.quantidadeMoedas = 0;
        this.quantidadeVidas = 1;
    }

    public void revigorar() {
        this.estamina = 100;
    }

    public void morrer() {
        this.quantidadeVidas--;
        this.estamina = 0;

        if (this.quantidadeVidas < 0) {
            quantidadeVidas = 0;
        } else {
            revigorar();
        }
    }

    public void coletarMoeda() {
        this.quantidadeMoedas++;

        if (this.quantidadeMoedas % 10 == 0) {
            this.quantidadeVidas++;
        }
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
                ", quantidadeMoedas=" + quantidadeMoedas +
                ", quantidadeVidas=" + quantidadeVidas +
                '}');
    }

    public void perderEstamina(){
        this.estamina = this.estamina - 10;
        if (this.estamina < 0) {
            this.estamina = 0;
        }
    }

    public void ganharEstamina(){
        this.estamina = this.estamina + 5;
        if (this.estamina > 100) {
            this.estamina = 100;
        }
    }

    public void crescer() {
        this.altura = this.altura * 2;
    }

    public void saltar() {
        if (this.nome.equals("Mario"))
            System.out.println("Pulando uma altura de " + this.altura * 0.5);
        if (this.nome.equals("Luigi"))
            System.out.println("Pulando uma altura de " + + this.altura * 2);
    }
}
```

## Classe Jogo

`Jogo.java`

```Java
import java.util.Random;

public class Jogo {
    private Personagem jogador1;
    private Personagem jogador2;

    public Jogo(Personagem jogador1, Personagem jogado2) {
        this.jogador1 = jogador1;
        this.jogador2 = jogado2;
    }

    public void jogar() {
        Random geradorAleatorio = new Random();

        int quantidadeColetaJogador1 = geradorAleatorio.nextInt(30);
        for (int i = 0; i < quantidadeColetaJogador1; i++) {
            jogador1.coletarMoeda();
        }

        int quantidadeColetaJogador2 = geradorAleatorio.nextInt(30);
        for (int i = 0; i < quantidadeColetaJogador2; i++) {
            jogador2.coletarMoeda();
        }

        System.out.println("Quantidade de vezes em que o jogador 1 coletou moedas: " + quantidadeColetaJogador1);
        System.out.print("Resultado final do jogador 1: ");
        jogador1.imprimeCaracteristicas();

        System.out.println("Quantidade de vezes em que o jogador 2 coletou moedas: " + quantidadeColetaJogador2);
        System.out.print("Resultado final do jogador 2: ");
        jogador2.imprimeCaracteristicas();
    }
}
```
## Classe com Método Main

`App.java`
```Java
public class App {

    public static void main(String[] args) {
        // Criando o personagem Mario
        Personagem mario = new Personagem("Mario", 40, 1.60);
        // Criando o personagem Luigi
        Personagem luigi = new Personagem("Luigi", 40, 1.80);
        // Criando o jogo
        Jogo jogo = new Jogo(mario, luigi);
        // Executando o jogo
        jogo.jogar();
    }
}
```

## Resultado da Execução no Console
```
Quantidade de vezes em que o jogador 1 coletou moedas: 11
Resultado final do jogador 1: Personagem{nome='Mario', altura=1.6, idade=40, estamina=100, quantidadeMoedas=11, quantidadeVidas=2}
Quantidade de vezes em que o jogador 2 coletou moedas: 22
Resultado final do jogador 2: Personagem{nome='Luigi', altura=1.8, idade=40, estamina=100, quantidadeMoedas=22, quantidadeVidas=3}
```

---
👈 [Voltar para aula](aula.md)