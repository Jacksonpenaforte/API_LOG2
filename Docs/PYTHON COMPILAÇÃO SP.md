# 📄 Compilação de Dados - 
**Data de criação:** 03/04/2026  
**Última atualização:** 17/04/26 
**Autores:** Jackson Penaforte e Marcelo R. Osako 

---

```python
# Importa a biblioteca necessária

import pandas as pd

# Monta o Google Drive para acessar os arquivos

from google.colab import drive
drive.mount('/content/drive')

# Define o caminho da pasta e o nome do arquivo CSV, onde estão os arquivos de dados

origem = '/content/drive/MyDrive/logteam/'
arq = origem + 'Transporte_de_Produtos_Quimicos_Perigosos_ou_Combustíveis..csv'

# Transforma todos os textos de todas as colunas em letras MAIÚSCULAS.

df = df.applymap(lambda s: s.upper() if type(s) == str else s)

#  Limpeza de Dados Numéricos

Aqui você resolve o problema de formatação brasileira (onde milhar é ponto e decimal é vírgula) para que o Python entenda o valor como um número real.
Remove pontos de milhar, substitui a vírgula decimal por ponto e converte a coluna para o tipo numérico (float).
df['Quantidade Transportada'] = (df['Quantidade Transportada'].str.replace('.', '', regex=False).str.replace(',', '.', regex=False).astype(float)

#  Exibe as 6 primeiras linhas do dataframe para conferência.

df.head(6)

# Conversão de Unidades (Metros Cúbicos para Litros)

Para manter a consistência, você identifica quem está em "Metros" e converte para "Litros".
Cria um filtro (máscara) para encontrar linhas onde a unidade de medida contém a palavra "METRO".
mask_metros = df['Unidade de Medida'].str.contains('METRO', na=False)

Multiplica por 1000 a quantidade das linhas filtradas (1 m³ = 1000L).
df.loc[mask_metros, 'Quantidade Transportada'] *= 1000

Altera o nome da unidade para "LITROS" nessas mesmas linhas.
df.loc[mask_metros, 'Unidade de Medida'] = 'LITROS'

# Filtragem por Produto e Tempo

Nesta etapa, você reduz o volume de dados apenas para o que te interessa (combustíveis específicos e anos recentes).
Filtra o dataframe para manter apenas os produtos que contenham as palavras-chave de combustíveis.
df_filtrado = df[df['Produto'].str.contains('GASOLINA|ETANOL|DIESEL|GLP|COMBUSTIVEIS', na=False)]

Converte a coluna 'Ano' para números, transformando erros em valores nulos (NaN).
df_filtrado['Ano'] = pd.to_numeric(df_filtrado['Ano'], errors='coerce')

Mantém no dataframe apenas os registros do ano de 2013 em diante.
df_filtrado = df_filtrado[df_filtrado['Ano'] >= 2013]

# Organização Final e Exportação

Você organiza os dados cronologicamente e salva o resultado final.
Ordena a tabela pelo ano, do mais antigo para o mais recente.
df_filtrado = df_filtrado.sort_values(by='Ano', ascending=True)

Redefine os números das linhas (índice) para que comecem do zero em sequência.
df_filtrado = df_filtrado.reset_index(drop=True)

Exibe as últimas 5 linhas do resultado final.
df_filtrado.tail(5)

Exibe informações técnicas da tabela (tipos de dados, memória usada, valores nulos).
df_filtrado.info()

Salva o dataframe limpo e filtrado em um novo arquivo CSV no seu Drive.
df_filtrado.to_csv(origem+'Planilha_Limpa_Filtrada.csv', index=False)

```
