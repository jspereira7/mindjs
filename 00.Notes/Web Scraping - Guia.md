# Introdução 

- IP é como o endereço, porta é como o numero do apartamento. 

- Um navegador web é somente um código, e um código pode ser dividido, separado em seus componentes básicos, reescrito, reutilizado, e você pode fazer com que ele aja como você quiser.

- Comece a nos endereços como arquivos, não em páginas. 

- Parser é o que interpreta e lê as tags no html, organizando as informações. 

- Ao escrever scrapers, é importante pensar no padrão geral de seu código a fim de lidar com as exceções e, ao mesmo tempo, deixá-lo legível. É provável que você queira também fazer uma intensa reutilização de código. Ter funções genéricas como getSiteHTML e getTitle (completas, com todo o tratamento para exceções) facilita fazer uma coleta de dados da web de forma rápida – e confiável.



---

## Lidando com logins e cookies (Ouro)

A maioria dos sites modernos usa cookies para controlar quem está logado e quem não está. Depois que um site autentica suas credenciais de login, ele as armazena no cookie de seu navegador, o qual, em geral, contém um token gerado pelo servidor, um timeout e informações de controle.

O site então usa esse cookie como uma espécie de prova de autenticação, que é exibida a cada página que você acessar durante o tempo que estiver no site.
- Basicamente o site quer que esses cookies aparecam na requisição de cada pagina que necessita estar logada. 

Podemos submeter um formulário de login o dia todo, mas, se não mantivermos o controle sobre o cookie que o formulário envia de volta, a próxima página acessada agirá como se jamais tivéssemos feito login.

Estamos basicamente lidando com autenticação. 

A biblioteca requests só perde para o selenium. 

-----

## Scraping com Java Script 

O JavaScript é, sem dúvida, a linguagem de scripting do lado cliente mais comum e mais bem aceita na web atualmente. Pode ser usado para coletar informações de monitoração de usuários, submeter formulários sem recarregar a página, incluir multimídia e também em jogos online completos. Até mesmo páginas de aspecto simples podem conter muitas porções de JavaScript. Podemos encontrá-lo entre tags script no código- fonte da página:

<script>
alert("vaitomarnocu")
</script>

### Ajax e HTML dinamico 

Se você já submeteu um formulário ou adquiriu informações de um servidor sem recarregar a página, é provável que tenha usado um site com Ajax.

Contrário ao que algumas pessoas pensam, o Ajax não é uma linguagem, mas um grupo de tecnologias utilizadas para executar determinada tarefa (pensando bem, é muito semelhante ao web scraping).

Ajax quer dizer Asynchronous JavaScript and XML (JavaScript Assíncrono e XML), e é usado para enviar e receber informações de um servidor web sem fazer outra requisição de página.

Assim como o Ajax, o DHTML (Dynamic HTML, ou HTML Dinâmico) é um conjunto de tecnologias usado com um propósito comum. O DHTML é composto de código HTML ou linguagem CSS – ou ambos – que mudam à medida que scripts do lado cliente modificam elementos HTML da página.

Um botão pode aparecer somente depois que o usuário mover o cursor, uma cor de fundo pode mudar com um clique ou uma requisição Ajax pode disparar a carga de um novo bloco de conteúdo.

Se fizer scraping de muitos sites, logo você vai deparar com uma situação em que o conteúdo visualizado em seu navegador não será igual ao conteúdo visto no código-fonte obtido do site.

Você verá o resultado de seu scraper e coçará a cabeça, tentando entender onde foi parar tudo que você está vendo exatamente na mesma página em seu navegador.

As duas situações são causadas porque seu scraper não executa o JavaScript que faz a mágica acontecer na página. Sem o JavaScript, o HTML simplesmente fica lá parado, e o site parecerá muito diferente de como será visto em seu navegador web, o qual executa o JavaScript sem problemas.

**Há apenas duas soluções:** 
- fazer scraping do conteúdo diretamente do JavaScript 
- Usar pacotes Python capazes de executar o JavaScript e fazer scraping do site conforme visualizado em seu navegador.

