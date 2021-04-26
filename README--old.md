## Projeto: Criação de aplicação de Gerenciamento de Cursos com Angular8 + NodeJS

- O intuito do projeto é criar uma aplicação de gerenciamento de cursos com Angular8 + NodeJS. Será utilizado uma api interna, que terá os cursos cadastrados. Essa api estará armazenada no proprio projeto (na pasta server do backend nodejs) e essa api será consumida para ser carregada no site os cursos que estão cadastrados. No projeto será simulado requisições http (put, post, get, delete) utilizando o nodejs como servidor backend. As requisições http apenas funcionará se o servidor BackEnd NodeJs estiver iniciado. Quando o servidor BackEnd for desativado, as requisições que foram realizadas no site serão descartadas.

## Ferramentas Utilizadas

##### IDE: 

- VSCode (ou alguma de sua preferencia)

##### NODEJS:

- Utilizei a versão v14.15.4. Mas pode ser a ultima disponivel no site (Versão LTS). Abaixo link para download: [ https://nodejs.org/en/]( https://nodejs.org/en/)

##### TYPESCRIPT

- O Angular usa a linguagem TypeScript como padrão, ao invés do JavaScript. Não é necessario instalar o typescript, pois vem junto com o angular. Foi usado os conceitos typescript para tipar as variaveis.

##### ANGULAR CLI
- Link de referencia: [https://cli.angular.io/](https://cli.angular.io/)

- Comando para instalar o angular: `$npm install -g @angular/cli`

- Comando para verificar versao do angular apos instalacao: `$ng version`

- Para criar novo projeto angular, execute o comando abaixo. Será criado a estrutura de pastas padrão do angular: `$ng new 'nome-do-projeto'`

- Depois terá tres perguntas:

	Pergunta1: Do you want to enforce stricter type checking and stricter bundle budgets in the workspace? This setting helps improve maintainability and catch bugs ahead of time. For more information, see [https://angular.io/strict](https://angular.io/strict) 
	 `$A primeira escolhi  'y'`

	Pergunta2:  Would you like to add Angular routing?
	`$A segunda escolhi 'n' para nao criar a rota. No projeto a rota foi criada posteriormente.`

	Pergunta3:  Which stylesheet format would you like to use?
	`$A terceira escolhi 'CSS'`

- Para iniciar o projeto informe o comando abaixo. Detalhe: Enquanto estiver codificando o codigo, para visualizar as alterações no navegador, necessario que o servidor do angular esteja iniciado com o comando abaixo.
	`$ng serve`

- Por padrão o angular utiliza a porta 4200, acesse o endereço abaixo para verificar a pagina inicial. Nessa pagina inicial é possivel acessar a documentação do angular.
	[http://localhost:4200/](http://localhost:4200/)

##### BOOTSTRAP

- Comando para instalar no projeto: `$npm install bootstrap`

##### FONT-AWESOME

- O Font Awesome é um conjunto de ícones baseados em webfont e CSS, lançado em 2012 pelo desenvolvedor Dave Gandy. A proposta é carregar uma webfont sem precisar utilizar icones salvos no projeto. Nesse projeto o font-awesome esta sendo utilizado para os icones do componente 'star' (os icones das estrelas serão carregados pelo font-awesome). Abaixo o comando para instalar no projeto:
	`$npm install font-awesome`


## Conceitos Utilizados

- Criação de modulos e componentes.
- Uso do 'Two-way Data Binding', no campo pesquisar.
	No codigo utiliza os colchetes e parenteses [()], para envio dos dados em mao dupla, ou seja, é quando quer exibir e alterar o valor da propriedade, de forma que irá se propagar todas as referencias dessa variavel.

- Injeção De Dependência.

- Utilização de Pipes para alterar os valores dos campos ( | ).

- Criação de Rotas para navegar entre os componentes.

- Criaçao de templates.

- Utilização de Formularios, Variaveis de Templates (representado com simbolo #).

- ngClass - para criação de classes dinamicas.

- ng-model: vincula o valor dos controles html (input, select, textarea) aos dados do aplicativo, ou seja, com ng-model é possivel vincular o valor de um campo de entrada a uma variavel criada no Angular.

- Construir um serviço.

- Recuperar Requisições em HTTP com NodeJS + Express (BackEnd). Fora da pasta do projeto foi criado uma pasta de nome 'server', e dentro dessa pasta foi criado uma outra pasta com o nome 'course-manager-server'. 
	O intuito de criar esse diretorio, foi para separar o servidor backend nodejs, do projeto principal. (' .\servers\course-manager-server ') . 
	Dentro da pasta 'course-manager-server', foi criado o arquivo 'server.js' e dentro do arquivo, foi criado as rotas para fazer as requisições de back-end. E ainda dentro dessa mesma pasta 'course-manager-server' foi criado o arquivo 'package.json', e adicionado os comandos abaixo:

```javascript
{
  "name": "course-manager-server",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "cors": "^2.8.5",
    "express": "^4.17.1"
  }
}
```

- Dentro da pasta do backend, (' .\servers\course-manager-server '), execute o comando abaixo, para instalar as dependecias do backend. Detalhe: as dependencias serão instaladas de acordo com o que consta no arquivo 'package.json', que esta dentro do novo diretorio que foi criado ('.\servers\course-manager-server'). 
`$npm install`

- Para iniciar o servidor backend do nodejs, utilize o comando abaixo. Deverá aparecer uma mensagem de 'Server Starded!' . Detalhe: Nao foi utilizado banco de dados, para testes, foi utilizado o nodejs, para simular as requisições http (put, post, get, delete). As requisições http apenas funcionará se o servidor BackEnd NodeJs estiver iniciado. Quando o servidor BackEnd for desativado, as alterações que foram realizadas no site serão descartadas.
`$node serve.js`

- Uso do RXJS Observable: 
	O Observable é uma funcionalidade da biblioteca do rxjs, que é instalada quando se cria uma nova aplicação do angular. Com seu uso, é possivel lidar com transferencia de dados assincrona, algo que em muitas vezes é semelhante as Promisses do Javascript.

- Segregrando Aplicação em Modulos:
	Utilizado o forChild: 
	O forChild é utilizado em modulos filhos. Isso diferencia do modulo Pai, que no projeto, o arquivo pai, é o arquivo 'app.module.ts'

	Criado Pasta Shared: 
	Nessa pasta foi armazenada os componentes pequenos e genericos, que podem ser compartilhados com outros modulos. 

	Criado Pasta Core:
	Nessa pasta foi armazenado componentes relacionado a regra do negocio ou que tem amarração maior com outros componentes que não são tão genericos, ou componente que são mais dificieis de serem compartilhados devido ao seu contexto especifico.

- Tratamento de Erros no Angular


## Link de referencia:

- [https://getbootstrap.com/docs/versions/](https://getbootstrap.com/docs/versions/)

- [https://www.typescriptlang.org/docs/](https://www.typescriptlang.org/docs/)

- [https://angular.io/docs](https://www.typescriptlang.org/docs/)

- O projeto publicado é referente ao treinamento do Curso Bootcamp - Angular Developer da Digital Innovation One [https://digitalinnovation.one](https://digitalinnovation.one).
