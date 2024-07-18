Olá, caro pessoal da DIO!

Gostaria muito de começar dizendo que adorei sinceramente o curso. O ensinamento passado contribuiu muito para o meu desenvolvimento técnico (apesar de ser um projeto no-code), a plataforma do SageMaker Canvas é muito interessante e tem muito a proporcionar, sendo então uma ferramenta valiosa.

Bom, a respeito do projeto que me empenhei para entregar a vocês a devolutiva, informo que escolhi o dataset que vocês disponibilizaram chamado "dataset-1000-com-preco promocional-e-renovacao-estoque". Notei que todos os datasets seguiam uma montagem semelhante de dados, porém o motivo de eu ter escolhido este dataset, é que o achei mais completo, com mais informações que poderiam ser levadas em consideração para a análise envolvendo a previsão de estoque. Apesar de ser um dataset com informações fictícias, acho importante praticar considerando um cenário real, em que todas os dados à disposição tem sua importância e podem influenciar nas análises.

Iniciei convertendo o arquivo do dataset para excel, pois o tipo de arquivo que vocês disponibilizaram, não era muito prático para ver os dados, e utilizei muito a ferramenta de filtragem do excel para visualizar melhor as informações e procurar os produtos que tiveram mais presença em determinadas situações. Talvez não seja a maneira mais prática de fazer isso, mas como eu já tenho mais afinidade com excel, optei em trabalhar dessa forma.

Na plataforma do SageMaker Canvas, importei o dataset; depois selecionei o campo que seria usado para previsão (no caso, quantidade_estoque), e então o id. Notei que a coluna de preco estava com uma mensagem escrita "Future values", e no início não entendi o que significava, e ao pesquisar, descobri que campos com informação de preço, a AWS considera um campo que pode impactar significativamente na análise, então ela deixou esse campo com esta informação. Aceitei as sugestões propostas de tornar 0 as células sem valores (apesar de eu ter notado que nenhuma célula estava sem valor, e achei isso muito bacana, pois vimos no curso que tendo células com valor 0 pode impactar na análise e causar uma falsa impressão). E escolhi a opção de "Standard Build" por ele oferecer uma previsão mais precisa.

Após esta fase, notei que de cara ele mostra que a coluna de FRAG_PROMOCIONAL foi considerada que causa impacto de até 89% na previsão. Passei para analisar os itens individualmente na fase de Predict, e comecei vendo como eram os percentis dos produtos mais baratos, e notei que alguns o percentil mostrava uma previsão consideravelmente ok de estoque (entre 55 e 69), e outros produtos mostrava um percentil de previsão bem baixo (entre 12 e 30). Descobri que alguns produtos com previsão baixa de estoque não haviam tido muitos dias de promoção. Então com base neste dataset fictício, podemos considerar que apesar do produto estar entre os mais baratos, as vendas podem ser maiores se ele entrar mais em promoção. Porém notei que não é necessariamente uma regra, pois o segundo produto mais barato, é um dos que menos estiveram em promoção e ainda, a previsão de estoque dele é alta (entre 65 e 77). 

Analisando os produtos mais caros, notei que os produtos do topo dessa análise tem uma boa venda (entre 55 e 75), sendo assim, uma previsão de estoque na acima da média, enquanto que outros que são um pouco mais baratos do que estes, e ainda se encontram em valor bem maior em comparação aos produtos mais baratos, tem uma previsão de estoque um pouco baixa (entre 40 e 55) . Isso me faz considerar que os clientes que tem intenção de pagar um valor maior na produto, preferem os produtos mais caros, que devem prometer mais benefícios e qualidade, do que os produtos que são um pouco mais baratos do que estes.

Também cheguei na conclusão de que os produtos que estão no meio, na comparação de preço, que não possuem muitos dias promocionais, também podem ser menos vendidos.

Então, podemos chegar na conclusão, de que os produtos mais caros e os produtos mais baratos são bem vendidos, podendo talvez os produtos no meio termo, ter uma venda um pouco menor. 

Tenho ciência de que este dataset é fictício, e acho que os dados foram gerados aleatoriamente igual os datasets mostrados no curso, então acho difícil conseguir achar insights com precisão e tendências concretas, porém participar do projeto ainda me acrescentou muito e foi de grande valor.

Obrigada, pessoal da Dio, e até uma próxima!

Atenciosamente,

Anna Magnani
