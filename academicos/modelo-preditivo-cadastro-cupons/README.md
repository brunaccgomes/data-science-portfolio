# Modelo Preditivo para Campanha de Marketing

## Introdução
Documentar as fases de um projeto em Data Science para elaborar e implantar modelo de aprendizado de máquina, baseado no seguinte contexto:

"A empresa Bebidas Ltda., uma das maiores companhias de bebidas do país, pertencente ao setor econômico de comércio e varejo, tem como objetivo
aumentar o faturamento referente a venda de seus produtos e reforçar sua marca entre seus consumidores através da campanha de marketing e relacionamento
denominada “Promoção Cadastro Que Dá Premios”.
Nossa agência tem a missão de atuar, através das equipes de Planejamento e Mídia, em ações de relacionamento com o público consumidor através do
hotsite da promoção, redes sociais, televisão e canais de comunicação via e-mail, sms e whatsapp.
Nosso time de Planejamento e Mídia (Stakeholders) será suportado pela área de Inteligência de Dados. A equipe, composta por cientistas e analistas de
dados, atuará nas bases históricas das edições anteriores e na base gerada durante a campanha atual.
A área de Inteligência de dados será responsável por desenvolver e implementar um modelo de aprendizado de máquina para informar a quantidade aproximada de produtos cadastrados diariamente."

### Objetivo do Projeto

Respaldar as ações de relacionamento com o consumidor de acordo com o volume diário de cadastros de produtos e participantes da promoção, através do auxílio de aprendizando de máquina.
Esse Modelo Preditivo será desenvolvido e avaliado, inicialmente, com os dados históricos e implementado para a base atual, sendo monitorada e ajustada durante a campanha corrente.


