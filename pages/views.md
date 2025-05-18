### [Manual](../Readme.md) / [Instalação](installation.md) / [Primeiros Projetos](first_steps.md) / [Rotas](routes.md) / [Controllers](controllers.md) / Views

<h1 id="introduction">Views</h1>

<abbr title="Visões">Views</abbr>, são visões produzidas do lado do servidor e retornadas ao usuário. Este modelo é conhecido como modelo <abbr title="Web View">Tradicional</abbr>, onde as requisicões são processadas do lado do servidor e enviadas para o cliente como informação.

Atualmente há um método mais moderno de desenvolvimento web, em que consiste na separação do front-end com o back-end, por meio de uma api, ao decorrer do manual serão mostrados mais detalhes sobre desenvolvimento web utilizando <abbr title="Application Programming Interface">APIs</abbr>.

---

### Modelo Tradicional

- As views são literalmente as páginas da aplicação, ou seja, o front-end, onde serão aplicados o <abbr title="HyperText Markup Language">html</abbr> e <abbr title="Cascating Style Sheet">css</abbr> da página.
    As views podem ser referenciadas nas rotas e também nas ações do controladores, através da instrução:

    view('nome_da_view');

    Nota Pessoal: as Views tem este tratamento pois são consideradas como objetos, e realmente são, uma vez que condensam em si um pacote do html, css e scripts do php, em um tratamento no framework, sendo assim, podem ser utilizadas em retornos de função como de ações de controladores, usando linha de código no final da ação:

    [...]
    
    return view('nome_da_view');
    
    [...]

<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="controllers.md"><img src="../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#introduction"><img src="../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="routes/parameters.md"><img src="../assets/next-page.svg"></img></a></div>
</div>