#### Executando JavaScript em python com selenium

O Selenium funciona fazendo os navegadores carregarem o site de modo automático, obtendo os dados necessários e até mesmo capturando imagens de tela ou verificando se determinadas ações ocorrem no site.

O Selenium não contém o próprio navegador web; uma integração com navegadores de terceiros é necessária para a execução.

Se o Selenium fosse executado com o Firefox, por exemplo, você veria uma instância do Firefox ser aberta em sua tela, ele acessaria o site, e as ações que você tivesse especificado no código seriam executadas.

Ele carrega os sites na memória e executa o JavaScript da página, mas faz isso sem nenhuma renderização de imagens do site para o usuário. Ao combinar o Selenium com o PhantomJS, podemos executar um web scraper bastante eficaz, que lide com cookies, JavaScript, cabeçalhos e tudo que for necessário, com facilidade.

A biblioteca Selenium é uma API chamada no objeto WebDriver. O WebDriver é um pouco parecido com um navegador quanto à sua capacidade de carregar sites, mas também pode ser usado como um objeto BeautifulSoup para encontrar elementos da página, interagir com eles (enviar texto, clicar etc.) e executar outras ações para direcionar os web scrapers.

Nos casos em que ele exerça impactos sobre o modo de fazer scraping do site, o JavaScript pode ser facilmente executado com ferramentas como o Selenium, a fim de gerar a página com HTML simples cujo scraping aprendemos a fazer na primeira parte do livro.

Lembre-se de que só porque um site usa JavaScript não significa que todas as ferramentas tradicionais de web scraping devam ser jogadas pela janela. O propósito do JavaScript, em última análise, é gerar código HTML e CSS que seja renderizado pelo navegador, ou fazer uma comunicação dinâmica com o servidor por meio de requisições e respostas HTTP. Se o Selenium for usado, o HTML e o CSS da página podem ser lidos e interpretados como você faria com o código de qualquer outro site; as requisições e respostas HTTP podem ser enviadas e tratadas pelo seu código com as técnicas apresentadas nos capítulos anteriores, mesmo sem o uso do Selenium.

## Scraping atráves de Apis

Tradicionalmente, o JavaScript tem sido um obstáculo para os web crawlers em toda parte. Em algum momento na história antiga da internet, podíamos ter a garantia de que uma requisição ao servidor web devolveria os mesmos dados que o usuário veria no navegador se fizesse essa mesma requisição.

À medida que o JavaScript e a geração e carga de conteúdo via Ajax se tornaram mais presentes, essa situação passou a ser menos comum. No Capítulo 11, vimos uma maneira de resolver o problema: usar o Selenium para automatizar um navegador e buscar os dados. É uma solução simples. Quase sempre funciona.

O problema é que, quando temos um “martelo” tão potente e eficaz como o Selenium, todo problema de web scraping começa a se parecer bastante com um prego.

Neste capítulo, veremos como contornar totalmente o JavaScript (sem a necessidade de executá-lo ou sequer carregá-lo!) e ir direto à fonte dos dados: as APIs que os geram.

---

Uma API define uma sintaxe padronizada que permite a um software se comunicar com outro, mesmo que tenham sido escritos em linguagens diferentes ou estejam estruturados de modo distinto.

Uma API nem sempre precisa ser usada “pela internet”, e não necessariamente envolve qualquer tecnologia web.

A documentação dessas APIs em geral descreve rotas ou endpoints como URLs que podem ser requisitados, com parâmetros variáveis, seja no path do URL ou como parâmetros de GET.

A maioria das apis usa apenas metodos: 

- GET 
	- Podemos pensar em GET como uma requisição que dissesse: “Ei, servidor web, por favor, obtenha/me dê essas informações”.
	- Uma request get não modifica nada no servidor de destino.
- POST
	- POST é usado quando preenchemos um formulário ou submetemos informações, supostamente para um script de backend no servidor.
	- Sempre que fizermos login em um site, estaremos enviando uma requisição POST com o nome do usuário e uma senha criptografada (ou esperamos que esteja).
	- Se fizermos uma requisição POST com uma API, estaremos dizendo: *“Por favor, armazene essas informações em seu banco de dados”.*
