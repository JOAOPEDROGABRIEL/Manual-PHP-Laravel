### [Manual](../Readme.md) / [Instalação](installation.md) / [Primeiros Projetos](first_steps.md) / [Rotas](routes.md) / Controladores

<h1 id="introduction">Controladores</h1>

- Controllers, servem para agrupar a lógica por trás do que deve ser feito, em função da rota a ser endereçada, por um determinado cliente.

    Ao acessar uma rota da aplicação, esta rota, por sua vez estará associada a um ```controller``` (controlador) e uma ```action``` (ação), definida dentro do controlador, contendo uma lógica do que deve ser feito na aplicação, em função da rota que foi acessada.

    Esta organização e separação das rotas do controlador, permite separar melhor o código, dando responsabilidades claras para cada parte do framework.

    Embora as rotas possuam uma função de ```$callback```, o ideal é referenciar as requisições para os controladores, para então efetuarmos as tratativas com base nas requisições, e mantendo clara a separação entre rotas e controladores.

- A importância da separação se dá pelo motivo:

    Rotas: As rotas são mais voltadas para as requisições dos verbos http assim como os middawares, que podem ser aplicados nas requisições de respostas, incluindo também as questões de segurança da aplicação.

    Controladores: O foco está na lógica para fornecer os requisitos do negócio, a partir as ações definidas dentro dos controladores, é que são definidas as funções da aplicação em função do que foi requisitado para ela fazer, através de uma rota.



<h1 id="applyingknowledge">Configurando Controladores com Laravel</h1>

- Para isto serão aplicados as alterações utilizando os Controladores:

    | ```Controller``` | ```Actions``` |
    | :----------------------- | :-----------: |
    | ```PrincipalController``` | ```principal()``` |
    | ```UserController``` | ```sobrenos``` |
    | ```ContatoController``` | ```contato()``` |


- Para Criar um controlador, podemos utiliazar o comando:

 ```[terminal no diretório do projeto]: php artisan make:controller <nome_controlador>```

Após a criação do controlador, deve-se criar uma função para que seja referenciada na rota:

    No Controlador:
        [...]

        public function <nome_função>(){
        // Execução da Função
        }

        [...]

Respeitando assim, as respectivas Responsabilidades de cada interação.

    Na Rota:
        [...]

        Route::get($uri, [\App\Http\Controllers\<Nome do Controlador>::class, '<Nome da Função>']);

        [...]


<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="routes.md"><img src="../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#introduction"><img src="../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="views.md"><img src="../assets/next-page.svg"></img></a></div>
</div>