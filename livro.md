## Sincronização

### Introdução

Diferente de um sistema local, o sistema distribuído não possui uma memória compartilhada, pois possuem computadores diferentes, com processadores diferentes, e assim, memórias diferentes. Por se tratar de um ambiente com diversas variáveis, é necessário trabalhar com a sincronização. 

A sincronização é uma solução utilizada para problemas de ordem de eventos, no caso de qual evento precede o outro, defasagem interna, onde os computadores tem diferenças de hora entre si, defasagem externa, onde a hora do computador é diferente da real, entre outros.

Existem dois tipos principais de Relógios e suas formas de sincronização, os relógios lógicos e físicos.

### Relógios Lógicos

Os relógios lógicos são aqueles que não precisam necessariamente ser sincronizados ao horário real, mas sim a ordem em que os eventos dentro de um sistema ocorre. Para isso, os eventos tem de se comunicar, caso contrário, não há necessidade de sincronização, visto que não existe interação entre os processos.

Como o algoritmo de Lamport mostra, a forma de ordenar os eventos dos processos ocorre pela sincronização entre processos participantes. O processo posterior sempre se ajusta a contagem do processo anterior.

![relogio_logico](https://i.imgur.com/Uo1uoT2_d.webp?maxwidth=760&fidelity=grand)

### Relógios Físicos

Os relógios físicos são aqueles que que são sincronizados fisicamente com o horário real, este podendo ser baseado em GMT, TAI ou o mais famoso, UTC (Universal Coordinated Time).

Diferente do algortimo de Laport, um algoritmo proposto para a solução é o de Berkeley, que não efetua a sincronização entre eventos e processos, mas sim sincroniza o relógio dos computadores com o tempo exato e real.

O algoritmo é composto pelo Servidor de Tempo (Daemon), e as máquinas (computadores), onde o servidor "pergunta” tempo que cada máquina possue, e com base nas respostas, envia o tempo real e correto para ser ajustado nos computadores.

![relogio_fisico](https://i.imgur.com/wF67SMR_d.webp?maxwidth=760&fidelity=grand)

Vale lembrar que outro ponto levado em conta, no algoritmo de Berkeley, é o tempo em que a resposta chega da máquina até o servidor e vice-versa, além do atraso de entrega de informação da rede, sempre levando em conta esse tempo 
necessário para entrega de informação na hora do ajuste do relógio.

---

## Mais sobre o tema

Existem alguns outros conceitos e elementos pertencentes do tema, sendo esses:

- Relógios de Quartzo
- Relógios Atômicos
- GPS
- NTP
- PTP

### Relógios de Quartzo
Esses relógios possuem esse nome pelo fato de possuirem literalmente um elemento de quartzo em sua composição, que em formato de garfo, vibra numa frequência 32768 Hz,
que são transformados em energia mecânica para o funcionamento do relógio.

![quatz](https://i.imgur.com/T0KIual_d.webp?maxwidth=760&fidelity=grand)

### Relógios Atômicos
Este tipo de relógio leva esse nome por utilizar uma frequência energética a partir de átomos de césio ou rubídio. Um pouco diferentes dos de quatzo, os relógios atômicos 
vibram a uma frequência de 9192631770 Hz, sendo extremamente estáveis e menos suscetíveis a variações por motivos externos, como mudança de temperatura, envelhecimento, os 
tornando muito mais precisos.

![atomic](https://i.imgur.com/87RsbTD_d.webp?maxwidth=760&fidelity=grand)

### GPS
O Global Positioning System é uma rede de satélites que trasmitem vários sinais para a terra, como o tempo e localização. As máquinas em terra captam sinais dos satélites
para a sincronizar com relógios atômicos deles, usando trilateração para determinar a posição e o tempo com alta precisão.

![gps](https://i.imgur.com/s7zGk03_d.webp?maxwidth=760&fidelity=grand)

### NTP
Utilizado para a sincronização de relógios entre computadores de uma mesa rede, o Network Time Protocol funciona pode funcionar de forma similar ao algoritmo de Berkeley, 
onde o um cliente solicita as informações sobre o horário atual, e o servidor fornece informações para que esse ajuste o seu relógio de acordo. O NTP também pode operar de 
modo que envie informações para vários cliente ao mesmo tempo, como um broadcast.

![ntp](https://i.imgur.com/j9PP59x_d.webp?maxwidth=760&fidelity=grand)

### PTP
Similar ao NTP, o Precision Time Protocol, no geral, trabalha com uma forma mais precisa de ajuste e sincronização de horário, com a precisão na faixa de nanosegundos, 
que é possivel com a implementação de hardware mais sofisticado junto a algoritmos mais complexos, geralmente utilizados em sistemas que precisam de extrema precisão temporal, 
como sistemas financeiros.

![ptp](https://i.imgur.com/esdUvO5_d.webp?maxwidth=760&fidelity=grand)
