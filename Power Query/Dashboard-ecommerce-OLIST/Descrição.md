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

