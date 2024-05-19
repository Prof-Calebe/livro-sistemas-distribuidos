**Sistemas Distribuídos**

**Definição:** “Conjunto de sistemas computacionais que realizam algum tipo de comunicação o qual o usuário não consegue ver”

**Metas e desafios de SD**

Facilidade de uso, Transparência, Heterogeneidade, Concorrência e Sincronização de processos, Abertura, Segurança, Escalabilidade e Transparência

**Pergunta:** Como garantir a escalabilidade?

R: Através de uma infraestrutura robusta, balanceamento de carga e replicação dos dados.

**Distribuição dos dados:**

- Replicação de dados: cópias dos dados, armazenadas em vários nós
- Particionamento: dados são divididos em partes menores e armazenados em diferentes nós.

**Sistemas Centralizados:** o servidor gerencia todos os dados e processos

**Sistemas Descentralizados:** os dados e processos são distribuídos através de vários computadores (nós) 

**Modelos de Arquiteturas de Sistemas Distribuídos**

- Cliente - Servidor
  - Centralizada
- Camadas
  - divisão do software em camadas com interfaces bem definidas
- Peer-to-Peer (P2P)
  - não existe hierarquia e todos os nós podem ser clientes e servidores
- Híbrido
  - combinação de diferentes modelos para atender as necessidades da aplicação

**Pergunta: Como os nós se comunicam entre si?**

R: através de protocolos de comunicação, mensagens síncronas e assíncronas e ordenação de mensagens 

**Protocolo**

- Regra de comunicação, ambos os lados precisam ter para se comunicar

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.001.png)

Cliente - Servidor: Arquitetura Centralizada (AC) → Vulnerável

`					`Vs

Melhor alternativa: Arquitetura Híbrida / Distribuída (AD)

**Pergunta: “Quantos processo temos numa arquitetura centralizada cliente-servidor?**

R: 2, 1 para cliente, 1 para servidor

**Arquitetura Centralizada** - 2 processos

**Arquitetura Distribuída** - mais que 2 processos → vários pedaços de software distribuídos

para isto: 

- Protocolo → sem resposta definitiva, durante os processos, os nós podem conversar uns com os outros

**Pontos Positivos de Sistemas Distribuídos:**

- Escalabilidade
- Distribuição de carga
- Tolerância à falhas
- Flexibilidade

**Pontos Negativos de Sistemas Distribuídos:**

- Comunicação e rede
- Alto custo de infraestrutura
- Segurança
- Complexidade

**Comunicação Ponto-a-Ponto ou Peer-to-Peer**

- Num grupo, todos os pedaços do software podem conversar uns com os outros para resolver um problema
- pedaços ou nós independentes
- Alta escalabilidade, distribuição de carga 
- Arquitetura Híbrida ou Descentralizada

**Comunicação: 					Mensagem**

- Ponto-a-Ponto:				- Bufferizada / Não Bufferizada
- Comunicação Coletiva			- Bloqueante / Não Bloqueante

**Mensagem:** 

- **Bufferizada:** a mensagem é armazenada num buffer antes de ser enviada, garantindo que a mensagem não seja perdida caso o destinatário esteja indisponível
- **Não Bufferizada:** a mensagem é enviada diretamente ao destinatário sem ser armazenada no buffer, podendo resultar na perda da mensagem

- **Bloqueante:** um processo só será executado assim que a mensagem seja confirmada como recebida pelo destinatário
- **Não bloqueante:** um processo pode ser executado sem precisar esperar a confirmação da mensagem recebida

“Um Sistema Distribuído, tem escalabilidade ou tolerância à falhas, se há um, não há outro”

**Arquitetura Distribuída (AD)**

- MPI → Peer-to-Peer e Coletiva

  Obrigatoriamente tem estrutura fechada

**Pergunta: Na perspectiva do Broadcast, o que significa a primitiva ser Não Bufferizada e Bloqueante?**

**R:** Todos os outros processos irão esperar todos os demais terminarem de receber a mensagem e o P0 terminar os envios para que possa continuar o resto das instruções do processo.

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.002.jpeg)		**OU**	    ![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.003.jpeg)

`	   	`figura 1						      figura 2

Na figura 1, nota-se que é visível a ordem dos processos, partindo do Processo 0, até o 6°, resultando em 6 tempos.

Na figura 2. redesenhando o modelo de entrega, a mensagem é enviada para o processo à direita, num tempo 1, considere este o P1. Já que ambos P0 e P1 possuem a mensagem, ambos enviam a mesma, para outros processos, num tempo 2, considerando os processos deste tempo de P3 e P4.

