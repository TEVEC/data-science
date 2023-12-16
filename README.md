# Teste Prático de Detecção de Fraudes em Pagamentos

## Introdução
Neste teste prático, você será desafiado a criar um modelo de detecção de fraudes em transações de pagamento. Utilizaremos um conjunto de dados público para simular um cenário de detecção de fraudes.

## Passo 1: Conjunto de Dados
- Escolha um conjunto de dados público de transações de pagamento. Você pode selecionar um dos seguintes conjuntos de dados ou optar por um de sua preferência:
    - [Credit Card Fraud Detection (Kaggle)](https://www.kaggle.com/mlg-ulb/creditcardfraud)
    - [Synthetic Financial Datasets For Fraud Detection (Kaggle)](https://www.kaggle.com/ntnu-testimon/paysim1)
    - [Credit Card Transactions (UCI Machine Learning Repository)](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)
- Documente a fonte do conjunto de dados e verifique se ele está disponível publicamente.

## Passo 2: Organização do Conjunto de Dados
- Organize os dados de pagamento de maneira adequada, incluindo limpeza, tratamento de valores ausentes e formatação dos tipos de dados.

## Passo 3: Criação do Modelo
- Crie um modelo de detecção de fraudes utilizando uma árvore de decisão ou algum modelo a sua escolha.
- Divida o conjunto de dados em conjuntos de treinamento e teste.
- Treine o modelo no conjunto de treinamento e avalie seu desempenho no conjunto de teste, utilizando métricas como precisão, recall, F1-score e matriz de confusão.

## Passo 4: Conclusão de Insights
- Em um Jupyter Notebook ou script Python, concentre-se na análise e interpretação dos resultados obtidos com o modelo.
- Resuma as principais descobertas e insights obtidos a partir do modelo de detecção de fraudes.
- Destaque as características mais importantes identificadas pelo modelo e explique como esses insights podem ser usados para melhorar a segurança de pagamentos ou tomar decisões de negócios.
- Crie visualizações, gráficos ou tabelas que ajudem a comunicar os insights de maneira eficaz.
- Forneça um resumo narrativo que conte uma história com base nos resultados e insights.

## Passo 5: Faça seu pull request
- Crie um pull request neste repositório
- Adicione o Jupyter Notebook ou script Python ao repositório.
- Inclua um README.md caso aplicável para algum intrução específica na hora de avaliar o teste.


## Observações
- Respeite os termos de uso e as licenças do conjunto de dados escolhido, atribuindo crédito adequado, se necessário.

Boa sorte e divirta-se criando seu teste prático de detecção de fraudes em pagamentos!


# infracommerce

## Solução Proposta

Os notebooks deste projeto visam a construção de um modelo para Inadimpência.
Para isto foram utilizados algoritmos de Árvore de Decisão, Florestas aleatórias e Redes Neurais afim de identificar qual teria a melhor resposta para este problema. 

Inclusive, há recomendação no site onde foi baixado o dataset para utilização de redes neurais para fazer o modelo.
Foi escolhido para esta análise o arquivo do site https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients, o terceiro da lista do repositório encaminhado. O mesmo não continha dados faltantes.
No arquivo requirements.txt tem as instalações que foram feitas no prompt para que o modelo pudesse ser construído e o dataset é o de no nome "defaultCreditcardClients.xls".
Para este processo seletivo, os arquivos que devem ser abertos são os notebooks infracommerce.ipynb e infracommerce_RedeNeural.ipynb. O primeiro notebook tem as predições feitas com Arvore de Decisão e Florestas Aleatórias e o segundo notebook o modelo foi gerado usando Rede Neural.

Para identificação dos melhores hiperparâmetros foi utilizada as bilbioteca GridSearchCV, RandomizedSearchCV que ajuda a identificar os hiperparêmetros que dão melhor resposta nos modelos tanto na Árvore de Decisão e Floresta Aleatória quanto no modelo com redes neurais artificiais.

## Conclusão: 

Era esperado que o modelo usando redes neurais apresentasse uma melhor performance nas métricas em geral, pois no site fonte do dataset também sugeria a utilização de redes neurais. E de fato foi o que ocorreu. Apesar de as métricas terem resultados muito próximos do modelo Random Forest
Foi o que melhor respondeu na precisão pra Inadimplência 71%, Recall 100% superior aos dos outros dois e com o mesmo F1-Score 88%.

Sobre a matriz de confusão: O algoritmo utilizando as redes neurais foi o que melhor trouxe também respostas para verdadeiros negativos e falsos negativos, o que traz melhor retorno financeiro e menos problemas de relacionamento com o cliente.
Porém, embora os modelos tenham apresentado desempenhos muito próximos, para predição de fraude o modelo de floresta aleatória, neste estudo, se apresentou melhor nas métricas em relação aos demais modelos. Foi o que melhor respondeu na precisão pra fraude 73%, Recall 98% superior aos dos outros dois e com o mesmo F1-Score 89%.

Sobre a matriz de confusão: O algoritmo de redes neurais foi o que melhor trouxe também respostas para verdadeiros negativos e falsos negativos, o que traz melhor retorno financeiro e menos problemas de relacionamento com o cliente.

