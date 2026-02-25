# Aula 02

## Objetivos

- Compreender o que é a tarefa de classificação e as diferentes formas de avaliar o desempenho de um classificador;
- Preparar um experimento computacional para treinamento e avaliação de desempenho de um classificador;
- Trabalhar com um modelo simples (linear) de classificação $\rightarrow$ regressão logística.

## Materiais

- [Classificação](https://github.com/EA991-Lab/utils/blob/main/materiais/topico_02_intro_classificacao.pdf?raw=True)
- [Modelos tradicionais de classificação](https://github.com/EA991-Lab/utils/blob/main/materiais/topico_03_modelos_classificacao.pdf?raw=True)

## Scikit-learn

A API do Scikit-learn foi desenvolvida seguindo alguns princípios, como:
- consistência: todos os objetos compartilham uma interface relativamente simples e padronizada;
- inspeção: todos os hiperparâmetros de um estimador podem ser acessados diretamente via variáveis públicas instanciáveis, e todos os parâmetros aprendidos (ajustados) podem ser acessados por variáveis com um sufixo tipo underscore (_). 
- não-proliferação de classes: adotar formatos (classes) usuais para representar *datasets* e variáveis;
- composição: os blocos construtores podem ser reutilizados tanto quanto possível. Por exemplo, é fácil criar uma *pipeline* (ou, mais formalmente, um estimador do tipo `Pipeline`) a partir de uma sequência arbitrária de *transformers* seguido de um estimador final.
- valores razoáveis são pré-definidos como o padrão para os parâmetros.

**Padrão adotado:**

Estimators
: qualquer objeto que pode estimar alguns parâmetros com base em um conjunto de dados é chamado de estimador (por exemplo, um `SimpleImputer` é um estimador). A estimação em si é realizada pelo método `fit()`, que recebe um conjunto de dados como parâmetro, ou dois no caso de algoritmos de aprendizado supervisionado — o segundo conjunto de dados contém os rótulos. Qualquer outro parâmetro necessário para guiar o processo de estimação é considerado um hiperparâmetro (como a opção `strategy`de um `SimpleImputer`).

* Transformers: alguns estimadores (como um `SimpleImputer`) também podem transformar um conjunto de dados (daí o nome transformadores). Mais uma vez, a API é simples: a transformação é realizada pelo método `transform()`, que recebe um conjunto de dados e retorna sua versão transformada. Essa transformação geralmente depende dos parâmetros aprendidos, como é o caso de um `SimpleImputer`. Todos os transformadores também possuem um método conveniente chamado `fit_transform()`.

* Predictors: por fim, alguns estimadores são capazes de fazer previsões para um conjunto de amostras (daí o nome preditores). Dois exemplos simples são os modelo `LinearRegression` e `LogisticRegression`. Um preditor possui um método `predict()` que recebe um conjunto de dados com novas instâncias e retorna as previsões correspondentes. Ele também possui um método `score()`, que mede a qualidade das previsões para um conjunto de teste. 

Referências:
https://arxiv.org/abs/1309.0238 - API scikit-learn

