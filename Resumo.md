## <a name="_ouoh1vfi41f1"></a>O que são processos?
- Unidades de programa em execução com estado próprio.
- Possuem contador de programa e área de memória.
- Essenciais para a execução de tarefas de forma concorrente e independente em sistemas operacionais.

**Composição Detalhada de um Processo:**

- **Área de Texto:** Armazena o código-fonte do programa em execução.
- **Área de Dados:** Contém variáveis ​​e outras estruturas de dados utilizadas pelo programa.
- **Área de Stack:** Gerencia a execução de funções e chamadas de método.

**Ciclo de Vida de um Processo:**

- **Criação:** Alocação de recursos e inicialização do processo.
- **Execução:** O processo é executado pelo sistema operacional.
- **Espera:** O processo aguarda a liberação de recursos ou a conclusão de outras tarefas.
- **Pronto:** O processo está pronto para ser executado novamente.
- **Termino:** O processo é finalizado e seus recursos são liberados.

**Sistemas Operacionais e Threads**

- **Gerenciamento de Processos:**
  - **Escalonamento:** Define a ordem de execução dos processos.
  - **Sincronização:** Garante que os processos acessem recursos compartilhados de forma ordenada.
  - **Comunicação entre processos:** Permite que os processos troquem informações.
## <a name="_y9tlwfi7nag"></a>Sistemas Distribuídos
**O que são Sistemas Distribuídos?**

- São conjuntos de computadores interconectados que se comunicam e colaboram para realizar uma tarefa específica.
- Apresentam vantagens como escalabilidade, disponibilidade, tolerância a falhas e flexibilidade.
- Trazem desafios como heterogeneidade, segurança, confiabilidade e gerenciamento de concorrência.

  |Distribuição horizontal|Distribuição vertical|
  | :-: | :-: |
  |<p>Distribuição dos recursos de processamento e armazenamento em diversos computadores.</p><p></p>|Distribuição dos recursos em camadas, com diferentes níveis de abstração.|

**Desafios:**

- **Transparência:** Alcançar total transparência nos sistemas distribuídos é um desafio, afetando a experiência do usuário e a integração com outros sistemas.
- **Heterogeneidade:** A heterogeneidade dos ambientes computacionais dificulta o desenvolvimento de software funcional em diversos equipamentos. 
- **Concorrência e Qualidade de Serviço:** Garantir a concorrência justa e a qualidade de serviço em ambientes distribuídos é crucial para evitar gargalos e falhas. 
- **Formatos de Comunicação:** A utilização de formatos de comunicação complexos, como JSON, pode trazer desafios de performance e legibilidade. 
- **Escalabilidade:** A escalabilidade é discutida em diferentes cenários, como ambientes de nuvem versus híbridos, considerando o impacto financeiro.

**Conceitos Básicos:**

- **Entidade:** Representa um objeto ou componente do sistema.
- **Serviço:** Encapsula um conjunto de funcionalidades oferecidas por uma entidade.
- **Nome:** Identifica uma entidade de forma única no sistema.
- **Endereço:** Indica a localização de uma entidade na rede.
- **Comunicação:** Permite que as entidades troquem informações.

**Exemplos de Sistemas Distribuídos:**

- Internet
- Redes sociais
- Sistemas de e-commerce
- Sistemas de jogos online
- Serviços de streaming

**Exemplo Detalhado: Sistema de Distribuição de Conteúdo (CDN)**

- Usa uma rede de servidores para distribuir conteúdo para usuários em diferentes localizações.
- **Objetivo:**
  - Reduzir o tempo de resposta para os usuários.
- **Funcionamento:**
  - O conteúdo é replicado em vários servidores da rede.
  - Quando um usuário solicita o conteúdo, ele é direcionado para o servidor mais próximo.
  - O processo pode ser otimizado migrando processos para servidores com menor tempo de resposta.

**Tipos de Arquiteturas:**

