# Aula 01 - O que é Orientação a Objetos ?

Assista ao vídeo:

  1. [O que é Orientação a Objetos ?](https://youtu.be/KlIL63MeyMY?t=274)

> É **#fundamental** que você assista ao vídeo. É **#opcional** _(embora bem interessante)_ que você leia o material complementar.

---

## Material Complementar

"Programação orientada a objetos é uma péssima ideia que só poderia ter nascido na Califórnia." -- Edsger Dijkstra

### Motivação: problemas do paradigma procedural

Orientação a objetos é uma maneira de programar que ajuda na organização e resolve muitos problemas enfrentados pela programação procedural.

Consideremos o clássico problema da validação de um CPF. Normalmente, temos um formulário no qual recebemos essa informação e depois temos de enviar esses caracteres a uma função que vai validá-lo, como no pseudocódigo abaixo:

```
cpf = formulario->campo_cpf
valida(cpf)
```

Alguém o obriga a sempre validar esse CPF? Você pode, inúmeras vezes, esquecer de chamar esse validador. Mas: considere que você tem 50 formulários e precise validar em todos o CPF. Se sua equipe tem três programadores trabalhando nesses formulários, quem fica responsável por essa validação? Todos!

A situação pode piorar: na entrada de um novo desenvolvedor, precisaríamos avisá-lo de que sempre devemos validar o CPF de um formulário. É nesse momento que nascem aqueles guias de programação para o desenvolvedor que for entrar nesse projeto - às vezes, é um documento enorme. Em outras palavras, todo desenvolvedor precisa saber de uma quantidade enorme de informações que, na maioria das vezes, não está realmente relacionada à sua parte no sistema, mas ele precisa ler tudo isso, resultando em um entrave muito grande!

Outra situação na qual ficam claros os problemas da programação procedural é quando nos encontramos na necessidade de ler o código que foi escrito por outro desenvolvedor e descobrir como ele funciona internamente. Um sistema bem encapsulado não deveria gerar essa necessidade. Em um sistema grande, simplesmente não temos tempo de ler todo o código existente.

Considerando que você não erre nesse ponto e a sua equipe tenha uma comunicação muito boa (perceba que comunicação excessiva pode ser prejudicial e atrapalhar o andamento), ainda temos outro problema: imagine que, em todo formulário, você também queira que a idade do cliente seja validada - o cliente precisa ter mais de 18 anos. Teríamos de colocar um if... Mas onde? Espalhado por todo seu código e, mesmo que se crie outra função para validar, precisaríamos incluir isso nos nossos 50 formulários já existentes. Qual é a chance de esquecermos um deles? É muito grande.

A responsabilidade de verificar se o cliente tem ou não 18 anos ficou espalhada por todo o seu código. Seria interessante poder concentrar essa responsabilidade em um lugar só para não ter chances de se esquecer disso.

Melhor ainda seria se conseguíssemos mudar essa validação e os outros programadores nem precisassem ficar sabendo disso. Em outras palavras, eles criariam formulários, e um único programador seria responsável pela validação: os outros nem saberiam da existência desse trecho de código. Impossível? Não, o paradigma da orientação a objetos facilita tudo isso.

O problema do paradigma procedural é que não existe uma forma simples de criar conexão forte entre dados e funcionalidades. No paradigma orientado a objetos, é muito fácil ter essa conexão por meio dos recursos da própria linguagem.

> Quais as vantagens?
> Orientação a objetos irá ajudá-lo bastante a se organizar e escrever menos, além de concentrar as responsabilidades nos pontos certos, flexibilizando sua aplicação e encapsulando na lógica de negócios.
> 
> Outra enorme vantagem, na qual você realmente economizará montanhas de código, é o polimorfismo das referências, que veremos em um capítulo posterior.

Fonte: [Caelum](https://www.caelum.com.br/apostila-java-orientacao-objetos/orientacao-a-objetos-basica#motivacao-problemas-do-paradigma-procedural).

---

👈 [Voltar para o índice](../README.md) ..... [Avançar para próxima aula](../aula02/aula.md) 👉