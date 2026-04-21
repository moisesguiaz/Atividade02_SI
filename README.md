# ❤️ Detecção de Doença Cardíaca com Regressão Logística

## 📌 Descrição do Projeto

Este projeto foi desenvolvido na disciplina **Sistemas Inteligentes (PAM0466)** com o objetivo de aplicar técnicas de **Aprendizado de Máquina** para prever a presença de doenças cardíacas.

A solução utiliza o algoritmo de **Regressão Logística**, um modelo de classificação supervisionada, aplicado ao dataset **Heart Disease Cleveland**, permitindo classificar pacientes entre:

* 🟢 Saudáveis
* 🔴 Com doença cardíaca

---

## 🎯 Objetivos

* Desenvolver um modelo de **classificação binária**
* Aplicar técnicas de **pré-processamento de dados**
* Avaliar o modelo com métricas estatísticas
* Interpretar os resultados obtidos

---

## 📊 Dataset

* **Nome:** Heart Disease Cleveland
* **Fonte:** UCI Machine Learning Repository
* **Total de registros:** 303
* **Atributos:** 13 variáveis + 1 variável alvo

### 🏷️ Variável alvo:

* `0` → Ausência de doença
* `1` → Presença de doença

---

## ⚙️ Etapas do Projeto

### 1. 📥 Análise Exploratória

Nesta etapa foram realizadas:

* Leitura dos dados com `pandas`
* Visualização inicial (`head()`)
* Estatísticas descritivas (`describe()`)

---

### 2. 🧹 Pré-processamento

#### ✔ Tratamento de valores ausentes

* Variáveis tratadas: `ca` e `thal`
* Estratégia: substituição pela **mediana**

#### ✔ Transformação da variável alvo

* Conversão para valores binários (0 e 1)

#### ✔ Divisão dos dados

* 80% treino / 20% teste
* Uso de **estratificação** para manter o equilíbrio das classes

#### ✔ Padronização dos dados

* Aplicação do `StandardScaler` para normalização

---

### 3. 🤖 Modelo de Machine Learning

* **Algoritmo:** Regressão Logística
* **Biblioteca:** Scikit-learn

### 📌 Função logística:

P(Y=1\mid X)=\frac{1}{1+e^{-(\beta_0+\beta_1X_1+\cdots+\beta_nX_n)}}

Essa função transforma os dados em uma **probabilidade entre 0 e 1**, indicando a chance do paciente ter doença cardíaca.

---

### ⚙️ Parâmetros do modelo

* `solver = liblinear`
* `max_iter = 1000`
* `random_state = 42`

---

## 📈 Avaliação do Modelo

O desempenho do modelo foi avaliado utilizando:

* **Acurácia** → taxa geral de acertos
* **Precisão** → qualidade das previsões positivas
* **Recall (Sensibilidade)** → capacidade de detectar doentes
* **F1-Score** → equilíbrio entre precisão e recall
* **AUC-ROC** → capacidade de separação das classes

---

## 📊 Resultados Visuais

### 🔷 Matriz de Confusão


A matriz de confusão mostra:

* Acertos do modelo
* Erros de classificação

📌 **Importante:**
Os **falsos negativos** (FN) são críticos, pois representam pacientes doentes não identificados.

---

### 🔶 Curva ROC

* Mede a capacidade do modelo de distinguir entre classes
* Quanto mais próxima do canto superior esquerdo, melhor
* A **AUC** indica a qualidade do modelo

---

## 📌 Interpretação

Os coeficientes do modelo indicam a influência das variáveis:

* ➕ Valores positivos → aumentam a chance da doença
* ➖ Valores negativos → diminuem a chance

📍 Em aplicações médicas, o **recall é mais importante que a acurácia**, pois reduz o risco de erro crítico.

---

## 🛠️ Tecnologias Utilizadas

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

---

## ▶️ Como Executar

### 1. Clonar o repositório

```bash
git clone https://github.com/moisesguiaz/Regress-o-Log-stica.git
```

### 2. Instalar dependências

```bash
pip install -r requirements.txt
```

### 3. Executar o projeto

```bash
jupyter notebook
```

---

## 📂 Estrutura do Projeto

```
📁 projeto/
 ├── Projeto_Regressao_Logistica.ipynb
 └── README.md
```

---

## 📚 Referências

* UCI Machine Learning Repository
* Pedregosa et al. (2011) – Scikit-learn

---

## 👨‍🏫 Informações Acadêmicas

* **Disciplina:** Sistemas Inteligentes
* **Professor:** Pedro Thiago Valério de Souza
* **Semestre:** 2026.1

---

## ✍️ Autores

* **Maria Karoline**
* **Moisés Guilherme**

---

## ⭐ Considerações Finais

O modelo apresentou bom desempenho na tarefa de classificação, sendo capaz de identificar padrões relevantes nos dados clínicos.

Este projeto demonstra a aplicação prática de técnicas de **Machine Learning na área da saúde**, evidenciando a importância da análise de dados para apoio à decisão médica.

---

