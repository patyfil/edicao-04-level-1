# Aula 10 - Pilares da POO: Polimorfismo

Assista aos vídeos: 

  1. [Polimorfismo - Parte 1](https://youtu.be/9-3-RMEMcq4?t=35)
  1. [Polimorfismo na prática com Java - Parte 1](https://youtu.be/NctjqlfKC0U?t=33)
  1. [Polimorfismo - Parte 2](https://youtu.be/hYek1xqWzgs?t=35)
  1. [Polimorfismo na prática com Java - Parte 2](https://youtu.be/b7xGYh3NHZU?t=34)

> É **#fundamental** que você assista ao vídeo. É **#opcional** _(embora bem interessante)_ que você faça o exercício.

---

## Exercício

Visando exercitar os conceitos de polimorfismo por sobrecarga e sobreposição, vamos aprimorar o nosso projeto do jogo Mario Bros, aprimorando a classe Personagem que ainda possui alguns comportamentos que não comportam a estrutura de herança que implmentamos nas aulas anteriores. Para refina-la, vamos utilizar as ideias do polimorfismo e aplicar as regras nas suas respectivas classes especializadas

### Sobreposição
* Vamos aprimorar o método de crescer, pois cada personagem cresce para um tamanho diferente.
  * Torne o método crescer abstrado e código a regra de crescimento nas classes especializadas conforme decrito a seguir.
  * Para o Mario, quando ele crescer, sua nova altura é 50% maior que a sua altura atual.
  * Para o Luigi, quando ele crescer, sua nova altura são 75% maior que a sua altura atual.
  * Para o Yoshi, quando ele crescer, sua nova altura é 10% maior que a sua altura atual.
  * Note que para isso você precisará tornar a sua altura acessível para as classes filhas. Lembra dos modificadores de acesso vistos na aula 3? Revise-os caso não lembre, pois precisará aqui.

### Sobrecarga
* Vamos atualizar o comportamento do metodo de saltar. Agora os personagens poderão saltar e saltar sobre obstaculos.
  * Atualize o metodo `saltar()` para que ele imprima uma mensagem de que o personagem está pulando 50% da sua altura.
  * Crie uma sobregcarga do metodo `saltar()` para que ele pule uma altura 50% maior que o altura do objeto a sua frente. A altura do objeto será recebida como parâmetro nesta sobrecarga.

_**Após** fazer o exercício, dá uma conferida na [nossa solução](resolucao.md)._

---

👈 [Voltar para aula anterior](../aula09/aula.md)
👈 [Voltar para o índice](../README.md)