- **Cliente-servidor:** Um servidor fornece serviços aos clientes.
- **Multicamada:** Os componentes do sistema são organizados em camadas com diferentes responsabilidades.
- **Peer-to-peer:** Todos os computadores no sistema desempenham funções semelhantes.
- **Híbrido:** Combinação de diferentes modelos para atender às necessidades específicas da aplicação.
- **Threads:**
  - Permitem que um processo seja dividido em tarefas menores que podem ser executadas em paralelo.
  - **Benefícios para sistemas distribuídos:**
    - **Paralelismo:** Permite que várias tarefas sejam executadas ao mesmo tempo.
    - **Concorrência:** Permite que várias tarefas competem por recursos.

**Sistema de Nomeação e DNS:**

- Exemplo de sistema de nomeação amplamente utilizado na internet.
- Traduz nomes de domínio legíveis por humanos em endereços IP numéricos.
- Fornecem mecanismos para localizar serviços dentro do sistema distribuído.
- Permite localizar serviços dentro do sistema.

**Middleware e Integradores de Software:**

- Facilitar a comunicação entre diferentes partes de um sistema distribuído, independentemente da arquitetura subjacente.
- Simplifica a integração e interoperabilidade entre componentes heterogêneos.
- Reduz a complexidade do desenvolvimento e da manutenção.
- Aumenta a flexibilidade e a escalabilidade do sistema.
- **Serviços:**
  - Tradução de protocolos.
  - Roteamento de mensagens.
  - Gerenciamento de transações.


## <a name="_fpfhla7d9sup"></a>**Arquiteturas Centralizadas vs. Descentralizadas**

##

|<a name="_uttlb4iclua"></a>Característica|Arquitetura Centralizada|Arquitetura Descentralizada|
| :- | :- | :- |
|Conceito|Um único ponto de controle gerencia todos os recursos e dados do sistema.|Ausência de um ponto de controle central, com tarefas e decisões distribuídas entre diversos nós.|
|Arquitetura|Em camadas, com servidor central.|Distribuída, sem servidor central.|
|Nomeação de Serviços|Centralizada.|Distribuída.|
|Pontos de Falha|Únicos: Falha do componente central compromete todo o sistema.|Múltiplos: Falha de um nó não impacta todo o sistema.|
|Escalabilidade|Limitada: Dificuldade em lidar com o aumento da demanda.|Alta: Capacidade de lidar com um grande número de usuários e dados.|
|Tolerância a Falhas|Baixa: Falha do componente central compromete todo o sistema.|Alta: Menos suscetíveis a falhas, pois não dependem de um único ponto de controle.|
|Gerenciamento|Centralizado: Fácil de implementar e gerenciar.|Mais complexo: Maior dificuldade de projetar e gerenciar.|
|Segurança|Menor superfície de ataque.|Maior superfície de ataque, exigindo mecanismos de segurança robustos.|
|Flexibilidade|Menor: Dificuldade em se adaptar a novas necessidades.|Maior: Podem ser facilmente adaptados a novas necessidades.|
|Democracia|Centralizada: Poder de decisão concentrado em um único ponto.|Distribuída: Poder de decisão distribuído entre os participantes da rede.|
|Custo de Implementação|Baixo: Menor investimento inicial.|Alto: Maior investimento inicial.|
|Custo de Manutenção|Baixo: Fácil de diagnosticar e solucionar problemas.|Alto: Maior dificuldade em diagnosticar e solucionar problemas.|
## <a name="_c4vvfqk3y8i"></a>MicroServiços vs. Monolíticos
**Qual escolher?**

- **Monolítica:**
  - Aplicativos simples
  - Priorizar facilidade de desenvolvimento e gerenciamento
- **Microsserviços:**
  - Aplicativos complexos que precisam de escalabilidade e resiliência
  - Priorizar facilidade de manutenção e desenvolvimento de novas funcionalidades
##

