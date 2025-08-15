
**Autor:** Guilherme Junqueira (Hacker)
## Aula 01 - Introdução

![[Pasted image 20250103171059.png]]

Em [[Python]], não reinvente a roda, use o que já está programado.

Em qualquer profissão de tecnologia, saber python é uma mão na roda.

Editor de código: recomendado usar o "pycharm".


## Aula 02 - Entrada/Saida e Operadores matemáticos.

==**Entrada,Saida de arquivos e operadores matematicos:**

Primeira coisa que precisamos aprender é a saida de arquivos (mostrar algo).

Em python é print("STRING")

Dentro da função print só é aceito texto, mas o python converte outros tipos de dados pra texto automaticamente.

- Uma IDE é essencial para programar programas grandes, pelo auto-complit do código.

Para quebrar linha usamos o comando "\n" dentro de uma string

Comando para deixar colunas alinhadas "\t"

==**Variáveis/Objetos**

Criar variáveis 

Exemplo:

Nome = "Neymar"

Então se eu der um print, e passar essa variavel Nome, ele vai printar o valor que está dentro dessa variavel.

Podemos colocar qualquer coisa em variaveis, funções, classes etc...

Float:
O que é ?
	Um numero flutuante que é quebrado por ponto, exemplo 1.80 (Sempre um float tem ponto) 

Função type = mostrar o tipo da variavel 

Tipos de dados que mais vamos usar no dia a dia:
	String, Int (inteiro) e float.

Concatenar, é juntar varios elementos em um só. 

Formas de concatenar= 
- Usando "," (Mais usado)
- Usando "+"

OBS: Usando o + o python não converte os int's em strings, é preciso converter manualmente. 
	Exemplo: Str (VARIAVELAQUI)

Usando o + para concatenar,não é adicionado espaço ao printar. Mas você pode adicionar os espaços manualmente dentro da string.

A vantagem de usar o "+" é que você pode colocar tudo dentro de uma variável.

**Função input:** Podemos usar a função de input para pegar o valor da variável de acordo com o preenchimento do usuario.
	Obs: Essa função sempre vai imprimir uma str.

Exemplos:
	
*Concatenação com virgula:* 
	print(nome, 'tem', idade, 'anos e', altura, 'de altura')
	
*Concatenação com simbolo de mais:* 
	print(nome + 'tem' + str (idade) + 'anos e' + str (altura) + 'de altura')

## Aula 03 - Operadores Lógicos



O que são operadores lógicos ? 
	é um operador que vai operar os dados, exemplo 1 + 1, o simbolo de "mais" é um operador lógico.

**Dado booleano (Boolean):** Esse tipo de dado só tem dois resultados.
	True ou false, ou 1 ou 0.

Esse tipo de dado é importante para o programa tomar decisões sozinho.

**IMPORTANTE:** um unico simbolo de igual(=) é usado para definir valores em uma variavel. Dois simbolos de igual(== ) é para comparar valores.
	Ex: Nome = João (1 igual)
	Ex: 1 == 1 (Aqui você está perguntando se 1 é igual a 1 pro python)
		Ele vai responder com True ou False

Podemos usar também outros meios para comparar:
Exemplo: 2 > 2 (Estamos perguntando se 2 é maior do que 2)


Comparadores: == != >  < >=  <=
	Podemos usar tbm, "and" ou "or".


**Função IF:** Se x dado for False ou True, execute o código identado abaixo.

**Função Else:** Sigfica"então", então no se o codigo do IF não for executado, execute esse codigo identado da função else.

**Função Elif:** Se o código do if já foi executado, não precisa testar as opções seguintes. 
Obs: Se fosse somente if, seria executado todos os if's independente se algum if foi executado.

**NOT:** Se colocarmos o not na frente de algo, ele vai inverter, transformar tudo o que é Falso em verdadeiro e vice versa.

Essas funções são muito importantes pro programa tomar decisões soazinho, através de comparações.

## Aula 04 - Strings e listas 

A lista é uma estrutura de dados.

Como criar uma lista ?
	lista = [] (Separamos os itens da lista por virgula, e dentro da lista, podemos colocar varios dados, separando por virgula)

