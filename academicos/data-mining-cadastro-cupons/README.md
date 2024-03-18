# Algoritmos para Ciência de Dados

Atividade Prática - 4º Período - 1º Semestre 2024 

## 1. **Análise de Clusters e Regras do Apriori**: 

- Para realizar essa tarefa, você deve primeiro executar o algoritmo de agrupamento no conjunto de dados escolhido usando o Weka. 
- Após a geração dos clusters, você deve analisar as características de cada cluster, como a média, mediana, moda e outras estatísticas descritivas dos atributos dentro de cada cluster. 
- Em seguida, execute o algoritmo Apriori para gerar regras de associação. 
- Compare as regras geradas com os clusters, procurando por padrões ou características que possam ser explicados pelas regras. 
- Por exemplo, se uma regra indica que a compra de um item A leva frequentemente à compra de um item B, e você observa que os clientes no cluster 1 compram frequentemente os itens A e B juntos, isso pode indicar uma relação entre a regra e o cluster.

### **Explicação**

- A análise de clusters é uma técnica de aprendizado não supervisionado que agrupa instâncias semelhantes em clusters. 
- Cada cluster contém instâncias que são semelhantes entre si e diferentes das instâncias em outros clusters. 
- As regras do Apriori, por outro lado, são uma forma de aprendizado supervisionado que busca encontrar relações ou associações entre atributos. 
- Ao comparar os clusters e as regras, você pode obter insights sobre os padrões subjacentes nos dados.

## 2. **Experimento com o Conjunto de Dados Iris**: 

- Para realizar essa tarefa, você deve primeiro carregar o conjunto de dados "iris.csv" no Weka. 
- Em seguida, execute o algoritmo KMeans, variando o número de clusters (k) de 2 a, digamos, 10. 
- Para cada valor de k, observe o erro RMS (Root Mean Square). 
- Plote um gráfico do erro RMS em função do número de clusters. 
- O melhor número de clusters é geralmente aquele que resulta no menor erro RMS, embora outros fatores possam entrar em consideração, como a interpretabilidade dos clusters.

### **Explicação**

- O conjunto de dados Iris é um conjunto de dados clássico na aprendizagem de máquina, contendo medidas de comprimento e largura da sépala e da pétala para três espécies de íris.
- O algoritmo KMeans é um algoritmo de agrupamento que tenta dividir o conjunto de dados em k clusters, minimizando a soma das distâncias quadradas entre cada instância e o centroide de seu cluster. 
- O erro RMS é uma medida de quão bem o modelo se ajusta aos dados; um menor erro RMS indica um melhor ajuste. 
- Ao plotar o erro RMS em função do número de clusters, você pode determinar o número ótimo de clusters para o conjunto de dados.
