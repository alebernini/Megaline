# Megaline – Análise de Planos de Telefonia Pré-Pagos

Este projeto tem como objetivo realizar uma análise de dados da empresa de telecomunicações **Megaline**, que oferece dois planos pré-pagos: **Surf** e **Ultimate**. A equipe comercial busca entender qual dos planos gera mais receita para otimizar o orçamento de publicidade.

## 🧾 Descrição do Projeto

Analisamos o comportamento de **500 clientes** com base em dados de chamadas, mensagens e uso de internet ao longo de 2018. A análise envolve:

- Limpeza e preparação dos dados;
- Cálculo da receita mensal por usuário;
- Estatísticas descritivas do uso dos planos;
- Visualizações para compreensão do comportamento dos usuários;
- Testes estatísticos para validar hipóteses sobre a receita dos planos e regiões.

## 💡 Objetivo

Determinar, com base em evidências estatísticas, **qual plano (Surf ou Ultimate) gera mais receita em média**, além de explorar padrões de uso entre diferentes regiões.

## 📦 Dados Utilizados

Os dados estão organizados em cinco arquivos CSV:

- `megaline_users.csv`: informações cadastrais dos usuários
- `megaline_calls.csv`: dados sobre chamadas realizadas
- `megaline_messages.csv`: dados sobre mensagens enviadas
- `megaline_internet.csv`: dados de uso da internet
- `megaline_plans.csv`: detalhes dos planos Surf e Ultimate

## 📝 Descrição dos Planos

### Surf

- 💵 Preço mensal: $20  
- Inclui: 500 min, 50 SMS, 15 GB  
- Excedente:  
  - Minuto: $0.03  
  - SMS: $0.03  
  - GB adicional: $10  

### Ultimate

- 💵 Preço mensal: $70  
- Inclui: 3.000 min, 1.000 SMS, 30 GB  
- Excedente:  
  - Minuto: $0.01  
  - SMS: $0.01  
  - GB adicional: $7  

> Obs: chamadas são arredondadas para cima a cada minuto. O tráfego web mensal é arredondado para cima em GB.

## ⚙️ Etapas do Projeto

### 1. Preparação dos Dados

- Conversão de tipos de dados
- Tratamento de valores ausentes e inconsistências
- Agregação mensal do uso por usuário

### 2. Cálculo da Receita

Para cada usuário, foi calculada a **receita mensal**, somando:
- Cobranças por uso excedente (minutos, mensagens, dados)
- Preço fixo mensal do plano

### 3. Análise Exploratória

- Estatísticas descritivas (média, desvio padrão, variância)
- Histogramas de uso e receita
- Comparação entre planos e regiões

### 4. Teste de Hipóteses

- **Hipótese 1:** A receita média entre usuários dos planos Ultimate e Surf é diferente.
- **Hipótese 2:** A receita média de usuários da área NY-NJ é diferente da dos demais.

## 📊 Principais Ferramentas

- `pandas`, `numpy` – manipulação de dados
- `matplotlib`, `seaborn` – visualizações
- `scipy.stats` – testes estatísticos

## 📁 Estrutura do Projeto

📦 Megaline
├── 📁 data/
│ ├── megaline_calls.csv
│ ├── megaline_messages.csv
│ ├── megaline_internet.csv
│ ├── megaline_users.csv
│ └── megaline_plans.csv
├── 📄 README.md
└── 📄 megaline_analysis.ipynb


## ✅ Status do Projeto

🟢 **Concluído** – A análise foi realizada com sucesso, e as conclusões podem orientar decisões estratégicas sobre publicidade e alocação de recursos. 
Na análise dos dados comparando os dois planos Ultimate e Surf foi identificado que: 
• A quantidade de chamadas é maior para o plano Surf em todos os meses do ano, sendo a maior em janeiro. Nos últimos quatro meses do anos, essa diferença se torna menor; 
• A quantidade mínima que os usuários necessitam é bem maior em Surf do que em Ultimate;
• A média de duração de chamadas está entre 400-500;
• A duração das chamadas em Ultimate é maior do que em Surf no primeiro trimestre;
• O volume de tráfico é maior no último trimestre;
• A hipótese nula de que as receitas dos dois planos são iguais foi rejeitada.


