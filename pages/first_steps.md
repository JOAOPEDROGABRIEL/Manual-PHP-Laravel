### [Manual](../Readme.md) / [Instalação](installation.md) / Primeiros Projetos

<h1 id="introduction">Criação de Projetos Laravel</h1>

- Consiste na Recuperação de Projetos (Frameworks), já existentes conforme disponibilizados pela distribuidora, Laravel no Packagist.

- Antes da criação de quaisquer projetos Laravel, há um procedimento no ```php.ini```, onde consiste em localizar o argumento ```extention=fileinfo```, e remover o 'ponto e vírgula' (;) antes do comando para descomentar o atributo, permitindo assim a criação dos projetos.

## Criação de Projetos Laravel ( Via Composer )

- O comando necessário para criar um projeto laravel é o seguinte:

```[cmd-let]: composer create-project --prefer-dist laravel/laravel (Nome do Projeto)```

    Nota:
        Leva um tempo para recuperar os pacotes caso não tenham sido recuperados anteriormente.

## Criação de Projetos Laravel ( Via Laravel Installer )

- O comando necessário para criar um projeto laravel utilizando o laravel installer já é um pouco diferente:

```[cmd-let]: laravel new (Nome do Projeto)```

- Entretanto é necessário que o "Laravel Installer", esteja instalado na Máquina.

## Complementação

- Para fechar sempre mantenha a [Documentação do Laravel](https://laravel.com/docs/7.x/releases) Aberta, para consultas ativas, e/ou referências de código.


<h1 id="artisantools">Artisan Management Tools</h1>

- No ambiente de produção, nos encontramos muitas vezes no âmbito de gerenciar as funções do sistema, para isto nós referenciamos o __Artisan__, que nada mais é do que um pacote com diversos comandos e ferramentas de manipulação do servidor php durante o desenvolvimento.

- Com o comando artisan, podemos iniciar o servidor automáticamente sem a necessidade de definir um endereço prévio, facilitando assim o rápida troca de informações do servidor.

  Para isto, utilizamos o comando: ```[terminal]: php artisan serve```, em que inicia o servidor com base em um ip local dinâmico.

- Aos tópicos que serão introduzidos neste momento são aos de controle de desenvolvimento, onde geram o acesso do servidor por meio de comandos em que controlam o acesso para que seja realizada devida manutenção, em caso de falhas reconhecidas, correção de bugs ou grandes atualizações do sistema, ainda com o servidor em funcionamento ou não.

A base do Comando é:

  ```[terminal]: php artisan <instrução>```

onde, ```<instrução>```, pode ser:

  | ```<instrução>``` | Funcionalidade |
  | :--------------: | :----------------- |
  | ```down``` | Põe o Servidor no Modo de Manutenção, fazendo-o com que, mesmo que aberto, fique indisponível para acesso temporáriamente. |
  | ```up``` | Retira o Servidor do Modo de Manutenção, disponibilizando o acesso novamente aos usuários. |


Os demais comandos serão referenciados ao decorrer do aprendizado.

---

<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="installation.md"><img src="../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#introduction"><img src="../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="routes.md"><img src="../assets/next-page.svg"></img></a></div>
</div>