# Machine Learning com MongoDB

Projeto de Machine Learning desenvolvido em Python, utilizando dados armazenados no MongoDB Atlas para treinar modelos capazes de analisar produtos e prever se eles possuem um alto volume de vendas.

O projeto foi desenvolvido como uma forma de praticar conceitos de Ciência de Dados e Machine Learning, trabalhando desde a conexão com o banco de dados até o treinamento, avaliação e comparação de diferentes modelos.

## 🚀 Tecnologias utilizadas

- **Python:** linguagem utilizada no desenvolvimento.
- **MongoDB Atlas:** armazenamento dos dados dos produtos.
- **PyMongo:** conexão entre Python e MongoDB.
- **Pandas:** organização e manipulação dos dados.
- **NumPy:** suporte para operações numéricas.
- **Scikit-learn:** criação, treinamento e avaliação dos modelos.
- **Python-dotenv:** gerenciamento das variáveis de ambiente.

## 📌 Como funciona o projeto?

O projeto utiliza informações de produtos armazenadas em uma coleção do MongoDB para realizar análises e previsões.

O processo é dividido em algumas etapas:

### 1. Conexão com o MongoDB

O projeto utiliza variáveis de ambiente para acessar o MongoDB Atlas e buscar os documentos armazenados na coleção de produtos.

Os dados são carregados utilizando o PyMongo e organizados em um DataFrame com o Pandas.

### 2. Preparação dos dados

Antes de treinar os modelos, os dados passam por algumas transformações:

- Conversão das categorias dos produtos em colunas numéricas utilizando `get_dummies()`.
- Conversão dos valores de vendas ("Sim" e "Não") para `1` e `0`.
- Separação das informações utilizadas para previsão (`X`) e do resultado esperado (`y`).
- Divisão dos dados em conjuntos de treinamento e teste.

### 3. Treinamento dos modelos

O projeto utiliza quatro algoritmos de classificação para analisar os produtos e prever se eles venderam muito.

| Modelo | Objetivo |
|---|---|
| Regressão Logística | Realizar previsões de classificação a partir das características dos produtos. |
| Árvore de Decisão | Criar regras para classificar os produtos. |
| Random Forest | Combinar várias árvores de decisão para realizar previsões. |
| KNN | Classificar produtos com base nas características dos produtos mais semelhantes. |

Os modelos são treinados com os mesmos dados de treinamento, permitindo comparar seus resultados.

### 4. Avaliação dos resultados

Após o treinamento, cada modelo realiza previsões utilizando os dados de teste.

Para avaliar o desempenho, são utilizadas duas métricas:

- **Accuracy:** mostra a proporção de previsões corretas em relação ao total de previsões.
- **Matriz de Confusão:** permite visualizar a quantidade de acertos e erros do modelo em cada classe.

O projeto também apresenta as regras utilizadas pela Árvore de Decisão e a importância das características dos produtos segundo o Random Forest.

### 5. Previsão de um novo produto

Após treinar os modelos, o projeto utiliza um novo produto como exemplo para testar as previsões.

São informados o preço, o estoque e a categoria do produto.

Cada modelo realiza sua própria previsão, indicando se acredita que o produto venderá muito ou não.

### 6. Agrupamento com K-Means

Além dos modelos de classificação, o projeto também utiliza o K-Means, um algoritmo de aprendizado não supervisionado.

Diferentemente dos modelos anteriores, ele não utiliza a informação de vendas como referência para criar os grupos.

O algoritmo procura identificar três grupos de produtos com características semelhantes, considerando suas informações numéricas.

Ao final, são apresentados:

- Quantidade de produtos em cada grupo.
- Média de preço, estoque e vendas de cada grupo.
- Grupo ao qual o novo produto pertence.

## ⚙️ Como executar o projeto

### 1. Clone o repositório


git clone https://github.com/nicolassantana0505/Machine-Learning-com-Banco-de-Dados.git


### 2. Entre na pasta do projeto


cd Machine-Learning-com-Banco-de-Dados


### 3. Crie um ambiente virtual


python3 -m venv venv


Ative o ambiente virtual:


source venv/bin/activate


### 4. Instale as dependências


pip install pandas numpy scikit-learn python-dotenv pymongo


### 5. Configure as variáveis de ambiente

Crie um arquivo chamado `.env` na raiz do projeto:

MONGO_URL=sua_url_de_conexao
MONGO_DB=nome_do_banco
MONGO_COLLECTION=nome_da_colecao


Substitua os valores pelos dados do seu MongoDB Atlas.

### 6. Execute o projeto


python3 main.py


*Caso seu arquivo principal tenha outro nome, substitua `main.py` pelo nome correspondente.*

## 📚 O que foi praticado?

Durante o desenvolvimento, foram trabalhados conceitos importantes de Python, Ciência de Dados e Machine Learning:

- Conexão com banco de dados MongoDB.
- Manipulação e preparação de dados com Pandas.
- Separação entre dados de treinamento e teste.
- Aprendizado supervisionado e não supervisionado.
- Treinamento e comparação de diferentes algoritmos.
- Avaliação de modelos utilizando métricas de classificação.
- Previsão de resultados para novos dados.
- Agrupamento de dados utilizando K-Means.

---

Projeto desenvolvido com o objetivo de colocar em prática os conhecimentos adquiridos em Python, análise de dados e Machine Learning.