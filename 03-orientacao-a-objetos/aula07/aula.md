# Aula 07 - Relacionamento entre Classes

Assista aos vídeos: 

  1. [Relacionamento entre Classes](https://youtu.be/GLHbxDU9iBA?t=98)
  1. [Objetos Compostos em Java](https://youtu.be/BfrbCQ3XcrA?t=34)

> É **#fundamental** que você assista ao vídeo. É **#opcional** _(embora bem interessante)_ que você faça o exercício.

---

## Exercício

![Luigi](https://lh6.ggpht.com/-KFZvUxoCM3w/TjdVSdTBbYI/AAAAAAAAA04/jy-GNdnHi40/Luigi_thumb%25255B1%25255D.png?imgmax=800)

Em **Mario Bros**, Luigi é apenas uma troca de paleta de cores de Mario com os mesmos controles e habilidades sem diferenças físicas. Mario e Luigi são retratados como encanadores onde tentam se livrar de monstros nos esgotos.

Em **Super Mario Bros**, os irmãos vão ao Reino do Cogumelo para salvar a Princesa Toadstool que fora capturada pelo terrível Bowser. Neste jogo Luigi tinha os mesmos poderes de Mario e mesma velocidade, incluindo Power-Ups. Também uma troca de paleta apenas para ter um modo de dois jogadores. Em **The Lost Levels**, não havia a opção de dois jogadores, mas Luigi estava lá podendo saltar mais alto que Mario.

Já em **Super Mario Bros. 2**, Luigi teve sua primeira aparição com um personagem diferente de Mario. Ele também podia saltar mais alto que Mario, mas notava-se uma diferença em seus gráficos. Luigi se mostrou mais alto e magro que o irmão bigodudo.

Vamos evoluir o nosso projeto do Mario que estamos construindo desde a segunda aula. A partir de agora, vamos incluir o personagem do Luigi nos nosso cenários e aplicar regras que implementem a diferença que ele foi ganhando com relação Mario ao longo do tempo, conforme descrição acima. Para tal, codifique as seguintes mudanças:
* Renomear a classe mario para `Personagem`.
* Elemine o construtor default (sem argumentos).
* Criar um método `saltar()` que imprime a altura que o personagem pula.
   * Quando o personagem se chamar "Mario", ele pula uma altura equivalente a 50% da sua própria altura.
   * Quando o personagem se chamar "Luigi", ele pula o dobro da sua altura.

Por fim, crie uma classe com método `main()`, instancie objetos do Mario e do Luigi e teste sua implementação.

Fonte: [nintendoblast](https://www.nintendoblast.com.br/2011/08/perfil-luigi-mario.html).

---

👈 [Voltar para aula anterior](../aula06/aula.md) ..... [Avançar para próxima aula](../aula08/aula.md) 👉    