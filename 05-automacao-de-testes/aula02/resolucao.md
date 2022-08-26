# Aula 02 - Resolução do exercício

1. Para esta ação podemos resolver com um ou dois comandos que contemplem um `cy.get` para capturar o elemento e um `cy.click` para clicar no mesmo. O resultado pode ficar em um destes formatos:
   
```javascript
    let elemento = cy.get(‘seu-seletor’)
    elemento.click()
```

```javascript
    cy.get(‘seu-seletor’).click()
```

1. Existem várias formas de realizar as asserções. Como exemplo você pode utilizar um `expect` ou então um `.should` logo após capturar o valor que deseja verificar. Seguem duas formas de implementar estas validações:
 
```javascript
    cy.url().then( minhaUrl =>{
        expect(minhaUrl).to.include('reset')
    })
```

```javascript
    cy.url().should('include', 'reset')
```

---
👈 [Voltar para aula](aula.md)