Na função print, podemos passar qual item da lista queremos que seja imprimido, usando indice (simbolo de colchetes [  ])
	Exemplo: print(lista_nome[2])

Pra imprimir o ultimo item da lista, podemos usar o simbolo de menos 
	Exemplo:[-1]

Para usar métodos usamos um ponto(.) e assim podemos usar métodos naquela lista.

Exemplo: varialvel1.Split, varialvel1.remove, .clear, etc...

**Conceito de fStrings:**

O **f** antes da string é para criar uma **f-string**, que significa "formatted string" (string formatada). 

É uma maneira fácil e poderosa de incluir valores de variáveis diretamente dentro do texto.

Imagine que você quer dizer algo usando o nome de uma pessoa:

Por exemplo, você tem uma variável chamada nome e quer dizer: **"Olá, João!"**. Com uma f-string, você pode fazer assim:

![[Pasted image 20250104155828.png]]

- O f antes das aspas permite que você escreva expressões dentro das chaves **{}** na string.
- O Python substitui automaticamente as chaves `{}` pelo valor da variável ou cálculo que você colocou ali.

## Aula 05 - Estrutura de laço (While e FOR)


As estruturas de laço servem para repetir ações de forma facil.

---
Estrutura de laço **FOR**(PARA):

Imagine que você tem uma lista de amigos e quer convidar cada um para uma festa. Com o **for**, você pode dizer para o computador: "Para cada amigo na lista, me diga o nome dele":

Exemplo:

![[Pasted image 20250104153845.png]]

O **for** pega um item de cada vez da lista e faz o que você pedir com ele.

---
Estrutura de laço **WHILE**(ENQUANTO)

O **While** é como um "enquanto isso for verdade" enquanto tal variável foi True, execute os códigos abaixo.

O laço **while** continua repetindo o que está dentro dele até que a condição (variavel) deixe de ser verdadeira.

Exemplo:

![[Pasted image 20250104154023.png]]


---

**Diferença** de **While** e **For**:

- **While**: é usado quando você não sabe exatamente quantas vezes algo precisa ser repetido, mas sabe uma condição para parar.

- **For**: é usado quando você sabe exatamente o número de vezes ou tem uma lista para percorrer.

While e for são estruturas fundamentais e existem em qualquer linguagem de programação.

---

**Break:** Serve para parar o looping de repetição.

O **break** é como um "sinal vermelho" para o laço. Ele diz: **"Pare o que você está fazendo e saia do laço agora!"**

Vamos imaginar um jogo simples:

- Você está procurando por um tesouro em uma caverna cheia de baús.
- Cada baú pode ter ouro ou estar vazio.
- Assim que você encontrar ouro, você para de procurar.

Exemplo:

Break no **for**

![[Pasted image 20250104154442.png]]

Break no **while**

![[Pasted image 20250104155014.png]]

Quando usar o **break**?

- Quando você tem uma condição que faz o laço parar antes de chegar ao fim.

- Ele é útil para economizar tempo e recursos, evitando que o computador continue fazendo algo desnecessário.

## Aula 6 - Tuplas, dicionarios e conjuntos.

São objetos de coleção.

**Tupla** (Tuple):

Oque é ? 
	Ela é parecida com a lista, mas ela não é mutavel, você não consegue adicionar métodos nela (.append,.clear etc...)


Como criar: Só usar aspas ()

---

**Dicionário (dict):**
	Usar o caracter de chave {chave: valor, chave2: valor}
	O dicionário é bem parecido com o json.

Dicionário é muito eficiente para buscar itens.

---

Conjunto = {valor, valor}
	Você vai usar quando você não quer dados repetidos.

Conjunto é muito bom para pesquisar itens, diferente da lista,a busca é instantanea, sem percorrer a lista inteira, consumindo menos recursos do pc.

----

Se o seu programa está lento... pode ser o tipo de dado que vc está usando.

----


Syntaxe de criação desses dados:

lista = []
tupla = ()
dicionario = {}
conjunto = set ()

Você também pode colocar tipos de dados um dentro do outro.

## Aula 7 - Funções e Métodos.

Estamos usando métodos e funções des do inicio do curso.
	Exemplo: Estamos usando o print que é uma função.

No pycharm tudo que está em azul é uma função.

