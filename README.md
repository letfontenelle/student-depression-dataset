# 🧠 Análise de Depressão em Estudantes

## 📋 Sobre o Projeto

Este projeto apresenta uma análise completa de dados sobre depressão em estudantes, utilizando técnicas de ciência de dados e machine learning para identificar fatores de risco e desenvolver modelos preditivos.

### 🎯 Objetivos

- **Identificar** os principais fatores associados à depressão em estudantes
- **Desenvolver** modelos de machine learning para predição de casos de depressão
- **Fornecer** insights acionáveis para intervenções preventivas
- **Criar** uma ferramenta de triagem para identificação de estudantes em risco

## 📊 Dataset

O dataset contém **27.901 registros** de estudantes com **18 variáveis** relacionadas a:

- **Demografia**: Idade, Gênero, Cidade
- **Acadêmico**: Pressão Acadêmica, CGPA, Satisfação com Estudos, Horas de Estudo
- **Profissional**: Pressão no Trabalho, Satisfação no Trabalho
- **Estilo de Vida**: Duração do Sono, Hábitos Alimentares
- **Psicológico**: Pensamentos Suicidas, Histórico Familiar de Doenças Mentais
- **Socioeconômico**: Estresse Financeiro
- **Target**: Depressão (0: Não, 1: Sim)

### 📈 Distribuição dos Dados

- **Casos Não Depressivos**: ~60% dos registros
- **Casos Depressivos**: ~40% dos registros
- **Balanceamento**: Dataset relativamente balanceado

## 🛠️ Tecnologias Utilizadas

### 📚 Bibliotecas Principais

```python
# Manipulação de Dados
pandas==2.0.3
numpy==1.24.3

# Visualização
matplotlib==3.7.2
seaborn==0.12.2
plotly==5.15.0

# Machine Learning
scikit-learn==1.3.0

# Persistência
joblib==1.3.2
```

### ⚙️ Ferramentas

- **Python 3.8+**
- **Jupyter Notebook**
- **Git** para versionamento
- **conda/pip** para gerenciamento de dependências

## 📈 Principais Resultados

### 🎯 Performance dos Modelos

| Modelo | Accuracy | AUC Score | F1-Score |
|--------|----------|-----------|----------|
| **Random Forest** | **0.847** | **0.891** | **0.823** |
| Rede Neural | 0.834 | 0.878 | 0.811 |

### 🔍 Top 5 Fatores de Risco

1. **Pensamentos Suicidas** (correlação: 0.74)
2. **Histórico Familiar** (correlação: 0.42)
3. **Duração do Sono < 5h** (correlação: 0.38)
4. **Alta Pressão Acadêmica** (correlação: 0.31)
5. **Baixa Satisfação com Estudos** (correlação: -0.29)

### 📊 Insights Principais

- **71%** dos estudantes com pensamentos suicidas apresentam depressão
- Estudantes que dormem **menos de 5 horas** têm **2.3x** mais risco
- **Histórico familiar** aumenta o risco em **89%**
- **Mulheres** apresentam taxa ligeiramente maior (43% vs 38%)

## 🔧 Features Desenvolvidas

### 🆕 Features Criadas

```python
# Features derivadas para melhor predição
1. High_Risk_Profile          # Combina histórico familiar + pensamentos suicidas
2. Poor_Sleep_Quality         # Sono < 5 horas
3. High_Academic_Pressure     # Pressão acadêmica >= 4
4. Unhealthy_Lifestyle        # Combina sono ruim + alimentação inadequada
```

### 🎛️ Pré-processamento

- **Tratamento de valores ausentes**: Imputação por mediana (numérica) e moda (categórica)
- **Codificação de categóricas**: One-Hot Encoding para ML, Label Encoding para correlação
- **Normalização**: StandardScaler para variáveis numéricas
- **Validação de dados**: Tratamento robusto de inconsistências

## 📊 Visualizações Disponíveis

### 📈 Principais Gráficos

1. **Distribuição da variável target**
2. **Taxa de depressão por fatores demográficos**
3. **Matriz de correlação entre variáveis**
4. **Importância das features (Random Forest)**
5. **Curvas ROC comparativas**
6. **Análise de fatores de risco**

### 🎨 Executar Visualizações

```python
# executar notebook específico (student_depression_notebook_with_cv.ipynb)
```

## 🧪 Validação e Testes

### ✅ Validação Cruzada

- **5-Fold Cross Validation**
- **Stratified sampling** para manter distribuição
- **Métricas múltiplas**: Accuracy, Precision, Recall, F1-Score, AUC

### 🔍 Análise de Erros

- **Matriz de confusão detalhada**
- **Análise de falsos positivos/negativos**
- **Curva Precision-Recall**
- **Feature importance analysis**

## 📝 Limitações e Considerações

### ⚠️ Limitações

1. **Dados auto-reportados**: Possível viés de resposta
2. **Corte transversal**: Não estabelece causalidade
3. **População específica**: Limitado a estudantes
4. **Variáveis ausentes**: Fatores socioeconômicos detalhados

### 🎯 Próximos Passos

1. **Coleta longitudinal** para análise temporal
2. **Validação externa** em outras populações
3. **Incorporação de dados objetivos** (wearables, registros acadêmicos)
4. **Desenvolvimento de app móvel** para triagem
5. **Integração com sistemas de saúde estudantil**

## 👥 Autores

- Carlson Verçosa
- Caio Tenório
- Leticia Fontenelle
- Luca de Roldão
- Vitor Queiroz

## 🙏 Agradecimentos

- Comunidade científica por disponibilizar o dataset
- Bibliotecas open-source utilizadas
- Revisores e colaboradores do projeto

**⚡ Análise de Depressão em Estudantes - Transformando dados em insights para melhor saúde mental estudantil**
