## Classe Mario

`Personagem.java`
```Java
public abstract class Personagem {
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

## Classe Mario

`Mario.java`
```Java
public class Mario extends Personagem{
    private Yoshi yoshi;

    public Mario(String nome, int idade, double altura) {
        super(nome, idade, altura);
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
        
        // Tentando instanciar um objeto do tipo Personagem, mas não é possível porque a classe é abstrata. Por isso, a linha está comentada.
        //Personagem personagem = new Personagem("Mario", 40, 1.60);
        
        // Criando o personagem Mario
        Mario mario = new Mario("Mario", 40, 1.60);

        // Criando o personagem Luigi
        Luigi luigi = new Luigi("Luigi", 37, 1.80);

        // Criando o personagem Yoshi
        Yoshi yoshi = new Yoshi("Yoshi", 94, 0.85);

        // Teste para verificar se o Mario monta no Yoshi
        mario.imprimeMontadoYoshi();
        mario.montarNoYoshi(yoshi);
        mario.imprimeMontadoYoshi();

        // Teste para verificar se o Luigi voa
        luigi.voar();

        // Teste para verificar se a velocidade do yoshi aumenta a cada 2 frutas comidas
        System.out.println("Velocidade atual: " + yoshi.getVelocidade());
        yoshi.comerFruta();
        System.out.println("Velocidade atual: " + yoshi.getVelocidade());
        yoshi.comerFruta();
        System.out.println("Velocidade atual: " + yoshi.getVelocidade());
        yoshi.comerFruta();
        yoshi.comerFruta();
        System.out.println("Velocidade atual: " + yoshi.getVelocidade());
    }
}
```

## Resultado da Execução no Console
```
Mario não está montado no Yoshi
Mario está montado no Yoshi
Luigi está voando
Velocidade atual: 10
Velocidade atual: 10
Velocidade atual: 20
Velocidade atual: 40
```

---
👈 [Voltar para aula](aula.md)