Como criar uma função?
	def nome_função (parametro_que_vai_ser_passado):
		var_resp = parametro1 + parametro2
		return var_resp

Criar uma função é util para não precisar reescrever codigo, criando uma função, você pode usar ela no programa inteiro.

A função também não precisa de obrigatoriamente ter parametros nem return.

**Criar uma função:**

def nomedafuncaoaqui (nome_parametro):
	variavel_x = max(parametro_passado_antes)
	print(variavel_x)

Após isso é só chamar a função:

nomedafuncao(parametro pra executar a função)

## Aula 8 - Argumentos e Linhas de Comando.

Estávamos executando nossos programas com inputs, agora podemos executar eles com argumentos pelo terminal.
	Exemplo: python3 scriptmaluco.py --argumentoaqui

Com isso, pelo argumento passado, eu falo pro meu programa o que ele tem que fazer.
	Exemplo: argumento1 = faz login automatico

Para isso precisamos importar a biblioteca sys

**O que são bibliotecas ?** São códigos já escritos, e quando você importa a biblioteca pra dentro do seu programa, é possivel usar os métodos e funções já escritas daquela biblioteca criada...

Syntaxe: import nome_biblioteca
Ou for nome_biblioteca import nome_classe
## Aula 9 - Orientação a objeto

A **Programação Orientada a Objetos (POO)** é um jeito de organizar o código para que seja fácil de entender, criar, e modificar.

Em vez de escrever tudo solto, você divide o programa em **objetos**, que são como caixinhas mágicas que guardam informações (dados) e podem realizar ações (funções).

---

==O que é um **objeto**?

Um **objeto** é como algo do mundo real. Imagine que você quer criar um programa sobre carros. Cada carro:

- Tem características, como cor, modelo, e velocidade.
- Pode fazer coisas, como acelerar ou frear.

Na POO, você cria **classes** para definir o que os objetos terão e o que poderão fazer.

Para cada objeto, criamos um arquivo, com as classes e métodos do objeto.

---

O que é uma **classe**?

Uma **classe** é como a "fábrica" ou o "molde" de onde os objetos nascem. A classe define **o que os objetos sabem** (dados) e **o que eles fazem** (métodos).

Exemplo:

![[Pasted image 20250104161246.png]]

- `__init__`: É o "construtor" que cria o objeto. Ele define os **atributos** (como `cor` e `modelo`) de cada objeto.
- `self`: Representa o próprio objeto (pense como o "eu" do carro).
- As **classes** sempre começamos com a primeira letra do nome maiúscula
- Para usar a classe em outros arquivos, precisamos importar o arquivo da classe.


**Criando objetos (instâncias)**

Agora que temos o molde `Carro`, podemos criar nossos próprios carros:

![[Pasted image 20250104161626.png]]


**Pra que usar POO?**

- Organização: O código fica mais limpo e organizado, porque você agrupa os dados e funções em um unico lugar (os objetos.)
- Reutilização: Você pode criar vários objetos a partir de uma unica classe.
- Flexibilidade: É mais facil adicionar ou modificar funcionalidades.

---

**RESUMO DOS CONCEITOS BÁSICOS:**

**Classe:** É o molde(receita/características/plano) para criar objetos.

**Objeto:** Uma coisa específica criada a partir de uma classe (exemplo, um carro vermelho chamado Fusca)

**Atributos:** As informações/características do objeto (exemplo, cor, marca)

**Métodos:** As ações que o objeto pode fazer (exemplo, acelerar, frear).

------

**Herança na POO:**

O conceito de **herança** nas classes é como passar características de "pais" para "filhos".

Na POO, uma classe pode herdar atributos e métodos de outra classe, para reaproveitar código e facilitar a organização

Exemplo:

Você tem uma classe geral chamada **"Animal"** que define características e ações básicas de qualquer animal. 

Depois, pode criar classes mais específicas, como **"Cachorro"** e **"Gato"**, que herdam tudo da classe **"Animal"**, mas também podem ter características próprias.


Criando classe "pai"(Animal):

![[Pasted image 20250104163342.png]]


Criando classe "filha" (Cachorro):
	A classe cachorro herda tudo da classe Animal.

![[Pasted image 20250104163451.png]]

