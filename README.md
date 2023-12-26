# Análise de Redações do ENEM com PLN: Identificação de Textos por IA ou Humanos

Este repositório contém um projeto de Processamento de Linguagem Natural (PLN) aplicado a redações do Exame Nacional do Ensino Médio (ENEM) do Brasil. O objetivo é classificar os textos em duas categorias: escritos por Inteligência Artificial (IA) e escritos por humanos. O projeto é implementado em Python e utiliza várias bibliotecas de PLN.

## Acesso ao Notebook

O projeto está disponível em um Jupyter Notebook hospedado no Google Colab. Para acessar e executar o código, clique no link abaixo:

- [Notebook PLN_ENEM_ANALYSIS no Google Colab](https://colab.research.google.com/drive/1W_8MZTPCfqG5cDI24fdqmFjPdEqhKYT2?usp=sharing)

## Configuração Inicial

### Bibliotecas Necessárias
- **Pandas**: Para manipulação de dados.
- **spaCy**: Biblioteca avançada de PLN.
- **Numpy** e outras bibliotecas auxiliares.

### Configurações Adicionais
- Montagem do Google Drive para acessar arquivos de dados.
- Download do modelo de linguagem em português para spaCy.

### Sobre o spaCy
- [Documentação do spaCy](https://spacy.io/usage): Utilizado para criação de pipelines de processamento em português.

## Processamento dos Dados

### Carregamento dos Dados
- Leitura dos dados de treino e teste (arquivos `TrainENEM.csv` e `TestENEM.csv`) utilizando Pandas.

### Pré-processamento
- Definição de pontuações e stop words em português.
- Carregamento do modelo de linguagem spaCy em português.
- Função de pré-processamento: conversão para minúsculas, lematização, remoção de stop words e pontuações.
- Aplicação do pré-processamento nos conjuntos de treino e teste.

### Preparação para o Treinamento
- Transformação da classe `is_IA` em formato adequado usando um dicionário para as categorias "IA" e "HUMANO".

## Criação e Treinamento do Classificador

- Criação de um modelo spaCy em branco.
- Adição da camada de classificação de texto (textcat) com categorias "IA" e "HUMANO".
- Treinamento com os dados, incluindo embaralhamento e atualização do modelo.

## Avaliação do Modelo

- Realização de previsões nos dados de teste.
- Cálculo da precisão (accuracy) e geração da matriz de confusão para avaliar o desempenho.

## Análise Adicional: Bag of Words

- Análise de dependência e visualização gráfica das relações entre palavras.
- Criação e exibição de uma nuvem de palavras a partir dos textos analisados.
