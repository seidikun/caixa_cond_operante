# caixa_cond_operante

O projeto é composto de um programa que opera como monitoramento de um experimento de condicionamento operante por reforço positivo de sagui-comum (Callithrix jacchus) dentro de uma caixa limitadora em que o ambiente é controlável.
O animal é treinado a tocar uma de duas barras, cada uma associada a um som típico de vocalização (phee ou trill), ao receber recompensa quando toca a barra correta após o estímulo sonoro.

O programa que faz esse monitoramento é caixa_cond_operante.py, disponível neste repositório. Ele leva em conta se o animal experimental possui habituação à caixa condicional operante e então realiza uma sequência de observações de treino, em que:
- é detectada sua aproximação a uma das barras
  - quando ocorrer, uma recompensa é dada 
- um dos dois tipos de sons vocalizados é emitido, cada um correspondendo a uma barra
- é detectado o toque a uma das barras
  - se a barra tocada for a correta, novamente o animal ganha recompensa
  - caso contrário, nada acontece
  
O treino é temporizado e 3 finalizações são possíveis:
1. O animal tocou pelo menos 20 vezes as barras corretas antes do esgotamento do tempo
2. O animal tocou 50 vezes as barras corretas antes do esgotamento do tempo
3. O animal não conseguiu tocar a quantidade mínima de vezes e o tempo esgotou

**Importante**:
- foram utilizadas bibliotecas auxiliares numpy.random, para gerar número randômico, e time, para gerar pausa temporizada durante a execução do código.
- foi criada uma função, devido à clareza de leitura de código que ela trás
