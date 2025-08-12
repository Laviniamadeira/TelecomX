## 📞 TelecomX - Análise de Churn de Clientes

## 📋 Descrição do Projeto

Este projeto realiza uma **análise completa de churn** (evasão de clientes) de uma empresa de telecomunicações, utilizando técnicas de **ciência de dados** e **análise exploratória** para identificar os principais fatores que levam ao cancelamento de serviços.

A análise revela insights acionáveis que podem reduzir significativamente a taxa de churn da empresa, atualmente em **25,72%**.

## 🎯 Objetivos

- **🔍 Investigar** os principais fatores que influenciam o churn de clientes
- **📊 Realizar** análise exploratória completa dos dados (EDA)
- **📈 Identificar** padrões e correlações relevantes para o negócio
- **💡 Fornecer** insights acionáveis para estratégias de retenção
- **🚀 Preparar** base para modelagem preditiva (Parte 2)

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas** - Manipulação e análise de dados
- **NumPy** - Computação numérica
- **Matplotlib** - Visualizações estáticas
- **Seaborn** - Visualizações estatísticas
- **Jupyter Notebook** - Ambiente de desenvolvimento
- **Git/GitHub** - Controle de versão

## 📂 Estrutura do Projeto

```
TelecomX/
│
├── 📓 TelecomX_BR.ipynb      # Notebook principal com análise completa
├── 📄 TelecomX_dicionario.md       # Dicionário de dados
├── 📋 README.md                    # Este arquivo
```

## 🔄 Metodologia - Processo ETL

### 📥 **Extract (Extração)**
- Importação de dados do formato JSON
- Carregamento via pandas com normalização automática

### 🔧 **Transform (Transformação)**
- Normalização de colunas aninhadas (customer, phone, internet, account)
- Padronização de nomenclatura (snake_case)
- Encoding de variáveis categóricas (Yes/No → 1/0)
- Conversão de tipos de dados adequados
- Feature engineering (criação da variável `contas_diarias`)

### 📊 **Load & Analysis (Carga e Análise)**
- Análise descritiva completa
- Visualizações por variáveis categóricas e numéricas
- Análise de correlações
- Geração de insights acionáveis

## 📈 Principais Resultados

### 🔍 **Descobertas Críticas:**

| **Fator de Risco** | **Taxa de Churn** | **Impacto** |
|---------------------|-------------------|-------------|
| Contrato Month-to-month | **41,32%** | 🔴 Alto |
| Pagamento Electronic check | **43,80%** | 🔴 Alto |
| Internet Fiber optic | **40,56%** | 🔴 Alto |
| Clientes novos (≤12 meses) | **45,78%** | 🔴 Crítico |
| Sem parceiro/dependentes | **32,01% / 30,34%** | 🟡 Médio |

### 💡 **Insights Principais:**
- **Paradoxo do Valor**: Clientes que pagam mais têm maior propensão ao churn
- **Fator Tempo**: Primeiros 12 meses são críticos para retenção
- **Estabilidade Familiar**: Clientes com vínculos familiares são mais fiéis
- **Flexibilidade vs Fidelidade**: Contratos flexíveis aumentam risco de saída


## 🏆 Destaques

Este projeto demonstra competências em:
- ✅ **ETL** (Extract, Transform, Load)
- ✅ **Análise Exploratória de Dados**
- ✅ **Storytelling com Dados**
- ✅ **Business Intelligence**
- ✅ **Visualização de Dados**

---

