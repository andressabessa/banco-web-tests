# banco-web-tests

Testes automatizados do App Web do Banco

## Objetivo do Projeto

Este projeto tem como objetivo demonstrar aos alunos como automatizar testes de aplicações web utilizando o framework [Cypress](https://www.cypress.io/). Ele serve como um guia prático para a criação de testes automatizados, organização de código com Custom Commands e geração de relatórios de execução.

## Componentes do Projeto

- **Cypress**: Framework de testes end-to-end utilizado para automatizar a interação com a aplicação web.
- **Custom Commands**: Comandos personalizados criados para reutilizar e organizar melhor o código dos testes.
- **cypress-mochawesome-reporter**: Ferramenta para geração de relatórios detalhados e interativos dos testes.
- **Dependências**: Todas as dependências necessárias estão listadas no arquivo `package.json`.

## Pré-requisitos

Antes de executar os testes, certifique-se de que os seguintes serviços estão em execução:

1. **API**: [banco-api](https://github.com/juliodelimas/banco-api)
2. **Aplicação Web**: [banco-web](https://github.com/juliodelimas/banco-web)

## Guia de Instalação e Execução

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/banco-web-tests.git
   cd banco-web-tests
   ```

2. Instale as dependências do projeto:
   ```bash
   npm install
   ```

3. Execute os testes:
   ```bash
   npx cypress open
   ```
   Ou para execução em modo headless:
   ```bash
   npx cypress run
   ```

4. Para gerar relatórios com o `cypress-mochawesome-reporter`:
   ```bash
   npx cypress run --reporter mochawesome
   ```

Os relatórios gerados estarão disponíveis na pasta `cypress/reports`.

## Organização dos Testes

Os testes estão organizados em diferentes arquivos dentro da pasta `cypress/e2e`. Cada arquivo cobre um conjunto específico de funcionalidades da aplicação web.

### Custom Commands

Os Custom Commands estão localizados no arquivo `cypress/support/commands.js`. Eles foram criados para facilitar a reutilização de código e melhorar a legibilidade dos testes. Exemplos de comandos personalizados incluem:

- **Login automatizado**: Um comando para realizar login na aplicação com credenciais padrão.
- **Preenchimento de formulários**: Comandos para preencher campos de formulários de maneira dinâmica.
- **Validação de mensagens de erro**: Comandos para verificar mensagens de erro exibidas na interface.

Para criar novos comandos, basta adicionar ao arquivo `commands.js` seguindo o padrão existente.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Licença

Este projeto está licenciado sob a licença MIT.

