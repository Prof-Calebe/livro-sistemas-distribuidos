# Sincronização

# Problemas da Sincronização

-   Os processos estão em máquinas que possuem horários diferentes (defasagem interna)
-   A hora dos relógios das máquinas estão diferentes do horário “real” (Defasagem externa)
-   Máquinas podem ter Clock de máquina diferentes, estão um relógio pode estar mais acelerado que o outro (defasagem variável)


# Por que é importante a sincronização de processos?

-   Aplicações bancárias
-   Aplicações de tempo real
-   Versionamento

## Sincronização de relógio

Partindo da premissa que processos que não se comunicam, não precisam sincronizar os seus relógios, eles apenas precisam “concordar” com a ordem dos eventos.

#### Relógio lógico

-   definem logicamente o tempo de cada evento
-   Relógios lógicos são usados onde não a necessidade de sincronizar o relógio precisamente, apenas determinar a ordem dos eventos.

#### Como funciona o Relógio lógico?

<p align="center"> 
  <img src="https://github.com/Fernandolin/livro-sistemas-distribuidos/blob/main/logico.png" alt="img">
</p>

A figura (a) mostra a conversa entre 3 processos.

**P1** envia **m1** (tempo 6) e **P2** recebe **m1** (tempo 16).

**P2** envia **m2** (tempo 24) e **P3** recebe **m2** (tempo 40).

O problema está na volta.

Quando **P3** envia **m3** (tempo 60) e **P2** recebe **m3** (tempo 56)

> Como **P2** está com o relógio **atrasado** em relação a **P3** e lembrando que relógios lógicos precisam **APENAS** garantir a **ORDEM** dos eventos, **P2** na Figura (b) captura o tempo de envio da mensagem **m3** de **P3** que é 60 unidade de tempo e adiciona 1 unidade de tempo no seu próprio relógio, com isso **P2** sincroniza logicamente a **ordem dos eventos**.

#### Relógio Físico

-   São para cenários onde o tempo precisa ser ajustado precisamente

- Um relógio bastante utilizado é o UTC.

#### Para sincronizar com relógios físicos, podemos usar o Algoritmo de Berkeley.

-   O servidor central pergunta para cada processo que horas são.
-   O servidor compara com tempo correto e pede para cada máquina ajustar o seu relógio (Lembrando que o servidor calcular o tempo da mensagem chegar em cada máquina e adiciona no ajuste)

<p align="center"> 
  <img src="https://github.com/Fernandolin/livro-sistemas-distribuidos/blob/main/fisico.png" alt="img">
</p
