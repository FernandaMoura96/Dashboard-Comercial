# 📊 Dashboard Comercial | Power BI

Dashboard desenvolvido em **Power BI** para análise do desempenho de uma operação comercial entre 2022 e 2024.

O projeto reúne indicadores de faturamento, volume vendido, ticket médio e quantidade de clientes, permitindo analisar os resultados por **período, marca, localização e gênero**.

![Visão geral do Dashboard Comercial](screenshots/completo.png)

## 📑 Sumário

- [Sobre o projeto](#-sobre-o-projeto)
- [Objetivo](#-objetivo)
- [Perguntas de negócio](#-perguntas-de-negócio)
- [Principais indicadores](#-principais-indicadores)
- [Análises disponíveis](#-análises-disponíveis)
- [Principais insights](#-principais-insights)
- [Interatividade](#-interatividade)
- [Galeria](#-galeria)
- [Medidas DAX](#-medidas-dax)
- [Tecnologias utilizadas](#-tecnologias-utilizadas)
- [Estrutura do repositório](#-estrutura-do-repositório)
- [Como executar o projeto](#-como-executar-o-projeto)
- [Aprendizados](#-aprendizados)
- [Autora](#-autora)

## 💼 Sobre o projeto

Este projeto transforma dados comerciais armazenados em arquivos Excel em um dashboard executivo e interativo.

A solução foi construída para facilitar o acompanhamento dos resultados e apoiar a identificação de tendências, padrões de consumo e concentração de receita. Os visuais respondem de forma objetiva às principais perguntas de negócio e permitem diferentes níveis de exploração dos dados.

## 🎯 Objetivo

Desenvolver um painel que permita:

- Monitorar os principais indicadores comerciais;
- Acompanhar a evolução mensal do faturamento;
- Comparar o desempenho das marcas;
- Analisar a distribuição das vendas por gênero;
- Identificar diferenças de desempenho entre regiões;
- Explorar os resultados por meio de filtros e interações;
- Traduzir dados brutos em informações relevantes para o negócio.

## ❓ Perguntas de negócio

| Pergunta | Recurso utilizado |
|---|---|
| Qual é o faturamento total? | Cartão **Receita** |
| Quantas unidades foram vendidas? | Cartão **Qtd. Vendida** |
| Qual é o ticket médio? | Cartão **Ticket Médio** |
| Quantos clientes realizaram compras? | Cartão **Qtd. de Clientes** |
| Como o faturamento evoluiu ao longo do tempo? | Gráfico de área por ano e mês |
| Qual marca apresenta o maior faturamento? | Gráfico de barras por marca |
| Qual marca lidera o faturamento em cada região? | Mapa de faturamento |
| Como as unidades vendidas estão distribuídas por gênero? | Gráfico de rosca |

## 📈 Principais indicadores

Os valores abaixo representam a visão geral do dashboard, sem aplicação de filtros.

| Indicador | Resultado |
|---|---:|
| **Receita total** | **R$ 548,51 milhões** |
| **Quantidade vendida** | **2,12 milhões de unidades** |
| **Ticket médio** | **R$ 478,65** |
| **Quantidade de clientes** | **18 mil** |

> Os indicadores são recalculados automaticamente conforme os filtros e as seleções aplicados no dashboard.

## 🧩 Análises disponíveis

O dashboard contém os seguintes elementos:

- **Cartões de KPI:** apresentam receita, quantidade vendida, ticket médio e quantidade de clientes;
- **Gráfico de área:** exibe a evolução mensal do faturamento entre janeiro de 2022 e dezembro de 2024;
- **Gráfico de rosca:** apresenta a distribuição das unidades vendidas entre os gêneros feminino e masculino;
- **Mapa:** permite analisar o faturamento por localização e identificar a marca de maior desempenho em cada área;
- **Gráfico de barras:** compara o faturamento total das marcas em ordem decrescente.

## 🔎 Principais insights

### Concentração do faturamento

A **Contoso** responde por aproximadamente **41% da receita**, com cerca de **R$ 224 milhões** em faturamento.

As três marcas com melhor desempenho - Contoso, Northwind Traders e Litware - concentram aproximadamente **82% do faturamento total**, indicando forte dependência das marcas líderes.

### Evolução temporal

Em 2022, o faturamento mensal permaneceu principalmente entre **R$ 4 milhões e R$ 6 milhões**.

A partir de janeiro de 2023, os resultados passaram para uma faixa aproximada entre **R$ 14 milhões e R$ 25 milhões**, demonstrando uma mudança relevante no patamar de vendas.

### Pico de faturamento

O maior resultado mensal ocorreu em meados de 2024, quando o faturamento alcançou aproximadamente **R$ 25 milhões**. Ao final do período analisado, houve redução para cerca de **R$ 15 milhões**.

### Perfil das vendas

O público feminino representa **55,2% das unidades vendidas**, equivalente a aproximadamente **1,17 milhão de unidades**. O público masculino responde por **44,8%**, com cerca de **950 mil unidades**.

> **Observação:** a análise por gênero utiliza a quantidade de unidades vendidas, e não o faturamento.

## 🖱️ Interatividade

Os elementos do dashboard possuem interação cruzada. Ao selecionar uma marca, região, período ou gênero, os demais visuais são atualizados automaticamente.

Entre as funcionalidades disponíveis estão:

- **Filtro por marca:** seleção de uma barra para analisar exclusivamente os resultados da marca escolhida;
- **Filtro por localização:** seleção de uma região no mapa;
- **Filtro por período:** seleção de um ponto no gráfico para analisar um mês específico;
- **Filtro por gênero:** seleção de uma categoria no gráfico de rosca;
- **Drill-down:** navegação entre os níveis de ano e mês;
- **Tooltips:** exibição dos valores detalhados ao posicionar o cursor sobre os elementos.

Para remover uma seleção, clique novamente no elemento selecionado ou em uma área vazia do visual.

## 🖼️ Galeria

### Indicadores principais

![Cartões de KPI](screenshots/cartao_kpi.png)

### Evolução do faturamento

![Evolução mensal do faturamento](screenshots/fat_mes_ano.png)

### Distribuição das vendas por gênero

![Vendas por gênero](screenshots/fat_genero.png)

### Análise geográfica e desempenho por marca

![Faturamento por localização e marca](screenshots/faturamento_local.png)

### Exemplos de interação

<p align="center">
  <img src="screenshots/demo_1.png" alt="Exemplo de interação 1" width="48%">
  <img src="screenshots/demo_3.png" alt="Exemplo de interação 2" width="48%">
</p>

<p align="center">
  <img src="screenshots/demo-2.png" alt="Exemplo de interação 3" width="48%">
</p>

## 🧮 Medidas DAX

As principais métricas do dashboard seguem a lógica apresentada abaixo:

```dax
Total Vendido =
SUM(Vendas[Qtd_Vendida])
```

```dax
Faturamento =
SUM(Vendas[Faturamento])
```

```dax
Ticket Médio =
DIVIDE(
    [Faturamento],
    DISTINCTCOUNT(Vendas[ID_Pedido])
)
```

```dax
Qtd. de Clientes =
DISTINCTCOUNT(Vendas[ID_Cliente])
```

> Os nomes das tabelas e colunas acima são ilustrativos. Consulte o arquivo `dashboard_comercial.pbix` para verificar as medidas e os campos utilizados no modelo original.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação no projeto |
|---|---|
| **Power BI Desktop** | Modelagem, criação das medidas e desenvolvimento dos visuais |
| **DAX** | Cálculo das métricas e dos indicadores |
| **Power Query** | Importação e preparação dos dados |
| **Microsoft Excel** | Armazenamento das bases utilizadas como fonte |
| **Git e GitHub** | Versionamento e documentação do projeto |

## 📂 Estrutura do repositório

```text
Dashboard-Comercial/
├── data/
│   └── arquivos de origem em Excel
├── screenshots/
│   └── imagens e demonstrações do dashboard
├── dashboard_comercial.pbix
└── README.md
```

- **`dashboard_comercial.pbix`:** arquivo principal, contendo o modelo de dados, as medidas DAX e os visuais;
- **`data/`:** arquivos Excel utilizados como fonte de dados;
- **`screenshots/`:** imagens do dashboard e exemplos de interação;
- **`README.md`:** documentação do projeto.

## 🚀 Como executar o projeto

### Pré-requisito

Para abrir e explorar o arquivo, é necessário instalar o **Power BI Desktop**, disponível gratuitamente para Windows.

### Instalação

1. Clone este repositório:

```bash
git clone [github.com](https://github.com/FernandaMoura96/Dashboard-Comercial.git)
```

2. Acesse o diretório do projeto:

```bash
cd Dashboard-Comercial
```

3. Abra o arquivo `dashboard_comercial.pbix` no Power BI Desktop.

4. Caso seja necessário atualizar a origem dos dados, acesse:

```text
Transformar dados > Configurações da fonte de dados > Alterar origem
```

5. Selecione a pasta `data/` disponível no repositório.

6. Atualize os dados e explore o dashboard por meio dos gráficos, cartões e filtros.

## 📚 Aprendizados

Durante o desenvolvimento deste projeto, foram trabalhadas as seguintes competências:

- Criação de medidas DAX com soma, divisão e contagem distinta;
- Preparação e organização das fontes de dados;
- Construção de cartões de indicadores;
- Escolha de visuais adequados para diferentes perguntas de negócio;
- Configuração de filtros cruzados, drill-down e tooltips;
- Organização visual e hierarquia das informações;
- Interpretação de indicadores comerciais;
- Comunicação de insights por meio de visualização de dados.

## 👩‍💻 Autora

**Fernanda Moura**

Projeto desenvolvido para fins de estudo, prática e composição de portfólio em análise de dados e Business Intelligence.
