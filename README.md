# Projeto-Titanic
Esse repositório foi criado para **[competição no Kaggle sobre o desastre do Titanic](https://www.kaggle.com/competitions/titanic/overview)**

<img src="https://github.com/mike-antunes/Projeto-Titanic/blob/main/img/ACCURACY.png" />

## [Etapa 1: Primeiro modelo](https://github.com/mike-antunes/Projeto-Titanic/blob/main/An%C3%A1lise_do_Titanic_-_Parte_1.ipynb)
- Foi feito nessa etapa o processo básico de Data Wrangling e Data Cleaning sobre os dados. Depois foi utilizado 3 modelos algoritmos: Árvore de Classificação, KNN e Regressão Logística. Foi avaliado esses modelos utilizando a acurácia e a matriz de confusão. **O score retornado pelo Kaggle foi de 0,66746.**

## [Etapa 2: Tratamento das Variáveis](https://github.com/mike-antunes/Projeto-Titanic/blob/main/An%C3%A1lise_do_Titanic_-_Parte_2.ipynb)
- Foi feito o mesmo processo basico da etapa 1 para organização basica e limpeza dos dados . Foi utilizado lambda function e OneHotEncoder para fazer o tratamento das variáveis. Foi utilizado os mesmos modelos vistos na Etapa 1 **O score retornado pelo Kaggle foi de 0,76555.**

## [Etapa 3: Se aprofundando ainda mais para os tratamentos dos dados](https://github.com/mike-antunes/Projeto-Titanic/blob/main/An%C3%A1lise_do_Titanic_-_Parte_3.ipynb)
- Ajuste nas escalas dos dados para as coluna "Age" e "Fare". Entendendo melhor as colunas "SibSp(n° de irmão/cônjuges a bordo do Titanic)" e "Parch(n° de pais/filhos a bordo do Titanic)". Após isso, foi criado duas colunas para separar quem estava com familiares e quem estava sozinho para ter uma estimativa sobre a taxa de sobreviventes de ambos. Depois surgiu a análise de correlação entre todas as variáveis para selecionar quais se relacionam melhor para a utilização em modelos.     **O score retornado pelo Kaggle foi de 0,77033.**

## [Etapa 4: Selecionando outros algoritmos para fazer a previsão](https://github.com/mike-antunes/Projeto-Titanic/blob/main/An%C3%A1lise_do_Titanic_-_Parte_4.ipynb)
- Os algoritmos que foram usados nessa etapa froam a Regressão Logística (vamos nos manter pois foi o com os melhores resultados nas etapas anteriores), RandomForest e MLPCLASsifier (Redes Neurais).
O MLPClassifier (um algoritmo de Redes Neurais) obteve maior acurácia nos dados de validação entre todos os modelos vistos até agora, porém ao usar esse modelo nos dados de teste (que faremos a submissão) o resultado foi pior que na etapa 3, mostrando que provavelmente tivemos um overfitting do nosso modelo.
**O score retornado pelo Kaggle foi de 0,69856.**

## [Etapa 5: Selecionando outros algoritmos para fazer a previsão](https://github.com/mike-antunes/Projeto-Titanic/blob/main/An%C3%A1lise_do_Titanic_-_Parte_5.ipynb)
- Agora foi utilizado o GridSearchCV para determinar as melhores configurações para os 3 modelos que utilizamos na etapa anterior.
Nesse caso, o modelo escolhido foi aquele que utilizou o RandomForest melhorando consideravelmente em relação à etapa 4 e foi melhor que na etapa 3.
**O score retornado pelo Kaggle foi de 0,78229.**
