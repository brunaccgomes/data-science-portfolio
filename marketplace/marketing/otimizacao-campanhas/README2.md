# Projeto de Data Science e Analytics - Monitoramento da Efetividade de Campanha de Marketing

### 0. Contexto
Um campanha de marketing foi criada para atrair usuários para plataforma de e-commerce através de anúncios patrocinados em diversos sites. 

**Fluxo:**   
    **1.** O usuário clica no anúncio e é direcionado para plataforma de cadastro.  
    **2.** O usuário preenche todos os campos e submete o cadastro.   
    **3.** O usuário vai até sua caixa de e-mail e confirma sua conta através do link no e-mail enviada pela plataforma para ativar sua conta.   
    **4.** O usuário enfim é redirecionado para página inicial do e-commerce.
   
A equipe de data science foi acionada para monitorar o volume no número de acesso a plataforma de e-commerce e orientar nas tomadas de decisão.
Para isso foram elaborados 2 projetos 
Inicialmente a equipe mas acredita que o fluxo da campanha não é o ideal, pois o passo 2 (cadastro do usuário) é muito longo e provavelmente os usuário estão desistindo de continuar o fluxo.

## Projeto 1
### 1. Objetivo do Projeto
Realizar uma análise descritiva da efetividade da campanha de marketing, identificando padrões e pontos de desistência no fluxo do usuário, 
utilizando visualizações e métricas descritivas para entender o comportamento dos usuários ao longo da campanha

### 2. Coleta de Dados
- Fonte de Dados: Logs de eventos da plataforma, incluindo informações sobre cliques nos anúncios, registros de cadastro, 
confirmações de e-mail e redirecionamentos para a página inicial.
- Formato: Registros de eventos estruturados/**CSV?**. **(ENCONTRAR O DATASET) E (CRIAR PASTA DATASET)**

### 3. Pré-processamento de Dados
- Limpeza e Transformação: 
  - Tratar valores ausentes, se houver.
  - Normalizar os dados, se necessário.

### 4. Análise Exploratória de Dados (EDA)
- Visualização de Padrões:
  - Criar gráficos de funil para representar a jornada do usuário.
  - Identificar taxas de conversão em cada etapa do processo.

### 5. Engenharia de Features
- Feature:
  - Tempo decorrido entre o clique no anúncio e a conclusão do cadastro.

### 6. Modelagem ML (Opcional)
- Tarefa: Identificar padrões não óbvios ou insights mais complexos. **(PRA QUÊ)**
- Algoritmo Escolhido: Técnicas de clustering (por exemplo, K-Means) para segmentar usuários com comportamentos similares.

### 7. Avaliação e Validação do Modelo (Opcional)
- Método de Avaliação: Métricas descritivas como médias, medianas, percentis. **(JUSTIFICAR)**
- Validação: Análise temporal para identificar mudanças ao longo do tempo.

## Projeto 2
### 1. Objetivo do Projeto
Realizar uma análise descritiva da efetividade da campanha de marketing, identificando padrões e pontos de desistência no fluxo do usuário. 

### 2. Coleta de Dados
- Fonte de Dados: Logs de eventos da plataforma, incluindo informações sobre cliques nos anúncios, registros de cadastro,
- confirmações de e-mail e redirecionamentos para a página inicial.
- Formato: Registros de eventos estruturados/**CSV?**. **(ENCONTRAR O DATASET) E (CRIAR PASTA DATASET)**

### 3. Pré-processamento de Dados
- Limpeza e Transformação: 
  - Tratar valores ausentes, se houver.
  - Normalizar os dados, se necessário.

### 4. Análise Exploratória de Dados (EDA)
- Visualização de Padrões:
  - Criar gráficos de funil para representar a jornada do usuário.
  - Identificar taxas de conversão em cada etapa do processo.

### 5. Engenharia de Features
- Exemplo de Feature:
  - Tempo decorrido entre o clique no anúncio e a conclusão do cadastro.

### 6. Modelagem ML (Opcional)
- Tarefa: Identificar padrões não óbvios ou insights mais complexos. **(PRA QUÊ)**
- Algoritmo Escolhido: Técnicas de clustering (por exemplo, K-Means) para segmentar usuários com comportamentos similares.

### 7. Avaliação e Validação do Modelo (Opcional)
- Método de Avaliação:Métricas descritivas como médias, medianas, percentis. **(JUSTIFICAR)**
- Validação: Análise temporal para identificar mudanças ao longo do tempo.
