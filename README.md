# Análise de Vendas AluraStore

## Visão Geral

Este repositório contém um Jupyter Notebook (`AluraStoreBr.ipynb`) detalhando uma análise abrangente dos dados de vendas de quatro filiais distintas da AluraStore. A análise explora diversas métricas de desempenho, incluindo faturamento, volume de vendas por categoria, satisfação do cliente, desempenho de produtos, custos de frete e distribuição geográfica das vendas.

## Objetivo

O objetivo principal desta análise é comparar o desempenho das quatro Lojas AluraStore com base em dados históricos de vendas. Os insights derivados são usados para fornecer uma recomendação baseada em dados ao "Senhor João" sobre qual loja seria a candidata mais adequada para uma potencial venda, considerando um equilíbrio entre desempenho financeiro, satisfação do cliente e aspectos operacionais.

## Fonte dos Dados

A análise utiliza quatro arquivos CSV, cada um representando dados de vendas de uma loja:

*   **Loja 1:** `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_1.csv`
*   **Loja 2:** `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_2.csv`
*   **Loja 3:** `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_3.csv`
*   **Loja 4:** `https://raw.githubusercontent.com/alura-es-cursos/challenge1-data-science/refs/heads/main/base-de-dados-challenge-1/loja_4.csv`

Os principais pontos de dados incluem: Detalhes do produto (`Produto`), Preço (`Preço`), Custo do frete (`Frete`), Data da compra (`Data da Compra`), Vendedor (`Vendedor`), Local da compra (`Local da compra`), Avaliação do cliente (`Avaliação da compra`), Tipo de pagamento (`Tipo de pagamento`), Número de parcelas (`Quantidade de parcelas`), Latitude (`lat`) e Longitude (`lon`).

## Análises Realizadas

O notebook abrange as seguintes etapas analíticas:

1.  **Carregamento dos Dados e Exploração Inicial:** Importando bibliotecas necessárias (Pandas, Matplotlib, Seaborn) e carregando os datasets.
2.  **Análise de Faturamento:** Calculando e comparando o faturamento total (soma de `Preço`) para cada loja.
3.  **Vendas por Categoria:** Analisando o volume de vendas para cada categoria de produto (`Categoria do Produto`) em todas as lojas.
4.  **Satisfação do Cliente:** Calculando e comparando a avaliação média do cliente (`Avaliação da compra`) para cada loja.
5.  **Desempenho de Produtos:** Identificando os produtos (`Produto`) mais e menos vendidos dentro de cada loja.
6.  **Análise do Custo de Frete:** Calculando e comparando o custo médio de frete (`Frete`) por loja.
7.  **Análise Geográfica:**
    *   Mapeando locais de venda usando Latitude (`lat`) e Longitude (`lon`).
    *   Visualizando a distribuição geográfica das vendas por loja usando gráficos de dispersão.
    *   Identificando áreas de concentração de vendas usando mapas de densidade (Heatmaps / KDE plots).
    *   Analisando potenciais influências geográficas no desempenho das lojas.

## Principais Descobertas e Conclusão

*   **Faturamento:** A Loja 1 gerou o maior faturamento total, enquanto a Loja 4 gerou o menor. As Lojas 2 e 3 tiveram faturamentos comparáveis e robustos.
*   **Mix de Vendas:** Todas as lojas vendem bem nas categorias principais como 'eletronicos' e 'moveis'. A Loja 3 lidera em 'moveis', a Loja 1 em 'eletronicos'. A Loja 4 não domina nenhuma categoria principal em comparação com as outras.
*   **Avaliações dos Clientes:** Todas as lojas mantêm médias de avaliação altas (próximas a 4.0), com a Loja 3 e a Loja 2 ligeiramente à frente. A Loja 1 teve a média marginalmente mais baixa.
*   **Custos de Frete:** A Loja 4 se beneficia do menor custo médio de frete, enquanto a Loja 1 tem o maior.
*   **Geografia:** As vendas estão distribuídas nacionalmente, com sobreposição significativa entre as lojas. Concentrações ocorrem em grandes áreas urbanas e potencialmente perto das origens das lojas (SP, RJ, DF, RS). Nenhuma desvantagem geográfica clara foi encontrada para a Loja 4 com base apenas na localização do cliente.

**Recomendação:** Com base na análise geral, particularmente no faturamento total significativamente menor em comparação com as outras lojas, **a Loja 4 é recomendada como a principal candidata para venda.** Embora tenha vantagens como o baixo custo médio de frete, estas não parecem compensar o menor desempenho financeiro relativo às Lojas 1, 2 e 3.

## Visualizações

A análise é suportada por diversas visualizações, incluindo:

*   Gráfico de Barras: Faturamento Total por Loja
*   Gráfico de Barras Agrupadas: Volume de Vendas por Categoria e Loja
*   Gráfico de Dispersão: Preço vs. Custo do Frete
*   Gráfico de Barras Horizontais: Avaliação Média do Cliente por Loja
*   Gráfico de Dispersão: Distribuição Geográfica das Vendas por Loja
*   Mapa de Densidade (Heatmap / KDE Plot): Densidade Geográfica das Vendas (Todas as Lojas)

## Tecnologias Utilizadas

*   Python 3.x
*   Pandas
*   Matplotlib
*   Seaborn
*   Jupyter Notebook / Google Colab

## Como Executar

1.  Clone este repositório:
    ```bash
    git clone <url-do-repositorio>
    cd <nome-do-repositorio>
    ```
2.  Certifique-se de que você tem Python instalado.
3.  Instale as bibliotecas necessárias:
    ```bash
    pip install pandas matplotlib seaborn
    ```
    *(Observação: Se estiver executando localmente, você pode precisar do `jupyter` também: `pip install jupyter`)*
4.  Abra o notebook `AluraStoreBr.ipynb` usando Jupyter Notebook, JupyterLab, Google Colab, VS Code ou outro ambiente compatível.
5.  Execute as células sequencialmente para reproduzir a análise e as visualizações. O notebook busca os dados diretamente das URLs de origem.
