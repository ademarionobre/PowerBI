# Estudo de caso Clube do Livro - Projeto e-commerce

Resquisitos para montar dashboard e-commerce vendas e assinaturas de livros.

O clube cresceu bastante, agora ele tem duas gerentes comerciais: a Morgana e a Milena. Elas estão nos contratando justamente porque elas precisam analisar algumas métricas muito importantes para conseguirem tomar decisões futuras baseadas nessas métricas.

E não só que façamos análises dessas métricas, mas também deixemos de forma visual e clara para que elas consigam entender e visualizar em qualquer plataforma, até no celular, de repente.

Elas sentaram conosco e explicaram o que elas precisavam visualizar, e nós pedimos para elas uma base de dados para que consigamos fazer essas análises.  
Elas passaram uma base de dados dentro do _Google Planilhas_, o e-commerce adota esse software de planilhas.
_______
## Requisitos do cliente
- Querem visualizar quantas pessoas na nossa base de clientes não estão com as assinaturas ativas, tanto em números absolutos quanto em porcentagem também.
  - Seria bem importante visualizar esse número porque elas iam direcionar algumas campanhas de marketing para tentar trazer de volta os clientes que não estão com a assinatura mais ativa.

- Qual é a profissão que mais compra dentro do e-commerce para?
  - Afim de , direcionar os livros justamente de interesse para essas carreiras.

- Querem saber o número de pessoas desempregadas da base de dados

- Métrica vendas do Clube do Livro. Definidas algumas metas de vendas semanais.
  - Usar visual tipo indicador (velocímetro).

- Querem visualizar algumas informações como uma **tabela** para facilitar um pouco a consulta. Elas querem informações bem específicas. Iremos usar um visual de tabela.

- Elas querem saber como o e-commerce está indo em função do tempo, qual é a evolução ou involução em função do tempo.
- Querem também visualizar essas métricas como, por exemplo, vendas em relação às semanas. Fazer previsão do que tende a acontecer.

- O e-commerce quer comparar algumas categorias. Ele quer saber, na base de livros, quais são os livros que ele tem maior quantidade, divididos por assunto.
  - Visual gráficos de barras.

- Solicitaram visualizar a questão das entregas por cidade, mas de forma visual, através de um mapa.
________
**Considerações**  
A base é uma **planilha com cinco abas** e cada uma dessas abas está comunicando alguns dados. A primeira aba é o catálogo de livros, temos uma série de livros que estão na base de dados deles que eles vendem, dividida pelo **assunto, pelo valor, pelo código** e **pelo autor**. Temos aqui algumas informações.

Na outra aba, temos a base de dados dos clientes, com vários nomes, idades, gêneros, uma gama de informações que vamos precisar usar para fazer as análises que elas vão pedir para nós.

Também temos uma planilha menor, que são as vendas por semana. Temos algumas semanas linkadas com o valor de vendas das semanas respectivas e com o valor de metas, quanto o e-commerce queria vender naquele período e o quanto ele vendeu de fato.

Temos outra aba com os acessos na página, temos as datas e os acessos respectivos naquele dia. E também temos outra aba com o número de livros vendidos na respectiva data também.  
______
**Etapas**  
Podemos trazer a base de dados direto para o PowerBI ou via link (planilha compartilhada).  

~~“Arquivo > Publicar na Web”, agera um link da planilha. No PowerBI, “Obter dados” opção “Web”.~~

Fazer a conexão pela Web através do link. Vou deixar selecionado o “Básico” e, na “URL”, colar o link. Então, através desse link, ele já vai fazer para nós a importação.

~~Ele trouxe para nós cinco tabelas – clicar agora para fazer uma pré-visualização – e ele também trouxe algumas outras tabelas sugeridas. Analisar se faz sentido ou não.~~

Selecionar primeiro a “Tabela” que, provavelmente, vai ser respectiva à primeira aba, relativa ao catálogo de livros. Criado uma coluna “Index” que não precisaremos, também tem uma linha em branco. Tratar esses dados.  

Criado um “Index” e uma linha em branco em todas as abas.  

Estar repetindo a primeira aba, mas mesclando algumas colunas que, para nós, não faz sentido. Como já olhamos que as de cima estão trazendo o que precisamos, então vemos que as sugeridas podemos descartar.  

Etapa “Transformar dados” para fazermos a alteração, removermos essa coluna de “Index” que ele trouxe e essa primeira linha.

Abrir o **Power Query**. Já está selecionado a “Tabela 5” a primeira coluna, remover porque é o “Index” que nós não precisamos. “Remover Linhas”, tirar as linhas em branco.

Agora que o título está como “Column2”, “Column3”, promover a primeira linha como cabeçalho. “Usar a primeira linha como cabeçalho”, acionar para promover.

"Renomear” para ficar igual – “Número de livros vendidos”.

Repetir o mesmo processo com todas as abas.

“Renomear”, “Acessos na página”. 

“Renomear”, “Vendas por semana”.

“Renomear”, “Links”.

“Renomear”, “Catálogo de livros”.

“Fechar e aplicar”. Analisar e visualizar a base de dados pronta para fazer a análise, a construção do dash e linkar os visuais.

Só lembrando que, claro, esses dados que estamos trazendo aqui já estão tratados, nós fizemos alguns tratamentos de importação, mas os dados em si já estão estruturados para fazermos as análises e escolhermos os nossos visuais.

Como a base estava toda tratada, pulou o fluxo de etapas de ETL (Extract Treatment and Load - extrair, tratar e carregar os dados).
