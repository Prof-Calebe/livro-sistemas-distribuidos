# Sistemas Distribuídos

Sistemas distribuídos são conjuntos de computadores independentes que trabalham como um sistema único, interconectados pelas redes de comunicação, como a internet, intranet, computação móvel, etc. Suas principais características são:

## Características

### Transparência

Tornar a distribuição dos recursos e processos invisível para os usuários:
- **Transparência de acesso**: Ocultar como os recursos são acessados.
- **Transparência de localização**: Ocultar onde os recursos estão alocados.
- **Transparência de migração**: Ocultar a movimentação dos recursos e processos.

### Escalabilidade

Capaz de adicionar mais recursos, como máquinas (adicionar mais usuários ao sistema), sem aumentar o custo e, além disso, aumentar o processamento e armazenamento, sem perder o desempenho.

### Segurança

Possui certos problemas, sendo eles:
- **Autenticação**: Verificar a identidade dos usuários.
- **Autorização**: Determinar os níveis de acesso que cada usuário autenticado tem.
- **Confidencialidade**: Garantir que os dados sejam acessíveis apenas por partes autorizadas.
- **Solução**: Criptografias, capazes de manter os dados sigilosos na rede, apesar de sofrer de outros problemas como DDoS.

### Tratamento de Falhas

Deve haver tratamento para os erros do sistema.

### Heterogeneidade

Construção a partir de várias redes, sistemas operacionais, hardware, linguagens de programação. Permite maior flexibilidade e interoperabilidade, porém exige maior manutenção e deixa maior vulnerabilidade em questões de segurança.

# Middleware

O Middleware é um software que atua como intermediário no sistema distribuído, responsável por facilitar a comunicação entre os componentes, permitindo que trabalhem de forma coesa e eficiente. 

Responsável pela interoperabilidade entre os sistemas, ou seja, permite que as aplicações se comuniquem e trabalhem juntas independentemente das diferenças em hardware, sistemas operacionais, ou linguagens de programação, além de oferecer interfaces mais simples e uniformes para os desenvolvedores.