|<a name="_1fnx05qvqvrb"></a>Característica|Monolítica|Microsserviços|
| :- | :- | :- |
|Implementação|Simples: A simplicidade inicial da arquitetura monolítica pode dificultar mudanças complexas no futuro.|Complexa: Microsserviços exigem mais tempo e esforço no início, mas oferecem maior flexibilidade a longo prazo.|
|Gerenciamento|Simples: O gerenciamento de uma aplicação monolítica é mais intuitivo (um único código-fonte)|Complexo: Microsserviços exigem ferramentas e expertise específicos para gerenciar diversos serviços interligados.|
|Escalabilidade|Difícil: Escalar verticalmente (adicionando recursos a um único servidor) em monolitos pode ser desafiador.|Fácil: Microsserviços permitem escalar horizontalmente (adicionando mais servidores) de forma mais granular e eficiente.|
|Manutenção|Difícil para aplicativos complexos: Encontrar e corrigir bugs em monolitos complexos pode ser trabalhoso. |Fácil: Microsserviços facilitam a identificação e o isolamento de problemas, pois cada serviço é um módulo independente.|
|Resiliência|Baixa: Se um componente da aplicação monolítica falhar, todo o sistema pode ser afetado.|Alta: Microsserviços, por serem independentes, podem tolerar falhas em um serviço sem impactar todo o sistema.|
|Desenvolvimento de novas funcionalidades|Difícil: Adicionar novas funcionalidades em uma aplicação monolítica pode ser lento e arriscado.|Fácil: Microsserviços permitem desenvolver e implementar novas funcionalidades de forma mais rápida e segura, pois cada serviço pode ser modificado independentemente|
|Monitoramento|Simples: Monitorar uma aplicação monolítica é simples (um único ponto de acesso para coletar métricas). |Complexo: Microsserviços exigem ferramentas e técnicas mais robustas para monitorar diversos serviços interligados.|
|Custo de infraestrutura|Menor: O custo inicial de infraestrutura para uma aplicação monolítica pode ser menor (roda em um único servidor).|Maior: Microsserviços exigem mais servidores para distribuir os serviços (aumento inicial do custo). A longo prazo, a escalabilidade horizontal pode levar a um custo total de infraestrutura menor.|
|Segurança|Mais fácil: Implementar medidas de segurança em uma aplicação monolítica pode ser mais fácil (um único ponto de ataque).|Mais difícil: Em microsserviços, a segurança se torna mais complexa (multiplicidade de serviços e necessidade de proteger cada um individualmente).|
|Desempenho|Pode ser menor: O desempenho de uma aplicação monolítica pode ser afetado pela interdependência dos seus componentes. |Pode ser maior: Microsserviços podem oferecer melhor desempenho, pois permitem distribuir o processamento entre diversos servidores e otimizar a utilização de recursos.|
|Confiabilidade|Mais alta: A arquitetura monolítica, por ser um sistema único, pode apresentar maior confiabilidade geral. Se um componente falhar, todo o sistema pode ser afetado. |Mais baixa: Microsserviços, por serem mais resilientes a falhas em serviços individuais, podem ter uma confiabilidade geral menor, mas com menor impacto em caso de problemas.|
|Simplicidade|Mais simples: A simplicidade da arquitetura monolítica facilita o aprendizado e a manutenção para equipes pequenas. |Mais complexa: Microsserviços exigem maior conhecimento técnico e podem ser mais desafiadores para gerenciar, especialmente em projetos de grande escala.|
|Transparência|Menos transparente: A interdependência dos componentes em uma aplicação monolítica pode dificultar a compreensão do funcionamento do sistema como um todo.|Mais transparente: Microsserviços, por serem modulares e independentes, oferecem maior transparência, facilitando o entendimento e a depuração de problemas.|
|Concorrência|Mais difícil: Implementar concorrência em uma aplicação monolítica pode ser desafiador (interdependência dos componentes). |Mais fácil: Microsserviços facilitam a implementação de concorrência, pois cada serviço pode ser executado em paralelo, otimizando o desempenho e a utilização de recursos.|



