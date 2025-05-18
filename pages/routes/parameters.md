### [Rotas](../routes.md) / Inserção de Parâmetros

<h1 id="introduction">Inserção de Parâmetros nas Rotas:</h1>

Receber parâmetros em rotas no Laravel permite que você crie URLs dinâmicas, o que facilita a organização e o gerenciamento de dados, além de tornar a aplicação mais escalável e flexível. Os parâmetros permitem identificar recursos específicos ou realizar ações específicas com base nos dados passados na URL. 

- As Rotas podem Receber Parâmetros como parte da requisição em sua lógica a partir do comando:
        
        [...]

        Route::get('/<nome_da_rota>'/{<parametro>}, function(<tipo> $<parametro>) {
            //lógica da rota

            //exemplo de uso de parâmetro:
            echo "O valor do parâmetro é: $<parametro>";
        });

        [...]

- Nota Pessoal:

        Referencia de Valores são identificados pela instrução:

            $<nome_da_variável>

### Uso das Variáveis em Strings:
| Uso | Aspas | Informações |
| :-- | :---: | :---------- |
| Comum | ```''``` | ```string texto_variavel = 'texto aqui'.$<nome_da_variavel>;``` |
| Interpolado | ```""``` | ```string texto_variavel = "texto interpolado com $<nome_da_variavel> aqui!";``` |

### Uso de Variáveis Opcionais:

- A aplicação destas variáveis pode ser opcional, correspondente a solicitação do usuário:

        Route::get(
            '/contato/{nome?}/{categoria?}/{assunto?}/{mensagem?}', 
            function(
                string $nome = Desconhecido, 
                string $categoria = Outros, 
                string $assunto = Outro, 
                string $mensagem = 'Mensagem Não Informada!') {
            echo "Estamos Aqui $nome! \n";
            echo "Categoria: $categoria \n";
            echo "Assunto: $assunto \n";
            echo "Mensagem: $mensagem";
        });

### Ordem de Prioridade

- Entretanto, quando estamos utilizando o framework laravel, falamos de uma limitação em questão de rotas, uma vez que o framework só entenderá o que foi passado, se os parâmetros forem organizados por prioridade sendo os conteúdos a esquerda de maior prioridade, e os da direira de menor prioridade de inserção, levando a preferir organizar os conteúdos opcionais a direita, para melhor entendimento do framework!

        Maior Prioridade <----------------------------------- Menor Prioridade
        
                ... get('/<rota>/{arg1}/{arg2}/{arg3}/.../{argx?}') ...

### Filtragem de Parâmetros:

- Filtrar dados em rotas no Laravel é fundamental para criar aplicações web eficientes e flexíveis. Isso permite que você personalize as respostas da sua aplicação com base em critérios específicos, como parâmetros de consulta ou valores de sessão, e execute ações antes de manipular dados, como autenticação ou validação:

        Route::get(
            '/contato/{nome}/{categoria_id}', 
            function(
                string $nome, 
                int $categoria_id) {
            echo "Estamos Aqui $nome! - Categoria: $categoria_id";
        })->where('categoria_id', '[0-9]+');

- Para filtrar utilizamos o método ```where``` ao final da instrução route, contendo as instruções :

    ```...->where('variável_relacionada', 'expressão_e-ou_intervalo_de_valores');```

<div style="display: flex; align-items: center; justify-content: space-between; width: 100%; height: 35px;">
  <div style="width: 5%; background-color: transparent;"><a href="../views.md"><img src="../../assets/back-page.svg"></img></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="../routes.md"><img src="../../assets/back-directory.svg"></a></div>
  <div style="width: 5%; background-color: transparent;"><a href="#"><img src="../../assets/next-page.svg"></img></a></div>
</div>