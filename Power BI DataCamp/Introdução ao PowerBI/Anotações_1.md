## Introdução ao Power BI

O Power BI é uma ferramenta que permite explorar dados de forma interativa para obter insights. O Power BI permite que você relate informações de maneira eficaz por meio de visualizações personalizáveis fáceis de usar.
https://docs.microsoft.com/en-us/power-bi/create-reports/sample-retail-analysis

Visualização de dados no Power BI - A representação visual dos dados permite que as pessoas interpretem e analisem os dados mais rapidamente. Por exemplo, é mais fácil encontrar o ano mais lucrativo em um gráfico de barras do que percorrer uma planilha!

Por que o Power BI? Existem várias ferramentas para inteligência de negócios, então por que Power BI? De acordo com o Gartner, o Power BI é a principal ferramenta de BI. Mais de 97% das empresas da Fortune 500 usam o Power BI. No total, o Power BI tem mais de seis milhões de clientes. Você já está convencido? Vamos aprender mais!

Componentes do Power BI - O Power BI é composto de dois componentes: área de trabalho e serviço. O Power BI Desktop é uma ferramenta de análise de dados e criação de relatórios disponível em seu computador local. Ele inclui recursos poderosos, como o Query Editor, e é gratuito. Neste curso, usaremos o Power BI Desktop. O serviço Power BI é a versão em nuvem do Power BI. Os relatórios podem ser editados no serviço Power BI, mas não em toda a extensão da área de trabalho. Em vez disso, o principal objetivo do serviço Power BI é compartilhar e distribuir relatórios. Normalmente, você usará o Power BI Desktop para criar um relatório e o serviço do Power BI para compartilhar esse relatório.

Power BI Profissional - Este curso usará a versão gratuita do Power BI. Existe uma versão paga chamada Power BI Pro. A versão gratuita tem a maioria das funcionalidades, no entanto, o Power BI Pro permite que você publique trabalhos na plataforma de nuvem do Power BI, incluindo seu aplicativo móvel. O Power BI Pro também permite que você colabore com outros usuários do Power BI. Embora estejamos usando a versão gratuita, tudo o que você aprender neste curso será aplicável à versão paga.

Interface do Power BI - Vamos percorrer rapidamente a interface do Power BI. Na primeira vez que o Power BI Desktop é iniciado, ele exibe a tela de boas-vindas. Na tela de boas-vindas, você pode obter dados, ver fontes recentes ou abrir relatórios recentes. Selecione o ícone fechar para fechar a tela de boas-vindas.

Interface do Power BI - três exibições - Ao longo do lado esquerdo estão os ícones para as três exibições: Relatório, Dados e Modelo. Você pode alterar as exibições selecionando qualquer um dos ícones.

Interface do Power BI - Exibição de relatório - A exibição de relatório é a exibição padrão. Nesta exibição, você pode criar relatórios e visuais.

Interface do Power BI - Exibição de dados - Na exibição de dados, você pode ver os dados usados ​​no modelo de dados associado ao seu relatório.

Interface do Power BI - Exibição do modelo - Na exibição Modelo, você pode ver e gerenciar os relacionamentos entre tabelas em seu modelo de dados.

Interface do Power BI - Área da tela - Vamos voltar para a visualização do relatório. A área da tela no meio é onde as visualizações são criadas e organizadas.

Interface do Power BI - painel Filtros - No painel Filtros, você pode filtrar visualizações de dados.

Interface do Power BI - Painel de visualizações - No painel Visualizações, você pode adicionar, alterar ou personalizar visualizações.

Interface do Power BI - painel Campos - Finalmente, o painel Campos mostra os campos disponíveis. Você pode arrastar esses campos para a tela, o painel Filtros ou o painel Visualizações para criar ou modificar visualizações.

Conjunto de dados da Wide World Importers (WWI) - Neste capítulo, usaremos dados de uma empresa fictícia chamada Wide World Importers, uma importadora e distribuidora atacadista de produtos inovadores que opera em São Francisco.

Estrutura do conjunto de dados da Wide World Importers (WWI) - Frequentemente, um conjunto de dados é composto por mais de um arquivo. O mesmo vale para este conjunto de dados; vamos dar uma olhada. O Power BI foi projetado para funcionar com uma estrutura de banco de dados comum chamada esquema em estrela. Se você nunca ouviu falar do esquema estelar, não se preocupe! Tudo o que você precisa saber por enquanto é que ele usa tabelas de fatos e dimensões. Você pode criar uma relação entre essas tabelas por meio de colunas de chave, para que o Power BI saiba que elas estão relacionadas. Uma tabela de fatos contém eventos ou transações. No nosso caso, o arquivo FactSales contém todas as vendas feitas na Wide World Importers. As tabelas de fatos possuem tabelas de dimensões que contêm mais informações sobre cada transação. Por exemplo, a tabela de dimensões, DimCustomer, contém as informações de contato de cada cliente. Existem quatro outras tabelas de dimensão, como você vê listadas aqui.
