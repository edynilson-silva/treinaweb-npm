# Npm - Gerenciador de pacotes para JavaScript

[Link do curso](https://www.treinaweb.com.br/curso/npm-gerenciador-de-pacotes-para-javascript)

### Após instalar o **Node.js**, podemos verificar se o **Node.js & NPM** foram instalados corretamente:
```
node -v | npm -v | npm --version
```
### Instalar a última versão do NPM:
```
npm install npm@latest -g
```
#### Buscar um pacote:
```
npm search nomePacote
```
#### Ou podemos buscar diretamente, pelo site: www.npmjs.com

### Instalando um pacote (*npm install nomePacote*)
```
npm install lodash
```
#### Em versões anteriores, é necessário adicionar a flag *--save* ou *-s*
```
npm install vue --save
```
#### Instalar versão específica:
```
npm install lodash@4.17.3
```
#### Passar intervalo de versões:
```
npm install lodash@">2.0.0 <4.0.0"
```
#### Instalar a versão mais recente:
```
npm install nomePacote@latest
```
#### Observação: Podemos trocar o *install* por *i*
#### Detalhe: Se queremos importar um pacote instalado globalmente:
```
var lodash = require('lodash');
```
#### Enquanto um pacote local, dentro da pasta node_modules do projeto. Utilizamos o **./**
```
var myFile = require('./myFile');
```

### Criando um Package.json

#### Podemos utilizar "duas variantes":
```
npm init
```
#### Nesta primeira é feita algumas perguntas, na criação do arquivo. (nome do projeto, versão, descrição, arquivo de entrada, comando de teste, repositório do git e palavras chaves, nome do autor e licença)
```
npm init --yes
```
#### Enquanto no segundo script, essas perguntas são ignoradas.

### Ler arquivo Package.json
```
npm install
```
