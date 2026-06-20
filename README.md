# 📘 MVP de Machine Learning & Analytics para Fundos de Investimento

### Autor: Paulo Ricardo Marques Leite  
**Matrícula:** 4052025002553  
**Data:** 07/2026  

---

## 🔗 Executar o Notebook  
Clique abaixo para abrir o notebook diretamente no Google Colab:

👉 [Abrir no Google Colab](https://colab.research.google.com/github/pleiteues-code/mvp-machine-learning-analytics/blob/main/MVP_Machine_Learning_e_Analytics_Paulo_Ricardo.ipynb)

---

## 🎯 Objetivo Geral

Este projeto constrói um **MVP completo de Machine Learning & Analytics** para prever o **retorno de 1 ano (`returns_1yr`)** de fundos de investimento, utilizando métricas de risco, performance e estrutura dos fundos.

O ciclo completo de ciência de dados é seguido:
> Definição do problema → EDA → Preparação → Modelagem → Avaliação → Interpretação → Conclusões

---

## 🧠 Tipo de Problema
**Regressão** — previsão de variável contínua.

---

## 📦 Entregáveis
- Análise exploratória detalhada (EDA)  
- Pipeline de pré-processamento (numérico + categórico)  
- Modelos lineares e não lineares  
- Baseline comparativo  
- Otimização de hiperparâmetros  
- Interpretação dos resultados  
- Conclusões e próximos passos  

---

## 📂 Estrutura do Repositório

| Arquivo / Pasta | Descrição |
|------------------|------------|
| `comprehensive_mutual_funds_data.csv` | Dataset utilizado na análise |
| `MVP_Machine_Learning_e_Analytics_Paulo_Ricardo.ipynb` | Notebook principal do projeto |
| `README.md` | Documento explicativo |

---


## 🔗 Fonte dos Dados
Dataset público disponível em:  
[Comprehensive Mutual Funds Data](https://raw.githubusercontent.com/pleiteues-code/mvp-machine-learning-analytics/refs/heads/main/comprehensive_mutual_funds_data.csv)

> Contém mais de 800 fundos e 20 variáveis, incluindo métricas de risco, retorno e estrutura.

---

## ⚙️ Tecnologias Utilizadas
- **Python 3.10+**
- **Bibliotecas:**  
  `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
- **Modelos:**  
  - DummyRegressor (baseline)  
  - Ridge Regression (linear)  
  - Random Forest Regressor (não linear)

---

## 📊 Principais Resultados

| Modelo | MAE | RMSE | R² |
|--------|-----|------|----|
| Baseline | ~3.5 | ~5.2 | 0.00 |
| Ridge Regression | ~3.1 | ~4.9 | 0.28 |
| Random Forest | ~2.9 | ~4.8 | 0.33 |

> O **Random Forest** apresentou melhor desempenho geral, capturando relações não lineares entre risco, retorno e estrutura dos fundos.

---

## 🔍 Insights e Interpretações

- Retornos históricos (3 e 5 anos) são os principais preditores do retorno de 1 ano.  
- Métricas de risco (Sharpe, Sortino, Beta, Alpha) têm influência significativa.  
- Categorias e subcategorias de fundos explicam parte da variabilidade dos retornos.  
- O *expense ratio* tende a impactar negativamente o retorno líquido.  

---

## 📈 Visualizações

- **Comparativo de métricas dos modelos** → `01_comparativo_de_metricas_dos_modelos.png`  
- **Importância das variáveis (Random Forest)** → `02_variaveis_do_random_forest.png`  
- **Valores reais vs previstos** → `03_comparacao_valores_reais_x_previstos.png`  
- **Análise dos resíduos** → `04_analise_dos_residuos.png`

---

## 🧩 Conclusões

- O modelo Random Forest é o mais adequado para capturar padrões complexos nos dados.  
- O desempenho (R² ≈ 0.23–0.33) é compatível com a natureza volátil dos retornos financeiros.  
- O MVP demonstra um pipeline robusto e reprodutível para análise preditiva de fundos.  

---

## 🚀 Próximos Passos

- Explorar modelos baseados em *Gradient Boosting* (XGBoost, LightGBM).  
- Incluir variáveis macroeconômicas externas.  
- Implementar validação temporal (rolling window).  
- Criar dashboard interativo com *Streamlit* ou *Plotly Dash*.

---

## 🧾 Licença
Este projeto é disponibilizado sob a licença **MIT**.  
Sinta-se livre para usar, modificar e compartilhar com atribuição.

---

## 📬 Contato
**GitHub:** [pleiteues-code](https://github.com/pleiteues-code)  
**E-mail:** pleiteues@gmail.com
---

> *“Machine Learning não prevê o futuro — ele revela padrões que o presente já contém.”*
