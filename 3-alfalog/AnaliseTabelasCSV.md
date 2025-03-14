# Arquivos
### exportação/importação por município (Arquivos: EXP_COMPLETA_MUN.csv/IMP_COMPLETA_MUN.csv)

- <span style="color: green;">**CO_ANO**: Ano</span>
- <span style="color: green;">**CO_MES**: Mês</span>
- **SH4**: Código para classificação de mercadorias no comércio exterior
- <span style="color: green;">**CO_PAIS**: Código do país de destino/origem do produto</span>
- <span style="color: green;">**SG_UF_MUN**: Código da UF de origem/destino do produto</span>
- **CO_MUN**: Código do município da empresa declarante (município onde a empresa está registrada ou onde exerce suas atividades)
- <span style="color: green;">**KG_LIQUIDO**: Quilograma líquido (peso do produto puro, sem a embalagem)</span>
- <span style="color: green;">**VL_FOB**: Valor da mercadoria em dólares americanos antes do transporte internacional e dos custos adicionais relacionados ao frete</span>

### exportação/importação por NCM (Arquivo: EXP_COMPLETA.csv e IMP_COMPLETA.csv)

- <span style="color: green;">**CO_ANO**: Ano</span>
- <span style="color: green;">**CO_MES**: Mês</span>
- **CO_NCM**: Código NCM (Nomenclatura Comum do Mercosul)
- **CO_UNID**: Códigoo da unidade estatística, como quilogramas, unidades, metros, entre outros
- <span style="color: green;">**CO_PAIS**: Código do País de destino/origem do produto</span>
- <span style="color: green;">**SG_UF_NCM**: Código da UF de origem/destino do produto</span>
- **CO_VIA**: Meio de transporte utilizado
- **CO_URF**: Código da URF de embarque/desembarque (Alfândega ou um posto da Receita Federal)
- **QT_ESTAT**: Quantidade estatística (Quantidade de mercadoria envolvida na transação)
- <span style="color: green;">**KG_LIQUIDO**: Quilograma líquido (peso do produto puro)
- <span style="color: green;">**VL_FOB**: Valor da mercadoria em dólares americanos</span>
- <span style="color: yellow;">**VL_FRETE**: Valor do Frete (Exclusivo para importação)</span>
- <span style="color: yellow;">**VL_SEGURO**: Valor do Seguro (Exclusivo para importação)</span>

### Códigos SH4 e SH6 (Arquivo: NCM_SH.csv)

- <span style="color: green;">**CO_SH6**: Código SH (Sistema Harmonizado) de 6 dígitos (Código possível de ser relacionado com os dados do arquivo NCM.csv)</span>
- **NO_SH6_POR**: Descrição da mercadoria
- **NO_SH6_ESP**: Descrição da mercadoria
- **NO_SH6_ING**: Descrição da mercadoria
- <span style="color: green;">**CO_SH4**: Código SH (Sistema Harmonizado) de 4 dígitos (Código possível de ser relacionado com os dados dos arquivos EXP_COMPLETA_MUN.csv e IMP_COMPLETA_MUN.csv)</span>
- <span style="color: green;">**NO_SH4_POR**: Descrição da mercadoria</span>
- **NO_SH4_ESP**: Descrição da mercadoria 
- **NO_SH4_ING**: Descrição da mercadoria
- **CO_SH2**: Código não usado
- **NO_SH2_POR**: Descrição da mercadoria
- **NO_SH2_ESP**: Descrição da mercadoria
- **NO_SH2_ING**: Descrição da mercadoria
- **CO_NCM_SECROM**: Código não usado
- **NO_SEC_POR**: Descrição da mercadoria
- **NO_SEC_ESP**: Descrição da mercadoria
- **NO_SEC_ING**: Descrição da mercadoria

Obs: SH é igual ao NCM, porém o número do SH define quantos dígitos foram utilizados. Ex: NCM = 49011000, SH6 = 490110, SH4 = 4901

### Código NCM (Arquivo: NCM.csv)

- <span style="color: green;">**CO_NCM**: Código NCM (Nomenclatura Comum do Mercosul)</span>
- **CO_UNID**: Códigoo da unidade estatística, como quilogramas, unidades, metros, entre outros.
- <span style="color: green;">**CO_SH6**: Código SH6 (Sistema Harmonizado), código de 6 dígitos utilizado de base para a formação do NCM.</span>
- **CO_PPE**: Pauta de Produtos Exportados
- **CO_PPI**: Pauta de Produtos Importados
- **CO_FAT_AGREG**: Código de Fator Agregado
- **CO_CUCI_ITEM**:  Classificação Uniforme do Comércio Internacional
- **CO_CGCE_N3**: Classificação por Grandes Categorias Econômicas
- **CO_SIIT**: Código do Sistema Internacional de Identificação de Tributos
- **CO_ISIC_CLASSE**: Código da classificação Internacional Padrão por Atividade Econômica
- **CO_EXP_SUBSET**: ??
- <span style="color: green;">**NO_NCM_POR**: Descrição da mercadoria</span>
- **NO_NCM_ESP**: Descrição da mercadoria
- **NO_NCM_ING**: Descrição da mercadoria

### Países (Arquivo: PAIS.csv)

- <span style="color: green;">**CO_PAIS**: Código do País</span>
- **CO_PAIS_ISON3**: Código do País em ISO 3166-1
- **CO_PAIS_ISOA3**: Código do País em ISO 3166-1 (Alfa-3) (Sigla do país)
- <span style="color: green;">**NO_PAIS**: Nome do País</span>
- **NO_PAIS_ING**: Nome do País em Inglês 
- **NO_PAIS_ESP**: Nome do País em Espanhol

### Unidade Federativa (Arquivo: UF.csv)

- <span style="color: green;">**CO_UF**: Código da Unidade da Federação</span>
- <span style="color: green;">**SG_UF**: Sigla da Unidade da Federação</span>
- <span style="color: green;">**NO_UF**: Nome da Unidade da Federação</span>
- **NO_REGIAO**: Nome da região geográfica do Brasil

### Município (Arquivo: UF_MUN.csv)

- <span style="color: green;">**CO_MUN_GEO**: Código do Município</span>
- **NO_MUN**: Nome do Município (Letras Maiúsculas)
- <span style="color: green;">**NO_MUN_MIN**: Nome do Município (Letras Maiúsculas e Minúsculas)</span>
- **SG_UF**: Sigla da Unidade da Federação

### Códigoo da unidade estatística (Arquivo: NCM_UNIDADE.csv)

- <span style="color: green;">**CO_UNID**: Códigoo da unidade estatística</span>
- **NO_UNID**: Nome da unidade de medida
- <span style="color: green;">**SG_UNID**: Abreviação da unidade de medida</span>

# Entidades

### NCM_SH
- **CO_NCM**: int PK
- **CO_SH6**: int
- **CO_SH4**: int
- **CO_UNID**: int FK
- **NO_NCM_POR**: varchar

### PAISES
- **CO_PAIS**: int PK
- **NO_PAIS**: varchar

### UF
- **CO_UF**: int PK
- **SG_UF**: varchar
- **NO_UF**: varchar

### MUNICIPIO
- **CO_MUN_GEO**: int PK
- **NO_MUN**: varchar

### UNIDADE
- **CO_UNID**: int PK
- **SG_UNID**: varchar










