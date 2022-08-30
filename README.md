> Autor: Vinícius Luiz
> Email: vlsf2@cin.ufpe.br
> Data: 2022-08-29

# Adult Data Set - Census

## Introdução

**Preveja se a renda excede US$ 50 mil/ano com base nos dados do censo. Também conhecido como conjunto de dados "Renda do Censo".**  
A extração foi feita por Barry Becker do banco de dados do Censo de 1994. Um conjunto de registros razoavelmente limpos foi extraído usando as seguintes condições: ((AAGE>16) && (AGI>100) && (AFNLWGT>1)&& (HRSWK>0))  

https://archive.ics.uci.edu/ml/datasets/adult

## Requisitos
- Python
- Scikit Learn
- Matplotlib
- Seaborn

## Conjunto de dados
- Numérica discreta
	- age (idade)
	- education-num (anos de estudo)
	- hour-per-week (horas trabalhadas por semana)
- Numérico contínua
	- final-weight (no. de pessoas que o censo acredita que o registro representa)
	- capital-gain (ganho de capital)
	- capital-loos (perda de capital)
- Categórico norminal
	- workclass (classe de trabalho)
	- marital-status (estado civíl)
	- occupation (ocupação)
	- race (raça) 
	- sex (sexo)
	- native-country (país de origem)
- Categórico ordinal
	- education (estudo)
	- **income (renda)**

## #1 - Exploração dos dados
Nessa etapa, é realizado a análise exploratória de dados, de modo que seja possível determinar quais técnicas de tratamento será realizado sobre os dados, além disso, essa fase possui o intuito de estudar o comportamento das variáveis em conjunto com outras.
- Probabilidade de acertar o target de modo aleatório
- Dimensionalidade de atributos categóricos
- Distribuição dos dados
- Correlação entre dados
- Outliers
- Análise de renda agrupado por categorias

## #2 - Tratamento dos dados
- Separando base de treino e teste antes do pré-processamento para evitar data leakage
- Remoção de atributos redundantes
- Transformar features categóricas em numéricas com **Target Encoder**
- Transformar features categóricas em dummies
- Normalizando features numéricas com **MinMax Scaler**

## #3 - Seleção de Features
- Utilizando RFE (Recursive Feature Elimination)
- Ajustando base de dados para cada modelo (Random Forest, Logistic Regression, SVM Linear, Decision Tree)

## #4 - Avaliação de Algoritmos
- Otimização de hiperparâmetros
  - Random Forest
  - Logistic Regression
  - SVM Linear
  - SVM
  - Decision Tree

- Cross Validation com os hiperparâmetros encontrados
- Teste de normalidade dos resultados
- ANOVA - Análise de variação dos dados
- Teste Tukey

## #5 - Aplicação do modelo na base de teste
- Matriz de confusão
- Classification report