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
#### Ainda no package.json, há o *devDependencies* para listarmos os pacotes que estamos usando apenas no **desenvolvimento** (Coisas que no cliente ou servidor não precisarão ser instalados)

#### Para instalar o pacote no *devDependencies* ( *--save-dev* ou *-D*)
```
npm install nomePacote --save-dev 
```
### Instalar pacotes por repositórios GIT
```
npm i url-github
```
### Atualizar pacotes
```
npm update
```
> **Detalhe:** **npm update** atualiza para a versão melhor indicada, atualizará tudo.
#### Podemos especificar também: 
```
npm update nomePacote
```
#### Verificar pacotes desatualizados:
```
npm outdated
```
#### Desinstalando pacotes:
```
npm uninstall nomePacote 
```
>**Exemplo:**
```
npm uninstall lodash jquery
```
> Caso utilize uma versão antiga do npm, não será retirado do **devDependencies**. É necessário, passar a flag **--save-dev**.
```
npm uninstall lodash --save-dev
```
#### Instalação de Pacotes Globalmente:
```
npm install -g http-server
```
> Podemos trocar a flag **_install_**, por **_i_**. Além de inserir **_-g_** no comando.
#### Encontrar diretório onde arquivos do npm estão:
```
npm config get prefix
```
#### Atualizando pacotes globais
```
npm outdated -g
```
#### Atualizar apenas o que estiver na raiz
```
npm outdated -g --depth=0
```
#### Listar o que tem instalado globalmente
```
npm ls -g --depth=0
```
#### Atualizar os pacotes
```
npm update -g
npm update -g nomePacote
```
#### Listando e desinstalando pacotes globais
```
npm ls -g --depth=0
npm uninstall -g nomePacote
```
> No primeiro comando: listei o que tem instalado globalmente

#### Criando Pacotes

> Necessário possuir um **_package.json_**, em seguida, dar um **_npm init_** e **responder as perguntas**.