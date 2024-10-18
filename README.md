# Power BI Dashboard: Visão de Clientes e Vendas

Este projeto consiste na criação de dois dashboards interativos no Power BI, integrados a uma base de dados pública gerenciada no PostgreSQL, com o objetivo de fornecer insights detalhados sobre a clientela e o desempenho das vendas em uma loja fictícia.

## 📊 Visão Geral dos Dashboards

### 1. **Visão da Clientela**
Este dashboard oferece uma análise detalhada sobre os clientes da loja:
- **Total de Consumidores:** Número total de usuários cadastrados.
- **Distribuição Geográfica:** Gráfico demonstrando a distribuição da clientela por estado.
- **Faixa Etária:** Gráfico categorizando os clientes por faixa etária.
- **Compras por Região:** Quantidade de compras realizadas por cada região.
- **Evolução dos Cadastros:** Gráfico temporal que exibe o crescimento do número de clientes ao longo do tempo.
- **Filtro por Região**: Utizei uma função DAX para agrupar os Estados por região ( uma vez que essa informação não constava na tabela originalmente ), e criei um filtro que permite segmentar as informações para cada região do país.
  
  ![dashboard_ecommerce_clientes](https://github.com/user-attachments/assets/f0d78175-4f14-4145-aede-458661e27476)


### 2. **Visão de Vendas**
Este dashboard foca no desempenho de vendas da loja:
- **Faturamento Total:** Valor total das vendas realizadas.
- **Quantidade de Produtos Vendidos:** Número de unidades vendidas.
- **Total de Vendas:** Número total de transações.
- **Evolução do Faturamento:** Gráfico de linha que exibe o faturamento acumulado ao longo do tempo.
- **Vendas por Categoria:** Exibe as categorias de produtos mais vendidas.
- **Produtos Mais Vendidos:** Lista os produtos com maior volume de vendas.
- **Vendas por forma de pagamento:** Relaciona as formas de pagamento utilizadas nas vendas
- **Filtro por Estado**: Permite a filtragem das informações para cada estado do país.
  
  ![dashboard_ecommerce_vendas](https://github.com/user-attachments/assets/4cf78f1b-c907-449c-b118-35c519aa3466)


## 🗂 Estrutura do Banco de Dados

A base de dados utilizada está organizada em três tabelas principais:

- **usuarios:** Informações sobre os clientes, com colunas `cod_usuario`, `data_cadastro`, `faixa_etaria`, `estado`, e `cidade`.
- **produtos:** Detalhes sobre os produtos da loja, com colunas `cod_produto`, `nome_produto`, `categoria_produto`, e `valor_produto`.
- **vendas:** Dados sobre as transações realizadas, contendo `cod_usuario`, `cod_produto`, `data_compra`, `forma_pagamento`, `quantidade`, `valor_compra`, `data_prevista_entrega`, e `data_entrega`.

## ⚙️ Integração Power BI e PostgreSQL

Os dados foram integrados diretamente do PostgreSQL ao Power BI, permitindo a criação de visualizações dinâmicas e insights que auxiliam na tomada de decisões estratégicas para a loja.

## 🚀 Como Executar este Projeto

1. **Clonar o Repositório**
   ```bash
   git clone https://github.com/devleomarinho/dashboard-ecommerce.git
2. **Configurar a Conexão ao PostgreSQL**
   - Certifique-se de que o banco de dados PostgreSQL está configurado e rodando.
   - No Power BI, vá até a aba de **Transformar Dados** e atualize a conexão com as credenciais corretas para acessar o banco de dados.
   - Verifique se a conexão foi estabelecida corretamente e se os dados foram carregados sem erros.

3. **Abrir os Dashboards**
   - Após configurar a conexão com o banco de dados, abra o arquivo `dashboard_ecommerce.pbix` no Power BI Desktop.
   - Verifique se todas as visualizações estão carregando corretamente com base nos dados da sua base PostgreSQL.

4. **Atualizar os Dados**
   - Para garantir que os dados estejam sempre atualizados, utilize a função de atualização de dados no Power BI. Isso pode ser feito de forma manual ou programando uma atualização automática, caso tenha acesso ao Power BI Service.

## 📅 Tecnologias Utilizadas

- **Power BI:** Ferramenta utilizada para visualização de dados e criação dos dashboards.
- **PostgreSQL:** Banco de dados utilizado para armazenar e organizar as informações de clientes, produtos e vendas.
- **Git:** Utilizado para controle de versão do projeto e compartilhamento de código.

## 📈 Insights e Benefícios

Com esses dashboards, a loja tem acesso a informações estratégicas para a tomada de decisões:
- **Monitorar o perfil dos consumidores**, identificando áreas geográficas e faixas etárias com maior volume de compras.
- **Analisar o desempenho de vendas** e identificar produtos e categorias com maior rentabilidade.
- **Acompanhar tendências de crescimento**, com uma visão clara da evolução de cadastros de clientes e vendas ao longo do tempo.