### Mapa Mental
[ver no mindmeister](https://mm.tt/app/map/3067556396?t=AcNaBcSsEt)

![MapaMental](https://github.com/brunaccgomes/data-science-portfolio/assets/93496254/3474be64-3ce6-489e-9ced-1ca23e23ab0e)

### Fases do Projeto

### 1. Definição do Problema
  A empresa Bebidas Ltda., uma das maiores companhias de bebidas do país, pertencente ao setor econômico de comércio e varejo, tem como objetivo
aumentar o faturamento referente a venda de seus produtos e reforçar sua marca entre seus consumidores através da campanha de marketing e relacionamento
denominada “Promoção Cadastro Que Dá Premios”.

  Nossa agência tem a missão de atuar, através das equipes de Planejamento e Mídia, em ações de relacionamento com o público consumidor através do
hotsite da promoção, redes sociais, televisão e canais de comunicação via e-mail, sms e whatsapp.

  Nosso time de Planejamento e Mídia (Stakeholders) será suportado pela área de Inteligência de Dados. A equipe, composta por cientistas e analistas de
dados, atuará nas bases históricas das edições anteriores e na base gerada durante a campanha atual.

  A área de Inteligência de dados será responsável por desenvolver e implementar um modelo de aprendizado de máquina.

- **Modelo Preditivo:** Informar a quantidade aproximada de produtos cadastrados diariamente.
    - O principal objetivo é respaldar as ações de relacionamento com o consumidor de acordo com o volume diário de cadastros de produtos e
participantes da promoção.
    - Esse modelo preditivo será desenvolvido e avaliado, inicialmente, com os dados históricos e implementado para a base atual, sendo monitorada e
ajustada durante a campanha corrente.

### 2. Coleta de Dados
- **Bases de Dados Históricas:**
  - Distribuídas por ano de edição da campanha em arquivos de formato .CSV.
  - Serão disponibilizadas em servidor FTP do cliente.
  - O acesso ao servidor para extração do arquivo será manual, informando login e senha disponibilizados pelo cliente, e extração será feita via download dos arquivos.
- **Bases de Dados Ativa:**
  - Disponibilizadas em servidor FTP do cliente em arquivos de formato .CSV.
  - O acesso ao servidor e extração dos dados serão realizados diariamente em processo automatizado via comandos .BAT;
  - Os arquivos serão copiados para diretório no servidor da agência.
    
### 3. Pré-processamento de Dados
- Os registros dos arquivos serão analisados em processo de verificação de codificação dos arquivos e carregados em base stage no servidor SQL
Server.
- A de limpeza, normalização e transformação nos dados, tratando valores ausentes, removendo duplicatas e ajustando formatos serão realizadas via
execução de um conjunto de Stored Procedures e Triggers implementadas para estas tarefas.
- Após execução dessas etapas, os dados tratados serão armazenados nas tabelas
  
### 4. Análise Exploratória de Dados (EDA)
- As análises serão realizadas na ferramenta Jupyter Notebook usando linguagem Python.
- **Análise Inicial:**
	- Tipo de cada atributo (numérico, categórico, data, etc.).
	- Distribuição da Variável Alvo (quantidade diária de cadastros):
		- Identificar se há valores discrepantes (outliers).
		- Escolher a transformação adequada se a distribuição não for normal.
 - **Estatísticas Descritivas:**
	- Calcular estatísticas descritivas para variáveis numéricas (média, mediana, desvio padrão, mínimo, máximo) para obter uma compreensão básica da
distribuição dos dados.
- **Análise Temporal:**
	- Analisar a tendência temporal dos cadastros ao longo do tempo.
	- Criar gráficos de séries temporais para identificar sazonalidades, tendências e padrões cíclicos.
- **Análise de Categorias:**
	- Analise a distribuição dos cadastros por categoria de produto. Pode ser útil entender quais categorias têm maior ou menor participação na promoção.
- **Correlações:**
	- Calcule as correlações entre a variável alvo e as demais variáveis. Isso ajuda a identificar quais atributos têm maior impacto na quantidade decadastros.
- **Visualização de Dados:**
	- Utilize gráficos como histogramas, boxplots e scatter plots para visualizar a distribuição das variáveis e identificar possíveis relações entre elas.
- **Tratamento de Outliers:**
	- Caso haja outliers, avalie se eles devem ser removidos, transformados ou tratados de alguma forma.
- **Análise de Relações Multivariadas:**
	- Caso tenha várias variáveis, análise relações multivariadas para identificar interações complexas entre os atributos.

### 5. Engenharia de Features
- Identificar features que capturem informações relevantes para o comportamento da variável alvo (quantidade diária de cadastros) com base nos atributos
fornecidos no dataset de cadastro de cupom do produto (data do cadastro, categoria do produto, nome do produto).
- **Possíveis features:**
	- **Data do Cadastro:**
		- Pode ser útil extrair informações temporais, como dia da semana, mês e ano, para capturar padrões sazonais.
	- **Categoria do Produto:**
		- Converta a categoria do produto em variáveis dummy (one-hot encoding) para que o modelo possa interpretar a informação categórica.
	- **Nome do Produto:**
		- Dependendo da quantidade de produtos, pode ser útil converter o nome do produto em um identificador único ou extrair características
relevantes.
	- **Características Temporais Adicionais:**
		- Pode-se incluir características como feriados, eventos especiais ou promoções sazonais que possam influenciar o comportamento dos
cadastros.
	- **Variáveis de Tendência Temporal:**
		- Criar variáveis que representem tendências temporais, como a contagem cumulativa de cadastros até o momento.
	- **Lags Temporais:**
		- Incluir lags da variável alvo (quantidade diária de cadastros) para capturar padrões temporais e possíveis efeitos de defasagem.
	- **Características Estatísticas:**
		- Estatísticas descritivas, como média, mediana, desvio padrão, podem ser calculadas para períodos específicos.
	- **Interações entre Atributos:**
		- Considere criar features que representem interações entre a categoria do produto e a data do cadastro, por exemplo.
    
### 6. Modelagem, Avaliação e Validação de Modelo
- **Regressão Linear:**
  - **Descrição:** Modelo simples que assume uma relação linear entre features e a variável alvo. Adequado para relações lineares aproximadas.
  - **Métodos de Avaliação:**
    - MAE (Erro Médio Absoluto)
    - MSE (Erro Quadrático Médio)
    - R² (Coeficiente de Determinação)
  - **Métodos de Validação:**
    - Validação Cruzada (K-Fold)
    - Leave-One-Out Cross-Validation (LOOCV)
- **Regressão Bayesiana:**
  - **Descrição:** Modelos que incorporam incerteza nas previsões, úteis quando a incerteza é uma consideração importante.
  - **Método de Avaliação:**
    - Intervalo de Confiança Bayesiano
      - Em modelos bayesianos, o intervalo de confiança é frequentemente obtido a partir da distribuição posterior da estimativa.
  - **Métodos de Validação:**
    - Validação Cruzada (K-Fold)
    - Leave-One-Out Cross-Validation (LOOCV)        
   
### 7. Implementação e Integração
- Desenvolvimento do script de implementação algoritmo, na linguagem Python, usando biblioteca Pandas para manipulação de dados, biblioteca Scikit-learn
para modelagem, Matplotlib para visualização e OpenPyXL para escrever no Excel.
- Adicionar o script em diretório pré-determinado e referênciar path do script na lista de comando de execução em arquivo, já existente, de comandos .BAT.
- Execução da previsão dia a dia e integração do modelo escolhido em uma série temporal com a adição da previsão para o próximo dia, executado um loop
que iterará sobre cada dia, realizando a previsão e adicionando os resultados à série temporal.

### 8. Iteração e Ajuste
- No contexto da previsão diária, a iteração e ajuste do modelo são partes cruciais do ciclo de vida de um projeto de modelagem preditiva.
- **Acompanhamento do Desempenho:**
  - Monitorar regularmente o desempenho do modelo em dados de teste ou validação.
- **Análise de Resíduos:**
  - Analisar os resíduos do modelo para identificar padrões ou estruturas que podem indicar áreas de melhoria.
- **Atualização de Dados de Treinamento:**
  - Atualize o conjunto de treinamento para incorporar informações mais recentes.
- **Ajuste de Hiperparâmetros:**
  - Caso o modelo implementado envolver hiperparâmetros, ajustá-los para otimizar o desempenho.
- **Validação Cruzada:**
  - Realizar a validação cruzada para verificar a robustez do modelo.
- **Interpretação dos Resultados:**
  - Compreender a interpretação dos resultados do modelo, pois no nosso contexto as decisões de negócios dependem das previsões.
- **Comunicação com Stakeholders:**
  - Comunicar regularmente os resultados, ajustes e descobertas aos stakeholders relevantes através de apresentações de status de projeto e relatório
diário.
