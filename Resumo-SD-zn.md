# Introdução

### O que é um Sistema Distribuído ?

Sistema distribuído é o conjunto de computadores independentes, que conectados por uma rede, que atua como um único sistema na visão do usuário final.

### O que é um Middleware ?

---

É um software intermediário que trabalha entre os softwares e os sistemas operacionais.

A função do middleware é fazer com que a aplicação entre em contato com o sistema operacional de cada computador, permitindo a troca de informações entre sistemas de diferentes computadores, auxiliando com que no funcionamento e trabalho dos sistemas de forma distribuída.

<div align="center">
  
![middleware](https://i.imgur.com/nTWXnr1_d.webp?maxwidth=760&fidelity=grand)

</div>

---

## Arquitetura Cliente - Servidor

### O que é Arquitetura Cliente - Servidor?

É um modelo onde o cliente solicita dados/serviços/recursos (enviando solicitações) e o servidor fornece (processa e responde as solicitações).

Comunicação entre eles pode acontecer via sockets.

<div align="center">
  
![cliente_servidor](https://i.imgur.com/nZUkQD9_d.webp?maxwidth=760&fidelity=grand)

</div>


### Qauntos processos tenho no mínimo em uma arquitetura centralizada cliente - servidor?

2 processos (cliente e servidor)

### Qual a primeira stack de sistema de software depois de hardware?

O Sistema Operacional.

---

## Arquitetura Peer to Peer (P2P)

### O que é?

É um modelo descentralizado onde cada nó atua como cliente ou servidor.

Tipo torrent.

---

## Outros tipos de arquiteturas

### N camadas e Microservicos

N camadas - divide a aplicacao em varias camdas onde cada uma pode ser distribuida em diferentes servidores.

Microservicos - conjunto de servicos independentes onde cada um executa um processo diferente e se comunicam via API, por exemplo.

---

## Processos e Threads

### O que é? - Procesos

Entidades que possuem seu proprio espaco de memoria e executam programas.

### O que é? - Threads

Usam mesmo espaco de memeoria do processo pai e sao subdivisoes do processo pai.

---

## HTTP

### O que é HTTP?

É um protocolo composto or Header, Blank line e Body que possui porta padrão 80. (HTTPS - 443)

O HTTPS é criptografado (segurança), diferente do HTTP onde qualquer host consegue fazer uma requisição.
