# Bank Transactions Analysis with PySpark

Projeto simples de análise de transações bancárias utilizando PySpark.

A ideia do projeto foi praticar manipulação e análise de dados em um cenário parecido com o contexto financeiro, trabalhando com transações, agrupamentos e identificação de movimentações suspeitas.

---

# Tecnologias utilizadas

- Python
- PySpark
- Pandas
- Jupyter Notebook

---

# Objetivos do projeto

- Ler e tratar dados com PySpark
- Fazer análises básicas de transações
- Criar alguns indicadores simples
- Identificar transações suspeitas
- Praticar processamento de dados em maior escala

---

# Estrutura do projeto

```text
bank-transactions-pyspark/
│
├── data/
│   └── transactions.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── output/
│   └── suspicious_transactions.csv
│
├── requirements.txt
│
└── README.md
```

---

# Análises realizadas

Durante o projeto foram feitas análises como:

- quantidade de transações por cliente
- total gasto por cliente
- média de gastos
- identificação de transações acima de R$5000

---

# Exemplo de análise

```python
client_expenses = df.groupBy("client_id") \
    .agg(sum("value").alias("total_expenses")) \
    .orderBy(col("total_expenses").desc())
```

---

# Possíveis melhorias futuras

- adicionar dashboard em Power BI
- utilizar Machine Learning para fraude
- trabalhar com dados em tempo real
- criar análises mais avançadas de comportamento

---

# Como executar

## Instalar dependências

```bash
pip install -r requirements.txt
```

---

## Abrir o notebook

```bash
jupyter notebook
```

Abrir:

```text
notebooks/analysis.ipynb
```

---

# O que aprendi

Com esse projeto consegui praticar:

- manipulação de dados com PySpark
- agrupamentos e agregações
- limpeza de dados
- análise exploratória
- identificação de padrões simples em transações

Além disso, consegui entender melhor como ferramentas como PySpark podem ser utilizadas em contextos com grandes volumes de dados, como no setor bancário.