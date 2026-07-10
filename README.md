# 📊 Mini Pipeline de Análise de Dados — Vendas

Projeto de estudo criado para praticar conceitos de **ETL (Extract, Transform, Load)** utilizando **Python** e **Pandas**, simulando um cenário simples de análise de vendas de uma loja.

## 🎯 Objetivo

Demonstrar, de forma didática, como estruturar um pipeline de dados básico:

1. **Extract** — criação/leitura dos dados brutos (com valores propositalmente faltantes, simulando dados "sujos")
2. **Transform** — limpeza, tratamento de nulos, ajuste de tipos e criação de novas colunas
3. **Load** — exportação dos dados tratados e das análises geradas

## 🛠️ Tecnologias utilizadas

- Python 3
- Pandas
- NumPy

## 📁 Estrutura

```
.
├── pipeline_vendas.py              # Script principal do pipeline
├── vendas_tratadas.csv             # Gerado após a execução
├── faturamento_por_categoria.csv   # Gerado após a execução
└── README.md
```

## ⚙️ O que o script faz

- Cria um dataset fictício de vendas com valores nulos em algumas colunas (produto, preço e quantidade)
- Identifica e trata os valores faltantes de formas diferentes conforme o contexto:
  - Remove registros sem identificação do produto
  - Preenche preços faltantes com a média do respectivo produto (`groupby` + `transform`)
  - Preenche quantidades faltantes com um valor padrão conservador
- Corrige tipos de dados (datas e inteiros)
- Cria a coluna `valor_total` (preço × quantidade)
- Gera análises agregadas:
  - Faturamento total por categoria
  - Quantidade vendida por produto
  - Ticket médio das vendas
- Exporta os resultados tratados em arquivos `.csv`

## ▶️ Como executar

```bash
# Instalar dependências
pip install pandas numpy

# Rodar o script
python pipeline_vendas.py
```

## 📌 Observações

Este é um projeto de estudo com dados fictícios, criado para fixar conceitos fundamentais de manipulação e limpeza de dados com Pandas — como tratamento de valores nulos, agregações e agrupamentos — aplicáveis a cenários reais de pipelines de análise de dados.

## 👤 Autora

Desenvolvido por Laís como parte de estudos para processos seletivos na área de Desenvolvimento de Software / Análise de Dados.