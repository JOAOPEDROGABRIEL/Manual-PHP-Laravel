### [Manual](../Readme.md) / Instalação

<h1 id="introduction">Instalação dos Componentes Necessários</h1>

- [VS Code](#vscodeinstaller)
- [PHP](#phpinstaller)
- [Composer](#composerinstaller)
- [Laravel](#laravelinstaller)

<h1 id="vscodeinstaller">Visual Studio Code</h1>

- A instalação do Visual Studio Code pode ser feita a partir do site oficial do [VS Code](https://code.visualstudio.com/), assim que a instalaçao do instalador for concluída, o procedimento padrão é seguir as instruções propostas no instalador, sem muitas expecificações, apenas seguir aos padrões pré-estabelecidos.



<h1 id="phpinstaller">PHP</h1>

- A instalação do PHP se dá por alguns procedimentos manuais que devem ser tomados com cautela.

## Primeiro Passo

- Deve-se realizar o Download da distribuição do site oficial do [PHP](https://php.net).
    - Normalmente o arquivo está nomeado em ```php-<version>-<arquiteture_supported>.zip```, ou em ```CEP``` para versões 'safe threads'.

- Logo após a realização do arquivo compactado, deve-se descompactar o diretório e realizar a aloação dos arquivos na pasta raiz ```C:/``` do computador.

- Após a alocação dos arquivos, deverá ser feito a configuração do diretório do php, nas variáveis de ambiente disponível em __(Configurações => Sistema => Sobre => Configurações Avançadas do Sistema => Variáeis de Ambiente => Variável do Sistema => Path >>> Duplo Clique)__, então, deverá ser criado um novo registro ```path```, para o ambiente php, onde deverá copiar o caminho diretório de do php instalado, e colar na nova variável de ambiente.

- Após isso o php está configurado em qualquer pasta de acesso, e a qualquer usuário, para verificar se a instalação foi realizada sem erros, é só digitar no console (preferencia cmd-let do windows) o seguinte comando:  ```php --version```, se tudo correr bem o comando deverá trazer a versão do php instalado.

        Nota: Após a instalação e/ou configuração de ambiente, se ainda houver cmd-lets abertos, deverão ser reiniciados para que as variáveis de ambiente sejam respectivamente reconhecidas pelo cmd-let!

## Segundo Passo

- Após a instalação do PHP na máquina deverá ser realizado a alocação de memória para uso do php na máquina (O padrão é 128M, ou 128mb, o que é pouco levando em consideração os recursos necessários para o funcionamento do sistema php), podendo assim ser alocado mais memória conforme tabela:

    | Memória Alocada | Sigla |
    | :--------------- | :-----: |
    | 128 Mb (Padrão) | 128M |
    | 'x' Mb | xM |
    | 1 Gb | 1G |
    | 'x' Gb | xG |
    | ilimitado (Recomendada) | -1 |

- A configuração é feita no ```php.ini```, que deverá ser aberto em um editor de texto e profurado pela função ```memory_limit```, e alterar para a configuração recomendada, para maior performance.

<h1 id="composerinstaller">Composer</h1>

- A instalação do gerenciador de dependencias php, composer se deriva de algumas etapas, onde deverá ser realizado o acesso ao site oficial do [Composer](https://getcomposer.org/download), após o download, inicie o instalador e siga as instruções condizentes e manter aos padrões pré-estabelecidos no instalador.

    - Para verificar a concluidade da instalação do composer, basta apenas, digitar no cmd-let o seguinte comando:

        ```composer --version```

    - Se o comando retornar a versão do Composer significa que os pacotes foram instalados com sucesso.

            NOTA DE USUÁRIO: a configuração do "php.ini", não é previamente configurado, e se selecionado a caixa onde relaciona a criação de um novo arquivo "php.ini", será criado a partir de um framework de configuração mínima do composer, para mais funcionalidades, deverá ser realizado a cópia e renomeação do "php.ini-development" para "php.ini", para que seja aplicado as alterações, e reiniciar a instalação do composer.


            IMPORTANTE: As versões do composer e php, devem ser compatíveis umas com as outras para que não hajam conflitos de versões, onde acabam ocorrendo erros de compatibilidade.

- O controle de versão do Composer se dá pelo arquivo ```composer.phar```, facilitando a troca de versões no diiretório oficial do composer (Geralmente em ```C:\ProgramData\ComposerSetup\bin\composer.phar```).

<h1 id="laravelinstaller">Laravel</h1>

## Instalação do Laravel Installer

- No CMD-LET, deverá ser executado o seguinte comando para instalar o "Laravel_Installer":

```[cmd-let]: composer global require laravel/installer```

## Configuração de Ambiente

- Após a instalação do composer e do laravel, deverão ser realizados as respectivas configurações do ambiente Composer, como a configuração do acesso aos pacotes oficiais do composer, e a instalação do criador de projetos laravel, onde simplificará a criação de projetos. Para que os pacotes sejam respectivamente instalados com êxito, deverão ser realizado as respectivas configurações:

### Configuração do Ambiente Laravel Installer:

- Caso não seja automaticamente configurado deverá ser feito manual seguindo todo o caminho para a manipulação das variáveis de ambiente __(Configurações => Sistema => Sobre => Configurações Avançadas do Sistema => Variáeis de Ambiente => Variável do Sistema => Path >>> Duplo Clique)__, e adicionado o seguinte caminho:

```[path]: %USERPROFILE%\AppData\Roaming\Composer\vendor\bin```

### Recuperação de Pacotes com o Composer:

- Esta configuração, denomina ao composer o respectivo repositório onde serão recuperados os pacotes para a criação dos futuros projetos:

```[cmd-let]: composer config -g repo.packagist composer https://packagist.org```

### Utilização dos protocolos HTTPS e SSH para recuperação de pacotes do Github:

- Esta configuração, denomina ao composer a configuração dos protocolos https e ssh ao recuperar pacotes geridos pelo Github:

```[cmd-let]: composer config -g github-protocol https ssh```

---

Com tudo configurado estamos prontos para começar a [desenvolver nossos projetos](first_steps.md).


---

<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="../Readme.md"><img src="../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#introduction"><img src="../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="first_steps.md"><img src="../assets/next-page.svg"></img></a></div>
</div>
    