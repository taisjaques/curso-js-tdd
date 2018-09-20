# curso-js-tdd
*Exercícios e resumos das aulas do Curso JS com TDD na Prática* 

**Boas práticas**

1. Criar repositório no Github e iniciando git.
2. Criar conta no Npm e configurar o package.json do projeto de estudo com nome, email, licença, etc. 
3. Instalar package: npm install gitignore -g. Listar tipos de gitignore com: gitignote - types, e escolhendo para o proejto em JS: gitignore Node.
4. Criar README.md nos projetos, podendo utilizar como base: https://gist.github.com/PurpleBooth/109311bb0361f32d87a2. Com letras maiúsculas nomes de arquivos de apenas texto.
5. Escolher tipo de licença, podendo consultar elas no http://opensource.org/licenses. Criar o arquivo LICENSE.md, no mesmo nível do README.md, e colocar lá dentro o texto de descrição da licença escolhida no OpenShource. A licença recomendada é a do MIT.
6. Criar arquivo CONTRIBUTING.md para instruir as pessoas como contribuirem e utilizarem o repositório.
7. Utilizar um Styleguide para manter o padrão do código e organização. Algumas sugestões de styleguides são: https://github.com/airbnb/javascript e https://github.com/rwaldron/idiomatic.js. Além dos verificadores de código, que validam padrões configuráveis ou styleguides escolhidos, como jshint, jscs e o ESLint, mais usado.
8. Instalar ESLint, baseando no Getting Started do site https://eslint.org/ para instalar e salvar como dependência não global: `npm install eslint --save-dev` e inicializar com o comando `./node_modules/.bin/eslint --init`, configurar para o styleguide do AirBnb e para JavaScript. Após é só rodar `./node_modules/.bin/eslint <caminhoArquivo.js>` para relatório dos erros e avisos. Podendo utilizar o pluggin `https://willianjusten.com.br/analisando-seu-codigo-js-com-linter/`para agilizar a execução.
