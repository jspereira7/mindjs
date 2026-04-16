---
tags:
  - hacking
  - programacao
---
# Introdução 

As chamadas de api's representam impressionantemente 83% de todo o trafego web. 

E são extremamente lucrativas para os ciber criminosos, por dois motivos: 
1. Fonte abundante de informações sensiveis
2. Frequentes falhas de segurança

Quando você solicita um emprestimo ao banco, é uma api que consulta o seu historico de crédito. 

Se um cibercriminoso conseguir comprometer a api, ele terá acesso a informações precisosas.

Sua tarefa como pentester de api pode ser tão simples quanto fazer uma request para um end-point de uma api. 

Com esse livro nossa intenção é te mostrar como testar uma api com diversas vulnerabilidades. 

Nosso foco é em apis rest's. 

Primeio vc aprenderá ferrametas e técnicas para usar a api conforme o esperado. 

Em seguida vc sondará em busca de vulnerabilidades e irá aprender explorá-las. 

## O vicio de hackear apis web

> Os recursos mais valiosos do mundo não são o petroleo, mas sim os dados

A api faz com que um recurso valioso flutue num piscar de olhos. 

Em termos simples uma api, é uma tecnologia que permite a comunicação entre diferentes aplicações. 

Hackear apis não é dificil, depois que você sabe como elas funcionam, é simplemente saber fazer a requisição http correta.

É extremamente importe que você realize os ataques na prática, utilizando os laboratorios, e só depois tente implementar os seus proprios métodos de ataque. 

Parte 1 = Conhecimento necessario sobre aplicações web

Parte 2 = Configurar laborátorio de testes.

Parte 3 = Começar a hackear na prática. 

Metafora API x Restaurante: 
- Um aplicativo é como um restaurante. 
- A api é como um garçom. 
- A documetação é o cardápio. 
- Você pode fazer pedidos ao garçom com base no cardápio e o garçom te dará o que você pediu. 
- Os devs então podem fazer um aplicativo para atender a solicitação da forma que desejarem. 

Como um hacker você vai explorar cada canto do restaurante, vai aprender como ele funciona. 

Pode ser que você tente enganar o segurança, ou até mesmo fornecendo um token de autenticação roubado. 

Além disso vc vai analisar o cardapio em busca de maneiras de enganar a API para obter dados aos quais você não tem autorização, talvez convencendo o garçom a lhe entregar tudo o que ele tem. 

Você pode até convencer o dono da api te dar as chaves do restaurante. 

Esse livro é uma abordagem holistica ao hacking de apis. 

- Compreendendo como funcinam as aplicações web e a anatomia das apis web. 
- Dominanto as principais vulnerabilidades de api sob a perspectiva de um hacker.
- Aprender as ferrametas mais eficazes para hackear apis. 
- Realizar reconhecimento passivo e ativo de apis, para descobrir as capacidades da api, encontrar segredos expostos e analisar as funcionalidades da api. 
- Interagindo com apis e testando-as com o poder do fuzzing.
- Realizar uma variedade de ataques para descobrir vulnerabilidades de api. 

Você deve agir como um atacante que quer explorar a api. 

----

# Parte 1 - Como funcionam os Apps Web

Noções basicas: 

- Os aplicativos web funcionam com base no modelo client/servidor.
	- Navegador (Client) faz requests de recursos e as envia para computadores chamados servidores web.
- App Web se refere a softwares que são executados em um servidor web, como wipedia, linkedin etc... 

Os sites somente fornecem dados para a leitura, uma comunicação unilateral. 

Os apps web permitem que a comunicação ocorroa de maneira mutua, do server pa






