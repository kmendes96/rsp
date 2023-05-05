# Descritivo criado com intuito de gerar um algoritmo de Machine Learning para predição do número de operadores a cada 15 minutos nas planilhas Horario RSP
Projeto Github RSP: https://github.com/cvs2010/rsp

# Descrição do Modelo de Machine Learning
Já com os dados tabulados em DataFrames, iremos dividir os dados em 70% para treinamento e 30% para teste (validação)

## Primeiro Passo: Escolha do algoritmo de ML
- Qual algoritmo utilizaremos?

- Existem muitos tipos de algoritmos de machine learning, cada um com sua própria finalidade e propósito.

    - Os principais tipos de algoritmos de machine learning são:
      - Aprendizado supervisionado: nesse tipo de algoritmo, o modelo é treinado com dados rotulados para fazer previsões precisas em novos dados rotulados. Isso pode incluir tarefas como classificação (prever a classe de um objeto) ou regressão (prever um valor numérico).
      - Aprendizado não supervisionado: esse tipo de algoritmo é usado quando não há rótulos nos dados. Em vez disso, o modelo tenta encontrar padrões ou agrupamentos nos dados. Isso pode incluir tarefas como clustering (agrupar objetos semelhantes) ou redução de dimensionalidade (reduzir o número de recursos).
      - Aprendizado por transferência: esse tipo de algoritmo usa conhecimento prévio aprendido em uma tarefa para ajudar em outra tarefa relacionada. Por exemplo, um modelo treinado para reconhecer rostos humanos pode ser transferido para reconhecer expressões faciais.

- Os principais algoritmos de aprendizado supervisionado são:
      - Regressão Linear: um algoritmo de regressão que tenta encontrar uma relação linear entre os recursos e o valor alvo, geralmente usado para tarefas de previsão numérica.
      - Árvores de Decisão: um algoritmo que divide o espaço de recurso em regiões menores e mais específicas, criando uma árvore de decisão que pode ser usada para prever a classe de um objeto ou valor numérico.
      - K-Nearest Neighbors (K-NN): um algoritmo que encontra os k objetos mais próximos de um novo objeto e usa a classe desses objetos para prever a classe do novo objeto.
      - Support Vector Machines (SVM): um algoritmo que tenta encontrar o hiperplano que separa as classes com a maior margem possível, usado para problemas de classificação binária e multiclasse.
      - Redes Neurais Artificiais: um algoritmo inspirado no funcionamento do cérebro humano, que usa várias camadas de neurônios para aprender uma representação hierárquica dos recursos e prever a classe ou valor alvo.

- Pelo tema do nosso projeto, acredito que o aprendizado supervisionado com algoritmo de regressão linear seria uma opção mais adequada para o problema.

## Segundo Passo: Treinamento do modelo
- O objetivo aqui é ajustar os parâmetros do modelo de modo que ele possa fazer previsões precisas sobre novos dados.

## Terceiro Passo: Avaliar o desempenho do modelo
- Depois que o modelo é treinado, é importante avaliar o quão bem ele se comporta usando o conjunto de teste. Isso ajudará a determinar se o modelo está super ou subajustado e se há espaço para melhorias adicionais. Utilizando métricas como o erro médio quadrático (Mean Squared Error - MSE) e o coeficiente de determinação (R²), pode-se testar a acurácia do modelo.

## Quarto Passo: Ajustar o modelo
- Se o desempenho do modelo não for satisfatório, é possível ajustá-lo modificando seus parâmetros ou experimentando um algoritmo de aprendizado de máquina diferente. Isso pode envolver a realização de mais experimentos e avaliações para encontrar a configuração ideal do modelo.

## Quinto Passo: Testar o modelo com previsões
- Uma vez que o modelo é treinado e ajustado, ele pode ser usado para fazer previsões em novos dados. Isso pode envolver a implementação do modelo em um aplicativo ou pipeline de produção para uso em um cenário do mundo real.

