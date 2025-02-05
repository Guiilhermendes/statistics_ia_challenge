# README

## Descrição do Projeto

Este projeto consiste na análise de um conjunto de dados de faturamento ao longo de diferentes datas. Utilizamos a biblioteca `pandas` para manipulação e análise dos dados, e a biblioteca `matplotlib` para visualização gráfica.

## Estrutura do Notebook

### Importação de Bibliotecas

```python
import pandas as pd
import matplotlib.pyplot as plt
```

### Criação do Dicionário de Dados

```python
dict_invoice = {
    'data_ref': [
        '2023-01-01', 
        '2020-02-01', 
        '2021-03-01', 
        '2022-04-01', 
        '2023-05-01',
        '2023-06-01', 
        '2020-07-01', 
        '2021-08-01', 
        '2022-09-01', 
        '2023-10-01',
        '2022-11-01', 
        '2023-12-01',
        ],
    'valor': [
        400000, 
        890000, 
        760000, 
        430000, 
        920000,
        340000, 
        800000, 
        500000, 
        200000, 
        900000,
        570000, 
        995000,
        ]
}
```

### Criação do DataFrame

```python
df_invoice = pd.DataFrame.from_dict(dict_invoice)
```

### Visualização do DataFrame

```python
df_invoice
```

### Cálculo da Média dos Valores

```python
round(df_invoice.valor.mean(), 2)
```

### Gráficos

#### Gráfico de Barras

```python
df_invoice.plot.bar(x='data_ref', y='valor')
```

#### Gráfico de Linhas

```python
df_invoice.plot.line(x='data_ref', y='valor')
```

## Variáveis Presentes

- **df_invoice**: DataFrame do pandas contendo os dados de faturamento.
- **dict_invoice**: Dicionário contendo os dados de faturamento.

## Conclusão

Este notebook fornece uma análise básica dos dados de faturamento, incluindo a visualização gráfica e o cálculo da média dos valores. As bibliotecas `pandas` e `matplotlib` foram utilizadas para manipulação e visualização dos dados, respectivamente.