## <a name="_hrl5nlfzqo4"></a>Migração
**O que é?**

A migração de processos é o ato de mover um processo de uma máquina para outra.

**Vantagens:**

- **Balanceamento de carga:** distribuir o trabalho entre as máquinas para evitar sobrecarga.
- **Manutenção:** mover processos durante manutenções ou falhas em máquinas.
- **Atualizações de software:** implementar novas funcionalidades em máquinas atualizadas.
- **Desastres naturais:** proteger dados críticos em ambientes seguros na nuvem.
- **Tolerância a falhas:** mover processos para outros nós em caso de falhas.
- **Otimização de desempenho:** mover processos para nós com recursos mais adequados.

**Desafios:**

- **Heterogeneidade de ambientes:** diferenças de hardware, software e sistemas operacionais podem gerar incompatibilidades.
- **Dependências complexas:** identificar e gerenciar dependências de outros processos, serviços e recursos de rede.
- **Impacto na disponibilidade:** indisponibilidade temporária do processo durante a migração.
- **Garantia da integridade dos dados:** garantir a transferência completa e precisa dos dados para o novo ambiente.
- **Validação rigorosa:** realizar testes exaustivos para garantir o funcionamento correto no novo ambiente.

**Soluções:**

- **Virtualização:** usar máquinas virtuais para isolar processos e alocar recursos de forma eficiente.
- **Sincronização:** garantir a consistência dos dados e evitar conflitos em sistemas multiprocessados.
- **Mecanismos de sincronização:** semáforos, monitores e mutexes para controlar o acesso a recursos compartilhados.

**Abordagens de Migração:**

- **Manual:** transferência manual do processo e do seu estado, com risco de erros.
- **Automática:** ferramentas e scripts para automatizar o processo, reduzindo erros e otimizando o tempo.
- **Contínua:** transferência incremental do estado do processo, minimizando o impacto no desempenho.

**Exemplos de Uso:**

- **Nuvem:** balanceamento de carga de trabalho entre data centers.
- **Sistemas de alta disponibilidade:** garantir a execução de aplicativos mesmo com falhas em servidores.
- **Sistemas distribuídos:** mover tarefas entre diferentes nós.

**Vantagens:**

- **Escalabilidade:** aumentar a capacidade de processamento e armazenamento distribuindo tarefas.
- **Confiabilidade:** maior tolerância a falhas, pois a falha de um componente não compromete todo o sistema.
- **Disponibilidade:** maior disponibilidade de serviços, pois os recursos podem ser redirecionados em caso de falhas.

### <a name="_vjli4m3u5fqw"></a>Tipos de migração
##

