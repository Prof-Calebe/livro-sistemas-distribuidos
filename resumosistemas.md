# MPI (Interface de Passagem de Mensagens)

MPI é um paradigma de programação para comunicação entre processos em computadores paralelos. Esse modelo facilita a comunicação entre processos em diferentes tipos de máquinas, e define um padrão de interface, tornando a funcionalidade melhor, fazendo com que o desenvolvimento de aplicações paralelas seja mais eficiente. É bastante utilizado em supercomputadores e clusters para diversos tipos de usos.

## Tipos de Comunicação:

### Mensagens Bufferizadas:
**Definição:** Armazenadas em buffer até que o destinatário esteja pronto.  
**Vantagem:** Remetente não precisa esperar.  
**Desvantagem:** Pode haver sobrecarga de memória.

### Mensagens Não Bloqueantes:
**Definição:** Envio/recebimento ocorre sem esperar pela conclusão.  
**Vantagem:** Maior responsividade.  
**Desvantagem:** Aumenta a complexidade do código.

### Mensagens Não Bufferizadas:
**Definição:** Sem armazenamento intermediário.  
**Vantagem:** Simplicidade de implementação.  
**Desvantagem:** Pode causar atrasos.

### Mensagens Bloqueantes:
**Definição:** Processo espera até que a operação seja concluída.  
**Vantagem:** Sincronização estrita.  
**Desvantagem:** Baixa utilização de recursos.

## Solução Trivial para MPI:
Dividir o conjunto de dados entre os processos.

## Per-to-per
É um modelo de comunicação sem intermediários, ou seja, cada processo comunica diretamente com outros processos. E relacionado com a MPI, essa característica é essencial para sincronizar e coordenar tarefas na computação paralela.

Cada processo pode enviar e receber mensagens, e há duas formas que isso pode ser feito:
- **Bloqueantes:** Cada processo espera a conclusão da comunicação;
- **Não Bloqueante:** Cada processo continua outras operações enquanto a comunicação ocorre.

**Vantagens:** É mais eficiente, pois diminui a latência, eliminando intermediários; e é flexível, pois permite a comunicação de forma direta, otimizando a aplicação.

**Obstáculos:** Essa comunicação direta resulta em um difícil gerenciamento de conflito, pois a comunicação pode causar colisões; e complexidade na sincronização das mensagens recebidas, para deixá-las na ordem correta.

# RMI (Remote Method Invocation)

## Definição:
RMI é um protocolo em Java que permite a comunicação entre objetos em diferentes máquinas virtuais Java como se estivessem no mesmo local.

## Componentes:
- **Servidor:** Executa objetos remotos acessíveis por clientes.
- **Cliente:** Obtém referências a objetos remotos e invoca métodos.
- **Registro RMI:** Armazena e fornece referências a objetos remotos.
- **Stub:** Representa um objeto remoto no cliente, traduzindo chamadas de método em solicitações RMI.

## Vantagens:
- **Carregamento Dinâmico de Código:** Classes de objetos remotos podem ser carregadas dinamicamente, liberando execução de novos serviços sem reinicialização do servidor.
- **Transparência de Rede:** Comunicação parece com chamadas de método Java regulares.
- **Flexibilidade:** Adequado para diversos tipos de aplicações distribuídas.

# Coletivas em Computação Distribuída
- **Scatter:** Envia e espalha dados entre processos.
- **Gather:** Recolhe dados de vários processos para um processo raiz.
- **Reduce:** Combina dados de vários processos em um único resultado, essa coletiva é bastante utilizada em Big Data.

# Sincronização e Relógios
- **UTC (Universal Time Coordinated):** Padrão de tempo universal.
- **NTP (Network Time Protocol):** Principal protocolo para sincronização de relógios.

- **Relógios Lógicos:** Identificam a ordem dos eventos sem considerar o tempo real.

- **Relógios Físicos:** Devem ser iguais entre si e não divergir do tempo real.

Problemas que podem ser levados em consideração, incluem a incapacidade de regredir e a dificuldade de medir com precisão a latência da rede.
"""