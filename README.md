# Telecom X - Parte 2 📊📉
Previsão de Evasão de Clientes (Churn Prediction)

## 🧠 Propósito da Análise

Este projeto tem como objetivo principal prever a evasão de clientes (churn) de uma empresa de telecomunicações com base em variáveis relevantes extraídas de um conjunto de dados realista. A proposta está alinhada com estratégias de retenção de clientes, permitindo à empresa agir de forma proativa diante de sinais de possível evasão.

---

## 📁 Estrutura do Projeto

A estrutura de arquivos e diretórios do projeto é organizada da seguinte forma:

---

## 🧹 Preparação dos Dados

### 🔢 Extração do Arquivo Tratado e Remoção de colunas irrelevantes

### 🔧 Etapas de Transformação

- **Tratamento de valores ausentes**: Valores ausentes foram removidos ou tratados com imputação dependendo da variável.
- **Codificação**: As variáveis categóricas foram transformadas por meio de:
  - `LabelEncoder` para variáveis binárias
  - `OneHotEncoder` para variáveis com mais de duas categorias
- **Normalização**:
  - As variáveis numéricas foram normalizadas com `StandardScaler` para o modelo KNN.

### ✂️ Divisão dos Dados

- Os dados foram divididos em **70% treino** e **30% teste**, utilizando `train_test_split` com `stratify` para manter o equilíbrio das classes de churn.

---

## 🤖 Modelos Utilizados

- **KNN (K-Nearest Neighbors)**
- **Árvore de Decisão (Decision Tree)**

### Justificativas:

- **KNN** foi escolhido por sua simplicidade e eficiência em detectar padrões locais no conjunto de dados.
- **Árvore de Decisão** foi escolhida por sua interpretabilidade e por fornecer insights claros sobre a importância das variáveis.

---

## 📊 EDA – Análise Exploratória de Dados

Alguns dos principais insights obtidos:

- A maioria dos clientes que cancelam seus contratos estão nos primeiros meses de uso (`tenure` baixo).
- Clientes com contratos do tipo **mensal** e que usam **serviços de internet fibra** apresentam maiores taxas de churn.
- O valor da fatura mensal (`MonthlyCharges`) tende a ser maior entre os clientes que cancelam.
- Clientes que possuem dependentes ou parceiros têm menor probabilidade de evasão.

### Exemplos de Visualizações:

- Distribuição de clientes que saíram vs. permaneceram
- Gráficos de correlação entre variáveis numéricas
- Importância das variáveis segundo a árvore de decisão

---

## ▶️ Instruções para Execução

### 🧰 Bibliotecas Necessárias

Fazer upload do arquivo no Google Colab ou instalar as dependências para rodar em outras IDE:

```python
!pip install pandas numpy matplotlib seaborn scikit-learn
