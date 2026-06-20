# MVP – Sprint: Machine Learning & Analytics  
### Sprint: Machine Learning & Analytics — PUC‑Rio  
**Autor:** Paulo Ricardo Marques Leite  

---

## 🔗 Executar o Notebook  
Clique abaixo para abrir o notebook diretamente no Google Colab:

👉 [Abrir no Google Colab](https://colab.research.google.com/github/pleiteues-code/mvp-machine-learning-analytics/blob/main/MVP_Machine_Learning_e_Analytics_Paulo_Ricardo.ipynb)

---

## 📘 Sobre o Projeto
Este projeto apresenta um MVP de análise exploratória de fundos de investimento, com foco em **boas práticas de análise de dados**, **visualização clara** e **comunicação objetiva dos resultados**.

O objetivo é oferecer uma visão didática sobre métricas de risco e retorno, utilizando Python e ferramentas amplamente adotadas no ecossistema de Data Science.

---

## 🎯 Objetivos do Projeto
- Explorar métricas de risco e retorno de fundos de investimento.  
- Identificar padrões, distribuições e relações entre variáveis.  
- Aplicar boas práticas de análise de dados e visualização.  
- Criar um notebook claro, organizado e didático para avaliação acadêmica.  

---
## 📂 Estrutura do Repositório

| Arquivo / Pasta | Descrição |
|------------------|------------|
| `comprehensive_mutual_funds_data.csv` | Dataset utilizado na análise |
| `MVP_Machine_Learning_e_Analytics_Paulo_Ricardo.ipynb` | Notebook principal do projeto |
| `README.md` | Documento explicativo |

---

## 🧠 Principais Etapas do Trabalho
1. **Exploração e tratamento dos dados**  
2. **Construção do pipeline de modelagem**  
3. **Treinamento e otimização do modelo Random Forest**  
4. **Avaliação de desempenho (métricas e gráficos)**  
5. **Interpretação dos resultados e análise de variáveis**  
6. **Discussão de limitações e trabalhos futuros**

---

## 📊 Resultados
O modelo apresentou desempenho consistente, capturando padrões relevantes nos retornos dos fundos e demonstrando boa aderência visual entre valores reais e previstos.  
As análises gráficas e métricas confirmam a viabilidade da abordagem proposta.

---

## 📎 Requisitos
Para execução local:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

---

## 🧾 Conclusões
A análise exploratória permitiu compreender melhor o comportamento dos fundos de investimento a partir de métricas de risco e retorno.

Alguns pontos se destacam:

- Fundos mais arriscados tendem a apresentar retornos maiores, mas com grande dispersão — reforçando que risco elevado não garante desempenho superior.  
- O Sharpe Ratio mostrou diferenças relevantes entre categorias, evidenciando que a relação risco/retorno varia bastante conforme o tipo de fundo.  
- Os retornos de 1, 3 e 5 anos apresentaram correlações positivas, sugerindo certa persistência de desempenho ao longo do tempo.  
- A presença de outliers é parte natural do universo de fundos; por isso, optou-se por mantê-los nos dados originais, aplicando apenas ajustes visuais quando necessário.  
- As visualizações ajudaram a revelar padrões e assimetrias que não seriam facilmente percebidos apenas com estatísticas descritivas.  

No conjunto, o estudo reforça a importância de analisar múltiplas métricas simultaneamente e de interpretar risco e retorno de forma contextualizada, considerando tanto a categoria do fundo quanto sua consistência histórica.
