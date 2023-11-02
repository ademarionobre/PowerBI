# Dashboard Manutenção - Indicadores MTTB e MTTR

## MTBF e MTTR - Esses dois indicadores de manutenção permitem calcular a confiabilidade e disponibilidade dos equipamentos.  
Ambos são indicadores de manutenção, utilizando dados do próprio equipamento para prever possíveis falhas e determinar índices como confiabilidade e eficiência da equipe de manutenção.  

- **MTBF** significa Mean Time Between Failures, ou **tempo médio entre as falhas**. Considera três intervalos: **a primeira falha**, **o retorno à operação após a manutenção**, e uma **nova falha**

- **MTTR** é a sigla para Mean Time To Repair, que pode ser traduzido como **tempo médio de reparo**. De maneira simplificada, é o tempo entre a falha e o momento em que o sistema volta a operar após a manutenção.

📊[Link Dashboard manutençao](https://app.powerbi.com/groups/me/reports/45a6ca0c-2359-4c53-affe-dd383bbf6ee0/ReportSection13dded9667c5f9d07511?bookmarkGuid=Bookmark074615979cabd95ce3bf)  

### Calcular o MTBF  
O cálculo do MTBF é feito com base em três variáveis:
- Tempo Real de Disponibilidade (TD): período em que o ativo irá operar, sem precisar de nenhuma interrupção para reparo;
- Tempo Total de Manutenção (TM): período em que o ativo ficou inerte em virtude de manutenção e falhas;
- P (Parada): quantidade de vezes que a máquina ficou ociosa devido ao reparo.

Fórmula do MTBF.  
Para obter o MTBF, subtraia o tempo de disponibilidade do tempo de manutenção, e divida esse número pela quantidade de paradas:  
MTBF = (TD - TM) / P  
O aumento do MTBF indica que as técnicas de manutenção ou análise estão sendo aplicadas com eficiência.  

Fórmula do MTTR  
Para saber o MTTR, divida o tempo total de reparo pela quantidade de paradas.  
MTTR = Tempo Total de Manutenção/Número de Paradas  

Quanto menor for o resultado do MTTR, melhor a performance da equipe de manutenção.
__________
👍🏼