Agora você pode criar objetos da classe **Cachorro**, que já possuem os métodos e atributos da classe **Animal**:

![[Pasted image 20250104163559.png]]


**Porque usar herança?**

- Reutilizar código já escrito, evitar repetir o mesmo código em várias classes.
- Organização: Permite criar classes específicas sem duplicar o que já existe na classe "Pai"
- Facilidade de atualização: Se você precisar modificar algo, pode alterar na classe "pai", e todas as classes "filhas" recebem a mudança automaticamente.

## Aula 10 - Entrada e saída de arquivos

A entrada e saída de arquivos em Python permite que você **leia dados de arquivos** e **escreva dados em arquivos** diretamente do seu programa.

**Abrir arquivos:** para abrir o arquivo, use a função `open()`. isso cria uma ponte entre o programa e o arquivo.

**Ler/Escrever:** Após abrir o arquivo, você pode ler o conteúdo do arquivo, ou escrever novos dados no arquivo.

**Fechar o arquivo:** Você pode fechar o arquivo com o método `close()`


**Ler arquivos com with:** O `with` é uma maneira **segura e prática** de lidar com arquivos em Python. Ele:

1. **Abre o arquivo** para você.
2. **Fecha automaticamente** o arquivo quando você termina de usá-lo, mesmo que ocorra um erro no meio do código.

![[Pasted image 20250104172011.png]]

- arquivo é o nome temporario que você escolhe para se referir ao arquivo dentro do bloco do with.


Exemplo abrir arquivo:

![[Pasted image 20250104170106.png]]

No "modo" você diz o que você quer fazer com o arquivo:
 - r: Ler (read)
 - w: Escrever (Write) ele apaga todo conteúdo anterior.
 - a: Adicionar (append) ele adiciona dados ao final do arquivo sem apagar o conteudo
 - r+: Ler e escrever no arquivo.

**Exemplo:** Criando e escrevendo um arquivo.

![[Pasted image 20250104170327.png]]

- Usamos o modo `"w"` para escrever no arquivo.
- O **`with`** automaticamente fecha o arquivo depois.

**Exemplo:** Lendo um arquivo

![[Pasted image 20250104170426.png]]


Outras formas de ler:
- `readline()`: Lê **uma linha** de cada vez.
- `readlines()`: Lê todas as linhas e retorna uma lista.

**Exemplo:** Adicionando dados no arquivo

![[Pasted image 20250104170551.png]]

**Dicas:**
- Em arquivos grandes, use laços para ler linha por linha, evitando carregar tudo de uma vez na memória.
![[Pasted image 20250104170654.png]]
- No modo r, o python dá erro se o arquivo não existir.
- No modo w ou a, o python cria o arquivo automaticamente.
- Cuidado com o modo w, ele apaga tudo no arquivo se o já existir conteudo.

**Resumo:**
- `open()` abre arquivos para leitura ou escrita.
- Modos mais comuns: `"r"` (ler), `"w"` (escrever), `"a"` (adicionar).
- Sempre feche os arquivos ou use **`with`** para fazer isso automaticamente.
- Métodos úteis:
    - `read()`: Lê todo o conteúdo.
    - `readline()`: Lê uma linha por vez.
    - `write()`: Escreve no arquivo.

---

## Aula 11 - Tratamento de Erros e exceções (Try e Except)

O **`try` e `except`** são usados em Python para **tratar erros** no seu código. Eles permitem que você controle o que acontece quando algo dá errado, em vez de deixar o programa "quebrar" ou mostrar uma mensagem de erro para o usuário.

Para tratar os erros usamos a função try, que significar tentar.
	O python vai tentar fazer x. Caso não de certo, colocamos um except(Exceção).

Obs: Obrigatório usar o except junto com o try.

No except podemos definir se o except vai ser executado, pelo erro que o programa fez.

Exemplo: 
	![[Pasted image 20250104173734.png]]

Com isso podemos tratar varios erros de forma unica.

Podemos tratar todos os erros dessa forma abaixo:

![[Pasted image 20250104173953.png]]
	Usando a função Exception, e printando o erro depois.

Locais comuns para usar try e except:
 - Sempre que você vai acessar algo externo, usar try e except
 - Sempre que você vai executar algo que pode dar erro, usar try e except.

