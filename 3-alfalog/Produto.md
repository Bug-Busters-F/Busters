# API

O objetivo deste projeto é desenvolver uma plataforma web que disponibilize informações sobre o
desempenho  dos  Estados  Brasileiros  no  comércio  exterior, com  base  nos  dados  abertos  do
Ministério  do  Desenvolvimento,  Indústria,  Comércio  e  Serviços.  Essa  ferramenta  fornecerá  aos
tomadores  de  decisão  dados  claros  e  acessíveis,  permitindo  a  identificação  de  municípios  que
estejam em ascensão, estagnação ou declínio no mercado internacional.

Cargas passam por Unidades da Receita Federal (URF) localizadas em portos ou aeroportos para liberação de envios ao exterior ou direcionadas à outra URF.

Volume de dados:

- ~1.2M registros/ano
- ~15M total

## Requisitos

Veja o documento [Requisitos do Cliente](./Requisitos%20de%20Cliente%203ADS%20-%20Logística.pdf)

1. **Segmentação por Estado:** Apresenta informações detalhadas sobre cada município, incluindo:
   1. Principais cargas movimentadas.
   2. Ranking por valor agregado de exportação e importação.
   3. Evolução histórica da balança comercial.
2. **Busca e Filtros**: Ferramentas que permitam buscar cargas por código NCM e aplicar filtros personalizados para análise específica.
3. **Painel de Estatísticas**: Visualização gráfica interativa, apresentando a evolução da balança comercial dos municípios no período de 2014 a 2024.

Pontos de Destaque:

- Modelar Processos de Negócio usando técnicas VPC e BPMN
- Utilizar Estruturas de Dados
- Utilizar POO com ORM
- converter ncm para nome de carga
- Gráfico: valor agregado pelo tempo com filtragem por carga e por estado.

### Indicadores

Cards e gráficos.

- Quais são as principais alfândegas para transferência de carga?
- Quais mercados específicos atendemos (países destinos) fragmentados por estado?
- Valor agregado = valor fob (VL_FOB) dividido pelo peso (kg_liquido).
  - VL_FOB: valor da mercadoria no mercado internacional, sem inclusão dos custos com envio e seguro.
- Identificação  de  municípios  que estejam em ascensão, estagnação ou declínio no mercado internacional.
- Gráfico mostrando a tendência do Valor Agregado e do peso.
  - Na base do IBGE é possível obter dados da variação da produção. Assim, é possível projetar seus impactos no Valor agregado do produto.
- Mapa mundi de calor.

#### Sugestão para entendimento

Os alunos deverão investigar as seguintes questões (se possível):

- Análise Comparativa Regional: Como o desempenho comercial de um Estado se compara ao de outros?
- Identificação  de  Mercados  Emergentes:  Quais  países  têm  aumentado  a  importação  de produtos específicos dos de cada Estado Brasileiros?
- Geografia dos fluxos: Em quais localidades (Unidades de Receita Federal) são processas as
Exportações de cada Estado?
- Diversificação  de  Produtos:  Os  Estados  concentram  suas  exportações/importações  em
poucos produtos ou apresentam uma pauta diversificada?
- Análise de Vias de Transporte: Quais são os principais modais de transporte utilizados para
escoar exportações em nível de transporte internacional?
- Estudo  de  Sazonalidade:  Existem  padrões  sazonais  nas  exportações  de  determinados
produtos? Como as empresas locais lidam com essas variações?
- Mapeamento  de  Cadeias  Produtivas:  Quem  são  os  principais  fornecedores  e  clientes
internacionais  das  empresas  nos  municípios?  Como  essas  relações impactam  a economia
local?
- Análise de tendência e projeção: Quais as tendências de exportação? É possível criar um
modelo de projeção futura?

### Normalização, Tratamento e Análise dos Dados

- vias utilizadas: aérea, rodoviária ...
- Limpar a base de dados:
  - o que tiver kg=0, tirar da base
  - remover registros como cargas enviadas pela rodoviária para Arábia Saudita
  - relatório (fora do site): explicando os motivos da remoção dos registros e suas quantidades.

## Fontes de Dados

- [Comex Stat](https://www.gov.br/mdic/pt-br/assuntos/comercio-exterior/estatisticas/base-de-dados-bruta) - portal do governo
  - Dados abertos
  - NCM
  - URF
  - tabela auxiliar de vias (categorias)
- IBGE
  - Variação da Produção

## Requisitos Não Funcionais

- Aplicação Web
- NodeJS ou outro Backend
- React
- Banco de Dados Relacional

---

- Gráfico dos estados brasileiros interativo que abrirá as inforamções do estado
- Escolha no topo da página entre Exportação e Importação
- Busca de dados de 2014 a 2024
  - Exportação e importação
  - UF e cidades
  - NCM
  - URF existentes
- Filtragem
- Gráficos
- Mapa de Calor
- Normalização dos Dados
- Otimização (Estrutura de Dados e Algorítmos de Ordenação)

---

## Backlog do Produto

User Stories:

1. Como analista de dados quero fazer a limpeza dos dados de exportação e importação para que eu tenha somente dados válidos.
2. Como profissional de logística quero ter um painel Web para que eu possa visualizar os dados.
3. Como profissional de logística quero poder visualizar informações de importação e exportação de cada estado do Brasil para que eu possa analisá-los.
4. Como profissional de logística quero poder escolher um estado brasileiro para que eu possa visualizar informações de importação e exportação de cada URF desse estado.
5. Como profissional de logística quero poder escolher uma carga através do NCM para que eu possa visualizar informações de importação e exportação referente a cada tipo de carga.
6. Como profissional de logística quero filtrar informações para conseguir analisar apenas as informações relevantes à minha busca.

QT_ESTAT quant de estoque em certa unid de medidas

## Resumo

- Dados normalizados - MySQL
  - Relatório da normalização (não precisa estar no sistema) - quantas linhas tirou pelo motivo X
- dashboard - React/Web
- gráficos interativos e indicadores em cards - JS/React
  - Brasil
    - Evolução histórica da balança comercial.
    - Gráfico mostrando a tendência do Valor Agregado e do peso.
    - Principais cargas movimentadas
    - principais alfândegas para transferência de carga
  - Brasil de cada estado
    - mercados específicos atendemos (países destinos) fragmentados por estado
    - principais alfândegas para transferência de carga
    - Principais cargas movimentadas
    - Ranking por valor agregado de exportação e importação
    - Evolução histórica da balança comercial.
    - Gráfico mostrando a tendência do Valor Agregado e do peso.
  - Segmentação por estado mostrando de cada município (URF ?):
    - Principais cargas movimentadas
    - Ranking por valor agregado de exportação e importação
    - Evolução histórica da balança comercial.
    - Gráfico mostrando a tendência do Valor Agregado e do peso.
  - Segmentação por NCM + filtros personalizados
    - Número de cargas por vias utilizadas
    - Gráfico mostrando a tendência do Valor Agregado e do peso.
- filtragens
- mapa de calor
- Usuário fazer upload de dados (novo CSV)

- Sprint 1 - mostrar dados de um ano
- Automatizar os processos

### Perguntas para o cliente

- Na segmentação por estado mostrando de cada município, por ter muitos municípios, vamos mostrar uma tabela com os dados ou gostaria de mostrar as informações por UF?
