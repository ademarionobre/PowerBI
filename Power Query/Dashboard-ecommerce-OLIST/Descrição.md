![image](https://github.com/ademarionobre/PowerBI/assets/92057489/1e5ece79-031f-441d-8d9a-e51578e1013b)

## Projeto de análise de dados da OLIST

### Extração do dados.
#### Obtenção via conector csv e pasta local. 

A tela que ser abre apresenta coluna 'A origem do arquivo' que é justamente o idioma que vamos implementar para a leitura do arquivo. Normalmente quando lidamos com tipos de arquivos que temos caracteres especiais, ou então tem acentuação, que é normalmente a maioria dos casos o ideal colocar utf-8.
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/8598df65-bb4d-4150-956c-98a96e0a330c)
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/4beafc65-366f-4f74-9524-066f44e67961)

#### O Delimitador indica como os dados estão separados, nesse a planilha estar com colunas separadas por vírgula e portanto vamos manter 'virgula'.

#### Detecção dos tipos de dados, que normalmente já deixamos nessa base das 200 primeiras linhas. Com base nessas 200 primeiras linhas ele o Power Qeuery consegue definir o tipo de dado que tem dentro daquela coluna.

#### Demais datasets carregados, com o conector excel. Importado aba para o dataset orders e tabela para o dataset pyament.  

Observação: Importar a tabela, restringe a conexão com qualquer dado que esteja localizado na aba, mas fora das colunas da tabela. Já na aba, os dados dentro e fora da tabela são carregados. Assim, é preferível escolher a conexão com a tabela para evitar as possíveis "sujeiras" da aba.

#### Importando arquivo json hospedado no bucket S3 da amazon. Utilizando conector web.
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/cdd86770-b6ec-45ef-9433-7ba7480dd981)
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/0bd4e4e2-23b0-49a4-93a1-d11121593a8f)  
Necessário realizar tratamentos, visto haver apenas duas colunas no arquivo visto no PowerQuery.
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/31cc2709-d5e5-415c-b0e4-aadf09d27dd2)

# Refatorando procedimentos

![image](https://github.com/ademarionobre/PowerBI/assets/92057489/a12a50b6-6193-4ffe-89cf-6e2a16073fcc)  
Algo a reavaliar são as etapas aplicadas. Em muitos momentos, quando vamos realizando esses tratamentos, acabamos realizando um tratamento repetido. Acabamos, por exemplo, tipando os dados mais de uma vez, e isso é normal, mas é interessante que refatoramos essas etapas para que ela fique com o menor número de etapas possível.  
Se observarmos dentro do dataset pedidos, vemos que isso acontece. Temos um tipo alterado, e logo depois temos o tipo alterado 1, assim como cabeçalhos promovidos. Temos cabeçalhos promovidos e cabeçalhos promovidos 1. Podemos reduzir essas etapas aplicadas.   
Iremos utilizar o **editor avançado.**
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/db15e7e3-99a6-44a2-b121-f32fec89e878)  
Bastando deletar as linhas de comando referente a etapas repetidas.  
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/d1052826-c36c-4742-a37a-a12f73c1e9ea)
Por serem etapas encadeadas, iremos trocar o nome tipo alterado para o nome do dataset, para manter vínculo, e em seguida indicar o número 2 em linha removidas ao invés de 1.
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/99df4a8f-ec1b-4179-a52b-4e6b091f740b)  
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/dc468601-4122-4eff-b4ac-0665c7f64996)
Dessa forma reduziu número de etapas aumentando a performance no PQ e PBI.  
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/64560101-cf89-4399-9cf0-d906cf2264fa)  
Finalmente acessar o editor e renomear as etapas para manter o vínculo e aplicamos uma observaçao descritiva na etapa mesclada com o botão direto em propriedade.  
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/4343fb4c-58da-4ccc-9c45-1402486272f9)  
![image](https://github.com/ademarionobre/PowerBI/assets/92057489/a0c01793-3d4e-41f3-97e3-1b1c6c839030)![image](https://github.com/ademarionobre/PowerBI/assets/92057489/34250a19-f36c-4d14-965d-efeb96f6e435)

Esses procedimentos acima reduz tempo de aplica;áo no carregamento dos dados e facilita entendiemento de etapas.

# Desenvolvendo o Dashboard e publicando na web
