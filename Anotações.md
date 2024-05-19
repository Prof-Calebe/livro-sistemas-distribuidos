## Manuscritos

![Imagem do WhatsApp de 2024-05-19 à(s) 00 25 48_9faff09c](https://github.com/AnaJessicaSS/livro-sistemas-distribuidos/assets/92233185/4aab26fb-3b25-47c6-9aca-40c6d377eda6)
![Imagem do WhatsApp de 2024-05-19 à(s) 00 25 47_ffe3d443](https://github.com/AnaJessicaSS/livro-sistemas-distribuidos/assets/92233185/b824f244-4890-453a-a4ab-051030447bdc)

***
 
## Sistemas Distribuídos

**O que é:** envolve vários computadores interconectados colaborando para executar determinadas tarefas.

**Vantagens:** escalabilidade, disponibilidade e tolerância a falhas.

**Desvantagens:** heterogeneidade, segurança, concorrência, escalabilidade e complexidade na comunicação.

***

## Arquitetura Cliente-Servidor

**Clientes:** Inicia solicitações, composta por interfaces de usuário, envia solicitações para servidores.

**Servidores:** recebe solicitações, fornece serviços, processa operações e retorna resultados.

**Comunicação:** por meio de protocolos de rede HTTP, TCP / IP, UDP, pode ser síncrono ou assíncrono.

**Vantagens:** escalabilidade, desempenho, flexibilidade e facilidade de manutenção.

**Desvantagens:** rede dependente, custo de infraestrutura, ponto único de falha e latência de rede.  

***

## Sistemas Peer-to-Peer

**O que é:** todos os nós possuem capacidades equivalentes, sem um servidor central.

**Autonomia:** cada nó é independente, robustez e resiliência aumentadas.

**Arquitetura:** pode ser tanto totalmente descentralizada, quanto híbrida.

**Distribuição de recursos:** Equilibrada entre os nós.

**Protocolos:** BitTorrent, Gnutella, Kademlia, etc.

**Aplicativos:** incluem compartilhamento de arquivos, comunicação, redes sociais etc.

**Vantagens:** escalabilidade, robustez, distribuição de carga, etc.

**Limitações:** gerenciamento de recursos, segurança, descoberta de pares.

***

## MPI – Message Passing Interface

**Definição:** padrão de comunicação para sistemas distribuídos, responsável pela comunicação via mensagens entre processos.  
<br/>**Características:** permite a troca de informações por processos em sistemas distribuídos, muito utilizado em paralelismo de computadores e clusters;

**Funcionamento:** as mensagens são enviadas e recebidas de forma assíncrona, podendo ser usadas para coordenar a execução de tarefas em máquinas diferentes.

**Principais Conceitos:**

- comunicação ponto a ponto – a troca de mensagens ocorre entre dois processos específicos;
- comunicação coletiva – a troca de mensagens ocorre entre grupos de processos.

**Vantagens:**

- Eficiência na troca de informações com processos;
- Mais fácil de implementar algoritmos paralelos e distribuídos;
- Pode ser implementado com outros modelos de programação paralela.

**Desvantagens:**

- Deve se ter conhecimento e familiaridade do padrão MPI;
- Maior sobrecarga devido a comunicações de grandes distâncias ou volumes de dados.

**Aplicações:**

- Simulações científicas e computação de alto desempenho;
- Análise distribuída;
- Processo grande dados com múltiplos computadores em clusters.

***

## Sincronização de relógios em um sistema distribuído

**Relógios de quartzo e atômicos:** relógios de quartzo são usados em computadores como base para relógios mantidos em software. Relógios atômicos são mais precisos e utilizados em sistemas de sincronização.

**Tempo Universal Coordenado(UTC):** padrão global para coordenar a medição da passagem do tempo, baseado em relógios atômicos.

**Sincronização de relógios:** é o procedimento de ajustar os relógios em diferentes dispositivos para que eles marquem o mesmo tempo.

**Algoritmo de Cristian:** usado para sincronizar relógios com uma fonte externa de tempo confiável,

**Algoritmo de Berkeley:** sincroniza vários relógios em um sistema distribuído.

**Network Time Protocol \[NTP\]:** protocolo para sincronização de relógios em redes de computadores, com camadas hierárquicas para garantir precisão.

**Precision Time Protocol \[PTP\]:** especificação IEEE para sincronização sub-microssegundo de relógios.

**Nunca voltar no tempo:** Evitar ajustes bruscos nos relógios para evitar problemas como dados com data de edição anterior à data de criação.

**Usos de relógios sincronizados:** ordenação de eventos, alocação de recursos, autenticação etc.
