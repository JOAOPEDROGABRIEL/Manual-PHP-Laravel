### [Manual](../Readme.md) / [Instalação](installation.md) / [Primeiros Projetos](first_steps.md) / Rotas

<h1 id="introduction">Rotas</h1>

<div style="display: flex; align-items: center; height: 35px;">
<div style="width: 25%; background-color: transparent;">Configuração de Rotas</div>
<div style="width: 5%; background-color: transparent;"><a href="#applyingknowledge"><img src="../assets/next-page.svg"></img></a></div>
<div style="width: 70%; background-color: transparent;"></div>
</div>

### O que são rotas:

- Rotas são endereços onde, referenciam os caminhos existentes dentro da aplicação, para isto, quando acessamos um recurso através um endereço de url, estamos, na prática, acessando uma rota.

        Exemplos:

        Rota 1: https://www.minhaaplicacao.com.br
        Rota 2: https://www.minhaaplicacao.com.br/home
        Rota 3: https://www.minhaaplicacao.com.br/sobre
        Rota 4: https://www.minhaaplicacao.com.br/contato

### Tipos de Rotas:

- No Framework Laravel, temos 4 arquivos de rotas distintas, sendo elas:

    - API
    - Channels
    - Console
    - Web

- No Visual Studio, podemos acessar essas rotas no diretório ```...\<nome do projeto>\routes\```. As Rotas possuem um mecanismo de tratamento individualizado realizado pelo framework, rotas referidas a um respectivo endereço são interceptadas pelo framework e tratadas de maneira diferente na aplicação. As Respectivas Rotas:

| ```<Rota>``` | Interpretação da Aplicação |
| :----------: | :--------------- |
| ```Web``` | As rotas referenciadas neste arquivo, serão tratadas pelo servidor php, como páginas no estilo tradicional, ou páginas simples, com essas páginas do lado do backend fornecendo respostas as requisições permitindo a utilização de recursos como cookies e seção. |
| ```Api``` | As rotas de api, não suportam cookies ou seção, uma vez que utilizam comunicação de dados, em aplicações mais modernas, onde é separado o backend e frontend a partir de uma api, é muito comum que sejam utilizadas essas requisições, para transportar dados dos usuários. |
| ```Channels``` | Neste Arquivo, ficam armazenadas as configurações para comunicação em broadcast, onde utiliza de recursos de transmissão em tempo real, através do uso de recursos como 'Live Sockets', diferente do método tradicional, em que o cliente/frontend faz uma requisição para o servidor, e o servidor fornece uma resposta, este tipo de comunicação é adverso, sendo assim, a aplicação servidora, notifica os clientes, sobre as alterações do backend, possibilitando assim, que o frontend, renderize as alterações dinâmicamente, com base nas informações que foram fornecidas pelo servidor. |
| ```Console``` | A Principal Funcão deste arquivo, serve para a criação de comandos personalizados, onde serão executados pelo console, utilizando o __artisan__. |


<h1 id="applyingknowledge">Configurando Rotas no Laravel</h1>

- Para isto será configurado as rotas no arquivo ```Web```, do programa:
        
        /               < Tradicional
        /sobrenos       < Página Sobre nós
        /contato        < Página de Contato

O padrão de Configuração das Rotas é:
        Route::get('/', function () {
            return view('welcome');
        });

O Objeto ```Route```, possui verbos http, na qual se utilizam para controlar as requisições com o servidor para a aplicação, sendo eles:

- ```<Verbo HTTP>```:
    - get
    - post
    - put
    - delete
    - patch
    - options

O comando Route temos 2 parâmetros pre-definidos, sendo elas, uma entrada de uma 'URI', que é um endereço de onde aquela rota será definida, e uma função de callback, ou retorno de função quando aquela rota for acessada.

    Route::get($uri, $callback);

<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="first_steps.md"><img src="../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#introduction"><img src="../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="controllers.md"><img src="../assets/next-page.svg"></img></a></div>
</div>