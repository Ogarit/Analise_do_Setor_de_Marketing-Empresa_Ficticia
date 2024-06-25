# Análise do Setor de Marketing - Empresa X

## Descrição do Projeto

Este projeto tem como objetivo analisar os investimentos de marketing de uma empresa fictícias em três meios de comunicação: YouTube, Facebook e Jornal. A análise busca determinar se a empresa está obtendo retornos lucrativos e quais são os melhores investimentos. No final, um modelo de regressão é treinado para identificar os possíveis retornos para diferentes variáveis de investimento.

## Estrutura do Projeto

1. **Importação do Dataset**: Utiliza um dataset em formato CSV denominado `MKT.csv`, fornecido no Desafio 4 do Curso de Data Science da Escola DNC.
   
2. **Análise Descritiva**: Descreve as características do dataset, incluindo visualização inicial, estatísticas descritivas e correlações entre as variáveis.
   
3. **Análise Exploratória**: Utiliza as bibliotecas Seaborn e Matplotlib para visualizar a correlação entre os dados e identificar possíveis outliers.
   
4. **Tratamento de Outliers**: Os outliers são identificados e tratados utilizando o método de Tukey.

5. **Modelagem**: Três modelos de regressão são treinados e comparados:
   - Regressão Linear
   - DecisionTreeRegressor
   - XGBRegressor
   
   O modelo XGBRegressor é otimizado utilizando GridSearchCV e, em seguida, utilizado para prever os melhores cenários de investimento.

## Tecnologias Utilizadas

- **Pandas**: Para manipulação e análise de dados.
- **Seaborn** e **Matplotlib**: Para visualização de dados.
- **Scikit-Learn**: Para modelagem e avaliação dos modelos de regressão.
- **XGBoost**: Para modelagem e otimização do modelo de regressão.

## Conclusões

* **Facebook** mostrou uma maior correlação inicial com as vendas, sugerindo um aumento nos investimentos nesta plataforma.
* **Jornal** apresentou uma correlação baixa com as vendas, indicando que os investimentos nesta plataforma poderiam ser reduzidos.
* **YouTube** foi identificado, após a modelagem, como a plataforma com o maior retorno de investimento, seguido pelo Facebook.
* O investimento no Jornal mostrou-se irrelevante e deve ser redirecionado para as outras plataformas.

## Resultados da Modelagem

* **Regressão Linear**: RMSE de 1.8316
* **DecisionTreeRegressor**: RMSE de 1.2274
* **XGBRegressor**: RMSE de 0.8777 (antes da otimização)
* **XGBRegressor Otimizado**: RMSE de 0.8394

## Autores
* Tiago Marques Lima