- PUT 
	- Uma requisição PUT é utilizada para atualizar um objeto ou uma informação. Uma API pode exigir uma requisição POST para criar um novo usuário, por exemplo, mas poderá pedir uma requisição PUT para atualizar o endereço de email desse usuário
- DELETE
	- Serve para apagar dados de um banco de dados.
	- Métodos DELETE não são encontrados com frequência em APIs públicas, criadas essencialmente para disseminar informações ou para permitir aos usuários criar ou atualizar informações, e não para removê-las do banco de dados.

De modo diferente das requisições GET, as requisições POST, PUT e DELETE permitem enviar informações no corpo de uma requisição, além do URL ou da rota da qual os dados estão sendo requisitados.

Contudo, há um lado bom do JavaScript, Ajax e todas essas modernizações na web: como não formatam mais os dados em HTML, em geral os servidores atuam como wrappers finos em torno do próprio banco de dados. Esse wrapper simplesmente extrai dados do banco de dados e os devolve para a página por meio de uma API.

É claro que essas APIs não foram criadas com o intuito de serem usadas por nada nem ninguém além da própria página e, desse modo, os desenvolvedores não as documentam, e supõem (ou esperam) que ninguém as notará. Porém, elas existem.

----

#### Encontrando API'S não documentadas. 

Encontrar APIs não documentadas talvez exija um pouco de trabalho de detetive (para eliminar o trabalho de detetive, consulte a seção “Encontrando e documentando APIs de modo automático”), sobretudo em sites maiores, com muitas chamadas de rede. Em geral, porém, você as reconhecerá ao vê-las.

Caracteristicas comuns de chamadas as api's não documetadas: 
- Em geral, elas serão do tipo XHR.
  
- As APIs talvez nem sempre sejam óbvias, particularmente em sites grandes, com muitas funcionalidades que poderiam gerar centenas de chamadas durante a carga de uma única página. No entanto, encontrar a agulha metafórica no palheiro será muito mais fácil com um pouco de prática.

##### Documentando API'S não documentadas

Depois de ter encontrado uma chamada de API, em geral será conveniente documentá-la até certo ponto, sobretudo se seus scrapers dependerem

bastante dessa chamada. Talvez você queira carregar várias páginas do site, filtrando a chamada de API desejada na aba de rede no console da ferramenta de inspeção. Ao fazer isso, poderemos ver como as chamadas mudam de página para página, e identificar os campos que elas aceitam e devolvem.

**Qualquer chamada de API pode ser identificada e documentada se prestarmos atenção nos seguintes campos:**
- Método HTTP usado
- Entradas
	- Parâmetros do path
	- Cabeçalhos (incluindo cookies)
	- Conteúdo do corpo (para chamadas PUT e POST)
- Saidas
	- Cabeçalhos da resposta (incluindo os cookies definidos)
	- Tipo do corpo da resposta
	- Campos do corpo da resposta

#### Encontrando e documentando APIs de modo automático

A tarefa de localizar e documentar APIs pode parecer um pouco enfadonha e algorítmica. Isso ocorre porque, em sua maior parte, é assim mesmo.

Enquanto alguns sites podem tentar ofuscar o modo como o navegador obtém os dados, o que torna a tarefa um pouco mais complicada, encontrar e documentar APIs é essencialmente uma tarefa de programação.

Criei um repositório no GitHub em https://github.com/REMitchell/apiscraper que procura eliminar parte do trabalho pesado.

O programa usa Selenium, ChromeDriver e uma biblioteca chamada BrowserMob Proxy para carregar páginas, rastreá-las em um domínio, analisar o tráfego de rede durante a carga das páginas e organizar essas requisições em chamadas de API legíveis.

Várias partes são necessárias para que esse projeto execute. A primeira é o software propriamente dito.

----






## Veja também

- [[Automação e WebScraping (Ouro)]]
- [[Automação usando API não oficial]]
- [[Processo logar contas no automatico]]
- [[Learning AI - N8N]]
