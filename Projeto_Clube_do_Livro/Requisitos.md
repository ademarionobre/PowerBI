## Estudo de caso Clube do Livro - Projeto e-commerce

Resquisitos para montar dashboard e-commerce vendas e assinaturas de livros.

Como ele cresceu bastante, agora ele tem duas gerentes comerciais: a Morgana e a Milena. Elas estão nos contratando justamente porque elas precisam analisar algumas métricas muito importantes para conseguirem tomar decisões futuras baseadas nessas métricas.

E não só que façamos análises dessas métricas, mas também deixemos de forma visual e clara para que elas consigam entender e visualizar em qualquer plataforma, até no celular, de repente.

Elas sentaram conosco e explicaram o que elas precisavam visualizar, e nós pedimos para elas uma base de dados para que consigamos fazer essas análises. Vamos olhar essa base de dados juntos para entendermos melhor o que temos em mãos.

Elas passaram essa base de dados dentro do _Google Planilhas_, o e-commerce adora esse software de planilhas, e vamos dar uma analisada juntos agora, ver o que eles estão trazendo para nós.

Temos aqui uma **planilha com cinco abas** e cada uma dessas abas está comunicando alguns dados. A primeira aba é o catálogo de livros, temos uma série de livros que estão na base de dados deles que eles vendem, dividida pelo **assunto, pelo valor, pelo código** e **pelo autor**. Temos aqui algumas informações.

Na outra aba, temos a base de dados dos clientes, com vários nomes, idades, gêneros, uma gama de informações que vamos precisar usar para fazer as análises que elas vão pedir para nós.

Também temos uma planilha menor, que são as vendas por semana. Temos algumas semanas linkadas com o valor de vendas das semanas respectivas e com o valor de metas, quanto o e-commerce queria vender naquele período e o quanto ele vendeu de fato.

Temos outra aba com os acessos na página, temos as datas e os acessos respectivos naquele dia. E também temos outra aba com o número de livros vendidos na respectiva data também.

Podemos trazer essa base de dados direto para o PowerBI. Claro, se está no Google Sheets, eu poderia fazer a importação de maneiras diferentes, poderia baixar, de repente, no formato XLS, ou em outro formato, e importar para o PowerBI.

Mas eu vou aproveitar, vou gerar um link, vou fazer uma publicação na Web. Vou vir aqui em “Arquivo”, no próprio Google Planilhas

“Arquivo > Publicar na Web”, aí ele me gera um link. Vou clicar para selecionar esse link, vou dar “Ctrl + C” no meu teclado para copiar esse link, vou lá no nosso PowerBI, “Obter dados”. Na parte inferior de “Obter dados” eu clico e ele já vai me trazer a opção “Web”.

Vou fazer a conexão pela Web através daquele link. Vou deixar selecionado o “Básico” mesmo e, na “URL”, “Ctrl + V” para colar o que copiamos. Vou dar “Ok”. Então, através desse link, ele já vai fazer para nós a importação de uma maneira um pouco mais prática.

Ele trouxe para nós cinco tabelas – nós vamos clicar agora para fazer uma pré-visualização – e ele também trouxe algumas outras tabelas sugeridas. Vamos analisar se faz sentido ou não para nós.

Vou selecionar primeiro a “Tabela” que, provavelmente, vai ser respectiva à primeira aba, como olhamos relativa ao catálogo de livros. Nós percebemos que ele criou uma coluna “Index” que não vamos precisar, também tem uma linha em branco aqui. Vamos tratar esses dados.

Vamos só fazer a visualização primeiro, selecionando. Aqui eu tenho a minha segunda aba com os clientes; a minha terceira aba com as vendas por semana. Percebe que ele criou um “Index” e uma linha em branco em todas essas abas.

Isso é relativamente comum acontecer quando importamos pelo Google Planilhas. Aqui, a mesma situação e a quinta também. Vamos dar uma analisada nessas tabelas sugeridas que ele trouxe para nós.

Clicando aqui, vamos olhar. Ele está repetindo a primeira aba, mas mesclando algumas colunas que, para nós, não faz sentido. Como já olhamos que as de cima estão trazendo o que precisamos, então vemos que as sugeridas podemos descartar.

Vamos agora em “Transformar dados” para fazermos a alteração, removermos essa coluna de “Index” que ele trouxe e essa primeira linha.

Ele está abrindo o Power Query para nós. Já está selecionado aqui da “Tabela 5” a primeira coluna, vou clicar com o botão direito e remover porque é o “Index” que nós não precisamos. Também vou vir aqui em cima, na parte superior, em “Remover Linhas”, clico e peço para ele tirar as linhas em branco.

Agora que o título está como “Column2”, “Column3”, na verdade, vou pedir para ele promover a primeira linha como cabeçalho. Então, na parte superior, tenho aqui “Usar a primeira linha como cabeçalho”, vou clicar e ele já promoveu para mim.

Eu vou dar um nome, vou clicar com o botão direito na “Tabela 5” para ficar bem descritivo. Vou clicar em “Renomear” para ficar igual – “Número de livros vendidos”.

E vamos repetir o mesmo processo com todas as abas. Vou vir aqui na “4”, vou remover essa coluna, vou pedir para ele remover as linhas em branco.

Vou promover a primeira linha com cabeçalho, e vou renomear, “Renomear”, “Acessos na página”, “Enter”. E assim sucessivamente com todas as abas.

“Remover”, “Remover linhas em branco”, “Usar a primeira linha como cabeçalho”, “Renomear”, “Vendas por semana”.

“Remover”, “Remover linhas em branco”, “Usar a primeira linha como cabeçalho”, “Renomear”, “Links”.

E, por fim, eu comecei de trás para frente, “Remover”, “Remover linhas em branco”, “Usar a primeira linha como cabeçalho”, “Renomear”, “Catálogo de livros”, “Enter”.

Agora, nós podemos vir aqui em “Fechar e aplicar”, ele vai trazer para nós essa base de dados. Vamos analisar, no lado direito, vamos conseguir visualizar a nossa base de dados pronta para começarmos a fazer a nossa análise, a construção do dash e linkar os visuais.

Só lembrando que, claro, esses dados que estamos trazendo aqui já estão tratados, nós fizemos alguns tratamentos de importação, mas os dados em si já estão estruturados para fazermos as análises e escolhermos os nossos visuais.

Na vida real, você não vai pular essa etapa de ETL – para quem não sabe, “ETL” é Extract Treatment and Load, extrair, tratar e carregar os dados. Na vida real, esses dados vão vir todos bagunçados e você vai ter que perder um bom tempo trabalhando com eles.

Mas como o objetivo do nosso curso é focarmos mais na parte visual, na escolha dos visuais e aprofundar na característica e na possibilidade de cada um, isso tomaria muito tempo do nosso curso. Então, já trouxe os dados melhor estruturados para nós para que consigamos focar mais nos visuais.

Outra coisa importante, aproveitando, é que não vamos conseguir passar por todos os visuais no PowerBI, porque vão vários, mas vamos trabalhar com alguns que são muito utilizados no mercado e você vai se sentir confiante, baseado no que vamos ver aqui, para você explorar os outros por conta própria.

Vamos entender o porquê aquele visual é a melhor escolha para aquele tipo de dado e de métrica e também explorar um pouco mais a fundo as possibilidades de cada um.

Já temos a nossa base de dados importada, pronta para começarmos a construção do nosso projeto e do nosso dashboard.
