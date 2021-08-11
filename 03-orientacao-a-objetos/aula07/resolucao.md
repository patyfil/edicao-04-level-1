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

## Classe com Método Main

`App.java`
```Java
public class App {

    public static void main(String[] args) {
        System.out.println("Teste para verificar a altura do salto do Mario");
        Personagem personagem = new Personagem("Mario", 40, 1.60);
        personagem.imprimeCaracteristicas();
        personagem.saltar();
        System.out.println("---");

        System.out.println("Teste para verificar a altura do salto do Luigi");
        Personagem luigi = new Personagem("Luigi", 40, 1.80);
        luigi.imprimeCaracteristicas();
        luigi.saltar();
        System.out.println("---");
    }
}
```

## Resultado da Execução no Console
```
Teste para verificar a altura do salto do Mario
Personagem{nome='Mario', altura=1.6, idade=40, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Pulando uma altura de 0.8
---
Teste para verificar a altura do salto do Luigi
Personagem{nome='Luigi', altura=1.8, idade=40, estamina=100, quantidadeMoedas=0, quantidadeVidas=1}
Pulando uma altura de 3.6
---
```

---
👈 [Voltar para aula](aula.md)