|<a name="_dohcfv5rmut2"></a>|Descrição|Vantagens|Desvantagens|Exemplos|Cenários Ideais|
| :- | :- | :- | :- | :- | :- |
|Forte|Transfere todo o estado do processo, incluindo memória, arquivos abertos e descritores de rede.|<p>Máxima confiabilidade e robustez.</p><p></p><p>Ideal para processos críticos ou ambientes diferentes.</p>|<p>Complexa e demorada. </p><p></p><p>Requer mais recursos de rede e computação.</p>|Migração de máquina virtual.|<p>Processos que não podem ter interrupções. </p><p></p><p>Migração entre ambientes heterogêneos.</p>|
|Fraca|Transfere apenas parte do estado do processo, como a memória e os arquivos abertos.|<p>Rápida e simples. </p><p></p><p>Menor consumo de recursos.</p>|<p>Menos confiável e robusta.</p><p></p><p>O processo pode precisar ser reiniciado.</p>|<p>Recarregar uma página da web.</p><p></p><p>Transferência de arquivos pequenos.</p>|<p>Processos tolerantes a interrupções curtas. </p><p></p><p>Migração dentro do mesmo ambiente.</p>|
|Código|O código do processo é migrado para o novo nó e o processo é reiniciado.|Simples e fácil de implementar.|<p>Ineficiente para código grande ou reinicializações frequentes. </p><p></p><p>Pode perder parte do estado do processo.</p>|<p>Recompilação de software.</p><p></p><p>Atualização de aplicativos.</p>|<p>Código fonte leve e com pouca dependência de estado.</p><p></p><p>Migração frequente de processos.</p>|
|Dados|O estado do processo é migrado para o novo nó, mas o código do processo permanece no nó original.|<p></p><p></p><p>Mais eficiente do que a migração de código.</p>|<p></p><p></p><p>Complexa para estado de processo grande ou acesso a arquivos no nó original.</p>|<p>Sincronização de arquivos. </p><p></p><p>Replicação de bancos de dados.</p>|<p></p><p></p><p>Processos com grande volume de estado, mas código estável. </p><p></p><p>Migração entre ambientes com código similar.</p>|
|Máquina Virtual|Todo o ambiente de execução do processo, incluindo o sistema operacional e os arquivos, é migrado para o novo nó.|Máximo isolamento e portabilidade. <p></p> Ideal para processos críticos ou ambientes completamente diferentes.|Mais complexa e exige mais recursos.|<p>Migração de servidores em nuvem. </p><p></p><p>Consolidação de infraestrutura.</p>|<p>Processos sensíveis a mudanças de ambiente. </p><p></p><p>Migração para ambientes com alta disponibilidade.</p>|

## <a name="_5legkqhtup9g"></a>Ligação Forte x Ligação Fraca
**Ligação Forte de Código**

Uma **ligação forte de código** indica que um processo depende de elementos específicos da máquina em que está sendo executado. Isso significa que, ao migrar o processo para outro ambiente, ele precisa ser reiniciado para funcionar corretamente.

**Ligação Fraca de Dados**

Em contraste, uma **ligação fraca de dados** sugere que o processo pode continuar em execução após a migração, mesmo que alguns dados precisam ser transferidos. Isso ocorre porque o processo não depende de elementos específicos da máquina original.
##
## <a name="_gehziko4rfni"></a><a name="_2gbdozraigqp"></a>Nomenclatura
**Linha de execução:** Sequência de instruções que o processo executa ao longo do tempo.

**Arquitetura em Camadas:** Divisão do sistema em camadas com funções específicas, facilitando desenvolvimento, manutenção e escalabilidade.

**Abertura:** Capacidade do sistema de fornecer informações suficientes para que outras partes possam interagir e se integrar com ele.

**Frameworks:** São estruturas pré-construídas que agilizam o desenvolvimento de software, fornecendo funcionalidades básicas e otimizando o processo.
## <a name="_nxbrjss98ced"></a>Invocação de Método Remoto - RMI
**O que é RMI?**

RMI, ou Remote Method Invocation, é um protocolo para criar aplicativos distribuídos em Java. Ele permite que objetos em diferentes máquinas virtuais Java se comuniquem e interajam como se estivessem no mesmo local.

**Componentes de um aplicativo RMI:**

- **Servidor:** Executa os objetos remotos que podem ser acessados por clientes.
- **Cliente:** Obtem referências a objetos remotos no servidor e invoca seus métodos.
- **Registro RMI:** Armazena referências a objetos remotos e as fornece aos clientes.
- **Stub:** Representa um objeto remoto no cliente e traduz chamadas de método em solicitações RMI.

**Benefícios do RMI:**

- **Carregamento Dinâmico de Código:** O código das classes dos objetos remotos pode ser carregado dinamicamente na máquina virtual Java do cliente, permitindo a execução de novas tarefas sem reinicialização do servidor.
- **Transparência de Rede:** A comunicação entre objetos remotos parece com chamadas de método Java regulares, abstraindo a complexidade da rede.
- **Flexibilidade:** O RMI pode ser usado para diversos tipos de aplicações distribuídas, desde simples clientes-servidor até sistemas complexos baseados em agentes.

