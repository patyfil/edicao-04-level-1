## Classe Mario

`Personagem.java`
```Java
public abstract class Personagem {
    private String nome;
    protected double altura;
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
        System.out.println("Personagem{" +
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

    public abstract void crescer();

    public void saltar() {
        System.out.println(this.nome + " pulou uma altura de " + this.altura * 0.5);
    }

    public void saltar(double alturaObstaculo) {
        System.out.println("Altura do obstaculo: " + alturaObstaculo + ". " + this.nome + " pulou uma altura de " + alturaObstaculo * 1.5);
    }
}
```

## Classe Mario

`Mario.java`
```Java
public class Mario extends Personagem{
    private Yoshi yoshi;

    public Mario(String nome, int idade, double altura) {
        super(nome, idade, altura);
    }

    @Override
    public void crescer() {
        this.altura = this.altura * 1.5;
    }

    public void montarNoYoshi(Yoshi yoshi) {
        this.yoshi = yoshi;
    }

    public void imprimeMontadoYoshi(){
        if (this.yoshi != null) {
            System.out.println("Mario está montado no Yoshi");
        } else {
            System.out.println("Mario não está montado no Yoshi");
        }
    }
}

```

## Classe Luigi

`Luigi.java`
```Java
public class Luigi extends Personagem{
    public Luigi(String nome, int idade, double altura) {
        super(nome, idade, altura);
    }

    @Override
    public void crescer() {
        this.altura = this.altura * 1.75;
    }

    public void voar() {
        System.out.println("Luigi está voando");
    }
}

```

## Classe Yoshi

`Yoshi.java`
```Java
public class Yoshi extends Personagem{
    private int quantidadeFrutasComidas;
    private int velocidade;

    public Yoshi(String nome, int idade, double altura) {
        super(nome, idade, altura);
        this.quantidadeFrutasComidas = 0;
        this.velocidade = 10;
    }

    @Override
    public void crescer() {
        this.altura = this.altura * 1.1;
    }

    public void comerFruta() {
        quantidadeFrutasComidas++;
        if (this.quantidadeFrutasComidas % 2 == 0) {
            this.velocidade *= 2;
        }
    }

    public int getVelocidade() {
        return velocidade;
    }
}

```
## Classe com Método Main

`App.java`
```Java
public class App {

    public static void main(String[] args) {

        /// Criando o personagem Mario
        Mario mario = new Mario("Mario", 40, 1.60);

        // Criando o personagem Luigi
        Luigi luigi = new Luigi("Luigi", 37, 1.80);

        // Criando o personagem Yoshi
        Yoshi yoshi = new Yoshi("Yoshi", 94, 0.85);

        // Teste para verificar altura do Mario após o crescimento
        mario.imprimeCaracteristicas();
        mario.crescer();
        mario.imprimeCaracteristicas();

        // Teste para verificar altura do luigi após o crescimento
        luigi.imprimeCaracteristicas();
        luigi.crescer();
        luigi.imprimeCaracteristicas();

        // Teste para verificar altura do yoshi após o crescimento
        yoshi.imprimeCaracteristicas();
        yoshi.crescer();
        yoshi.imprimeCaracteristicas();

        // Teste para verificar altura do salto padrão
        luigi.saltar();
        mario.saltar();
        yoshi.saltar();

        // Teste para verificar altura do salto sobre obstaculos
        luigi.saltar(2);
        mario.saltar(3);
        yoshi.saltar(10);

    }
}
```

## Resultado da Execução no Console
```
Personagem{nome='Mario', altura=1.6, idade=40, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Personagem{nome='Mario', altura=2.4000000000000004, idade=40, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Personagem{nome='Luigi', altura=1.8, idade=37, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Personagem{nome='Luigi', altura=3.15, idade=37, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Personagem{nome='Yoshi', altura=0.85, idade=94, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Personagem{nome='Yoshi', altura=0.935, idade=94, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Luigi pulou uma altura de 1.575
Mario pulou uma altura de 1.2000000000000002
Yoshi pulou uma altura de 0.4675
Altura do obstaculo: 2.0. Luigi pulou uma altura de 3.0
Altura do obstaculo: 3.0. Mario pulou uma altura de 4.5
Altura do obstaculo: 10.0. Yoshi pulou uma altura de 15.0
```

---
👈 [Voltar para aula](aula.md)