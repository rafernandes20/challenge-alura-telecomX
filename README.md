📊 Telecom X — Análise de Evasão de Clientes (Churn)
📌 Visão Geral

Este projeto tem como objetivo analisar os fatores associados à evasão de clientes (Churn) na Telecom X.

A empresa enfrenta uma taxa relevante de cancelamentos e precisa entender quais características dos clientes e do serviço contratado estão mais associadas à saída da base.

A partir dessa análise exploratória, são gerados insights estratégicos que podem apoiar ações de retenção e o desenvolvimento de modelos preditivos de churn.

🎯 Objetivos do Projeto

Importar dados em formato JSON via API (GitHub RAW)

Realizar tratamento e limpeza dos dados (ETL)

Conduzir uma Análise Exploratória de Dados (EDA)

Identificar os principais fatores associados ao churn

Gerar recomendações estratégicas baseadas em dados

🛠 Tecnologias Utilizadas

Python 3

Pandas

NumPy

Matplotlib

Google Colab

📂 Estrutura do Projeto
TelecomX-Churn/
│
├── TelecomX_Data.json
├── TelecomX_Churn_Analysis.ipynb
└── README.md
🔄 Processo Realizado
1️⃣ Extração de Dados (E)

Dados carregados diretamente do arquivo JSON via URL pública.

Conversão para DataFrame utilizando pd.json_normalize().

2️⃣ Tratamento e Limpeza (T)

Foram realizados os seguintes ajustes:

Verificação de valores ausentes

Checagem e remoção de duplicados

Correção de tipo da variável Total Charges

Conversão do target Churn para variável binária (1 = Cancelou, 0 = Ativo)

Padronização de colunas

Criação da variável adicional:

Contas_Diarias = Monthly Charges / 30
3️⃣ Análise Exploratória (EDA)
📊 Taxa Geral de Churn

26,6% da base cancelou o serviço.

📈 Principais Variáveis Numéricas

Tenure (tempo de permanência)

Clientes churn permanecem em média ~18 meses.

Clientes ativos permanecem ~38 meses.

Clientes com até 6 meses apresentam churn superior a 50%.

Monthly Charges

Clientes que churnam pagam mensalidades maiores em média.

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

🔎 Principais Insights

O tempo de relacionamento é o principal fator associado à evasão.

Contratos mensais são significativamente mais arriscados.

Pagamentos não automáticos estão fortemente ligados ao churn.

Clientes com mensalidade mais alta apresentam maior probabilidade de cancelamento.

O perfil Senior Citizen merece atenção específica.

💡 Recomendações Estratégicas

Foco em retenção nos primeiros 6 meses.

Incentivar migração de contrato mensal para anual.

Oferecer benefícios para adesão ao pagamento automático.

Desenvolver estratégias específicas para clientes idosos.

Avaliar percepção de valor para planos com mensalidade elevada.

🚀 Próximos Passos

Feature Engineering para modelagem

One-Hot Encoding de variáveis categóricas

Construção de modelo preditivo (Logistic Regression / Random Forest)

Criação de score de risco de churn
