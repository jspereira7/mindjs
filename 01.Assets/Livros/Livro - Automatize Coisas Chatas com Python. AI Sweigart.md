
Este é o poder da programação de computadores. Um computador é como um canivete suíço que você pode configurar para inúmeras tarefas. Muitas pessoas passam horas clicando e digitando para executar tarefas repetitivas, sem saber que a máquina que estão usando poderia fazer seu trabalho em segundos se dessem as instruções certas.

----

**O que é programação ?** 

É simplesmente o ato de passar instruções para o computador executar.

Todos os programas usam instruções básicas como blocos de construção. Aqui estão algumas das mais comuns, em inglês:

- “Faça isso; depois faça aquilo.”
- “Se esta condição for verdadeira, execute esta ação; caso contrário, execute aquela ação.”
- “Faça esta ação exatamente 27 vezes.”
- “Continue fazendo isso até que essa condição seja verdadeira.”

----

**Você não precisa ser bom em Matematica**

Escrever programas envolve quebrar/dividir um problema em etapas individuais e detalhadas.

Da mesma forma, ao _depurar_ programas (ou seja, encontrar e corrigir erros), você observará pacientemente o que o programa está fazendo e encontrará a causa dos bugs. 

E como todas as habilidades, quanto mais você programa, melhor você se tornará.

---

**_Programação é uma atividade criativa_**

A diferença entre programação e outras atividades criativas é que, ao programar, você tem todas as matérias-primas necessárias no seu computador; você não precisa comprar nenhuma tela, tinta, filme, fio, tijolos de LEGO ou componentes eletrônicos adicionais.

Uma vez que seu programa é escrito, ele pode ser copiado perfeitamente um número infinito de vezes. 

Um suéter de tricô só pode ser usado por uma pessoa por vez, mas um programa útil pode ser facilmente compartilhado online com o mundo inteiro.

---

**Pesquise!**

Você frequentemente descobrirá que outra pessoa teve a mesma pergunta que você e que alguma outra pessoa útil já respondeu. Ninguém pode saber tudo sobre programação, então uma parte cotidiana do trabalho de qualquer desenvolvedor de software é procurar respostas para perguntas técnicas.

---

## **1 - NOÇÕES BÁSICAS DO PYTHON**

**Tipos de dados:**

Um _tipo de dado_ é uma categoria para valores, e cada valor pertence a exatamente um tipo de dado.

![[Pasted image 20250109160447.png]]

 Significado de um operador pode mudar com base nos tipos de dados dos valores próximos a ele. Por exemplo, + é o operador de adição quando opera em dois inteiros ou valores de ponto flutuante. 
 
 No entanto, quando + é usado em dois valores de string, ele une as strings como o operador _de concatenação de string_ .

O operador * multiplica dois valores inteiros ou de ponto flutuante. Mas quando o operador * é usado em um valor de string e um valor inteiro, ele se torna o operador _de replicação de string_

![[Pasted image 20250109160932.png]]

----

### **Armazenando valores em variáveis**

Uma _variável_ é como uma caixa na memória do computador onde você pode armazenar um único valor. 

Se você quiser usar o resultado de uma expressão avaliada mais tarde no seu programa, você pode salvá-lo dentro de uma variável.


**Declarações de atribuição:**

Você armazenará valores em variáveis ​​com uma _instrução de atribuição_ . Uma instrução de atribuição consiste em um nome de variável, um sinal de igual (chamado de _operador de atribuição_ ) e o valor a ser armazenado. Se você digitar a instrução de atribuição spam = 42 , então uma variável chamada spam terá o valor inteiro 42 armazenado nela.

![[Pasted image 20250109161206.png]]

**Sobrescrever Variáveis**

Uma variável é _inicializada_ (ou criada) na primeira vez que um valor é armazenado nela ➊ . 

Depois disso, você pode usá-la em expressões com outras variáveis ​​e valores ➋ . 

Quando uma variável recebe um novo valor ➌ , o valor antigo é esquecido, e é por isso que o spam foi avaliado como 42 em vez de 40 no final do exemplo. Isso é chamado de _sobrescrever_ a variável.


**Nomes de Variáveis:**

Você pode nomear uma variável qualquer coisa, desde que ela obedeça às três regras a seguir:

- Pode ser apenas uma palavra, sem espaços.
- Ele pode usar apenas letras, números e o caractere sublinhado ( _ ).
- Não pode começar com um número.
- Ideal começar com letras minúsculas.

Este livro usa _camelcase_ para nomes de variáveis ​​em vez de sublinhados; ou seja, variáveis ​​lookLikeThis em vez de looking_like_this .

----

#### **_A função print()_**

A função print() exibe o valor da string dentro de parênteses na tela.

_Você também pode usar esta função para colocar uma linha em branco na tela; basta chamar print() sem nada entre parênteses._

#### **_A função len()_**

Você pode passar para a função len() um valor de string (ou uma variável contendo uma string), e a função será avaliada como o valor inteiro do número de caracteres nessa string.


