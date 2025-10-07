# Resumo Estatístico — Loja de Peças de Moto (EDA)

## 1. Informações Gerais do Dataset

| Métrica                         | Valor     |
| ------------------------------- | --------- |
| **Período de análise**          | 2015–2025 |
| **Total de vendas registradas** | *113075*  |
| **Total de categorias únicas**  |  *223* |
| **Total de funcionários**       |  *9*       |


---

## 2. Estatísticas de Vendas

| Indicador                                  | Valor                            |
| ------------------------------------------ | -------------------------------- |
| **Ticket médio geral**                     | R$ 52,97                         |
| **Ticket médio pedido**                    | R$ 34,44                         |
| **Ticket médio crediário**                 | R$ 117,58                        |
| **Quantidade média de itens por venda**    | 2,9 UN                           |
| **Quantidade média de itens por pedido**   | 2,43 UN                          |
| **Quantidade média de itens por crediário**| 4,51 UN                          |
| **Produto mais vendido**                   | `OLEO SELENIA SPRINTA 4T 20W-50` |
| **Categoria mais vendida (volume)**        | Óleo                             |
| **Categoria mais lucrativa (faturamento)** | Pneu                             |
| **Período de maior venda (mês)**           | Agosto                           |
| **Período de menor venda (mês)**           | Fevereiro                        |

---

## 3. Estatísticas Temporais

| Indicador                              | Valor                                 |
| -------------------------------------- | ------------------------------------- |
| **Dias com vendas ausentes**           | Domingos (não funciona, geralmente)   |
| **Tendência de longo prazo**           | Crescimento até 2021, queda após 2022 |
| **Meses mais fortes (sazonalidade)**   | Julho a Outubro                       |
| **Meses mais fracos (sazonalidade)**   | Janeiro a Abril                       |
| **Dias da semana com maior movimento** | Segunda e Sexta-feira                 |

---

## 4. Funcionários e Desempenho

| Indicador                                  | Valor                                            |
| ------------------------------------------ | ------------------------------------------------ |
| **Funcionário com mais vendas**            | #3 e #4                                          |
| **Funcionário com ticket médio mais alto** | #9 e #0                                          |
| **Distribuição de vendas por funcionário** | Desbalanceada (poucos concentrando volume maior) |


---

## 5. Estrutura e Qualidade dos Dados

| Checagem                      | Resultado                                       |
| ----------------------------- | ----------------------------------------------- |
| Codificação categórica        | Aplicada a `Func` e `Categoria`                 |
| Normalização de preço         | Aplicado jitter log-normal para anonimização    |
| Frequência temporal detectada | Indefinida (`None`) — dados irregulares (dias sem vendas)         |
| Pedidos em datas diferentes | Existem `Ndoc` que estão presentes em dias diferentes (problema de números conflitantes) |
---

## 6. Destaques

* As **10 principais categorias representam cerca de 50% do faturamento total**.
* O comportamento de compra é **predominantemente unitário**, sugerindo oportunidade de promoções “leve 2”.
* **Categorias com alta rotatividade e faturamento simultâneo**: `OLEO`, `CABO`, `ROLAM.` — fundamentais para manter em estoque.
* **Picos sazonais** relacionados a clima: categorias como `CONJUNTO`, `KIT`, `BORR.` se destacam em meses chuvosos.
* Compras no crediário (`TIPO C`) tem o mesmo faturamento do pedido (`TIPO P`) apesar de ter metade da frequência, indicando pedidos mais caros.
* Funcionários `3` e `4` retratam mais de 90% do faturamento total em vendas.
---
