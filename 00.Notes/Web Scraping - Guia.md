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

Embora pareça interessante ver isso, prefiro que meus scripts executem de modo silencioso em segundo plano, portanto uso uma ferramenta chamada PhantomJS (http://phantomjs.org/) em vez de utilizar um navegador de verdade.

O **PhantomJS** é o que conhecemos como um navegador headless (sem cabeça).

Ele carrega os sites na memória e executa o JavaScript da página, mas faz isso sem nenhuma renderização de imagens do site para o usuário. Ao combinar o Selenium com o PhantomJS, podemos executar um web scraper bastante eficaz, que lide com cookies, JavaScript, cabeçalhos e tudo que for necessário, com facilidade.

A biblioteca Selenium é uma API chamada no objeto WebDriver. O WebDriver é um pouco parecido com um navegador quanto à sua capacidade de carregar sites, mas também pode ser usado como um objeto BeautifulSoup para encontrar elementos da página, interagir com eles (enviar texto, clicar etc.) e executar outras ações para direcionar os web scrapers.







