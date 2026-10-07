# Relatório Gerencial de Vendas com Power BI

Desafio de projeto da **Formação Power BI Analyst / DIO – Universia**.

Repositório de referência: [julianazanelatto/power_bi_analyst](https://github.com/julianazanelatto/power_bi_analyst)

## Objetivo

Criar um relatório gerencial de **2 páginas** com a sample **financials**, incluindo:

- Layout definido (faixa, título, cartões)
- Segmentador de data
- Visuais alternativos no mesmo espaço (barras/pizza e mapa/treemap)
- Botões + **Indicadores (Bookmarks)**
- Navegação entre páginas
- Publicação no Power BI Service (quando possível)

## Dataset

`dataset/Financial Sample.xlsx` → tabela `financials`

## Estrutura do repositório

```
.
├── dataset/
│   └── Financial Sample.xlsx
├── relatorio_Gerencial_Vendas.pbix
├── README.md
├── GUIA_PASSO_A_PASSO.md
└── ENTREGA_DIO.md
```

## Arquivo do projeto

`relatorio_Gerencial_Vendas.pbix`

## Estrutura do relatório

| Página | Nome | Conteúdo |
|--------|------|----------|
| 1 | Sales Report | KPIs, linha por mês, segmento (bar/pie), produto, país (map/treemap), botões e Clean |
| 2 | Lucro Report Detalhado | Segmentadores Year/Country, dispersão, treemap, cascata, tabela, botão voltar |

## Página 1 – passo a passo

### Layout

1. Forma retângulo azul à esquerda (menu)
2. Título: `Sales Report`
3. Texto opcional: `Formação Power BI Analyst - Desafio de Projeto da DIO`

### Segmentador

- Visual **Segmentação de dados**
- Campo: `Date`
- Estilo: **Entre**
- Título: `Selecione a data`

### Cartões (KPIs)

| Título | Campo |
|--------|-------|
| Total de Vendas | Soma de Sales |
| Unidades Vendidas | Soma de Units Sold |
| Descontos | Soma de Discounts |
| Vendas Brutas | Soma de Gross Sales |
| COGS | Soma de COGS |

### Gráficos fixos

1. **Linha / área:** `Month Name` + `Sales` → `Soma de Sales por Mês`
2. **Barras:** `Product` + `Sales` → `Sales x Produto`

### Visuais alternativos (empilhados)

**Sales x Segmento** (mesmo espaço):

- Barras: `Segment` + `Sales`
- Pizza/Rosca: `Segment` + `Sales`

**Sales x País** (mesmo espaço):

- Mapa: `Country` → Localização, `Sales` → Tamanho da bolha
- Treemap: `Country` + `Sales`

Use o painel **Seleção** (Exibição) para renomear e controlar visibilidade.

### Bookmarks e botões

Menu **Exibição → Indicadores** e **Seleção**.

| Bookmark | Visível | Oculto |
|----------|---------|--------|
| Bar | barras de segmento | pizza de segmento |
| Pie | pizza de segmento | barras de segmento |
| Map | mapa | treemap |
| Treemap | treemap | mapa |
| Clean | estado inicial (Bar + Map + filtros limpos) | — |

Para cada bookmark de troca de gráfico: marque só **Exibir** (visibilidade), desmarque dados/página atual.

Botões (**Inserir → Botões**):

- `Bar`, `Pie`, `Map`, `Treemap`, `Clean` → Ação tipo **Indicador**
- Seta / Página 2 → Ação **Navegação de página** → Página 2

## Página 2 – passo a passo

1. Renomear aba: `Lucro Report Detalhado`
2. Segmentadores: `Year` e `Country`
3. **Dispersão:** detalhes `Product`, eixo Y `Profit`, tamanho `Sales` (opcional)
4. **Treemap:** `Segment` + `Profit`
5. **Cascata:** eixo `Date` (Trimestre) + `Profit`
6. **Tabela:** `Year`, `Country`, `Soma de Profit`
7. Botão voltar → Navegação para Página 1

## Publicar no Service

1. **Arquivo → Publicar** (ou botão Publicar)
2. Escolha o workspace
3. No Power BI Service, abra o relatório e teste os botões

## Checklist de entrega (DIO)

- [x] Dataset financials
- [x] Página 1 com layout, KPIs, gráficos e segmentador
- [x] Visuais alternativos com bookmarks + botões
- [x] Página 2 de lucro
- [x] Navegação entre páginas
- [ ] Publicado no Power BI Service (quando a conta permitir)
- [x] Repositório GitHub com README + dataset + `.pbix`

## Links

- Dados e materiais: https://github.com/julianazanelatto/power_bi_analyst
- Curso DIO: *Criando Um Relatório Gerencial de Vendas com Power BI*
