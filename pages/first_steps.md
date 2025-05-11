### [Manual](../Readme.md) / [Instalação](installation.md) / Primeiros Projetos

# Criação de Projetos Laravel

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