Try e except são muito usadas em linguagens de alto nivel. 


## Aula 12 - Bibliotecas, PIP e Requisições Web 

O python possuir um gerenciador de pacotes proprio, chamado PIP
	Ele instala bibliotecas externas.

Para instalar bibliotecas externas é  ` pip install nome da biblioteca`

Utilize coisas que já estão prontas para te ajudar.

Para ser um bom programador você precisa focar na agilidade, desenvolver rápido.

Para requisições web, vamos utilizar a biblioteca requests.

O que é uma requisição web? Basicamente é entrar em um site.
	Protocolo HTPP

GET = PEGAR (Entrar em um site e pegar infos)
POST = Postar (Enviar informações)
Headers = é aonde vai as informações dessa requisição.

Status:

200 = Deu certo
404 = Essa pagina não existe
500 = Algum erro no servidor
403 = Você não tem permissão.

**Importante:** Sempre que for fazer uma requisição, usar o try e except.


O método para fazer uma requisição é bem simples:

Requests.get ou requests.post

Podemos criar uma variável com o nome cabeçalho, e criar um dicionário, e enviar essa variável com o cabeçalho personalizado que queremos.

![[Pasted image 20250104191045.png]]

Outra coisa muito importante é passa cookies:

![[Pasted image 20250104191236.png]]

Outra coisa importante é o data/body:

![[Pasted image 20250104191340.png]]


Com isso, você consegue fazer um brute-force pra ficar fazendo login em um site.
	Apartir de uma lista que você tiver

----

Se você quiser destrinchar paginas web, use a biblioteca beatifulsoup. Para webScraping etc...



## Aula 13 - API, Json e consultando listas de filmes.

O que é [[API]] ?
	São interfaces que você se comunica com outros programas. você irá passar parametros e ela irá te retornar algo.

O que é um json ? 
	É como se fosse um dicionário do python, bem parecido.

Inclusive você pode criar APIS personalizadas.

-----


## Aula 14 - Expressões regulares, procurando por e-mails.



Expressões regulares (regex) servem para encontrar padroes em dados. (Ex: Existe regex para encontrar um dado tipo email)

São importantes para procuramos por padrões em textos.

Vamos utilizar a biblioteca `re`

Expressoes regulares são chamadas de regex

No google você encontra padrões para varias coisas.

Se você for usar expressoes regulares, é sempre bom consultar a documentação, é dificil decorar tudo.

## Aula 15 - Consultando o clima e cotação do dolar

Primeiro de tudo, podemos pesquisar uma API que nos forneça essas informações de cotação do dolar.

Basicamente o que precisamos fazer para criar esses programinhas é achar uma API pra consultar o que queremos.

E depois tratar os dados do json para extrair a info que queremos, e depois printar na tela.

Bem simples.

Flow: 
1. Procurar API
2. Consultar API com requests
3. Tratar o Json
4. printar os resultados na tela


## Aula 16 - Publicando e pesquisando no Twitter

Vamos interagir com o twitter, publicando no twitter. Usando a API deles.

- Varias empresas estão investindo em criar API's abertas para o publico, se você tiver a ideia de um software inovador, você vai ganhar muito dinheiro!

O que significa API rest?
	Significa que a api vai receber dados em json, e te retornar dados em json.

Existe uma biblioteca no python pra fazer autenticação nas API'S, chamado oauth2

Vamos criar uma variavel pra cada autentição que a API solicita.

PIP install oauth2

Com Requests dá pra fazer requests para fazer autenticação etc...
	Estude mais como você pode fazer esse sistema de autenticação, dá trabalho!

Essa estrutura abaixo funciona pra qualquer aplicação que usa o oauth2 para autenticação: 

![[Pasted image 20250106161129.png]]

OBS: Não funciona mais

Estude a documentação das API'S que você quer usar.

Biblioteca que printa as coisas de forma organizada: pprint

## Aula 17 - Criando Bibliotecas 

Nessa aula vamos aprender a criar bibliotecas que vão ser usadas pra outras pessoas.

Pra que serve bibliotecas ? 
	Para usar códigos prontos feitos por outras pessoas.

O ouro é usar bibliotecas prontas, com funções e métodos prontos etc..


FIM DO CURSO!





