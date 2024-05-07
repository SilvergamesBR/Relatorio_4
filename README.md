# Relatorio 4

Essa e uma suite de testes para o site [Contact list app](https://thinking-tester-contact-list.herokuapp.com), antes de a executar deve ser instalado o cypress, para tal apenas siga os passos no site ([site cypress](https://www.cypress.io)), os relatorios foram gerados utilizando o mochawesome, para tal esse tambem deve ser instalado com o comando a seguir utilizando a ferramenta de comando de sua preferencia (npm install --save-dev mochawesome mochawesome-merge mochawesome-report-generator), alem disso o arquivo cypress.configs.js localizado na pasta onde o cypress for instalado tambem deve ser modificado para :
```
const { defineConfig } = require('cypress');

module.exports = defineConfig({

reporter: 'cypress-mochawesome-reporter',

e2e: {

setupNodeEvents(on, config) {

require('cypress-mochawesome-reporter/plugin')(on);

    },
  },
});
```
No arquivo e2e.js, localizado no caminho /cypress/support/e2e.js a partir da pasta onde o cypress foi instalado, deve ser adicionada a linha `import 'cypress-mochawesome-reporter/register'` logo abaixo de `import './commands'`, o arquivo Aula4.cy.js deve ser colocado na pasta e2e, caminho /cypress/e2e a partir do diretorio de instalacao do cypress.

Apos a preparacao para gerarmos o relatorio abriremos a nossa ferramenta de comandos e deve ser 
