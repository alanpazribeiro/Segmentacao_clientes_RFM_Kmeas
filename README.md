# Segmentacao_clientes_RFM_Kmeans
Projeto Final - Segmentação de usuários com base em seu perfil consumidor aplicando Machine Learning, Cohort e Análise RFM afim de obter insights de negócios.


## Parte 1 - 

## Parte 2 - 

## Parte 3 - 
 - Empresa: Everything Plus
 - Ramo: E-commerce
 - Objetivo do Projeto: Segmentação de usuários com base em seu perfil consumidor, afim de obter insights de negócios
### 1. Possíveis interessados
 - Equipe de Marketing
 - Gerentes de Produtos / Negócios
### 2. Utilização
 - Oferecer produtos mais direcionados aos perfis dos clientes
 - Campanhas de Marketing mais assertivas
### 3. Como será feito
 - 3.1 Verificando na base de dados informações como:
  - data da última compra (RFM)
  - data do último acesso à plataforma
  - quantidade de acessos diários e semanais até a efetivação da compra
  - quanto os usuários gastaram em média em suas últimas compras
  - taxa de conversão (novos clientes)
  - tempo até a primeira compra desde o primeiro acesso
  - receita média dos novos clientes
  - retorno do investimento em marketing
### 4. Execução
 - 4.1 Pré-processamento dos Dados
  - verificar integridade dos dados
  - tipo de dado de cada variável
  - dados nulos e faltantes
  - organização e renomeação das colunas
  - amplitude das variáveis numéricas e tipo de dados categóricos
  - valores duplicados
  - possíveis alterações/ajustes na coluna data/hora
  - deletar colunas desnecessárias
 - 4.2 Exploração dos Dados
  - construir tabelas e gráficos (barras, histogramas e boxplot)
  - verificar Taxa de retenção e Índice de Cancelamento dos usuários
  - análise de Cohort
  - calcular o valor do tempo de vida do usuário
  - verificar anomalias nos dados (as vendas diminuíram? por quê?)
  - verificar outliers e quais ações tomar
### 5. Segmentando os clientes
 - Verificar qual das abordagens melhor se encaixa no projeto (baseado nas variáveis disponíveis no conjunto de dados):
  - Cohort
  - RFM
  - Aplicar K-Means Clustering para agrupamento dos usuários:
### 6. Descrição dos Dados:
 - Conjunto de dados: 'ecommerce_dataset_us':
  - 'InvoiceNo:' número exclusivo da Nota Fiscal contendo 6 dígitos e atribuído a cada transação;
  - 'StockCode:' código exclusivo do produto atribuído a cada item;
  - 'Description': nome do item;
  - 'Quantity:' quantidade de cada item vendido;
  - 'InvoiceDate:' data e hora da emissão da nota fiscal referente aos itens comprados;
  - 'UnitPrice:' preço unitário de cada item;
  - 'CustomerID:' código exclusivo do cliente
