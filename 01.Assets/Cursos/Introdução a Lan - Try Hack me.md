
**Topologias de rede local (LAN)**:

Quando nos referimos ao termo "topologia", estamos, na verdade, nos referindo ao design ou aparência da rede em questão.

----

**Topologia em Estrela:**

A premissa principal de uma topologia estrela é que os dispositivos são conectados individualmente por meio de um dispositivo de rede central, como um switch ou hub.

Essa topologia é comumente encontrada hoje em dia devido à sua confiabilidade e escalabilidade - apesar do custo.

Qualquer informação enviada a um dispositivo nessa topologia é enviada por meio do dispositivo central ao qual ele se conecta. 

![[Pasted image 20250107190157.png]]


Como mais cabeamento e a compra de equipamento de rede dedicado são necessários para essa topologia, ela é mais cara do que qualquer uma das outras topologias. 

Mas, apesar do custo, ela fornece algumas vantagens... 
	Por exemplo, essa topologia é muito mais escalável, o que significa que é muito fácil adicionar dispositivos conforme a demanda pela rede aumenta.

Infelizmente, quanto mais a rede escala, mais manutenção é necessária para mantê-la funcional. 

Essa dependência de manutenção também pode tornar a solução de problemas de falhas muito mais difícil. 

Além disso, a topologia em estrela ainda é propensa a falhas - embora reduzida. 

Por exemplo, se o hardware centralizado que conecta dispositivos falhar, esses dispositivos não poderão mais enviar ou receber dados. 
	Felizmente, esses dispositivos de hardware centralizados geralmente são robustos.

-----

**Topologia de barramento**:

Essa conexão depende de uma única conexão que é conhecida como cabo backbone. 

Este tipo de topologia é semelhante à folha de uma árvore no sentido de que os dispositivos (folhas) surgem de onde os galhos estão neste cabo.

![[Pasted image 20250107190742.png]]



Como todos os dados destinados a cada dispositivo trafegam pelo mesmo cabo, ele é muito rapidamente propenso a ficar lento e com gargalos se os dispositivos dentro da topologia estiverem solicitando dados simultaneamente. 

Esse gargalo também resulta em uma solução de problemas muito difícil porque rapidamente se torna difícil identificar qual dispositivo está tendo problemas com os dados viajando todos pela mesma rota.

No entanto, dito isso, as topologias de barramento são uma das mais fáceis e econômicas de configurar devido aos seus custos, como cabeamento ou equipamento de rede dedicado usado para conectar esses dispositivos.

Por fim, outra desvantagem da topologia de barramento é que há pouca redundância em caso de falhas. 

Essa desvantagem ocorre porque há um único ponto de falha ao longo do cabo de backbone. 

Se esse cabo se rompesse, os dispositivos não poderiam mais receber ou transmitir dados ao longo do barramento.

-----

**Topologia em anel**:

A topologia em anel (também conhecida como topologia de token) ostenta algumas similaridades. Dispositivos como computadores são conectados diretamente uns aos outros para formar um loop, o que significa que há pouca necessidade de cabeamento e menos dependência de hardware dedicado, como em uma topologia em estrela.

Uma topologia em anel funciona enviando dados através do loop até que cheguem ao dispositivo de destino, usando outros dispositivos ao longo do loop para encaminhar os dados. Curiosamente, um dispositivo só enviará dados recebidos de outro dispositivo nesta topologia se não tiver nenhum para enviar a si mesmo. Se o dispositivo tiver dados para enviar, ele enviará seus próprios dados primeiro antes de enviar dados de outro dispositivo.

Como há apenas uma direção para os dados viajarem por essa topologia, é bem fácil solucionar quaisquer falhas que surjam. No entanto, essa é uma faca de dois gumes porque não é uma maneira eficiente de dados viajarem por uma rede, pois pode ter que visitar muitos dispositivos múltiplos antes de chegar ao dispositivo pretendido.

Por fim, topologias em anel são menos propensas a gargalos, como dentro de uma topologia de barramento, já que grandes quantidades de tráfego não estão viajando pela rede ao mesmo tempo. O design dessa topologia, no entanto, significa que uma falha como cabo cortado ou dispositivo quebrado resultará na quebra de toda a rede.

![](https://tryhackme-images.s3.amazonaws.com/user-uploads/5de96d9ca744773ea7ef8c00/room-content/4cea7a4b48eacbd4db0b0d5e32068596.png)

----

**O que é um Switch?**



[[Introdução a Redes - Try Hack me]]