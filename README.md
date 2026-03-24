# 🌌 AstroQuant-BTC: Pipeline de Big Data & Deep Learning para Criptoativos

## 📝 Descrição do Projeto

Este projeto implementa um pipeline de Engenharia de Dados de alta performance e um modelo de Deep Learning (LSTM) para a previsão e análise estratégica do Bitcoin (BTC-USD). O diferencial desta implementação é a utilização do motor DuckDB para processamento analítico em escala, superando as limitações de memória do Pandas através de SQL avançado.A abordagem trata o mercado financeiro como um sistema dinâmico complexo, aplicando filtros de sinal e memória de longo prazo para capturar tendências não-lineares.

## 🛠️ Stack TecnológicaData Engineering: 
### DuckDB (SQL Avançado: Window Functions, CTEs).
### Deep Learning: TensorFlow/Keras (Redes Neurais Recorrentes LSTM).
### Data Analysis: Pandas, NumPy, Scikit-Learn.
### Visualization: Matplotlib, Seaborn.
### Data Source: Yahoo Finance API (yfinance).

## 🔬 Diferenciais Técnicos
1. SQL Analítico com DuckDB: Em vez de processar indicadores técnicos em Python, utilizamos o DuckDB para realizar cálculos de RSI (Relative Strength Index) e Bandas de Bollinger diretamente no banco de dados via SQL. Isso demonstra competência em ferramentas de Modern Data Stack e otimização de performance.
2. Arquitetura Multimodal LSTM: O modelo foi treinado utilizando uma janela deslizante (Sliding Window) de 60 dias, processando vetores multimodais (Preço de Fechamento + RSI). A camada de Dropout foi estrategicamente inserida para evitar o overfitting, garantindo que a rede aprenda a tendência física do ativo e ignore o ruído estatístico.

## 📊 Resultados e Visualizações

### 📉 Previsão da Rede Neural vs. Dados Reais: 

O gráfico abaixo ilustra a capacidade da LSTM de seguir a tendência do mercado, capturando os ciclos de alta e baixa com alta fidelidade.

<img width="1190" height="630" alt="image" src="https://github.com/user-attachments/assets/c4d820f4-a369-45d4-8b9e-cbfb795dd9fa" />


### ⚖️ Backtesting da Estratégia: 

A validação experimental através do backtesting compara o retorno acumulado de um investimento passivo (Buy & Hold) contra as decisões de compra/venda sugeridas pela IA.

<img width="977" height="528" alt="image" src="https://github.com/user-attachments/assets/ae6b7ba8-3050-4970-b08b-6d457430f00c" />


## 📈 Conclusões

Convergência: O modelo apresentou uma perda (MSE) na ordem de $10^{-4}$, indicando um ajuste preciso aos padrões históricos.

Sinal vs Ruído: A integração do RSI via SQL funcionou como um filtro de momento, melhorando a assertividade das entradas em comparação com modelos puramente baseados em preço.

Eficiência: O uso do DuckDB reduziu drasticamente o tempo de processamento de indicadores técnicos, provando ser uma ferramenta essencial para análise de Big Data local.


🚀 Como Executar

Clone o repositório: git clone https://github.com/seu-usuario/astroquant-btc.git

Instale as dependências: pip install -r requirements.txt

Execute o notebook: jupyter notebook AstroQuant_BTC.ipynb

#### Desenvolvido por Gabriel Sales - Estudante PhD em Física UFU.
