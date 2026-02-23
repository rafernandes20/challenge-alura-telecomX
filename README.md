📊 Telecom X — Análise de Evasão de Clientes (Churn)
📌 Sobre o Projeto

Este projeto tem como objetivo analisar os fatores associados à evasão de clientes (Churn) na Telecom X.

A empresa enfrenta uma taxa relevante de cancelamentos e precisa entender quais características dos clientes e dos serviços contratados estão mais associadas à saída da base.

A partir de uma análise exploratória estruturada, foram identificados padrões comportamentais e operacionais que podem apoiar estratégias de retenção e o desenvolvimento de modelos preditivos.

🎯 Objetivos

Importar dados em formato JSON via API (GitHub RAW)

Aplicar processo de ETL (Extração, Transformação e Limpeza)

Realizar Análise Exploratória de Dados (EDA)

Identificar os principais fatores associados ao churn

Gerar recomendações estratégicas baseadas em dados

🛠 Tecnologias Utilizadas

Python 3

Pandas

NumPy

Matplotlib

Seaborn

Google Colab

🔄 Processo Analítico
1️⃣ Extração de Dados

Dados carregados diretamente do arquivo JSON disponibilizado via GitHub.

Conversão para DataFrame utilizando pd.json_normalize().

2️⃣ Limpeza e Tratamento

Foram realizadas as seguintes etapas:

Verificação de valores ausentes

Checagem e remoção de duplicados por customerID

Conversão da variável account.Charges.Total para formato numérico

Transformação da variável Churn para formato binário (1 = Cancelou | 0 = Ativo)

Padronização de colunas

Criação da variável derivada:

Contas_Diarias = account.Charges.Monthly / 30
3️⃣ Análise Exploratória (EDA)
📊 Taxa Geral de Churn

26,6% dos clientes cancelaram o serviço.

73,4% permanecem ativos.

📈 Variáveis Numéricas

Tenure (tempo de permanência)

Clientes churn: média ~18 meses

Clientes ativos: média ~38 meses

Faixa 0–6 meses apresenta churn superior a 50%

Monthly Charges

Clientes que cancelam pagam mensalidades maiores em média.

Total Charges

Clientes ativos apresentam maior valor acumulado (efeito direto do maior tempo de permanência).

📊 Variáveis Categóricas

Tipo de Contrato

Month-to-month → ~43% churn

One year → ~11%

Two year → ~2,8%

Método de Pagamento

Electronic check → ~45% churn

Pagamentos automáticos → ~15–17%

Senior Citizen

Clientes idosos apresentam churn significativamente maior (~41%).

Gênero

Diferença irrelevante.

4️⃣ Análise Avançada (Extra)
🔎 Correlação

Tenure possui a maior correlação negativa com churn (-0,35).

Cobrança mensal apresenta correlação positiva moderada (~0,19).

Observada alta colinearidade entre variáveis financeiras (Monthly, Total e Contas_Diarias).

📡 Engajamento — Quantidade de Serviços

Foi criada a variável Qtd_Servicos, representando o número de serviços contratados.

Resultado:

Clientes com poucos serviços apresentam maior churn (~44%).

Clientes com 7–8 serviços apresentam churn muito baixo (~5–12%).

📌 Insight:
Clientes mais engajados com o portfólio tendem a permanecer mais tempo na base.

🔎 Principais Insights

O tempo de relacionamento é o principal fator associado à evasão.

Contratos mensais são significativamente mais instáveis.

Pagamentos não automáticos apresentam maior risco.

Clientes com mensalidades mais altas tendem a churnar mais.

Maior engajamento (mais serviços) reduz significativamente o churn.

💡 Recomendações Estratégicas

Foco em retenção nos primeiros 6 meses.

Incentivar migração para contratos anuais.

Estimular adesão ao pagamento automático.

Desenvolver estratégias específicas para clientes idosos.

Criar políticas de cross-sell para aumentar engajamento.

🚀 Próximos Passos

Feature Engineering para modelagem preditiva

One-Hot Encoding de variáveis categóricas

Construção de modelo de churn (Logistic Regression / Random Forest)

Criação de score de risco operacional

📂 Estrutura do Repositório
TelecomX-Churn/
│
├── TelecomX_Churn_Analysis.ipynb
├── TelecomX_Data.json
└── README.md
👩‍💻 Autor

Raquel Fernandes
GitHub: https://github.com/rafernandes20
LinkedIn: https://[linkedin.com/in/raquelfernandes](https://www.linkedin.com/in/raquelafernandes20/)
