# Como foi implementado:
Importamos a biblioteca NumPy, que fornece suporte para trabalhar com matrizes e funções matemáticas eficientes.

- Definimos a função de ativação sigmoidal sigmoid(x), que retorna o valor da função sigmoid para um dado valor x. A função sigmoid é usada para introduzir não linearidade na saída da rede neural.

- Definimos os dados de treinamento treinamento_entrada e treinamento_resultado. treinamento_entrada é uma matriz 2D que contém os valores de entrada para os exemplos de treinamento. treinamento_resultado é uma matriz 2D que contém os valores de saída correspondentes para os exemplos de treinamento.

- Definimos uma semente aleatória para garantir a reprodutibilidade dos resultados gerados aleatoriamente pela rede neural.

- Inicializamos os pesos sinápticos pesos_sinapticos aleatoriamente com valores entre -1 e 1. Os pesos sinápticos são os parâmetros ajustáveis da rede neural que determinam a força das conexões entre os neurônios.

- Iniciamos o treinamento da rede neural usando um loop for que executa 10.000 iterações (você pode ajustar esse número de acordo com suas necessidades).

- Dentro do loop de treinamento, a matriz input_layer é atribuída aos dados de treinamento treinamento_entrada.

- Calculamos a saída da rede neural através da multiplicação da matriz de entrada pelo vetor de pesos sinápticos e aplicando a função de ativação sigmoidal. Isso é feito usando a função np.dot(input_layer, pesos_sinapticos).

- Calculamos o erro entre a saída real e a saída esperada usando a diferença entre treinamento_resultado e output.

- Calculamos o ajuste necessário para atualizar os pesos sinápticos usando o erro e a derivada da função sigmoidal aplicada à saída. Isso é feito através da fórmula ajuste = erro * output * (1 - output).

- Atualizamos os pesos sinápticos somando o produto da transposição da matriz de entrada (input_layer.T) pelo ajuste.

- Após o término do treinamento, definimos a nova situação que queremos prever e a transformamos em uma matriz 2D usando np.reshape(nova_situacao, (1, 3)).

- Fazemos a predição da saída para a nova situação, multiplicando a matriz da nova situação pelos pesos sinápticos atualizados e aplicando a função sigmoidal. Isso é feito usando np.dot(nova_situacao, pesos_sinapticos).

- Imprimimos a predição da saída para a nova situação.

