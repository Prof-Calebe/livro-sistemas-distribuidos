# Arquiteturas de sistemas distribuídos

## Cliente-Servidor
É realizado uma comunicação entre maquinas, as maquinas denomidadas como "servidores" são responsaveis por promover serviços
para as maquinas "cliente".
Vale resaltar que uma maquina pode executar diversos serviços podendo ser  cliente ou servidor.
Essa comunicação tem uma estruturação simples de requisição do cliente e resposta do servidor
Realizado atraves de protocolos de rede, como TCP/IP
Possue vatagens como  escalabilidade, segurança e confiabilidade.

Principais componentes de uma estrutura client-server:
- Cliente 
- Servidor
- Protocolos de comunicação
- Banco de dados
- Interface de programação de aplicativos (API)

Os recursos acima trabalham juntos para fornecer serviços ao Cliente.
A arquitura cliente-servidor é muito utilizado em infraestruturas de TI locais por conta de sua segurança, eficiência  e integração com outros sistemas.

## RPC/RMI
Chamadas Remotas de
Procedimentos (RPC)
O que é
É um protocolo que fornece o paradigma de comunicações de alto nível utilizado no sistema operacional.


Para que é usado
O RPC é usado para se comunicar entre processos em diferentes estações de trabalho em uma rede, além disso ele pode ser usado para realizar comunicações entre diferentes processos, ele torna possível a ligação dinâmica de programas remotos.

Vantagens do protoloco RPC
O RPC facilita o desenvolvimento de sistemas distribuídos.
Facilita a transferencia do gasto computacional para os servidores.

Limitações
Existem de possiveis atrasos e até possiveis falhas ao estabelecar o protocolo.Por conta do RCP precisar  de uma rede para se comunicar pode haver uma instabilidade.

Possiveis Problemas 
1. Cliente não consegue localizar o servidor
2. Mensagem de requisição do cliente para o
servidor é perdida
3. Mensagem de resposta do servidor para o
cliente é perdida

Utilização
Pode ser utilizar com TCP ou UDP


## Peer-to-Peer (p2p)
Comunicação feita de ponto a ponto,uma arquitetura de rede de computadores que se baseia na utilização de um servidor central usado para indentificar aqueles que requisitam um serviço.
Um dispodivo que faz parte da rede pode tanto receber dados quando disponibizar dados para outros dispositivos.
O exemplo mais comum de rede P2P utilizada é o torrent.

## Referências
- https://www.dimap.ufrn.br/~motta/dim070/Aula03.pdf
- Notas tiradas em aula