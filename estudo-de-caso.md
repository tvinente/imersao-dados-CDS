
# Diretrizes do Projeto

## O problema de negócio

Uma companhia área gostaria de realizar uma campanha de marketing para aumentar o número de passageiros que participam do programa de fidelidade da empresa.

O programa de fidelidade da empresa oferece 3 níveis de prêmios, representados pelos tipos de cartões de fidelidade. Os cartões são: Star, Nova e Aurora.

O time de marketing forneceu uma base de novos clientes para o time comercial entrar em contato e fazer a oferta da assinatura do programa de fidelidade. Porém, não há vendedores suficientes no time comercial para abordar todos os clientes.

Você foi contratado como Cientista de Dados para determinar qual a probabilidade de cada cliente assinar cada um dos 3 cartões do programa de fidelidade. Por exemplo, o cliente A tem probabilidade de 70% de assinar o cartão Star, 20% de assinar o cartão Nova e 10% de assinar o cartão Aurora.

Como essa informação está em mãos, o vendedor pode oferecer para o cliente A, o cartão
Star, diretamente.

## A resolução do problema

A resolução do problema será o desenvolvimento de um algoritmo de inteligência artificial (IA) capaz de calcular a probabilidade de um determinado cliente assinar cada um dos três programas de fidelidade, através dos dados históricos de clientes como dados demográficos, histórico de compras e comportamento de navegação no site da companhia aérea.

Ao fornecer os dados do cliente, a inteligência artificial indicará o programa de fidelidade mais adequado para cada cliente em uma janela web, na qual o time comercial poderá receber essa informação para entrar em contato com os clientes e fazer a oferta mais relevante, aumentando as chances de sucesso da área comercial.

## Objetivo da coleta de dados

O objetivo desta fase é reunir um conjunto de dados relevantes, confiáveis e representativos do problema que está sendo abordado no projeto.

Principais fontes de armazenamento de dados de uma empresa que podem ser usados em projetos de IA. Os tipos mais comuns de sistemas armazenadores de dados são:

 - **Bancos de dados relacionais:** Armazenam dados em tabelas com linhas e colunas, e são adequados para armazenar dados estruturados, como informações de clientes, produtos e transações.
 - **Armazenamento em nuvem:** Oferece serviços de armazenamento de dados na nuvem, permitindo que as empresas armazenem seus dados em servidores remotos e acessem-nos de qualquer lugar.
 - **Planilhas:** Ferramentas de planilhas como Excel e Google Sheets também são usadas como repositório de dados para organizar informações.
 - **Formulários:** Coletam dados inseridos manualmente pelos clientes e usuários de produtos ou ferramentas. Esses dados podem ser armazenados em planilhas ou banco de dados.

Para esse projeto vão usar os dados armazenados em um banco de dados chamado SQLite.

## Os dados

Os dados estão armazenados em 2 tabelas dentro do banco de dados são:

### flight_activity

Coluna   | Descrição
:------- | :------
loyalty_number | Identificador único do passageiro
year | Ano do voo
month | Mês do voo
flights_booked | Número de voos agendados
flights_with_companions | Números de voos com acompanhante
total_flight | Número total de voos
distance | Distância total percorrida por voos
points_accumulated | Quantidade de pontos acumulados no programa de fidelidade
points_redeemed | Quantidade de pontos recuperados do programa de fidelidade
dollar_cost_points_redeemed | Custo dos pontos recuperados

### flight_loyalty_history

Coluna   | Descrição
:------- | :------
loyalty_number | Identificador único do passageiro
country | País de residência
province | Província de residência
city | Cidade de residência
postal_code | Código postal ou CEP
gender | Gênero identificado
education | Nível de escolaridade
salary | Salário
marital_status | Estado civil
loyalty_card | Tipo de cartão do programa de fidelidade
clv | O valor total gasto pelo cliente nessa empresa
enrollment_type | Tipo de inscrição
enrollment_year | Ano da primeira inscrição
enrollment_month | Mês de inscrição
cancellation_year | Ano de cancelamento
cancellation_mont | Mês de cancelamento
