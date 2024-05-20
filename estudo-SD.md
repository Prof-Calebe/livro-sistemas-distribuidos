# CLUSTER
- Aglomerado de máquinas(nós)
- Visão de único sistema (single-image system)
- Implementação de Sistema Distribuído
- Utilização
	- Necessidade de alto porder computacional
-Sistema Distribuido = Descentralização das atividades, distribuiçao de recurso


# MPI
- Message-Passing Interface
- Interface que implementa primitivas de comunicação ponto-a-ponto e coletivas
- Responsável por todo o processo de estabeler comunicação
- Abstrai aspectos de protocolos de transporte

MPI usa o conceito de grupo - todo mundo faz parte de um mesmo grupo(comunicador) e cada processo é 
identificado por um "rank", um número.

Todos os processos são disparados (através de execução remota) nas máquinas determinadas. Nesse processo de
disparo o próprio startup do MPI já atribui um número ao processo(rank) o que facilita a comunicação
Uma máquina pode executar mais de um processo
Primitivas - comandos:
- MPI_Init - Inicia
- MPI_Comm_size - Número de processadores
- MPI_Comm_rank - Número(rank)
- MPI_Send - Envia
- MPI_Recv - Recebe
- MPI_Finalize - Sai do MPI

# Conceitos de Sistema Distribuido
Sistema Distribuido - coleção de computadores independentes que aparenta a seus
usuários ser um sistema único e coerente.
- Computadores independentes
- Um único sistema middleware
- Middleware - conecta programas separados e já existentes. Normalmente, fica entre a aplicação
e o SO.