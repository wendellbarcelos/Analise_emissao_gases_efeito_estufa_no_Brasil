# Projeto de Análise de Emissões de Gases de Efeito Estufa no Brasil

Fazemos parte de um órgão de fiscalização ambiental com o objetivo de analisar os dados de emissões de gases de efeito estufa no Brasil. Nossa tarefa principal é criar tabelas e visualizações que respondam às perguntas da **equipe de supervisão**, fornecendo insights claros e acionáveis. Para isso, utilizaremos bases de dados oficiais, como o inventário nacional de emissões de gases disponível no **SEEG**, e faremos cruzamentos com informações demográficas do **Censo IBGE**.


## Escopo do Projeto

### 1. **Filtragem e Transformação de Dados**
Os dados disponíveis incluem quatro categorias:
- **Emissão**: Registros das emissões de gases de efeito estufa.
- **Remoção**: Dados sobre gases retirados da atmosfera.
- **NCI**: Não contemplados no inventário nacional.
- **Bunkers**: Emissões de transporte internacional marítimo e aéreo.

Para focar no inventário nacional, removeremos os registros de **NCI** e **Bunkers**. Após o filtro, faremos transformações importantes no formato do **DataFrame**, alterando as colunas de anos (1970-2021) para:
- Uma coluna única com as informações dos anos;
- Uma coluna única para os dados de emissão.

Manteremos as colunas descritivas como "Nível 1 - Setor" até "Produto", garantindo a integridade das informações contextuais.


### 2. **Análise de Emissões por Tipo de Gás**
Para atender às solicitações da equipe de supervisão, realizaremos:
- **Agrupamento por gás**: Somaremos as emissões totais para identificar os gases mais emitidos no Brasil.
- **Emissões por setor**: Determinaremos as atividades econômicas mais poluentes para cada gás.
- **Gases por setor**: Identificaremos os gases mais emitidos por cada atividade econômica.

Utilizaremos técnicas avançadas de agrupamento de dados, incluindo a aplicação de índices múltiplos, para gerar tabelas que respondam diretamente às perguntas formuladas.


### 3. **Tendências de Emissão**
Criar uma visualização que mostre se as emissões médias de gases aumentaram ou diminuíram ao longo do tempo:
- Gráfico de emissão média por ano, separado por tipo de gás;
- Análise de tendências para identificar mudanças no comportamento das emissões.

Essa etapa ajudará a supervisionar o impacto de políticas públicas e identificar áreas prioritárias para intervenção.


### 4. **Cálculo de Emissão Per Capita**
Para calcular a **emissão per capita**, utilizaremos a fórmula:

\[
\text{Emissão per capita} = \frac{\text{Emissão Total}}{\text{População}}
\]

Essa análise será realizada com base nos seguintes passos:
1. **Importar dados populacionais**: Utilizaremos os dados do Censo IBGE para obter a população de cada estado.
2. **Limpeza de dados**: Resolver problemas na coluna de população, como:
   - Remoção de dígitos entre parênteses.
   - Substituição de pontos por separadores adequados.
3. **Unir dados de emissão e população**: Geraremos um gráfico relacionando o tamanho da população com a emissão de gases.


### 5. **Visualização Avançada**
Melhoraremos a visualização de dados utilizando a biblioteca **Plotly**, que permite criar gráficos interativos e de alta qualidade. Essas visualizações:
- Identificarão os estados correspondentes a cada ponto no gráfico;
- Destacarão estados com maior impacto ambiental, correlacionando população e emissão.


## Ferramentas e Tecnologias

- **Python**: Manipulação e análise de dados.
  - **Pandas**: Transformação e agrupamento de dados.
  - **NumPy**: Cálculos estatísticos.
  - **Plotly**: Criação de gráficos interativos.
- **VS Code**: Ambiente para codificação e análise.
- **SEEG**: Base de dados de emissões de gases de efeito estufa.
- **Censo IBGE**: Informações demográficas para cálculo de emissão per capita.


## Entregas do Projeto

1. **Tabelas**:
   - Emissões totais por gás;
   - Atividades econômicas mais poluentes para cada gás;
   - Gases mais emitidos por atividade econômica.
2. **Visualizações**:
   - Gráficos de tendências de emissão por ano e gás;
   - Gráfico interativo de emissão per capita por estado.
3. **Métricas Avançadas**:
   - Emissão total por estado;
   - Emissão per capita mais recente.


## Impacto Esperado

O projeto fornecerá insights críticos para apoiar a formulação de políticas públicas ambientais e monitorar o impacto das emissões no Brasil. As análises permitirão:
- Identificar os principais setores e gases responsáveis pelas emissões;
- Avaliar tendências históricas e possíveis melhorias no controle das emissões;
- Informar a população e gestores públicos sobre as disparidades regionais na emissão per capita.

Este projeto reforça o compromisso do órgão com a transparência e a eficiência no combate às mudanças climáticas.