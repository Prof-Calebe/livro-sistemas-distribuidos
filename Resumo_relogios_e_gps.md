## Relógios

Relógios de quartzo utilizam pequenas barras de quartzo cortadas a laser e, com o efeito piezoelétrico, vibram a 32.768 hertz (2^15). Quando dividido por 2, chega a 1 hertz, significando 1 hertz = 1 segundo. Eles possuem um erro de 1/2 segundo por dia dentro da faixa de 5 a 35 graus Celsius. Computadores também utilizam relógios de quartzo devido ao seu baixo custo. O contador gera interrupções em intervalos programados, que ajustam um relógio em software, o contador indireto C.

Relógio atômico: utiliza o átomo de césio, separando com um ímã os átomos com mais e menos energia. O átomo com menos energia passa por uma câmara onde é bombardeado com radiação, enchendo-o de energia. Outro ímã direciona-o para um detector, que envia informações ao controle da câmara de radiação. Este ajusta a intensidade da radiação, variando entre mais ou menos energia para passar ao átomo separado pelo primeiro ímã. Se o átomo for bombardeado com menos radiação e perder energia, ele sofrerá um desvio e não será captado pelo detector, o que ajustará novamente o controle da intensidade da câmara de radiação. Ele perde menos de um segundo em um milhão de anos e é usado para alta precisão, como, por exemplo, no GPS (Global Positioning System).

## Global Positioning System

GPS: 24 satélites ao redor da Terra ajudam em sua operação. Um receptor utiliza quatro deles para se localizar: um para corrigir o tempo do receptor e três para determinar sua posição.

O receptor recebe o tempo do satélite sincronizado e realiza outros contatos para se localizar. Ele calcula o tempo que o sinal levou para chegar até ele (o satélite marca a hora da mensagem enviada e ele marca quando a recebe), multiplica pela velocidade da luz para obter a distância. Essa distância é usada como o raio de uma esfera, sendo o satélite o seu centro. Repetindo o processo com o segundo satélite, o receptor acaba criando uma intersecção com as duas esferas, que limita um perímetro em elipse no globo. Com o terceiro satélite, o receptor consegue reduzir a localização para um único ponto (sendo a intersecção das 3 esferas).

## Tempo Atômico Internacional

TAI (Tempo Atômico Internacional) é a média dos valores de relógios atômicos espalhados pelo mundo, medindo "perfeitamente" o tempo. O UTC considera que o dia não tem exatamente 24 horas e leva em conta fatores naturais que podem alterar o centro de massa da Terra e sua rotação.

## Sincronização de Relógios

Podemos pegar o erro de um nó, por exemplo, 0,1 segundos (10%) em 1 segundo, e perceber que ele se dessincronizaria em 1 segundo. Logo, podemos realizar a sincronização a cada 1 segundo para mantê-lo corretamente sincronizado.

### Algoritmo de Cristian

Sincroniza o relógio de um cliente com o relógio de um servidor da seguinte forma:
1. O cliente envia uma requisição de tempo ao servidor.
2. O servidor responde imediatamente com a hora atual.
3. O cliente registra o tempo de envio e o tempo de recebimento da resposta.
4. O tempo de transmissão da resposta é estimado.
5. O cliente ajusta seu relógio para o tempo ajustado.

Essa aproximação considera a latência média de ida e volta, mas pode introduzir erro se as latências forem significativamente diferentes nos dois sentidos.

### Algoritmo de Berkeley

Exige que todos os nós participem de um processo de sincronização, dividindo-se em dois papéis: primário e secundário. O primário pergunta a todos os secundários "que horas são?" e, após receber as respostas, ajusta de acordo com o algoritmo de Cristian. O primário computa a média dos valores recebidos e envia ajustes para todos os secundários, que então realizam os ajustes fornecidos.

## Network Time Protocol (NTP)

É o protocolo de sincronização de tempo mais utilizado. Seus componentes são organizados em camadas, permitindo que a informação do tempo flua da camada inicial até a última. Os componentes podem alterar de camada à medida que ocorrem falhas ou são encontrados novos caminhos, utilizando o algoritmo de árvore geradora mínima Bellman-Ford, aumentando a tolerância a falhas.

### Formas de execução

- **Modo multicast**: Propaga o tempo em rede local.
- **RPC**: Utiliza o algoritmo de Cristian.
- **Simétrico**: Parecido com o algoritmo de Berkeley.
