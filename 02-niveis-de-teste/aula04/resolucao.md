# Aula 04 - Resolução do exercício

### Exemplo de cenário passo a passo:

#### Acessar o sistema com um usuário válido

| Ação                                           | Resultado                                 |
| ---------------------------------------------- | ----------------------------------------- |
| Acessar a aplicação                            | Devo ser direcionado para a tela de login |
| Preencher o campo de email com um email válido | Não deve ocorrer erro                     |
| Clicar no botão que "Proxima"                  | Devo ser direcionado para a tela de senha |
| Preencher o campo de senha com um valor válido | Não deve ocorrer erro                     |
| Clicar no botão que "Proxima"                  | Devo ser direcionado para a aplicação     |


### Exemplo de cenário utilizando Gherkin:

**Cenário**: Acessar o sistema com um usuário válido
**Dado** que acessei a aplicação
**E** fui direcionado para o login
**Quando** preencho meus dados de acesso corretamente
**Então** sou redirecionado para a aplicação

---
👈 [Voltar para aula](aula.md)
