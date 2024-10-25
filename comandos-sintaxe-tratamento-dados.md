## Comandos e sintaxe importantes para o tratamento de dados

### **Comando: Importar a biblioteca Pandas** - 
- Para manipulação e análise de dados.
  
import pandas as pd 

### **Comando: Import a biblioteca SQlite**
- Para conexão e manipulação de bancos de dados SQLite

import sqlite3 as sl3

### **Usar o comando "connect" da biblioteca sqlite3 para conectar ao banco de dados e guarde a conexão dentro da variável "conn"**
conn = sqlite3.connect( "database.db" )

conn = sl3.connect( "database.db" )

### **Coletando os dados**
- Seleciona todas as colunas da tabela flight_activity e realiza um join à esquerda com a tabela flight_loyalty_history com base na coluna loyalty_number.
  
consulta_atividade = """

SELECT *
FROM flight_activity fa

LEFT JOIN flight_loyalty_history flh

ON (fa.loyalty_number = flh.loyalty_number)

"""

### **Executando a consulta**

df_atividade = pd.read_sql_query(consulta_atividade, conn)

### **Comando do Pandas para selecionar linhas e colunas**

df = df1.iloc[linhas, colunas]

### **selecionando colunas de uma planilha** 
colunas = ['year', 'month', 'flights_booked',
'flights_with_companions', 'total_flights',
'distance', 'points_accumulated',
'points_redeemed', 'dollar_cost_points_redeemed',
'salary', 'clv', 'enrollment_year',
'enrollment_month', 'loyalty_card']

df_dados_limpos = df_atividade.loc[:, colunas]

### **Selecionando linhas de uma planilha**
linhas = ~df_atividade['salary'].isna()

df_dados_limpos = df_atividade.loc[linhas, colunas]

### **Verificando o numero de linhas vazias**
df_dados_limpos.isna().sum()

### **Verificando a quantidade de linhas**
numero_linhas = df_atividade.shape[0]

print( 'O numero de linhas eh:', numero_linhas )

### **Verificando a quantidade de colunas**
numero_colunas = df_atividade.shape[1]

print( 'O numero de linhas eh:', numero_linhas )

### **Descobrindo as informaçõess gerais sobre a planilha de dados**
df_atividade.info()

### **Somar a colunas "total_flights"**
df_atividade.loc[:, 'total_flights'].sum()

### **Somar a colunas "distance"**
df_atividade.loc[:, 'distance'].mean()

### **Valor mínimo de salário**
df_atividade.loc[:, 'distance'].min()

### **Valor máximo de salário**
df_atividade.loc[:, 'distance'].max()

### **Checando o número de dados faltante nas colunas**
df_atividade.isna().sum()


