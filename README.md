# curso-js-tdd
*Exercícios e resumos das aulas do Curso JS com TDD na Prática* 

**Seção 1: Boas práticas**

1. Criar repositório no Github e iniciando git.
2. Criar conta no Npm e configurar o package.json do projeto de estudo com nome, email, licença, etc. 
3. Instalar package: npm install gitignore -g. Listar tipos de gitignore com: gitignote - types, e escolhendo para o proejto em JS: gitignore Node.
4. Criar README.md nos projetos, podendo utilizar como base: https://gist.github.com/PurpleBooth/109311bb0361f32d87a2. Com letras maiúsculas nomes de arquivos de apenas texto.
5. Escolher tipo de licença, podendo consultar elas no http://opensource.org/licenses. Criar o arquivo LICENSE.md, no mesmo nível do README.md, e colocar lá dentro o texto de descrição da licença escolhida no OpenShource. A licença recomendada é a do MIT.
6. Criar arquivo CONTRIBUTING.md para instruir as pessoas como contribuirem e utilizarem o repositório.
7. Utilizar um Styleguide para manter o padrão do código e organização. Algumas sugestões de styleguides são: https://github.com/airbnb/javascript e https://github.com/rwaldron/idiomatic.js. Além dos verificadores de código, que validam padrões configuráveis ou styleguides escolhidos, como jshint, jscs e o ESLint, mais usado.
8. Instalar ESLint, baseando no Getting Started do site https://eslint.org/ para instalar e salvar como dependência não global: `npm install eslint --save-dev` e inicializar com o comando `./node_modules/.bin/eslint --init`, configurar para o styleguide do AirBnb e para JavaScript. Após é só rodar `./node_modules/.bin/eslint src/*.js` para relatório dos erros e avisos. Podendo utilizar o pluggin `https://willianjusten.com.br/analisando-seu-codigo-js-com-linter/`para agilizar a execução.
9. Criar arquivo `.editorconfig` com as configurações para as IDEs se basearem para formatar os arquivos e instalar o editorconfig na IDE, `https://editorconfig.org/`, se já não for.
10. Adicionar scripts na key "script" no package.json para facilitar a execução de códigos. Por exemplo: `script: { lint: ./node_modules/.bin/eslint src/*.js }`, rodando apenas com `npm run lint`.
11. Instalar Husky (`https://github.com/typicode/husky`) para rodar tasks automatizadas quando executados hooks do Git (precommit, prepush, etc.) (`https://git-scm.com/book/it/v2/Customizing-Git-Git-Hooks`). Rodar `npm install husky --save-dev` para instalar. Para utilizar é preciso apenas incluir na key scripts do package.json algum dos hooks disponíveis e no value a string do comando que é para rodar quando for disparado o hook. Caso ocorra algum erro na execução do script, o comando do git não será executado. Dica: evitar utilizar o pre-commit, porque pode estar incompleto o código e quebrando ao commitar propositalmente e daí não vai ser possível fazer o commmit, sendo indicado utilizar pre-push no lugar. Exercício: incluir `scripts: { prepush: 'npm run lint'}` no package.json.


**Seção 2: Aprendendo ES6**

1. Site para conhecer todas as features do ES6, comparar ES5 e ES6 e ver exemplos: `http://es6-features.org/`. Tabelas de compatibilidade das features dp ES6 nos navegadores, consultar quais navegadores tem suporte para cada feature do ES6: `http://kangax.github.io/compat-table/es6/`. Blogs para ler sobre e ver exemplos de ES6: `https://ponyfoo.com/articles/tagged/es6-in-depth` e `https://nipher.io/blog/`.  
2. As variáveis declaradas com "var" tem escopo global ou de função, se declarada dentro de uma função. Não importando se estão dentro de um bloco.
3. Já variáveis let tem escopo de bloco. Existindo apenas dentro de um bloco de if, por exemplo.
4. A variável const só pode ser declarada uma vez e não pode ser reatribuída. Sendo possível apenas alterar values e acrescentar novas keys ao objeto const. Para que uma variável seja imutável é necessário fazer Object.freeze(variavelName);
5. Hosting é a ação que o Javascript faz na leitura do código e pega todas variáveis declaradas com "var" e declara no top. Assim não dá erro de falta de declaração, se a variável for usada antes de declarada. Mas com "let" esse Hosting não ocorre e a falta da declaração vai estourar erro.
6. Arrow Functions: function() {} para () => {}, () => "retorna sozinho se for apenas uma linha" e não precisa dos parênteses se tiver apenas um parâmetro param => "Retorno": + param.
7. Arrow Function tem o this com comportamento diferente da função comum. Na função normal o this é o objeto em que ele é chamado dentro. Na Arrow Function é o contexto da função mais abrangente.

