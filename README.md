# Desafio-de-projeto

Visão geral

Este projeto utiliza uma tabela Financial SampleFinancials_origem para criar um star schema, separando os dados em tabelas de fatos e dimensões para facilitar a análise e melhorar o desempenho da consulta. A tabela original, , será ocultada e usada como backup.

Componentes do esquema em estrela:
Tabela de fatos ( F_Vendas)
Tabelas de Dimensões ( D_Produtos, D_Produtos_Detalhes, D_Descontos, D_Detalhes, D_Calendário)
Tabelas e Colunas

1. F_Vendas (Tabela de fatos)
SK_ID : Chave substituta para tabela de fatos.
ID_Produto : ID do produto.
Produto : Nome do produto.
Unidades vendidas : Número de unidades vendidas.
Preço de venda : preço pelo qual o produto foi vendido.
Faixa de desconto : Categoria de desconto.
Segmento : Segmento de clientes.
País : País de venda.
Vendedores : Vendedor ou equipe envolvida.
Lucro : Lucro gerado pela venda.
Data : Data da venda.

2. D_Produtos (Tabela de Dimensões do Produto)
ID_Produto : ID do produto.
Produto : Nome do produto.
Média de Unidades Vendidas : Média de unidades vendidas.
Média do Valor de Vendas : Valor médio de vendas.
Mediana do Valor de Vendas : Valor mediano de vendas.
Valor Máximo de Venda : Maior valor de venda.
Valor Mínimo de Venda : Menor valor de venda.

3. D_Produtos_Detalhes (Tabela de Dimensões de Detalhes do Produto)
ID_Produto : ID do produto.
Faixa de desconto : Categoria de desconto.
Preço de venda : preço pelo qual o produto foi vendido.
Unidades vendidas : Número de unidades vendidas.
Preço de fabricação : Custo de fabricação do produto.

4. D_Descontos (Tabela de Dimensões de Desconto)
ID_Produto : ID do produto.
Desconto : Porcentagem de desconto aplicada.
Faixa de desconto : Categoria de desconto.

5. D_Detalhes (Tabela de Dimensões de Detalhes de Vendas)
Atributos adicionais não abordados nas outras tabelas de dimensão (por exemplo, análise mais detalhada das características de vendas).

6. D_Calendário (Tabela de Dimensões do Calendário)
Criado usando a função DAX calendar()para gerar uma tabela de datas para análise baseada em data.
Uso
A estrutura do esquema em estrela aprimora a análise de dados permitindo consultas eficientes de dados de vendas em diversas dimensões, como produtos, descontos e tempo.