#### **_As funções str(), int() e float()_**

Se você quiser concatenar um inteiro como 29 com uma string para passar para print() , você precisará obter o valor '29' , que é a forma de string de 29 . A função str() pode receber um valor inteiro e será avaliada como uma versão de valor de string do inteiro, como segue:

![[Pasted image 20250109163445.png]]

As funções str() , int() e float() serão avaliadas como string, inteiro e formas de ponto flutuante do valor que você passar, respectivamente.

A função str() é útil quando você tem um inteiro ou float que deseja concatenar a uma string. A função int() também é útil se você tem um número como um valor de string que deseja usar em alguma matemática. Por exemplo, a função input() sempre retorna uma string, mesmo se o usuário digitar um número.

----

## **CONTROLE DE FLUXO**

A verdadeira força da programação não é apenas executar uma instrução após a outra como uma lista de tarefas de fim de semana.

Com base em como as expressões são avaliadas, um programa pode decidir pular instruções, repeti-las ou escolher uma das várias instruções para executar. 

Na verdade, você quase nunca quer que seus programas comecem da primeira linha de código e simplesmente executem cada linha, direto até o fim. 

_As instruções de controle de fluxo_ podem decidir quais instruções Python executar sob quais condições.

Antes de aprender sobre instruções de controle de fluxo, você precisa primeiro aprender como representar essas opções sim e não, e precisa entender como escrever esses pontos de ramificação como código Python. 

Para esse fim, vamos explorar *valores booleanos*, *operadores de comparação e operadores booleanos.*

**Valores booleanos:**
	Resultado apenas True ou False.

Quando inseridos como código Python, os valores Booleanos True e False não têm as aspas que você coloca em torno de strings e sempre começam com um _T_ ou _F_ maiúsculo , com o restante da palavra em minúsculas.

Ex: Spam = True

### **Operadores de comparação**

_Operadores de comparação_ , também chamados _operadores relacionais_ , comparam dois valores e avaliam até um único valor booleano (True ou False)

![[Pasted image 20250109165903.png]]

Os operadores == e != podem realmente trabalhar com valores de qualquer tipo de dado.

Os operadores < , > , <= e >= , por outro lado, funcionam corretamente apenas com valores inteiros e de ponto flutuante.

Os três operadores booleanos ( and , or , e not ) são usados ​​para comparar valores booleanos. 

Como operadores de comparação, eles avaliam essas expressões até um valor booleano. 

----

#### **_Condições_**

Condições sempre avaliam até um valor booleano, True ou False. 

Uma instrução de controle de fluxo decide o que fazer com base em se sua condição é True ou False , e quase todas as instruções de controle de fluxo usam uma condição.

#### **_Blocos de Código_**

Linhas de código Python podem ser agrupadas em _blocos_ . Você pode dizer quando um bloco começa e termina a partir do recuo das linhas de código. Há três regras para blocos.

- Os blocos começam quando o recuo aumenta.
- Blocos podem conter outros blocos.
- Os blocos terminam quando o recuo diminui para zero ou para o recuo de um bloco de contenção.

![[Pasted image 20250109171755.png]]

IF = Se
Else = Então


#### **_Declarações if_**

A cláusula de uma declaração if (ou seja, o bloco que segue a declaração if ) será executada se a condição da declaração for True.A cláusula é ignorada se a condição for False.

Ex: Se essa condição for verdadeira execute o código abaixo

![[Pasted image 20250109172040.png]]


#### **_Declarações else_**

Uma cláusula if pode ser opcionalmente seguida por uma instrução else . A cláusula else é executada somente quando a condição da instrução if é False .

else poderia ser lida como, “Se esta condição for verdadeira, execute este código.

#### **_Declarações elif_**

Embora apenas uma das cláusulas if ou else seja executada, você pode ter um caso em que deseja que uma das _muitas_ cláusulas possíveis seja executada.

 declaração elif é uma declaração “else if” que sempre segue uma declaração if ou outra declaração elif . Ela fornece outra condição que é verificada somente se todas as condições anteriores forem False . No código, uma declaração elif sempre consiste no seguinte:

Resumo: Se nenhum algum codigo anterior já foi executado, não faça nada. Só execute se todos os blocos anteriores não foram executados.

A cláusula elif é executada se age < 12 for True e name == 'Alice' for False . No entanto, se ambas as condições forem False , então ambas as cláusulas serão ignoradas.

![[Pasted image 20250109173206.png]]


Esse tipo de estrutura em uma linguagem de humanos seria:

“Se a primeira condição for verdadeira, faça isso. Caso contrário, se a segunda condição for verdadeira, faça aquilo. Caso contrário, faça outra coisa.”


Lembre-se de que, no máximo, apenas uma das cláusulas será executada e, para instruções elif , a ordem importa!

----

#### **_Instruções de loop while_**

Você pode fazer um bloco de código executar repetidamente usando uma instrução while . O código em uma cláusula while será executado enquanto a condição da instrução while for True .

