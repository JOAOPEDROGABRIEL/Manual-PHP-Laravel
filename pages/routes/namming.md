### [Rotas](../routes.md) / [Inserção de Parâmetros](parameters.md) / [Agrupamento de Rotas](grouping.md) / Nomeando Rotas

<h1 id="introduction">Nomeando Rotas</h1>


- Função do laravel onde chama-se a rota pelo nome e não pela rota em si.

- Para nomear uma rota basta chamar o método ```->name('<string>')``` após a rota

        Route::get($uri, $callback)->name('<name>);

- Aplicando nas Rotas criadas:

        Route::get('/', [\App\Http\Controllers\PrincipalController::class, 'principal'])->name('site.index');
        Route::get('/sobrenos', [\App\Http\Controllers\SobreNosController::class, 'sobrenos'])->name('site.sobrenos');
        Route::get('/contato', [\App\Http\Controllers\ContatoController::class, 'contato'])->name('site.contato');
        Route::get('/login', function() { return 'Login'; })->name('site.login');

        Route::prefix('/app')->group(function() {
            Route::get('/clientes', function() { return 'Clientes'; })->name('app.clientes');
            Route::get('/fornecedores', function() { return 'Fornecedores'; })->name('app.fornecedores');
            Route::get('/produtos', function() { return 'Produtos'; })->name('app.produtos');
        });

<h1>Real Propósito da Nomenclatura de Rotas</h1>

- A nomenclatura de rotas, tem o intuito de "apelidar", as rotas dentro do framework laravel fazendo assim que referências no código sejam simplificadas, exemplo:
    
        <a href="{{ route('site.route') }}">Route</a>

- A principal vantagem de se utilizar a nomenclatura de rotas, é a reciclagem do próprio código, uma vez que se a rota não for a mesma novamente, não irá importar já que a rota está sendo nomeada dentro do código, então os scrips continuarão funcionando corretamente sem que sejam inutilizado pelo framework, causado por uma má escrita das rotas, por parte do desenvolvedor.


<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="grouping.md"><img src="../../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="../routes.md"><img src="../../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#"><img src="../../assets/next-page.svg"></img></a></div>
</div>