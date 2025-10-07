# Insights ao longo da análise
* O número de produtos é alto, o que indica que o catálogo da loja é grande.
* Quando comparamos com a categoria vemos que os produtos são facilmente agrupáveis, então temos vários produtos de uma mesma categoria.
* 4 dos 5 produtos mais vendidos são óleo.
* As categorias mais vendidas são: Oleo, Retentor(RET.), Parafuso(PARAF.), Lampada(LAMP.) e Junta.
* As categorias que são menos vendidas podem ser encaixadas em outras categorias mais frequêntes, como x-pneu provavelmente é PNEU, LAMPADA pode ir para LAMP.(mais frequente). 
* A grande parte das peças são vendidas a uma única unidade, ou seja, a compra de muitos exemplares da mesma peça é raro. [(Sugerir um desconto para compra de 2 peças, como dois óleos, ou duas lampadas)]
* As 5 melhores categorias de faturamento, em ordem, são: *Pneu*, *Kit*, *Oleo*, *Bateria* e *Cilindro*.
* Os funcionários *3* e *4* foram os que mais realizaram vendas.
* Os funcionários *9* e *0* tem em suas vendas produtos mais caros.
* Apesar do número de vendas do tipo *P* ser o dobro do tipo *C*, o valor faturado nos dois tipos é bem próximo. Assumindo que o tipo *C* é **Crediário** e *P* sendo **Pedido**, pode-se pensar que os clientes com crediário utilizam-no para comprar peças mais caras e dividir em parcelas.
* Durante todo o período de dados, o nosso produto `OLEO SELENIA SPRINTA 4T 20W-50` é TOP 1 tanto em **Quantidade vendida** quanto em **Faturamento**.
* Foram no total 113075 vendas.
* O pandas não consegue detectar a frequência da vendas com ´df['Data'].dt.freq´, indicando possíveis falhas nas datas, ou dias faltantes. Para uma análise temporal precisaremos arrumar os dados e possivelmente fixar uma frequência. De fato encontramos dias que não há vendas registradas.
* Precisamos fazer uma análise mais profunda para entender a sazonalidade e as tendencias de curto e longo prazo.
* Durante o pedíodo de 2020 e 2021 as vendas alavancaram bastante.
* Desde 2022 até hoje, as vendas vem em queda. Por quê?
* Conseguimos detectar uma sazonalidade anual.
* Durante o período de dados que temos, conseguimos ver que os melhores meses tendem a ser de 7~10 (Julho a Outubro). Depois vamos ver quais as categorias/peças que mais sem em cada perído, assim teremos uma noção se será algo relacionado a clima, festas etc.
* Os piores meses de venda são os primeiros 4, ou seja (Janeiro à Abril)
* Sendo melhor mês `Agosto`, e pior mês `Fevereiro`.
* Entre 2020 e 2022 a loja teve um período de renda muito acima. Vamos analisar também.
* Separar por ano quais peças foram fundamentais para o faturamento, quais peças pararam de vender? Quais tem crescido a venda?
* Segunda e Sexta são os dias mais movimentados.
* O ticket médio é de R$52,97, para tipo `P` é de R$34,44 e para tipo `C` de R$117,58.
* Quanto a categorias com maior rotatividade e venda de estoque temos 9 produtos que aparecem nos 11 anos no top 10: `ARRUELA`, `CABO`, `JUNTA`, `LAMP.`, `OLEO`, `PARAF`, `RET.`, `PORCA`, `ROLAM`.
* Para o valor de faturamento total, temos apenas 5 categorias presentes em todos os 11 anos, sendo elas `BATERIA`, `CILINDRO`, `OLEO`, `KIT` e `PNEU`. Nos anos de 2018 até 2024 são ainda consistentemente top 5 faturamento da loja. As outras categorias que devem ser mencionadas também para o top 10 são `CABO`, `CAPACETE`, `PISTAO/ANEL`, `CAMARA` e `ROLAM.`.
* Com essas duas noções anteriores podemos ver que `OLEO`, `CABO` e `ROLAM.` são importantes sempre ter em estoque, pois tem rotatividade alta e também influenciam no faturamento.
* O faturamento da loja depende em média, 50% dos produtos top 10.
* A categoria `CONJUNTO` aparece no top de faturamento nos meses 4,5 e 7. São os meses de chuva.
* Dos meses 5 à 9 a categoria `KIT` aparece. São meses de chuva. Além disso a categoria `BORR.` aparece nos meses 12 e 1 o que pode indicar que existe uma razão, já que são meses subsequentes.
* (NÃO DEU CERTO) mudar o heatmap da função de análise de categoria para variação de vendas ao invés do valor fixo (Ao fazer percebi que o heatmap vai comparar as vendas de um mês em comparação com o mês passado, o que quase inviabiliza a análise dos melhores meses)
* Para a análise de mais de um mês de aumento de vendas é necessário pensar em alguma forma de análise conjunta dos meses. (Talvez observar aumentos grandes e sequencias de quedas muito pequenas indiquem meses bons e claro, crescentes conjuntas)
* A análise por média não foi boa pois um mês com uma alta desproporcional atrapalha a entender a sazonalidade, então vou usar a abordagem da mediana, um exemplo demonstrado com as categorias `LAMP.` e `CAPACETE`.