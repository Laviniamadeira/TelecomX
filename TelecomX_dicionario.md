# 📚 Dicionário de Dados - TelecomX

## 📋 Informações Gerais
- **Total de Variáveis**: 22 campos
- **Registros**: 7.267 clientes únicos
- **Período**: Dados históricos de clientes
- **Tipo**: Dataset de telecomunicações para análise de churn

---

## 🔍 Variáveis do Dataset

### 🆔 **Identificação**
| Variável | Nome Original | Tipo | Descrição Detalhada |
|----------|---------------|------|---------------------|
| `id_cliente` | `customerID` | Texto | Código único de identificação de cada cliente (ex: "0002-ORFBO") |

### 🎯 **Variável Target (Objetivo)**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `cancelamento` | `Churn` | Binária | Se o cliente cancelou os serviços da empresa | 0 = Cliente Ativo<br>1 = Cliente Cancelou |

### 👤 **Informações Demográficas**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `genero` | `gender` | Binária | Gênero do cliente | 0 = Feminino<br>1 = Masculino |
| `idoso` | `SeniorCitizen` | Binária | Se o cliente tem 65 anos ou mais | 0 = Não é idoso<br>1 = É idoso (65+) |
| `possui_conjuge` | `Partner` | Binária | Se o cliente possui cônjuge/parceiro(a) | 0 = Não possui<br>1 = Possui |
| `possui_dependentes` | `Dependents` | Binária | Se o cliente possui dependentes (filhos, familiares) | 0 = Não possui<br>1 = Possui |

### 📞 **Serviços de Telefonia**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `servico_telefonico` | `PhoneService` | Binária | Se possui serviço de telefone fixo | 0 = Não possui<br>1 = Possui |
| `multiplas_linhas` | `MultipleLines` | Binária | Se possui mais de uma linha telefônica | 0 = Uma linha ou nenhuma<br>1 = Múltiplas linhas |

### 🌐 **Serviços de Internet**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `servico_internet` | `InternetService` | Categórica | Tipo de conexão de internet contratada | "DSL" = Internet DSL<br>"Fiber optic" = Fibra Óptica<br>"No" = Sem internet |
| `seguranca_online` | `OnlineSecurity` | Binária | Serviço adicional de segurança online (antivírus, firewall) | 0 = Não contratado<br>1 = Contratado |
| `backup_online` | `OnlineBackup` | Binária | Serviço de backup automático na nuvem | 0 = Não contratado<br>1 = Contratado |
| `protecao_dispositivo` | `DeviceProtection` | Binária | Seguro para proteção de dispositivos | 0 = Não contratado<br>1 = Contratado |
| `suporte_tecnico` | `TechSupport` | Binária | Suporte técnico premium com prioridade | 0 = Não contratado<br>1 = Contratado |

### 📺 **Serviços de Streaming**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `tv_streaming` | `StreamingTV` | Binária | Serviço de streaming de TV/canais | 0 = Não contratado<br>1 = Contratado |
| `filmes_streaming` | `StreamingMovies` | Binária | Serviço de streaming de filmes | 0 = Não contratado<br>1 = Contratado |

### 📄 **Informações Contratuais**
| Variável | Nome Original | Tipo | Descrição Detalhada | Valores |
|----------|---------------|------|---------------------|---------|
| `meses_como_cliente` | `tenure` | Numérica | Número de meses que o cliente está na empresa | 0 a 72 meses |
| `tipo_contrato` | `Contract` | Categórica | Duração do compromisso contratual | "Month-to-month" = Mensal<br>"One year" = 1 ano<br>"Two year" = 2 anos |
| `fatura_online` | `PaperlessBilling` | Binária | Se o cliente recebe fatura digital (email) | 0 = Fatura impressa<br>1 = Fatura digital |
| `metodo_pagamento` | `PaymentMethod` | Categórica | Forma como o cliente paga a conta | "Electronic check" = Cheque eletrônico<br>"Mailed check" = Cheque correio<br>"Bank transfer" = Transferência<br>"Credit card" = Cartão crédito |

### 💰 **Informações Financeiras**
| Variável | Nome Original | Tipo | Descrição Detalhada | Unidade |
|----------|---------------|------|---------------------|---------|
| `custo_mensal` | `Charges.Monthly` | Numérica | Valor total pago mensalmente por todos os serviços | R$ (reais) |
| `custo_total` | `Charges.Total` | Numérica | Valor total já pago pelo cliente desde o início | R$ (reais) |

### 🔢 **Métricas Derivadas** *(Criadas durante a análise)*
| Variável | Tipo | Descrição Detalhada | Cálculo |
|----------|------|---------------------|---------|
| `custo_diario` | Numérica | Custo médio diário dos serviços | `custo_mensal / 30` |

---

## 📊 Estatísticas Resumo

### 🎯 **Distribuições Principais**
- **Taxa de Churn**: 25.72% (1.869 de 7.267 clientes)
- **Tempo Médio como Cliente**: 32.3 meses
- **Gasto Mensal Médio**: R$ 64.72
- **Gasto Total Médio**: R$ 2.276.71

### 👥 **Perfil Demográfico**
- **Gênero**: 50.6% masculino, 49.4% feminino
- **Idosos**: 16.3% da base
- **Com Cônjuge**: 48.4%
- **Com Dependentes**: 30.0%

### 📱 **Adoção de Serviços**
- **Telefone**: 90.3% dos clientes
- **Internet**: ~78% dos clientes
- **Streaming TV**: 38.4% dos clientes
- **Streaming Filmes**: 38.8% dos clientes

---

## ⚠️ **Observações Importantes**

### 🔧 **Tratamento de Dados**
- Valores "Yes/No" convertidos para 1/0
- Valores em branco tratados como missing
- Gênero convertido para numérico (Female=0, Male=1)
- Colunas renomeadas para português

### 📈 **Qualidade dos Dados**
- **Completude**: >99% dos campos preenchidos
- **Consistência**: Dados validados e limpos
- **Atualidade**: Snapshot histórico representativo
- **Relevância**: Todas as variáveis impactam o negócio

### 🎯 **Uso Recomendado**
- ✅ Análise de churn e retenção
- ✅ Segmentação de clientes
- ✅ Modelagem preditiva
- ✅ Análise de receita
- ❌ Não usar para identificação pessoal (dados anonimizados)

---
