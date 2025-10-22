# DeteccaoPhishing
# 🔒 Detecção de URLs de Phishing com Machine Learning

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SEU_USUARIO/SEU_REPOSITORIO/blob/main/Deteccao_Phishing_ML.ipynb)

> Projeto de Machine Learning para classificação automática de URLs maliciosas vs. legítimas

## 📋 Sobre o Projeto

Este projeto desenvolve um sistema de **detecção automática de URLs de phishing** utilizando técnicas clássicas de Machine Learning. O objetivo é classificar URLs como legítimas ou maliciosas, contribuindo para a segurança cibernética e proteção de usuários contra ataques de phishing.

**Instituição:** Universidade de Brasília (UnB)  
**Departamento:** Engenharia de Produção  
**Professor:** Dr. Andre Luiz Marques Serrano  
**Data:** Outubro de 2025

## 🎯 Objetivos

- Desenvolver modelo de ML capaz de identificar URLs de phishing
- Comparar diferentes algoritmos de classificação
- Alcançar alta taxa de detecção (Recall) mantendo baixos falsos positivos
- Criar solução pronta para implementação em sistemas de segurança

## 📊 Resultados Principais

| Métrica | Valor |
|---------|-------|
| **Accuracy** | 95.2% |
| **Precision** | 94.8% |
| **Recall** | 95.6% |
| **F1-Score** | 95.2% |
| **ROC-AUC** | 98.1% |

**Melhor Modelo:** Random Forest (Otimizado)

## 🗂️ Estrutura do Projeto

```
deteccao-phishing-ml/
│
├── Deteccao_Phishing_ML.ipynb    # Notebook principal (Google Colab)
├── README.md                      # Este arquivo
```

## 🚀 Como Usar

### Opção 1: Google Colab (Recomendado)

1. Clique no badge "Open in Colab" no topo deste README
2. Execute todas as células sequencialmente (`Runtime > Run all`)
3. Aguarde o treinamento dos modelos (~5-10 minutos)

## 📦 Dependências

```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
```

## 🔍 Metodologia

### 1. Análise Exploratória de Dados (EDA)
- Análise de correlação entre features
- Identificação de features mais relevantes
- Visualização da distribuição das classes
- Detecção de outliers e valores ausentes

### 2. Preparação dos Dados
- Divisão treino/teste (80/20) com estratificação
- Feature selection (SelectKBest com ANOVA e Mutual Information)
- Transformações testadas:
  - Dados originais
  - StandardScaler (normalização Z-score)
  - RobustScaler (robusto a outliers)

### 3. Modelagem
Algoritmos testados:
- ✅ **Regressão Logística** (Baseline)
- ✅ **Árvore de Decisão**
- ✅ **Random Forest** (Melhor modelo)

**Técnicas aplicadas:**
- Cross-validation (k=5 folds) com StratifiedKFold
- Grid Search para otimização de hiperparâmetros
- Análise de overfitting/underfitting

### 4. Avaliação
Métricas utilizadas:
- Accuracy, Precision, Recall, F1-Score
- ROC-AUC Score
- Matriz de Confusão
- Curvas ROC

## 📈 Principais Descobertas

### 1. Feature Importance
As características mais importantes para detecção de phishing:
- Comprimento da URL
- Presença de caracteres especiais (@, -, ~)
- Uso de endereço IP ao invés de domínio
- Número de subdomínios
- Presença de HTTPS

### 2. Performance dos Modelos

| Modelo | Accuracy | F1-Score | Tempo (s) |
|--------|----------|----------|-----------|
| Regressão Logística | 89.3% | 89.1% | 0.8 |
| Árvore de Decisão | 92.7% | 92.5% | 1.2 |
| **Random Forest** | **95.2%** | **95.2%** | 15.4 |

### 3. Impacto da Otimização
A otimização de hiperparâmetros trouxe:
- **+2.3%** de melhoria no F1-Score
- Melhor balanceamento Precision/Recall
- Redução de falsos negativos

## ⚠️ Pontos de Atenção

1. **False Negative Rate:** 4.4% (algumas URLs de phishing ainda passam)
2. **Evolução do Phishing:** Modelo precisa ser retreinado periodicamente
3. **Features Limitadas:** Análise apenas da URL (não do conteúdo da página)

## 🔧 Melhorias Futuras

- [ ] Incorporar análise de conteúdo HTML/JavaScript
- [ ] Implementar Deep Learning (LSTM para análise sequencial)
- [ ] Criar API REST para servir predições
- [ ] Desenvolver dashboard de monitoramento
- [ ] Implementar sistema de feedback dos usuários
- [ ] Adicionar detecção de anomalias

## 📚 Dataset

**Fonte:** [Phishing Dataset - GitHub](https://raw.githubusercontent.com/GregaVrbancic/Phishing-Dataset/master/dataset.csv)

**Características:**
- Total de amostras: ~11,000 URLs
- Features: 30+ características extraídas
- Classes: Balanceadas (50/50)
- Tipo: Features numéricas e binárias

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas** - Manipulação de dados
- **NumPy** - Operações numéricas
- **Scikit-learn** - Machine Learning
- **Matplotlib & Seaborn** - Visualização
- **Google Colab** - Ambiente de desenvolvimento

## 📝 Referências

1. Basit, A., Zafar, M., Liu, X., Javed, A. R., Jalil, Z., & Kifayat, K. (2021). A comprehensive survey of AI-enabled phishing attacks detection techniques. Telecommunications Systems, 76(1), 139-154.

2. Jain, A. K., & Gupta, B. B. (2018). A machine learning based approach for phishing detection using hyperlinks information. Journal of Ambient Intelligence and Humanized Computing, 10(5), 2015-2028.

3. UCI Machine Learning Repository: [Phishing Websites Dataset](https://archive.ics.uci.edu/ml/datasets/phishing+websites)

## 👨‍💻 Autor

**Helena Silveira Ventura**
- 🎓 Universidade de Brasília - Engenharia de Produção




---

⭐ Se este projeto foi útil, considere dar uma estrela!

**Desenvolvido com 💙 para tornar a internet mais segura**
