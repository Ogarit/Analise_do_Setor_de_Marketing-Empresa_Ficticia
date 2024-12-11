# Análise do Setor de Marketing - Empresa X

## Descrição do Projeto

Este projeto tem como objetivo analisar os investimentos de marketing de uma empresa fictícia em três meios de comunicação: YouTube, Facebook e Jornal. A análise busca determinar se a empresa está obtendo retornos lucrativos e identificar os melhores canais para alocar os recursos de marketing. Ao final, um modelo de regressão é treinado para prever os possíveis retornos com base nos diferentes níveis de investimento.

## Estrutura do Projeto

O projeto é dividido nas seguintes etapas:

1. **Importação do Dataset**  
   O dataset utilizado é o arquivo CSV `MKT.csv`, fornecido no Desafio 4 do Curso de Data Science da Escola DNC. Ele contém dados de investimentos e retornos em diferentes plataformas de mídia.

2. **Análise Descritiva**  
   Realiza-se uma análise inicial das características do dataset, com a visualização de dados e geração de estatísticas descritivas. Além disso, é feita a análise das correlações entre as variáveis.

3. **Análise Exploratória de Dados (EDA)**  
   Usando as bibliotecas Seaborn e Matplotlib, é realizada uma análise visual para identificar padrões e possíveis outliers nas variáveis de investimento e retorno.

4. **Tratamento de Outliers**  
   Os outliers são identificados utilizando o método de Tukey e tratados para melhorar a qualidade dos dados e a performance dos modelos.

5. **Modelagem Preditiva**  
   Três modelos de regressão são treinados e comparados:
   - **Regressão Linear**
   - **DecisionTreeRegressor**
   - **XGBRegressor**
   
   O modelo XGBRegressor é otimizado utilizando **GridSearchCV** para encontrar os melhores parâmetros e, em seguida, utilizado para prever os melhores cenários de investimento.

## Tecnologias Utilizadas

- **Pandas**: Para manipulação e análise de dados.
- **Seaborn** e **Matplotlib**: Para visualização de dados.
- **Scikit-Learn**: Para modelagem de regressão e avaliação dos modelos.
- **XGBoost**: Para modelagem e otimização do modelo de regressão.

## Conclusões

A análise dos dados de marketing revelou os seguintes pontos principais:

- **Facebook**: Apresentou a maior correlação com as vendas, sugerindo que aumentar os investimentos nesta plataforma poderia gerar retornos mais significativos.
- **Jornal**: Apresentou uma correlação baixa com as vendas, indicando que os investimentos nesta mídia poderiam ser reduzidos ou redirecionados.
- **YouTube**: Após a modelagem, foi identificado como a plataforma com o maior retorno sobre o investimento, seguido pelo Facebook.
- **Recomendação**: O investimento no Jornal se mostrou ineficaz e deve ser realocado para plataformas com maior potencial de retorno, como YouTube e Facebook.

## Resultados da Modelagem

| Modelo                              | RMSE   |
|-------------------------------------|--------|
| **Regressão Linear**                | 1.8316 |
| **DecisionTreeRegressor**           | 1.2274 |
| **XGBRegressor (Antes da Otimização)** | 0.8777 |
| **XGBRegressor (Otimizado)**        | 0.8394 |

## Como Rodar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Ogarit/Analise_do_Setor_de_Marketing-Empresa_Ficticia.git
2. **Instale as dependências**:
   - Se você estiver utilizando um ambiente virtual, crie e ative-o.
   - Instale as dependências utilizando o requirements.txt:
     ```bash
     pip install -r requirements.txt
3. **Execute o código**:
   - Para rodar a análise, execute o script principal:
     ```bash
     python main.py
4. **Visualize os Resultados**:
   - A análise será apresentada via gráficos gerados pelas bibliotecas Seaborn e Matplotlib.
