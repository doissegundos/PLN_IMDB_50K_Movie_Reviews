# PLN IMDB_50K_Movie_Reviews
Este projeto visa utilizar conhecimentos de Linguagem de Processamento Natural para realizar predições de sentimentos utilizando o dataset IMDB_50K_Movie_Reviews. Este dataset contém duas colunas onde uma é referente a um texto com uma critica de um filme e a outra coluna possui dados que dizem se a critica é positiva ou negativa. O objetivo deste trabalho é utilizar conceitos de limpeza de dados, visualização de dados, PLN e aprendizado de maquina para classificação dos dados.

### Processamento de Linguagem Natural - PLN
Os conceitos de PLN utilizados foram:

- **Normalização**: O processo de normalização no Processamento de Linguagem Natural trata de colocar todas as palavras em caixa baixa, retirando os acentos ou cedilha. Isto faz com que os algoritmos de análise não tratem palavras iguais como sendo diferentes apenas por apresentarem a letra inicial como maiúscula, ou um erro de acentuação, por exemplo.
- **Tokenização**: A tokenização quebra a estrutura de um texto em palavras.
- **Stop words**: As stop words são palavras que não adicionam sentido ao texto, pois são usadas para coesão e dar contexto, mas não fazem sentido específico quando olhadas individualmente. Portanto, o processo necessário em análises que usam Processamento de Linguagem Natural é eliminar as palavras vazias (stop words).
- **Lematização**: Tem como objetivo reduzir uma palavra à sua forma base e agrupar diferentes formas da mesma palavra. 
    > Exemplo: As palavras durmo, dormiu, dormirá... seria lematizada para apenas dormir
    
- **Stemização**: O termo stemização vem do inglês stemming, e representa o processo de reduzir palavras flexionadas ou derivadas a sua base. Neste processo a tarefa é transformar palavras próximas em uma só, como ficar apenas com o radical dos verbos ou transformar todos os substantivos para o singular.
 > Por exemplo: As palavras dormir, dormiu, dormirá... seria stematizada para apenas dorm
 
- **Vetorização - Bag of words**:O modelo bag-of-words é uma representação simplificadora usada no processamento de linguagem natural. Nesse modelo, um texto é representado como a bolsa  de suas palavras, desconsiderando a gramática e até mesmo a ordem das palavras.
 
#### Bibliotecas de PLN utilizadas:
- **NLTK**: Permite realização das etapas de tokenização, remoção de stop words, lematização e stemização.
- **SPACY**:  Permite realização das etapas de tokenização, remoção de stop words, lematização.

### Modelos de classificação

A classificação é responsável por atribuir uma classe a um objeto de acordo com suas caracteristicas.Essa classificação pode ser binária (duas classes, 1 ou 0) ou multiclasse (três ou mais classes). Os modelos de classificação utilizado para classificar os sentimentos em negativo e positivo foram:

- **Regressão Logistica**: A Regressão Logística  é comumente utilizada para estimar a probabilidade de uma instância pertencer a uma determinada classe. Aplica a função sigmoid. 
- **KNN**: O KNN realiza a classificação avaliando as caracteristicas dos K vizinhos mais próximos. 
- **Naive Bayes**: O Naive Bayes é baseado na aplicação do teorema de Bayes com suposições de independência fortes entre as características.
- **Arvores de decisão**: A árvore de decisões é uma técnica utilizada para Classificação e consiste em um mapa dos possíveis resultados de uma série de escolhas. Essas escolhas estão relacionadas a diversas decisões tomadas com base nas variáveis do banco de dados utilizado.
- **Perceptron**: É uma rede neural de camada única e um Perceptron de várias camadas é chamado de Rede Neural Artificial. O Perceptron é um classificador linear (binário). Além disso, é usado na aprendizagem supervisionada e pode ser usado para classificar os dados de entrada fornecidos.
- **Ensemble**: Tembém pode ser chamado de comite de classificação, uma vez que atribui uma classe a uma instancia de acordo com a votação de vários modelos de classificação.
- **Bagging**: Realiza a votação de um conjunto de previsores mas cada previsor é composto do mesmo modelo de classificação. Os dados de treinamento são divididos em conjuntos aleatorios para cada previsor.

### Métricas de avaliação

As métricas de avaliação utilizadas são disponibilizadas por meio da biblioteca Sklearn do Python. As métricas utilizadas foram: Acurácia, recall, precisão, f1 score, kappa e matriz de confusão. Os resultados deste projeto podem ser analisados utilizando o notebook PLN.ipynb ou resultados.ipynb.

### Visualização dos dados

As bibliotecas Seaborn e Matplotlib do Python foi utilizada para visualização dos dados. Muitas análises dos dados foram realizadas, as que se destacaram mais foram:

- Palavras que mais se repetem
- Tamanho das sentenças de acordo com o sentimento
- Nuvem de palavras
