# 📊 MVP Machine Learning & Analytics – Predição de Rentabilidade de Fundos de Investimento

### Autor: Paulo Ricardo Marques Leite  
**Matrícula:** 4052025002553  
**Data:** 07/2026  

---

## 🔗 Executar o Notebook  
Clique abaixo para abrir o notebook diretamente no Google Colab:

👉 [Abrir no Google Colab](https://colab.research.google.com/github/pleiteues-code/mvp-machine-learning-analytics/blob/main/MVP_Machine_Learning_e_Analytics_Paulo_Ricardo.ipynb)

---
<p align="center">
  <img src="/03_comparacao_valores_reais_x_previstos.png" width="700">
</p>

<p align="center">
Comparação entre os retornos reais observados e os retornos previstos pelo modelo Random Forest.
</p>
---
## 📌 Objetivo

Este projeto tem como objetivo desenvolver um modelo de Machine Learning capaz de prever a rentabilidade anual de fundos de investimento (`returns_1yr`) a partir de indicadores de risco, desempenho histórico, características estruturais e métricas de gestão.

O trabalho foi desenvolvido como MVP (Minimum Viable Product) para aplicação prática dos conceitos de Ciência de Dados e Machine Learning, contemplando todo o ciclo de desenvolvimento analítico:

* Análise Exploratória dos Dados (EDA)
* Tratamento e preparação dos dados
* Engenharia de atributos
* Construção de pipelines
* Treinamento de modelos preditivos
* Validação cruzada
* Otimização de hiperparâmetros
* Avaliação e interpretação dos resultados

---

## 📂 Dataset

O dataset contém informações de fundos de investimento, incluindo:

* Rentabilidades históricas
* Indicadores de risco
* Alpha
* Beta
* Sharpe Ratio
* Sortino Ratio
* Taxa de administração
* Patrimônio do fundo
* Idade do fundo
* Classificação e categoria

**Base utilizada:**

`comprehensive_mutual_funds_data.csv`

**Dimensões da base:**

* 814 fundos de investimento
* 20 atributos originais

---

## 🛠️ Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn

---

## 🔍 Engenharia de Atributos

Além das variáveis originais, foram criadas novas métricas para aumentar a capacidade preditiva dos modelos:

| Variável             | Descrição                                    |
| -------------------- | -------------------------------------------- |
| `return_gap`         | Diferença entre retorno de 3 e 5 anos        |
| `risk_return_ratio`  | Relação entre Sharpe e nível de risco        |
| `size_age_ratio`     | Relação entre patrimônio e idade do fundo    |
| `expense_per_rating` | Relação entre taxa de administração e rating |

A variável **Risk Return Ratio** destacou-se posteriormente entre os atributos mais importantes para o modelo final.

---

## 🤖 Modelos Avaliados

Foram comparados quatro modelos de regressão.

### 1. Dummy Regressor (Baseline)

Modelo utilizado como referência mínima de desempenho.

| Métrica | Resultado |
| ------- | --------: |
| R²      |    -0.009 |

---

### 2. Ridge Regression

Modelo linear com regularização para redução de overfitting.

| Métrica | Resultado |
| ------- | --------: |
| R²      |     0.280 |

---

### 3. Random Forest

Modelo baseado em múltiplas árvores de decisão.

| Métrica | Resultado |
| ------- | --------: |
| R²      |     0.517 |
| MAE     |     2.087 |
| RMSE    |     3.816 |

---

### 4. Gradient Boosting

Modelo de ensemble baseado em boosting sequencial.

| Métrica | Resultado |
| ------- | --------: |
| R²      |     0.516 |
| MAE     |     2.220 |
| RMSE    |     3.819 |

---

## 🏆 Modelo Selecionado

O **Random Forest** foi escolhido como modelo final por apresentar:

* Melhor desempenho no conjunto de teste;
* Menor erro absoluto médio (MAE);
* Menor RMSE;
* Boa capacidade de generalização;
* Facilidade de interpretação através da análise de importância das variáveis.

Durante a etapa de otimização com `RandomizedSearchCV`, os resultados permaneceram praticamente inalterados, indicando que a configuração inicial já estava próxima de uma solução adequada para o problema analisado.

---

## 📈 Principais Variáveis Identificadas

As variáveis mais importantes para a previsão dos retornos anuais foram:

| Variável           | Importância |
| ------------------ | ----------: |
| SD (Desvio Padrão) |       26.0% |
| Alpha              |       16.3% |
| Returns 5yr        |       10.1% |
| Beta               |        8.6% |
| Risk Return Ratio  |        5.3% |

---

## 📊 O que os Dados Revelam sobre a Performance dos Fundos

Os resultados mostram que a rentabilidade anual dos fundos está fortemente associada a indicadores clássicos de risco e desempenho.

Entre os fatores com maior influência sobre as previsões realizadas pelo modelo destacaram-se:

* Volatilidade do fundo (SD);
* Alpha;
* Histórico de rentabilidade em 5 anos;
* Beta;
* Relação entre risco e retorno.

Os achados sugerem que fundos capazes de gerar retorno consistente ajustado ao risco tendem a apresentar padrões de desempenho mais previsíveis do que aqueles avaliados apenas por características operacionais ou administrativas.

Outro ponto relevante é que o histórico de performance continua sendo uma fonte importante de informação para estimar resultados futuros, especialmente quando analisado em conjunto com métricas de risco e qualidade da gestão.

A análise também evidenciou que indicadores relacionados à geração de alpha e ao controle de volatilidade possuem papel central na explicação dos retornos observados, reforçando conceitos amplamente utilizados pela indústria de gestão de recursos.

De forma geral, o estudo demonstra que técnicas de Machine Learning podem ser utilizadas para identificar padrões relevantes no comportamento dos fundos de investimento, fornecendo suporte quantitativo para análises e processos de tomada de decisão.

---

## 📊 Resultado Final

O modelo final foi capaz de explicar aproximadamente:

### **52% da variabilidade dos retornos anuais dos fundos de investimento**

**Métricas finais:**

| Métrica | Resultado |
| ------- | --------: |
| R²      |     0.517 |
| MAE     |     2.087 |
| RMSE    |     3.816 |

Considerando a elevada complexidade e imprevisibilidade do mercado financeiro, esse resultado demonstra que técnicas de Machine Learning podem fornecer informações relevantes para apoiar análises quantitativas de fundos de investimento.

---

## 🚀 Possíveis Evoluções

Como extensões futuras do projeto, podem ser explorados:

* XGBoost
* LightGBM
* CatBoost
* Variáveis macroeconômicas
* Séries temporais
* Dados de mercado em tempo real
* Seleção avançada de atributos
* Explainable AI (SHAP Values)

---

## 📬 Contato
**GitHub:** [pleiteues-code](https://github.com/pleiteues-code)  
**E-mail:** pleiteues@gmail.com
---

> *“Machine Learning não prevê o futuro — ele revela padrões que o presente já contém.”*
