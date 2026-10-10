# 📊 Dashboard de Vendas — Power BI

Projeto de dashboard em Power BI com o objetivo de responder às principais perguntas de negócio de uma operação de vendas por meio de indicadores (KPIs) claros e acessíveis.

---

## 🎯 Objetivo

Construir um dashboard que permita acompanhar, de forma rápida, o desempenho comercial: quanto foi vendido, quanto foi faturado, quanto foi devolvido e qual a participação do canal online.

## ❓ Perguntas de Negócio

| # | Pergunta | KPI no dashboard |
|---|----------|------------------|
| 1 | Qual o total de produtos vendidos? | Soma de Qtd. Vendida |
| 2 | Qual o percentual de devolução? | % devolução |
| 3 | Qual o faturamento total? | Soma de Faturamento |
| 4 | Qual o ticket médio? | Ticket médio |
| 5 | Quantas vendas foram feitas online? | Vendas online / % Vendas Online |

## 📈 Resultados (KPIs)

| Indicador | Valor |
|-----------|-------|
| Total de produtos vendidos | **2,12 Mi** |
| Quantidade devolvida | **7,543 Mil** |
| % de devolução | **0,36%** |
| Faturamento total | **R$ 548,51 Mi** |
| Ticket médio | **R$ 478,65** |
| Vendas online (quantidade) | **216 Mil** |
| % de vendas online | **10,22%** |

### 💡 Principais insights

- O volume de **2,12 milhões de produtos vendidos** gerou **R$ 548,51 milhões** em faturamento.
- A taxa de devolução é **muito baixa (0,36%)**, indicando boa qualidade de produto/entrega.
- O canal online representa cerca de **10% das vendas**, o que indica espaço para crescimento nesse canal.

> ✏️ *Complemente esta seção com os insights que você encontrar ao finalizar o dashboard (por produto, região, período etc.).*

---

## 🖼️ Visualização do Dashboard

### Cartões de KPIs

<!-- Substitua o caminho abaixo pelo da sua imagem -->
![KPIs principais](images/kpis.png)

### Visão geral (dashboard final)

<!-- Adicione aqui o print do dashboard completo -->
![Dashboard final](images/dashboard-final.png)

### Análises adicionais

<!-- Adicione quantos prints quiser, por exemplo: vendas por mês, por produto, por região -->
![Análise 1](images/analise-1.png)
![Análise 2](images/analise-2.png)

> 💡 **Como adicionar imagens:** salve os prints na pasta `images/` do repositório e ajuste os nomes nos links acima.

---

## 🧮 Medidas (DAX)

> ⚠️ Ajuste os nomes de tabelas e colunas conforme o seu modelo de dados.

```DAX
Total Vendido = SUM(Vendas[Qtd_Vendida])

Total Devolvido = SUM(Vendas[Qtd_Devolvida])

% Devolução = DIVIDE([Total Devolvido], [Total Vendido])

Faturamento = SUM(Vendas[Faturamento])

Ticket Médio = DIVIDE([Faturamento], DISTINCTCOUNT(Vendas[ID_Pedido]))

Vendas Online = CALCULATE([Total Vendido], Vendas[Canal] = "Online")

% Vendas Online = DIVIDE([Vendas Online], [Total Vendido])
```

---

## 🛠️ Ferramentas Utilizadas

- **Power BI Desktop** — modelagem, medidas DAX e visualizações
- **DAX** — criação das métricas e KPIs
- **Excel (.xlsx)** — fonte dos dados utilizados no dashboard

## 📂 Estrutura do Repositório

```
├── README.md
├── data/        # Arquivos .xlsx com as bases de dados utilizadas
└── images/      # Prints do dashboard
```

- **`data/`** — disponibiliza os arquivos `.xlsx` usados como fonte do dashboard.
- **`images/`** — reúne as imagens do dashboard final e das análises (a serem adicionadas).

## 🚀 Como Usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/FernandaMoura96/NOME-DO-REPOSITORIO.git
   ```
2. Acesse a pasta `data/` e abra os arquivos `.xlsx` para conhecer as bases.
3. Importe as bases no **Power BI Desktop** e recrie as medidas DAX descritas acima.

## 📚 Aprendizados

- Criação de medidas em DAX (soma, razão, filtros por canal)
- Construção de cartões de KPI e organização visual de um dashboard
- Tradução de perguntas de negócio em indicadores

## 👩‍💻 Autora

**Fernanda Moura**
🔗 [GitHub](https://github.com/FernandaMoura96)