![[Pasted image 20250109174531.png]]

O loop para após cinco impressões porque o inteiro em spam aumenta em um no final de cada iteração do loop, o que significa que o loop será executado cinco vezes antes de spam < 5 ser False.

No loop while , a condição é sempre verificada no início de cada _iteração_ (ou seja, cada vez que o loop é executado). Se a condição for True , então a cláusula é executada e, depois, a condição é verificada novamente. Na primeira vez que a condição for considerada False , a cláusula while é ignorada.

#### **_Declarações break_**

Há um atalho para fazer com que a execução do programa saia de uma cláusula do loop while mais cedo. Se a execução atingir uma instrução break , ela sai imediatamente da cláusula do loop while . No código, uma instrução break simplesmente contém a palavra-chave break.

![[Pasted image 20250109175123.png]]

#### **_Declarações Continue_**

Assim como instruções break , instruções continue são usadas dentro de loops. Quando a execução do programa atinge uma instrução continue , a execução do programa imediatamente salta de volta para o início do loop e reavalia a condição do loop. (Isso também é o que acontece quando a execução atinge o fim do loop.)

![[Pasted image 20250109175636.png]]

Se o usuário digitar qualquer nome além de Josias ➊ , a instrução continue ➋ faz com que a execução do programa volte ao início do loop.

#### **_for Loops e a função range()_**

O loop while continua em loop enquanto sua condição for True (que é o motivo do seu nome), mas e se você quiser executar um bloco de código apenas um certo número de vezes? Você pode fazer isso com uma instrução de loop for e a função range().

![[Pasted image 20250109181041.png]]


---

## 3. Funções:

O Python fornece várias funções internas como essas, mas você também pode escrever suas próprias funções.

Uma _função_ é como um mini-programa dentro de um programa.


![[Pasted image 20250109192055.png]]

A primeira linha é uma declaração def ➊ , que define uma função chamada hello() . O código no bloco que segue a declaração def ➋ é o corpo da função. Este código é executado quando a função é chamada, não quando a função é definida pela primeira vez.

As linhas hello() após a função ➌ são chamadas de função. No código, uma chamada de função é apenas o nome da função seguido por parênteses, possivelmente com algum número de argumentos entre os parênteses. 

Quando a execução do programa atinge essas chamadas, ela salta para a linha superior da função e começa a executar o código ali. Quando atinge o fim da função, a execução retorna para a linha que chamou a função e continua se movendo pelo código como antes.


==Um dos principais propósitos das funções é agrupar códigos que são executados várias vezes. Sem uma função definida, você teria que copiar e colar esse código toda vez

**Sempre evite duplicar o código!** 
	porque, se decidir atualizá-lo (por exemplo, se encontrar um bug que precisa ser corrigido), você terá que se lembrar de alterar o código em todos os lugares em que o copiou.

Com a experiencia você vai desduplicar seus códigos, tornando seus programas mais fáceis e simples de ler...

**Funções com parametros:**

Quando você chama a função print() ou len() , você passa valores para elas, chamados _argumentos_ , digitando-os entre parênteses.

Você também pode definir suas próprias funções que aceitam argumentos.

![[Pasted image 20250109192547.png]]


Quando uma função é chamada com argumentos, os argumentos são armazenados nos parâmetros.

A execução do programa entra na função, e o parâmetro name é automaticamente definido como 'Alice' , que é o que é impresso pela instrução print()

!Uma coisa especial a ser notada sobre parâmetros é que o valor armazenado em um parâmetro é esquecido quando a função retorna.
	Então se você tentar chamar uma variavel que foi criada pela função, não irá funcionar...


#### **_Definir, Chamar, Passar, Argumento, Parâmetro_**

Definir uma função é criá-la, assim como uma declaração de atribuição como spam = 42 cria a variável spam . A declaração def _define_ a função sayHello()

A linha sayHello('Al') ➋ _chama_ a função agora criada, enviando a execução para o topo do código da função. 


Esta chamada de função também é conhecida como _passagem_ do valor da string 'Al' para a função. Um valor sendo passado para uma função em uma chamada de função é um _argumento_.

O argumento 'Al' é atribuído a uma variável local chamada name . Variáveis ​​que têm argumentos atribuídos a elas são _parâmetros_.

É fácil confundir esses termos, mas mantê-los claros garantirá que você saiba precisamente o que o texto deste capítulo significa.

### **RETURN em funções:**

Quando você chama a função len() e passa a ela um argumento como 'Hello' , a chamada da função é avaliada como o valor inteiro 5 , que é o comprimento da string que você passou. 

Em geral, o valor que uma chamada de função é avaliada é chamado de _valor de retorno_ da função.

Ao criar uma função usando a instrução def , você pode especificar qual deve ser o valor de retorno com uma instrução **return**.

Quando uma expressão é usada com uma instrução return , o valor de retorno é o que essa expressão avalia.

Parei aqui: ### **Âmbito local e global**

https://automatetheboringstuff.com/2e/chapter3/

