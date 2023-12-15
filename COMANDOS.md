// INICIALIZA UM PROJETO VAZIO
npm init -y

// INSTANCIA O TYPESCRIPT NO PROJETO
npm i typescript -D
ou
npm i typescript --save-dev

// NODE ENTENDE JAVASCRIPT E NÃO TYPE SCRIPT
npx tsc index.ts  // GERA UM JS A PARTIR DO TS
> vamos configurar o vscode para o node entender o typescript

// INSTANCIAR O TS-NODE
npm i ts-node -D

// INTEGRAÇÃO COM ESLINT
npm i eslint -D
npm i @typescript-eslint/eslint-plugin @typescript-eslint/parser -D
npm i prettier eslint-config-prettier eslint-plugin-prettier

// INSTALAR DEPENDÊNCIAS PARA ESLINT E PRETTIER
npm init @eslint/config
  > To check syntax, find problems, and enforce code style
  > JavaScript modules (import/export)
  > React
  ? Yes
  > Browser
  > JavaScript
  ? Yes
  > npm

// CRIAR .prettierrc.json
  {
      "trailingComma": "es5",
      "tabWidth": 2,
      "semi": true,
      "singleQuote": true
  }

// CRIAR .editorconfig
  root = true

  [*]
  indent_style = space
  indent_size = 2
  end_of_line = lf
  charset = utf-8
  trim_trailing_whitespace = true
  insert_final_newline = true

// CRIAR .eslintrc.js
{
  "editor.fontSize": 16,
  "window.zoomLevel": 0,
  "code-runner.executorMap": {
    "typescript": "npx ts-node --files --transpile-only"
  },
  "liveServer.settings.port": 5501,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "explicit",
    "source.fixAll": "explicit"
  },
  "git.autofetch": true,
  "javascript.updateImportsOnFileMove.enabled": "always",
  "eslint.rules.customizations": [],
  "prettier.configPath": "./.prettierrc.json",
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "cSpell.enableFiletypes": ["javascript"],
  "cSpell.language": "en,pt-BR",
  "editor.formatOnSave": true,
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "emmet.preferences": {},
  "emmet.includeLanguages": {
    "javascript": "javascriptreact"
  }
}

////////////////////////////////////////////////////////////////////////////////////

// CONFIGURAR WEBPACK PARA USO DE FRONT-END (WEBPACK GERA UM BUNDLE.JS COM A JUNÇÃO DOS ARQUIVOS)
npm i ts-loader webpack webpack-cli -D

// INSTANCIAR VALIDATOR E LODASH
npm i validator lodash
npm i @types/node @typs/validator @types/lodash -D

////////////////////////////////////////////////////////////////////////////////////

// COMPILAR (GERAR A DIST)
npx tsc

npx webpack -w
