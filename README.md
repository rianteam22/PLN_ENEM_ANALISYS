# PLN_ENEM_ANALISYS

Este código é uma implementação de um classificador de texto que visa identificar se um texto pertence à categoria "IA" (Inteligência Artificial) ou à categoria "HUMANO".

### Importação e instalação de bibliotecas:

Importa as bibliotecas necessárias, como pandas, spacy, random, numpy, e outras.

Monta o Google Drive para acessar os arquivos de dados.

Faz o download do modelo de linguagem em português para o spaCy.

### Carregamento da base de dados de treino e teste:
Lê os conjuntos de dados de treino (TrainENEM.csv) e teste (TestENEM.csv) usando o Pandas.

### Pré-processamento das redações:
Define uma lista de pontuações e palavras de parada (stop words) em português.

Carrega o modelo de linguagem em português do spaCy.

Define uma função preprocessamento para realizar o pré-processamento dos textos, que inclui: 
tornar o texto em letras minúsculas, 
lematização das palavras, 
remoção de stop words e pontuações.

Aplica a função preprocessamento aos textos de treino e teste para prepará-los para a classificação.

### Tratamento da classe:
Cria uma nova lista base_treino_final que transforma a classe original "is_IA" em um formato adequado para treinamento, usando um dicionário que indica se o texto pertence à classe "IA" ou "HUMANO".

### Criação do Classificador:
Cria um modelo spaCy em branco para treinamento.
Adiciona uma camada de classificação de texto (textcat) com duas categorias: "IA" e "HUMANO".
Inicia o treinamento do modelo com os dados de treino, onde os textos são embaralhados em lotes e atualiza o modelo com exemplos.

### Avaliação na base de teste:
Realiza previsões nos textos de teste e armazena as previsões em previsoes_final.

Calcula a precisão (accuracy) do modelo comparando as previsões com as respostas reais.

Calcula a matriz de confusão para avaliar o desempenho do modelo.

### BAG OF WORDS:
Realiza uma análise de dependência (dependency parsing) no texto de exemplo usando spaCy e exibe uma visualização gráfica das relações entre as palavras.
Cria uma nuvem de palavras (word cloud) com base nas palavras do texto e a exibe em um gráfico.
