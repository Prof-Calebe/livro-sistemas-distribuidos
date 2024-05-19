# Sistema Distribuído

## Conceito
* Um sistema distribuído é composto por componentes autônomos que colaboram entre si. 
Um aspecto importante desses sistemas é que, para os usuários, sejam eles pessoas ou programas, 
a interação parece ocorrer com um único sistema coeso. 
Em outras palavras, embora os componentes operem de forma independente, 
eles devem funcionar de maneira integrada para proporcionar uma experiência de uso unificada.

## Metas

### Transparência
* **Acesso**: Ocultar diferenças entre arquiteturas de máquinas e no modo de acesso a um recurso.
* **Localização**: Os usuários não podem dizer qual é a localização física de um recurso no sistema.
* **Migração**: Situação onde os recursos podem ser relocados enquanto estão sendo acessados sem que o usuário ou a aplicação percebam.
* **Relocação**: Usuário pode continuar usando quando vão de um lugar a outro.
* **Replicação**: Ocultar que um recurso é replicado.
* **Concorrência**: Um recurso pode ser compartilhado por diversos usuários concorrentes, deixando esse recurso em estado consistente.
* **Falha**: Quando um usuário não percebe que um recurso deixou de funcionar bem.

### Abertura
Um **sistema distribuído aberto** é um sistema que oferece serviços com base em regras padronizadas, descrevendo a sintaxe e a semântica desses serviços.
* **Interopabilidade**: Até que ponto duas implementaçõoes de sistemas ou componentes de fornecedores diferentes devem coexisttir e trabalhar em conjunto.
* **Portabilidade**: Até que pinto uma aplicação desenvolvida para um SD A pode ser executada sem modificações em um SD diferente B que tem a mesma interface que A.

### Escalabilidade
Pela conectividade mindial estar se tornando tão comum e de fácil acesso e utilização, a escalabilidade se torna uma das mais importantes metas de projeto para desenvolvedores de SD.
* 1. Um sistema pode ser escalável em relação a seu tamanho.
  2. um sistema escalável é aquele no qual o usuário e os recursos podem estar longe um dos outros.
  3. Fácil de ser gerenciado
* **Problemas**: Uma escalabilidade grande geralmente apresenta perda na capacidade de desempenho.

### Ciladas
Algumas premissas falsas que todos adotam ao desenvolver uma aplicação distribuída pela primeira vez:
* 1. A rede é confiável.
  2. A rede é segura.
  3. A rede é homogênea.
  4. A topologia não muda.
  5. A latência é zero.
  6. A largura de banda é infinita.
  7. O custo de transporte é zero.
  8. Há só um administrador.
     
## Tipos de Sistemas Distríbuídos
* **Sistemas de computação distribuídos** 
* **Sistemas de informação distribuídos**
* **Sistemas de embutidos distribuídos**

# Processos

## Conceito
* O conceito de processos é originário do campo de sistemas operacionais e basicamente ele é exemplificado
como um programa em execução. Porém falando de Sistemas Distribuídos outras questões mostram ser de iguais ou até de maior importância.

### Modelos
Três modos de contruir um servidor

| Modelo     | Character |
| ---      | ---       |
| Threads | Paralelismo, chamadas bloqueadoras de sistemas         |
| Processo monothread     | Sem paralelismo, chamadas bloqueadoras de sistemas        |
| Máquina de estado finito     | Paralelismo, chamadas de sistemas não bloqueadoras        |

## Virtualização
Separação entre ter uma única CPU e ser capaz de fingir que há mais delas pode ser estendida também a outros recursos.
* **Objetivo** Estender ou substituir uma interface existente de modo a imitar o comportamento de um outro sistema.

## *Cliente x Servidor*

## Clientes
A importância e a tarefa é proporcionar aos usuários meios de interagir com servidores remotos <br>
Modos:
* 1. Para cada serviço remoto, a máquina cliente terá uma contraparte separada que pode contatar o serviço pela rede.
  2. Oferecer acesso direto a serviços remotos oferecendo somente uma interface

## Servidor
Processo que implementa um serviço especídifo em nome de um conjunto de clientes.
* Etapas:
* 1. Espera por uma requisição que vem de um cliente.
  2. Assegura que ela seja atentida.
  3. Espera pela próxima requisição.
  
