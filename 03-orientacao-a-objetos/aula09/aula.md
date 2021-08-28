# Aula 09 - Pilares da POO: Herança

Assista aos vídeos: 

  1. [Herança - Parte 1](https://youtu.be/_PZldwo0vVo?t=34)
  1. [Herança na prática com Java - Parte 1](https://youtu.be/19IGAeoFKlU?t=33)
  1. [Herança - Parte 2](https://youtu.be/He887D2WGVw?t=33)
  1. [Herança na prática com Java - Parte 2](https://youtu.be/5pwV2WdD-_Y?t=34)

> É **#fundamental** que você assista ao vídeo. É **#opcional** _(embora bem interessante)_ que você faça o exercício.

---

## Exercício

![yoshi](https://playreplay.com.br/wp-content/uploads/2017/09/mario-socando-yoshi.jpg)


O **Yoshi** teve sua primeira aparição na aventura de Mario pelo Mundo dos Dinossauros em Super Mario World. Linguarudo e de fala estranha, o pequeno dinossauro logo se tornou um dos principais parceiros de Mario em suas aventuras pelos mundos mágicos criados pela Nintendo, ajudando e protegendo o nosso herói bigodudo de barriga avantajada. Determinado, corajoso, amigável e positivo, Yoshi sempre está disposto a ajudar seus amigos em qualquer situação. Por diversas vezes salvou sua ilha derrotando o King Bowser Koopa. Quando assume uma tarefa, só pára quando a cumpre por completo. Assim como nosso herói pançudo, Yoshi tem um apetite incrível, mas se restringe a comer frutas (principalmente melão). Com tamanho carisma, Yoshi logo se tornou dos personagens mais queridos e marcantes de toda a franquia Mario.

### Atividade

Baseado nos aprendizados sobre herança vistos nesta aula, vamos tonar o Mario, o Luigi e o Yoshi personagens especializados da classe jogador. Desta forma, passarão a compartilhar dos mesmos atributos e comportamentos da classe jogador, mas terão suas próprias características.

### Nível 1
* Torne a classe `Personagem` abstrata.
* Crie a classe `Mario` que extende `Personagem`.
* Crie a classe `Luigi` que extende `Personagem`.
* Crie a classe `Yoshi` que extende `Personagem`.
* Tente instanciar um objeto do tipo Personagem e veja o que acontece.

### Nível 2
* Para o `Mario`:
  * Adicione um atributo do tipo `Yoshi`.
  * Crie um método `montarNoYoshi()` que recebe um `Yoshi` como parâmetro.
    * Este metodo registra o `Yoshi` recebido no seu respectivo atributo.
  * Crie um método que imprime se o Mario está montado no `Yoshi`.
* Para o Luigi
  * Crie um método `voar()` que simplesmente imprime uma mensagem "Luigi está voando".

### Nível 3
* Para o `Yoshi`:
  * Crie um atributo para registrar a quantidade de frutas que ele come e que deve ser inicializado com 0.
  * Crie um atributo para registrar a velocidade e que deve ser inicializado com 10;
  * Crie um método `get` para a velocidade.
  * Crie um método `comerFruta()` que acrescenta 1 na quantidade de frutas comidas.
    * A cada 2 frutas, a velocidade do Yoshi dobra.

Por fim, crie uma classe com método `main()`, instancie objetos do Mario, do Luigi, do Yoshi e teste sua implementação.

_**Após** fazer o exercício, dá uma conferida na [nossa solução](resolucao.md)._

Fonte: [nintendoblast](https://www.nintendoblast.com.br/2009/05/perfil-yoshi.html).

---

👈 [Voltar para aula anterior](../aula08/aula.md) ..... [Avançar para próxima aula](../aula10/aula.md) 👉    