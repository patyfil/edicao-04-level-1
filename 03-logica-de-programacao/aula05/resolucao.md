# Aula 05 - Resolução dos exercícios

O nome das variáveis não é o mais relevante para a resolução destes exercícios. O principal aqui é o entendimento da lógica que deve ser aplicada para criação de cada variável. 😉

Fique à vontade para colocar valores fixos _(como a idade de maioridade ou a taxa de juros)_ em diferentes variáveis para melhorar a leitura e compreensão do código. 👊

1)
```javascript
    // mesmoNome = (nomeFulano == nomeBeltrano)
    nomeDoFulano = "Patrícia";
    nomeDoBeltrano = "Patrícia";
    mesmoNome = (nomeDoFulano == nomeDoBeltrano);
    console.log(mesmoNome);
```

2) 
```javascript
    // maiorDeIdade = (idade >= 18)
    idade = 45;
    maiorDeIdade = (idade >= 18);
    console.log(maiorDeIdade);
```

3) 
```javascript
    // valorComJuros = (valorBoleto * 1.1)
    valorBoleto = 200;
    valorComJuros = valorBoleto + (valorBoleto * 0.10)
    console.log(valorComJuros);
```

4) 
```javascript
    // mediaAritmetica = (item1 + item2 + item3 + item4 + item5) / 5
    item1 = 2;
    item2 = 2;
    item3 = 2;
    item4 = 2;
    item5 = 2;
    media = (item1 + item2 + item3 + item4 + item5) / 5
    console.log(media)
```

5) 
```javascript
    // lucroBruto = receitaLiquidaVendas - custoProdutosVendidos
    // margemBruta = (lucroBruto / receitaLiquidaVendas) * 100
    receitaLiquida = 1500
    custoProdutosVendidos = 10
    lucroBruto = receitaLiquida - custoProdutosVendidos;
    margemBruta = (lucroBruto / receitaLiquida) * 100
    console.log(margemBruta)
```

6)

```javascript
    saldo = 1000;
    saldo = saldo - 99.9;
    saldo = saldo + 2500;
    saldo = saldo - 0.1;
    saldo = saldo * 0.75;
    saldo = saldo / 2;

    console.log(saldo);
```

![resolucao](img/resolucao.PNG)

---
👈 [Voltar para aula](aula.md)