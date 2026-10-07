# Guia rápido – Relatório Gerencial de Vendas

Siga nesta ordem no **Power BI Desktop**.

## 0) Novo arquivo e dados

1. Abra o Power BI Desktop (arquivo novo / Sem título)
2. **Obter dados → Excel**
3. Abra: `desafio-relatorio-gerencial-vendas\dataset\Financial Sample.xlsx`
4. Marque **financials** → **Load / Carregar**
5. **Arquivo → Salvar como** →  
   `desafio-relatorio-gerencial-vendas\relatorio_Gerencial_Vendas.pbix`

## 1) Layout da Página 1

1. Renomeie a aba para `Sales Report`
2. **Inserir → Formas → Retângulo** (faixa esquerda, cor azul escuro)
3. **Inserir → Caixa de texto** → `Sales Report`
4. (Opcional) Caixa de texto: `Formação Power BI Analyst - Desafio de Projeto da DIO`

## 2) Segmentador de data

1. Visual **Segmentação de dados**
2. Campo: `Date`
3. Formato do segmentador → **Entre**
4. Título: `Selecione a data`

## 3) Cinco cartões

Crie 5 visuais **Cartão** com:

| Título do visual | Campo |
|------------------|-------|
| Total de Vendas | Sales |
| Unidades Vendidas | Units Sold |
| Descontos | Discounts |
| Vendas Brutas | Gross Sales |
| COGS | COGS |

## 4) Gráficos da Página 1

1. **Área ou Linha:** eixo `Month Name`, valores `Sales` → título `Soma de Sales por Mês`
2. **Barras:** eixo `Product`, valores `Sales` → `Sales x Produto`
3. **Barras** (segmento): `Segment` + `Sales` → nome no painel Seleção: `Sales x Segment - bar`
4. **Pizza**: `Segment` + `Sales` → `Sales x Segment - pie`  
   → redimensione para **ficar exatamente em cima** das barras de segmento
5. **Mapa**: Localização `Country`, tamanho `Sales` → `Sales x Country - map`
6. **Treemap**: `Country` + `Sales` → `Sales x Country - treemap`  
   → empilhe em cima do mapa

## 5) Bookmarks + botões

1. **Exibição → Seleção** e **Exibição → Indicadores**
2. No painel Seleção, oculte a pizza e o treemap (olho)
3. Crie indicador **Bar** (só Exibir)
4. Mostre pizza, oculte barras → indicador **Pie**
5. Estado com mapa visível e treemap oculto → **Map**
6. Treemap visível e mapa oculto → **Treemap**
7. Volte ao estado inicial (bar + map + filtros limpos) → **Clean** (pode gravar tudo)
8. **Inserir → Botões → Em branco** (5 botões): textos Bar, Pie, Map, Treemap, Clean  
   Ação de cada um: Tipo = **Indicador** → escolha o bookmark
9. Botão seta / “Página 2”: Ação = **Navegação de página** → página 2

## 6) Página 2

1. **+** nova página → renomear `Lucro Report Detalhado`
2. Segmentadores: `Year`, `Country`
3. Dispersão: `Product`, `Profit` (+ `Sales` no tamanho se quiser)
4. Treemap: `Segment` + `Profit`
5. Cascata: eixo Trimestre de `Date` + `Profit`
6. Tabela: `Year`, `Country`, `Profit`
7. Botão voltar → Navegação → `Sales Report`

## 7) Publicar e entregar

1. Salve o `.pbix`
2. **Publicar** no Power BI Service (se a conta permitir)
3. Suba a pasta no GitHub e entregue o link na DIO
