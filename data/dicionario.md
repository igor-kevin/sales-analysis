# Dicionário de Dados - Projeto Dados Loja

Este dicionário serve para informar o que cada coluna do dataset significa, dando exemplos e observações sobre o funcionamento.

| Coluna     | Tipo (pandas)  | Descrição | Exemplos / Observações |
|------------|-----------------|-----------|------------------------|
| **Data**   | datetime64[ns] | Data da venda do produto. | `2023-07-15` |
| **Produto**| category / str  | Nome do produto vendido. | `Filtro de óleo`, `Pastilha de freio` |
| **Quantidade** | int64 | Quantidade vendida neste item da venda. | `1`, `3` |
| **ValorMedio** | float64 | Valor médio unitário do produto nesta venda. | `45.90` |
| **Total** | float64 | Total da linha (Quantidade × ValorMedio). | `137.70` |
| **Func** | category | Código do funcionário que realizou a venda. | `1`, `7` |
| **Codigo** | int64  | Código interno do produto. | `12345` |
| **Categoria** | category | Categoria do produto. | `PNEU`, `OLEO` |
| **Ndoc** | int64 | Número identificador da venda (pedido). Pode se repetir para itens de um mesmo pedido. | `548213` |
| **Tipo** | category | Tipo de documento da venda. | `P`, `C` |


### Observações
- **Jitter**: Para proteger informações reais da loja, os valores de `ValorMedio` e `Quantidade` foram alterados com ruído estático.
- **Duplicidade**: `Ndoc` pode se repetir, pois o dataset é feito de maneira que cada produto vendido compõe uma linha.

### Versões do Dicionário
| Versão | Data | Alteração |
|-------|------|-----------|
| 0.1 | 2025-09-21 | Criação inicial do dicionário de dados. |