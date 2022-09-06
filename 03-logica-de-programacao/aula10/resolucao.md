# Aula 10 - Resolução dos exercícios

Lembre-se sempre: o algoritmo poderia ter sido criado com uma centena de detalhes diferentes. O importante é entender a ideia e obter o resultado final. 😉

```javascript
colaboradores    = ['Rhoger', 'Cléverson', 'Gleysberto', 'Nádio', 'Rosiméri', 'Regislane', 'Agripino', 'Wellison']
idades           = [      69,          66,           58,      61,         60,          64,         59,         55]
temposDeTrabalho = [      31,          29,           30,      26,         25,          24,         26,         29]

/* Função para verificar se um colaborador está apto para se aposentar, atendendo a pelo menos uma das seguintes regras:
 * - Ter pelo menos 65 anos de idade;
 * - Ter trabalhado no mínimo 30 anos;
 * - Ter pelo menos 60 anos de idade e 25 anos de trabalho.
 */
function verificarAposentadoria(nome) {

    colaborador = false
    idade = 0
    tempoTrabalho = 0

    // buscando um colaborador pelo nome
    for (posicao = 0; posicao < colaboradores.length; posicao++) {

        if (nome == colaboradores[posicao]) {
            colaborador = true
            idade = idades[posicao]
            tempoTrabalho = temposDeTrabalho[posicao]
        }
    }

    // se encontrar o colaborador, verifica as regras de aposentadoria
    if (colaborador) {
        
        porIdade = (idade >= 65)
        porTempoDeTrabalho = (tempoTrabalho >= 30)
        porIdadeComTempoDeTrabalho = (idade >= 60 && tempoTrabalho >= 25)

        // não importa qual regra seja atendida
        // se qualquer uma for, o colaborador pode se aposentar
        if (porIdade || porTempoDeTrabalho || porIdadeComTempoDeTrabalho) {
            console.log("Parabéns, já pode sair de férias eternas :)")
        } else {
            console.log("Infelizmente, ainda falta um tempo :(")
        }
    
    } else {
        console.log("Colaborador inválido :|")
    }
}


function verificarAposentadoria(nome) {
  colaborador = false;
  idade = 0;
  tempoTrabalho = 0;

  // buscando um colaborador pelo nome
  for (i = 0; i < colaboradores.length; i++) {
    if (nome == colaboradores[i]) {
      colaborador = true;
      idade = idades[i];
      tempoTrabalho = temposDeTrabalho[i];
    }
  }

  // se encontrar o colaborador, verifica as regras de aposentadoria
  if (colaborador) {
    porIdade = idade >= 65;
    porTempoDeTrabalho = tempoTrabalho >= 30;
    porIdadeComTempoDeTrabalho = idade >= 60 && tempoTrabalho >= 25;

    // não importa qual regra seja atendida
    // se qualquer uma for, o colaborador pode se aposentar
    if (porIdade) {
      console.log("Parabéns, já pode sair de férias eternas :)");
      console.log("Regra 1 - Tem pelo menos 65 anos de idade");
    } else if (porTempoDeTrabalho) {
      console.log("Parabéns, já pode sair de férias eternas :)");
      console.log("Regra 2 - Trabalhou no mínimo 30 anos");
    } else if (porIdadeComTempoDeTrabalho) {
      console.log("Parabéns, já pode sair de férias eternas :)");
      console.log("Regra 3 - Tem pelo menos 60 anos de idade e 25 anos de trabalho.");
    } else {
      console.log("Infelizmente, ainda falta um tempo :(");
    }
  } else {
    colaborador = false;
    console.log("Colaborador inválido :|");
  }

```

---
👈 [Voltar para aula](aula.md)