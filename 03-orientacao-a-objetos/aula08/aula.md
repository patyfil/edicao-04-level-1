# Aula 08 - Relacionamento de Agregação

Assista aos vídeos: 

  1. [Relacionamento de Agregação](https://youtu.be/ERdvijGtrq0?t=61)
  1. [Agregação entre Objetos com Java](https://youtu.be/8R9RpqpXI_c?t=34)

> É **#fundamental** que você assista ao vídeo. É **#opcional** _(embora bem interessante)_ que você faça o exercício.

---

## Exercício

Baseado no conteúdo visto nas últimas aulas, vamos criar um simulador simples do jogo onde os personagens apenas vão coletar moedas ao longo da execução. Para isso, vamos criar a classe que simula uma execução do jogo contendo os 2 personagens no cenário. Neste simulador, vamos coletar um numero aleatório de moedas e imprimir os dados dos jogadores no console após o término da partida. Siga o roteiro de implementação abaixo.

### Nivel 1
* Crie a classe `Jogo` com o seguinte modelo:
  * Deverá conter dois jogadores (`jogador1` e `jogador2`), ambos do tipo `Personagem`.
  * Deverá ter um construtor que recebe os dois personagens e os armazene no `jogador1` e `jogador2`.
  * Deverá ter um método que imprime os dados dos personagens do jogo.

### Nível 2
  * Deverá ter um método `jogar()` que coloca os dois jogadores a coletar moedas em um número aleatório entre 0 e 30 de repetições.
    * Deverá ser impressa a quantidade de vezes em que os jogadores coletaram moedas.
    * No final da execução deste método, deverão ser impressos os dados dos personagens do jogo para que possam ser verificadas a vida e a quantidade de moedas adquiridas ao longo da partida.

Por fim, crie uma classe com método `main()`, instancie objetos do Mario e do Luigi, crie uma instancia do jogo, simule o a execução do jogo por meio do método `jogar()` e teste sua implementação.

_**Após** fazer o exercício, dá uma conferida na [nossa solução](resolucao.md)._

---

👈 [Voltar para aula anterior](../aula07/aula.md) ..... [Avançar para próxima aula](../aula09/aula.md) 👉    