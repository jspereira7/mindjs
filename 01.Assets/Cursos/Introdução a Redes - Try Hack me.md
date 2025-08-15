**O que é uma rede ?**

Redes são simplesmente coisas conectadas. 
	Por exemplo, seu círculo de amizades: vocês estão todos conectados por causa de interesses, hobbies, habilidades e tipos semelhantes.

E na tecnologia é a mesma coisa, uma rede é formada por 2 dispositivos ou mais.

![[Pasted image 20250107175656.png]]


Resumo: 

Redes são apenas dispositivos conectados


---

**O que é a internet ?** 

A internet é uma rede gigante que consiste em varias pequenas redes conectadas entre sí.

Exemplo: É como tivesse 2 grupos de amigos que falam diferentes linguas, em um desses grupos, tem uma pessoa que fala ambas as linguas, e para esses 2 grupos fazerem amizade, eles se comuticam atraves desse amigo que fala as duas linguas, formando uma nova rede.

A internet é parecida com essa historia dos amigos:

![[Pasted image 20250107180235.png]]

Como a internet é composta de varias pequenas redes unidas, essas pequenas redes são chamadas de redes privadas, onde as redes que conectam essas redes privadas uma com a outra se chamam redes publicas.

Redes privadas = rede local da sua casa
Redes Publicas = internet 

-----

**Identificando dispositivos em uma rede:**

Para se comunicar em uma rede, os dispositivos devem tanto identificar os outros, quanto serem identificados.

Os dispositivos possuem 2 meios de identificação, sendo um deles imutavel:

- Endereço IP
- Mac Adress
-----
**IP (INTERNET PROTOCOL)**

![[Pasted image 20250107180805.png]]

Um ip possui 4 octetos, separados por pontos

É importante entender que os endereços IP podem mudar de dispositivo para dispositivo, mas não podem estar ativos simultaneamente mais de uma vez dentro da mesma rede.

Os dispositivos podem estar tanto em uma rede publica quanto privada.

Dependendo de onde eles estão, eles terão um IP publico ou privado.

IP publico = Serve para identificar dispositivos na internet.
IP privado = Serve para identificar um dispositivo entre outros dispositivos.

![[Pasted image 20250107181228.png]]

Esses dois dispositivos poderão usar seus endereços IP privados para se comunicarem entre si. 

Mas, qualquer dado enviado para a Internet de qualquer um dos dispositivos serão identificados pelo mesmo IP público.

Endereços IP públicos são fornecidos pelo seu **I** nternet **S** ervice **Provider** (ou **ISP** ) por uma taxa mensal (sua conta!)

Endereço IPv6 x IPV4:

![[Pasted image 20250107181523.png]]

**Mac Adress (Media access Control):**

Dispositivos na rede terão uma interface de rede física,  uma placa de microchip encontrada na placa-mãe do dispositivo. Esta interface recebe um endereço exclusivo na fábrica em que foi construída (o mac adress)

![[Pasted image 20250107181734.png]]

Uma coisa interresante é que esses dispositivos podem ser falsificados, com um processo de spoofing. (Fingindo ser outro dispositivo atraves do endereço de rede.)

Com isso é possivel quebrar firewalls de segurança, ao pegar o endereço Mac do administrador do sistema por exemplo, e quando você tentar conectar, você vai se passar pelo adm.

----

**PING:**

Ping é uma ferramenta de rede fundamental, ela usa pacotes ICMP (Internet Control Message Protocol) para mostrar o desempenho de uma conexão entre dispositivos, e se a conexão existe e é confiavel.

Pings podem ser realizados em dispostivos domesticos em uma rede ou sites da internet.

Já vem instalada em vários sistemas, como linux, windows e mac.

Para fazer um ping é simples:

Digite: **ping [IP adress] ou [website URL]**

------


Relacionados:

[[Introdução a Lan - Try Hack me]]




