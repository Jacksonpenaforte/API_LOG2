# 📄 Compilação de Dados – Importação e Exportação Nacional
**Data de criação:** 15/09/2025  
**Última atualização:** 10/11/2025  
**Autores:** Jackson Penaforte e Vitor Amaral  

---

```python
# Importa a biblioteca necessária
import pandas as pd

# Monta o Google Drive para acessar os arquivos
from google.colab import drive
drive.mount('/content/drive')

# Define o caminho da pasta onde estão os arquivos de dados
origem = '/content/drive/MyDrive/api_python/exportcao_importacao/'

# Define os caminhos dos arquivos CSV
arq_1 = origem + 'EXP_2023.csv'
arq_2 = origem + 'IMP_2023.csv'
arq_3 = origem + 'EXP_2024.csv'
arq_4 = origem + 'IMP_2024.csv'
arq_5 = origem + 'EXP_2025.csv'
arq_6 = origem + 'IMP_2025.csv'
ncm = origem + 'NCM.csv'
país = origem + 'PAIS.csv'
via = origem +'VIA.csv'
urf = origem + 'URF.csv'
uf_m = origem + 'UF_MUN.csv'
uf = origem + 'UF.csv'
sh = origem + 'NCM_SH.csv'

# Lê os arquivos de exportação e importação
exp23 = pd.read_csv(arq_1, low_memory=False, sep=';', encoding='UTF-8')
imp23 = pd.read_csv(arq_2, low_memory=False, sep=';', encoding='UTF-8')
exp24 = pd.read_csv(arq_3, low_memory=False, sep=';', encoding='UTF-8')
imp24 = pd.read_csv(arq_4, low_memory=False, sep=';', encoding='UTF-8')
exp25 = pd.read_csv(arq_5, low_memory=False, sep=';', encoding='UTF-8')
imp25 = pd.read_csv(arq_6, low_memory=False, sep=';', encoding='UTF-8')

# Lê tabelas auxiliares de referência
NCM = pd.read_csv(ncm, low_memory=False, sep=';', encoding='latin1')
PAÍS = pd.read_csv(país, low_memory=False, sep=';', encoding='latin1')
VIA = pd.read_csv(via, low_memory=False, sep=';', encoding='latin1')
URF = pd.read_csv(urf, low_memory=False, sep=';', encoding='latin1')
UF_MUN = pd.read_csv(uf_m, low_memory=False, sep=';', encoding='latin1')
UF = pd.read_csv(uf, low_memory=False, sep=';', encoding='latin1')
SH = pd.read_csv(sh, low_memory=False, sep=';', encoding='latin1')

# Une dados de exportação de 2023 a 2025
finalexp = pd.concat([exp23, exp24, exp25], ignore_index=True)

# Adiciona descrições de códigos e informações geográficas
finalexp = finalexp.merge(NCM[['CO_NCM','NO_NCM_POR']], on='CO_NCM', how='left')
finalexp = finalexp.merge(PAÍS[['CO_PAIS','NO_PAIS']], on='CO_PAIS', how='left')
finalexp = finalexp.merge(URF[['CO_URF','NO_URF']], on='CO_URF', how='left')
finalexp = finalexp.merge(VIA[['CO_VIA','NO_VIA']], on='CO_VIA', how='left')
finalexp = finalexp.merge(UF[['CO_UF','NO_UF','SG_UF']], left_on='SG_UF_NCM', right_on='SG_UF', how='left')

# Une dados de importação de 2023 a 2025
finalimp = pd.concat([imp23, imp24, imp25], ignore_index=True)

# Adiciona descrições e informações regionais
finalimp = finalimp.merge(NCM[['CO_NCM','NO_NCM_POR']], on='CO_NCM', how='left')
finalimp = finalimp.merge(PAÍS[['CO_PAIS','NO_PAIS']], on='CO_PAIS', how='left')
finalimp = finalimp.merge(UF[['CO_UF','NO_UF', 'SG_UF']], left_on='SG_UF_NCM', right_on='SG_UF', how='left')
finalimp = finalimp.merge(VIA[['CO_VIA','NO_VIA']], on='CO_VIA', how='left')

# Visualiza as últimas linhas dos dados tratados
finalimp.tail(5)

# Exporta os arquivos finais limpos
finalexp.to_csv(origem + 'finalexp.csv', index=False)
finalimp.to_csv(origem + 'finalimp.csv', index=False)
```
