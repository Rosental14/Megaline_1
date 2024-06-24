# Modelo de Recomendação de Planos da Megaline

## Descrição
Este projeto faz parte do curso de Ciência de Dados da TripleTen e envolve a criação de um modelo de classificação para a operadora de celular Megaline. 
O objetivo é analisar o comportamento dos clientes e recomendar um dos planos mais recentes: **Smart ou Ultra**, utilizando dados comportamentais de clientes que já migraram para os novos planos. O modelo deve alcançar uma acurácia mínima de 0,75.  
<br>

## Instalação
**Pré-requisitos**
* **Python 3.x:** (Qualquer versão do Python 3, como 3.6, 3.7, 3.8, etc.)
* **Bibliotecas Python:**
    * pandas
    * numpy
    * scikit-learn
    * matplotlib
    * seaborn

**Instruções de Instalação**
1.	**Clone o repositório:** git clone https://github.com/Rosental14/Megaline_1.git
2.	**Navegue até o diretório do projeto:**
3.	**Instale as dependências:** pip install -r requirements.txt
<br>

## Uso
1.	Abra o Jupyter Notebook
2.	Navegue até o arquivo projeto_megaline_1.ipynb e abra-o.
3.	Execute as células sequencialmente para reproduzir a análise e a criação do modelo.
<br>

## Funcionalidades  

### Etapas Iniciais
* **Importação de Bibliotecas:** pandas, numpy, scikit-learn, matplotlib e seaborn.  

* **Leitura dos Dados:** Carregamento do arquivo users_behavior.csv 

* **Informações Gerais:** Impressão das informações gerais do DataFrame para conferir tipos de dados e valores ausentes.  
<br>

### Divisão dos Dados
* **Divisão em Conjuntos:** Divisão dos dados em conjuntos de treinamento, validação e teste na proporção 80:10:10.
  
* **Características e Alvo:** Definição das colunas de características e do alvo.
<br>

### Estudo do Melhor Modelo
* **Modelos Testados:** Avaliação de três modelos de classificação: Árvore de Decisão, Floresta Aleatória e Regressão Logística.

* **Métricas de Avaliação:** Utilização da acurácia como métrica principal e consideração do tempo de execução dos modelos.
<br>

#### Árvore de Decisão
* **Hiperparâmetros:** Teste de diferentes valores para criterion, min_samples_leaf e max_depth.

* **Melhor Modelo:** Acurácia de 83.18% com max_depth=10, criterion='gini' e min_samples_leaf=7.

* **Tempo de Execução:** Aproximadamente 2.31 segundos.
<br>

#### Floresta Aleatória
* **Hiperparâmetros:** Teste de diferentes valores para bootstrap, max_depth e n_estimators.

* **Melhor Modelo:** Acurácia de 83.18% com max_depth=1, bootstrap=False e n_estimators=9.

* **Tempo de Execução:** Aproximadamente 7.67 segundos.
<br>

#### Regressão Logística
* **Modelo:** Utilização de solver='liblinear' e random_state=14.

* **Acurácia:** 71.34%.

* **Tempo de Execução:** Aproximadamente 0.01 segundos.
<br>

### Teste do Melhor Modelo
* **Treinamento Completo:** Treinamento do melhor modelo (Árvore de Decisão) com todos os dados disponíveis.

* **Acurácia no Conjunto de Teste:** 84.47%.
<br>

### Prova Real do Modelo
* **Comparação com Dados Aleatórios:** Acurácia de 84.5% com dados reais e aproximadamente 50% com dados aleatórios, comprovando a eficiência do modelo.
<br>

## Créditos
* **Autor:** Renan Rosental
<br>

## Contato
Para dúvidas e feedback, entre em contato via e-mail: renan.engal@gmail.com
