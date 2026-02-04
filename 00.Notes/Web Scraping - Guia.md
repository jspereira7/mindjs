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





