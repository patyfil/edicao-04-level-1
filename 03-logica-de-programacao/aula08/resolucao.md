# Aula 08 - Resolução dos exercícios

Relembrando e reforçando: há várias formas de se implementar um mesmo algoritmo.

As estruturas de repetição são uma prova disso. Um desenvolvedor pode ter preferência por usar o `while` enquanto outro pode preferir o `for`, mesmo que ambas as estruturas consigam gerar exatamente o mesmo resultado.

Na resolução dos exercícios `2` e `3`, inclusive, foi usado `for` por preferência do desenvolvedor. 😛

1)
  ** Utilizando `while`:
```javascript
// bandas = ["Creedence", "AC/DC", "Metallica", "Oasis", "Audioslave"]
// index = 0

// while (index < bandas.length) {
//     console.log(bandas[index])
//     index++
// }
    frutas = ["Banana", "Maçã", "Uva", "Abacaxi", "Limão"]
    i = 0
    while (i < frutas.length) {
        console.info(frutas[i])
        i++
    }
```

  ** Utilizando `do ... while`:
```javascript
// bandas = ["Creedence", "AC/DC", "Metallica", "Oasis", "Audioslave"]
// index = 0

// do {
//     console.log(bandas[index])
//     index++
// } while (index < bandas.length)
    frutas = ["Banana", "Maçã", "Uva", "Abacaxi", "Limão"]
    i = 0
    do {
        console.log(frutas[i])
        i++
    } while (i < frutas.length)
```

  ** Utilizando `for`:
```javascript
// bandas = ["Creedence", "AC/DC", "Metallica", "Oasis", "Audioslave"]

// for (index = 0; index < bandas.length; index++) {
//     console.info(bandas[index])
// }
    frutas = ["Banana", "Maçã", "Uva", "Abacaxi", "Limão"]
    for (i = 0; i < frutas.length; i++){
        // console.log(frutas[i])
        console.info(frutas[i]);
    }
```

2) 
```javascript
valores = [1, 2, 3, 5, 8, 13, 21, 23, 34, 55]

soma = 0
for (index = 0; index < valores.length; index++) {
    soma += valores[index]
}

media = soma / valores.length
console.log(media)

// ************* WHILE *************
soma = 0;
i = 0;
while (i < valores.length) {
  soma += valores[i];
  i++
}
media = soma / valores.length;
console.log(media);

// ************* DO WHILE *************
i = 0;
soma = 0;
do {
  soma += valores[i];
  i++;
} while (i < valores.length);
media = soma / valores.length;
console.log(media);

```

3)
```javascript
meuNome = "Patrícia";
nomeComum = false

nomesComuns = ["Miguel", "Laura", "Lucas", "Beatriz", "Guilherme", "Maria", "Gabriel", "Ana", "Arthur", "Júlia", 
"Enzo", "Alice", "Rafael", "Mariana", "João", "Larissa", "Gustavo", "Maria Eduarda", "Pedro", "Sofia", 
"Bernardo", "Isabela", "Matheus", "Helena", "Davi", "Camila", "Heitor", "Lara", "Henrique", "Valentina", 
"Bruno", "Letícia", "Samuel", "Luana", "Felipe", "Amanda", "Lorenzo", "Yasmin", "Benjamin", "Sophia", 
"Vinícius", "Rebeca", "Rodrigo", "Juliana", "Eduardo", "Bruna", "Diego", "Cecília", "Antônio", "Fernanda", 
"Leonardo", "Isadora", "Noah", "Lorena", "Nícolas", "Lívia", "Daniel", "Manuela", "Thiago", "Vitória"]

for (index = 0; index < nomesComuns.length; index++) {
    if (meuNome == nomesComuns[index]) {
        nomeComum = true
        break
    }
}

if (nomeComum) {
    console.log("É, nome comum :P")
} else {
    console.log("Diferentona, hein? XD")
}
```

---
👈 [Voltar para aula](aula.md)