**Exemplos de Uso do RMI:**

- **Mecanismo de Computação:** Um servidor que executa tarefas enviadas por clientes.
- **Monitoramento Remoto:** Um sistema que coleta dados de sensores remotos e os exibe em um painel central.
- **Aplicações Web Distribuídas:** Um site com componentes que residem em diferentes servidores.
## <a name="_9gjj7muxirhf"></a>MPI - Interface de Passagem de Mensagens
**O que é a MPI?**

A MPI (Interface de Passagem de Mensagens) é um paradigma de programação para computadores paralelos que facilita a comunicação entre processos em diferentes máquinas. Ela define uma interface padrão e funcionalidade para uma ampla gama de recursos de comunicação, tornando o desenvolvimento de programas paralelos mais portátil e eficiente.

**Por que usar a MPI?**

- **Portabilidade:** O código MPI pode ser executado em diversas plataformas, desde computadores paralelos com memória distribuída até redes de estações de trabalho.
- **Desempenho:** As implementações do MPI são otimizadas para oferecer alto desempenho em diferentes arquiteturas.
- **Flexibilidade:** A MPI permite a comunicação entre processos em sistemas heterogêneos, com diferentes arquiteturas de processador.
- **Eficiência:** O MPI evita operações desnecessárias e incentiva a reutilização de recursos, minimizando o overhead de comunicação.
- **Escalabilidade:** A MPI suporta a criação de subgrupos de processos e oferece funcionalidades que se adaptam ao número de processos na aplicação.
- **Confiabilidade:** A MPI garante a entrega confiável de mensagens, dispensando o programador da necessidade de verificar erros de comunicação.

**Impacto da MPI:**

- A MPI se tornou um padrão amplamente aceito e utilizado na computação paralela.
- Implementações do MPI estão disponíveis para diversas plataformas e arquiteturas.
- A MPI facilitou o desenvolvimento de aplicações paralelas eficientes e portáteis.


## <a name="_np2sp9jps7mw"></a>Perguntas dignas de provas

- **P: Qual a diferença entre um processo e uma thread?**
- **R:** Um processo é uma instância em execução de um programa, enquanto uma thread é uma unidade de execução dentro de um processo. Um processo pode ter várias threads, o que permite que o processo execute várias tarefas simultaneamente.

- **P: Qual a diferença entre um sistema centralizado e um sistema descentralizado?**
- **R:** Em um sistema centralizado, existe um único ponto de controle que gerencia todo o sistema. Já em um sistema descentralizado, os componentes do sistema são distribuídos em diferentes locais e se comunicam entre si.

- **P: Como funciona a distribuição horizontal em um sistema distribuído?**
- **R:** A distribuição horizontal envolve a replicação de dados e serviços em diferentes locais para aumentar a disponibilidade e o desempenho do sistema.

- **P: O que são microsserviços?**
- **R:** Microsserviços são uma arquitetura de software que divide o sistema em pequenos serviços independentes e autônomos.

- **P: Quais são os principais desafios dos sistemas distribuídos?**
- **R:** Os principais desafios dos sistemas distribuídos incluem nomeação de serviços, segurança, consistência de dados e tolerância a falhas.

- **P: A migração de processos é sempre necessária?**
- **R:** Não, apenas em situações como balanceamento de carga, gerenciamento de falhas ou otimização de desempenho.

- **P: Quais ferramentas são utilizadas para gerenciar processos em sistemas distribuídos?**
- **R:** Ferramentas como Docker e Kubernetes são populares para gerenciar processos em contêineres.

- **P: Quais são o número mínimos de “conexão” na arquitetura cliente e servidor?**
- **R:** Duas o cliente eo servidor.
