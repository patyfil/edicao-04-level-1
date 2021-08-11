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
        System.out.println("Teste para ver se o mario perde estamina");
        Mario mario = new Mario();
        mario.imprimeCaracteristicas();
        mario.perderEstamina();
        mario.imprimeCaracteristicas();
        System.out.println("---");

        System.out.println("Teste para ver se o mario ganha estamina");
        Mario mario2 = new Mario();
        mario2.imprimeCaracteristicas();
        mario2.perderEstamina(); // desconta 10
        mario2.perderEstamina(); // desconta 10
        mario2.ganharEstamina(); // ganhar 5
        mario2.imprimeCaracteristicas();
        System.out.println("---");

        System.out.println("Teste para ver se o mario mantém a estamina em 100 após o acréscimo acima deste valor");
        Mario mario3 = new Mario();
        mario3.imprimeCaracteristicas();
        mario3.ganharEstamina(); // ganhar 5
        mario3.ganharEstamina(); // ganhar 5
        mario3.imprimeCaracteristicas();
        System.out.println("---");

        System.out.println("Teste para ver se o mario mantém a estamina em 0 após o desconto até um valor menor que zero");
        Mario mario4 = new Mario();
        mario4.imprimeCaracteristicas();
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.imprimeCaracteristicas();
        mario4.perderEstamina(); // desconta 10
        mario4.perderEstamina(); // desconta 10
        mario4.imprimeCaracteristicas();
        System.out.println("---");

        System.out.println("Teste para ver se o mario cresce");
        Mario mario5 = new Mario();
        mario5.imprimeCaracteristicas();
        mario5.crescer();
        mario5.imprimeCaracteristicas();
        System.out.println("---");
    }
}
```

## Resultado da Execução no Console
```
Teste para ver se o mario perde estamina
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=90}
---
Teste para ver se o mario ganha estamina
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=85}
---
Teste para ver se o mario mantém a estamina em 100 após o acréscimo acima deste valor
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
---
Teste para ver se o mario mantém a estamina em 0 após o desconto até um valor menor que zero
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=0}
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=0}
---
Teste para ver se o mario cresce
Mario{nome='Mario Bros', altura=1.5, idade=40, estamina=100}
Mario{nome='Mario Bros', altura=3.0, idade=40, estamina=100}
---
```

---
👈 [Voltar para aula](aula.md)