Note, que na figura 2, é possível alcançar 8 processos, em apenas 3 unidades de tempo, enquanto na figura 1, foi necessário 7 tempos para alcançar o mesmo número de processos.

**Porém há um problema:** a latência da rede e a largura da banda podem causar a colisão entre mensagens, não garantindo a entrega da mensagem no processo.

**MPI Scatter:** distribuição da informação entre todos os processos participantes do grupo

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.004.png)

**MPI Gather:** inverso do Scatter, este recebe a informação dos processos

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.005.png)

**MPI Reduce:** realiza a redução de um espaço com vários processos a um espaço único para melhor entendimento dos dados

Comunicação entre processos: 

- Ponto-a-Ponto → Não Bufferizada e Bloqueante
- Coletiva

**Sincronização**

Se ocorrem dois eventos em um Sistema Distribuído, como decidir quem ocorreu primeiro?

R: Baseado no tempo do computador 1, ele será o primeiro, e com base no tempo de um computador 2, o 2 terá ocorrido primeiro.

**Relógios de Quartzo:** devido ao efeito Piezoelétrico, vibra a 32768 = 2^15 Hz³ e podem errar na medição do tempo no máximo 1/2s por dia

**Relógios Atômicos:** utilizam das transições de energia entre átomos para adquirir uma medição de tempo mais precisa, além de fornecerem um tempo preciso para calcular posições de GPS

**Tipos de defasagem:**

- Defasagem interna: acontece quando na comparação entre os relógios internos, os tempos diferem um do outro.
- Defasagem externa: ocorre quando, os relógios diferem da hora real externa
- Defasagem variável: ocorre quando os clocks dos relógios diferem uns dos outros, ou seja, um relógio está mais acelerado ou está mais desacelerado

**Aplicações da Sincronização:**

- Identificar mensagens 
- Aplicações de tempo real: sistema de monitoramento de uma usina nuclear
- Controle de versões: se a versão de uma aplicação está atualizada ou não

**Sincronização de Lamport:**

A Sincronização do relógio não precisa ser absoluta

- Se dois o processos não interagem entre si, não precisam ser sincronizados

**Relógios Lógicos:**

- Necessidade da consistência interna dos relógios
- Ordem dos eventos 
- Em suma: dizer qual evento ocorreu primeiro

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.006.png)



**Relógios Físicos:**

- Usado somente quando os relógios devem ser iguais e não diferentes do tempo real 
- Algoritmo de Berkeley: permite sincronizar múltiplos nós uns com os outros. Este algoritmo assume o que não há uma "fonte da verdade" do tempo, mas sim a necessidade de que todos os processos convirjam para um mesmo valor do relógio.

**Algoritmo de Berkeley**

![](Aspose.Words.53652099-0f25-49b4-bdd5-ebc470560d9c.007.png)

1. Primário pergunta que horas são e verifica a hora
1. Secundário 1 e Secundário 2 respondem com o valor do relógio e é calculada a diferença entre ambos 
1. No horário atual, os ajustes são enviados para os Secundários


**Global Positioning System (GPS):** Sistema que usa satélites para fornecer tempo preciso e determinar a posição de receptores por trilateração. Receptores sincronizados com os satélites calculam a distância e posição.

Para determinar a posição de um dispositivo, o GPS usa sinais de sinais de satélite para triangulação, por padrão, são necessários no mínimo 4 satélites, 3 para localização geográfica e 1 para verificação do tempo

**Coordinated Universal Time (UTC):**  padrão global baseado através da média de relógios atômicos ao redor do mundo. Define fusos horários com base na rotação da Terra e garante uma referência precisa e consistente para a medição do tempo em escala global.

**Algoritmo de Cristian:** usa o relógio do cliente para ajustar o tempo com base na latência da rede.

**Network Time Protocol (NTP):** protocolo utilizado para sincronização de tempo em redes de computadores, organizando os  dispositivos em camadas hierárquicas para garantir níveis de sincronização diferentes

**Precision Time Protocol (PTP):** utilizado para sincronização de tempo sub-microssegundo em redes, utilizando interfaces de rede especializadas para marcar eventos com alta precisão. .

**Nunca mais voltar no tempo:** se está sincronizado e funcional, não se deve fazer grandes alterações no relógio para evitar a dessincronização.

**Perguntas**

Qual é o impacto da falta de sincronização precisa de tempo em uma rede de computadores?

R: Causa diferenças nos registros de logs entre servidores.

Por que é importante usar UTC para sincronização de tempo em sistemas distribuídos?

R: O UTC garante um padrão de tempo consistente independente da localização
