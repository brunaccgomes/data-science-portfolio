# Data Mining no Estudo do Peso de Recém-Nascidos em São Paulo (2021)

## Introdução

Este notebook foi desenvolvido no ambiente Google Colab utilizando a linguagem de programação Python. Os principais pacotes utilizados incluem numpy, pandas, scikit-learn, entre outros. O objetivo principal deste estudo é analisar dados relacionados ao peso de recém-nascidos no momento do parto, com foco específico no estado de São Paulo, Brasil, durante o ano de 2021.

### Objetivo do Estudo
Busco verificar a influência de determinados fatores (atributos) no peso dos recém-nascidos. Para atingir esse objetivo, pretendo empregar técnicas de aprendizado de máquina não supervisionado, incluindo métodos preditivos de classificação e regressão.

## Contexto

Este estudo se enquadra no contexto mais amplo de Data Mining, que envolve a descoberta de padrões, tendências e informações valiosas em grandes conjuntos de dados. Utilizando métodos preditivos, buscamos explorar e compreender os dados relacionados ao peso de recém-nascidos no estado de São Paulo durante o ano de 2021.

### Justificativas para o Uso de Métodos Preditivos em Data Mining

1. **Identificação de Padrões e Relacionamentos:**
   - Métodos preditivos ajudarão na identificação de padrões complexos nos dados, contribuindo para uma compreensão mais profunda dos fatores que influenciam o peso dos recém-nascidos.

2. **Caracterização dos Fatores Influenciadores:**
   - Os modelos preditivos permitirão a caracterização da importância relativa de cada atributo na determinação do peso do recém-nascido, enriquecendo a análise dos fatores influenciadores.

3. **Visualização de Resultados:**
   - Visualizações de dados geradas pelos modelos preditivos serão ferramentas eficazes para comunicar padrões e insights descobertos durante a análise de Data Mining.

4. **Validação de Hipóteses:**
   - Os modelos preditivos podem ser utilizados para validar ou refutar hipóteses prévias sobre a relação entre determinados fatores e o peso dos recém-nascidos.

5. **Entendimento do Comportamento dos Atributos:**
   - A análise do comportamento dos atributos, facilitada pelos métodos preditivos, fornecerá insights sobre a interação entre diferentes variáveis.

6. **Análise de Importância dos Atributos:**
   - Métodos de análise de importância de atributos serão aplicados para destacar quais variáveis são mais relevantes na explicação das variações no peso dos recém-nascidos.

## Dataset
- Os dados usados nesse estudo, foram extraídos através da plataforma DATASUS https://datasus.saude.gov.br/transferencia-de-arquivos/.
- O formato do arquivo extraído é .dbc e convertido para .csv.
   - O processo de conversão não é foco desse experimento, logo essa transformação não será contemplada aqui.

- Para realizar o download do arquivo, os seguintes filtros foram aplicados:
   - Fonte: SINASC - Sistema de Informação de Nascidos Vivos
   - Modalidade: Dados
   - Tipo de Arquivo: DN - Declaração de nascidos vivos 1994 a 2022
   - Ano: 2021
   - UF: SP
