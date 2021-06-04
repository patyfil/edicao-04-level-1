# Aula 06 - Resolução do exercício

Há mais de uma forma de criar este algoritmo. Como já falamos anteriormente, dificilmente duas pessoas criam um algoritmo exatamennte igual. Portanto, se o seu código ficou muito diferente do nosso, _don't worry_. O importante é o resultado. 😊

_Obs.: caso você queira executar o código abaixo, lembre-se de atribuir valores às variáveis `peso` e `altura`._

```javascript
altura = ...
peso = ...

imc = peso / (altura * altura)

classificacao = ""
grau = 0

if (imc < 18.5) {
    classificacao = "magro"

} else if (imc < 25) {
    classificacao = "normal"

} else if (imc < 30) {
    classificacao = "com sobrepeso"
    grau = 1

} else if (imc < 40) {
    classificacao = "obeso"
    grau = 2

} else {
    classificacao = "obeso com gravidade"
    grau = 3
}

console.log("Seu IMC é", imc)
console.log("Você é considerado", classificacao)

if (grau > 0) {
    console.log("Cuidado! Você está acima do peso recomendado pela OMS.")

    if (grau == 3) {
        console.log("É importante procurar um médico para avaliar sua saúde.")
    }
}
```

---
👈 [Voltar para aula](aula.md)