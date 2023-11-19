# Segmentacao_clientes_RFM_Kmeans
Projeto Final - Segmentação de usuários com base em seu perfil consumidor aplicando Machine Learning, Cohort e Análise RFM afim de obter insights de negócios.


## Parte 1 - 
Você recebeu uma tarefa analítica de uma loja online internacional. Seu predecessor não conseguiu completá-la: eles lançaram um teste A/B e depois desistiu. Eles deixaram apenas as especificações técnicas e resultado dos testes.

### Descrição técnica:
 - Nome do teste: recommender_system_test
 - Grupos: A(controle) e B(funil de novos pagamentos)
 - Data de início: 07-12-2020
 - Data de quando paparam de receber novos usuários: 21-12-2020
 - Data de término: 01-01-2021
 - Público: 15% de novos usuários da região da UE
 - Propósito do teste: testando mudanças relacionadas à introdução de uma recomendação do sistema melhorada
 - Resultado esperado: em até 14 dias após o cadastro, usuários mostram uma conversão melhor nas visualizações de página do produto (o evento product_page event), ao adicionar itens ao carrinho (product_cart), e compras (purchase). A cada etapa do funil product_page → product_cart → purchase, terá ao menos 10% de aumento.
 - Número esperado de participantes do teste: 6000
#### Arquivo 1: Calendário de Eventos de Marketing para 2020 - ('ab_project_marketing_events_us.csv'):
  - name: nome dos eventos de marketing;
  - regions: as regiões onde as campanhas serão realizadas;
  - start_dt: as datas de início da campanha;
  - finish_dt: as datas finais da campanha;
#### Arquivo 2: Usuários que se cadastraram na loja online de 7 a 21 de dezembro de 2020 - ('final_ab_new_users_upd_us.csv')
  - user_id: identificação do usuário;
  - first_date: data do cadastro;
  - region: região de localidade do usuário;
  - device: tipo de dispositivo utilizado para o cadastro
#### Arquivo 3: Eventos dos novos usuários dentro do período de 7/12/2020 até 1/1/2021 - ('final_ab_events_upd_us.csv')
  - user_id: identificação do usuário;
  - event_id: data e hora do evento;
  - event_name: tipo do evento;
  - details: dos dados adicionais sobre o evento (por exemplo, o total do pedido em USD para eventos purchase)
#### Arquivo 4: Tabela com os participantes do teste - ('final_ab_participants_upd_us.csv')
  - user_id: identificação do usuário;
  - ab_test: o nome do teste;
  - group: grupo do teste que o usuário pertencia;
#### Faça o download dos dados de teste, veja se foi realizado corretamente, e analise os resultados.
___________________________________________________________________

## Parte 2 - 
Banco de dados de um dos serviços concorrentes nesse mercado que contém dados sobre livros, editoras, autores, e classificação de clientes e avaliação de livros. Essa informação será usada para gerar uma proposição válida para o novo produto.

### 1. Descrição dos dados:
 - Arquivo 1: contém informações sobre os livros - (books — livros):
  - book_id — identificador do livro
  - author_id — identificador do autor
  - title — título
  - num_pages — número de páginas
  - publication_date — data de publicação
  - publisher_id — identificador da editora
 - Arquivo 2: contém informações sobre os autores - (authors — autores):
  - author_id — identificador do autor
  - author — autor
- Arquivo 3: contém informações sobre as editoras - (publishers — editoras):
  - publisher_id — identificador da editora
  - publisher — editora
 - Arquivo 4: contém informações sobre as classificação dos usuários - (ratings — classificações):
  - rating_id — identificador da classificação
  - book_id — identificador do livro
  - username — o nome do usuário que avaliou o livro
  - rating — classificação
 - Arquivo 5: contém informações sobre as dados sobre revisão dos clientes - (reviews — avaliação):
  - review_id — identificador da revisão
  - book_id — identificador do livro
  - username — o nome do usuário que revisou o livro
  - text — o texto da revisão

### 2. Tarefa
   1. Encontre o número de livros lançados depois de 1 de janeiro de 2000.
   2. Encontre o número de avaliações e a classificação média para cada livro.
   3. Identifique a editora que lançou o maior número de livros com mais de 50 páginas (isso vai ajudar você a excluir brochuras e publicações parecidas da sua análise).
   4. Identifique o autor com a média mais alta classificação de livros: olhe apenas para livros com pelo menos 50 classificações.
   5. Encontre o número médio de avaliações entre usuários que classificaram mais do que 50 livros.

### 3. Instruções para completar a tarefa
   1. Descreva os objetivos do estudo.
   2. Estude as tabelas (imprima as primeiras linhas).
   3. Faça uma consulta SQL para cada uma das tarefas.
   4. Enuncie os resultados de cada consulta no Caderno.

### 4. Descreva suas conclusões para cada uma das tarefas.
____________________________________________________
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
