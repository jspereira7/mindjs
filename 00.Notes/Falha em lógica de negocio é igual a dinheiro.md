---
tags:
  - hacking
  - money
---
Hoje em dia o maior alvo dos hackers para ganhar dinheiro é a falha na lógica de negocios do sistema. 

**O que é uma Business Logic Flaw na prática:**

É quando você _usa o sistema como ele foi projetado_, mas de uma forma que o desenvolvedor não previu. Exemplos clássicos:

- Colocar preço negativo num carrinho de compras e receber dinheiro de volta
- Comprar um item, fazer o processo de devolução, e ficar com o item e o dinheiro
- Pular etapas de um fluxo de pagamento manipulando a ordem das requisições
- Usar um cupom de desconto infinitas vezes

---

Genial, podemos usar as IAs para ter ideias de como explorar a lógica de negocio de xyz sistema, e tirar vantagem disso... 

---

**Falhas em lógica de negocio = $ Money**

## Exemplo mercado de afiliados

**Os players do ecossistema** (exatamente como você conhece):

- **Merchant** — paga comissão por cliques, cadastros, compras
- **Affiliate** — coleta comissão por CPC ou CPA
- **Customer** — a pessoa que converte
- **Affiliate Network** — a tecnologia que conecta e monitora tudo

**Como deveria funcionar:** O afiliado coloca um link com seu ID. O usuário clica → recebe um cookie com o AffiliateID → se comprar dentro do período, o afiliado recebe comissão. Simples.

**Cookie Stuffing — 2002:**

A primeira grande fraude. O sistema assumia que o usuário precisava _clicar_ no link para receber o cookie. Mas tecnicamente isso nunca foi obrigatório — qualquer requisição HTTP ao endpoint da rede já setava o cookie.

Então ao invés de um link clicável, o afiliado usava:

```html
<img src="http://AffiliateNetwork/p?program=50&affiliate_id=100/">
```

ou um iframe invisível (width=0, height=0).

O visitante do site do afiliado recebia o cookie **sem clicar em nada**, sem saber. Se depois fosse ao merchant e comprasse, a comissão ia para o afiliado fraudulento.

**Escalada — posting em qualquer lugar:** Afiliados agressivos perceberam que podiam postar esse código em fóruns, livros de visitas, redes sociais — qualquer lugar que renderizasse HTML. O cookie era setado em qualquer pessoa que visitasse aquelas páginas. Os fóruns mostrados no slide — BlackHatWorld, SEO Black Hat — eram exatamente onde essas técnicas eram discutidas e vendidas.

**A defesa de 2005 e o bypass de 2007:**

As redes começaram a monitorar referers e taxas de conversão suspeitas. A resposta dos fraudadores: postar o código em páginas **HTTPS**. O protocolo HTTP (RFC 2616) especifica que navegadores não devem enviar o header `Referer` quando vêm de uma página segura para uma não-segura — então a origem some, sem rastro.

Em 2008 já usavam DNS-Rebinding, GIFAR e Flash malware para o mesmo fim.
### Gaming referral incentives — o mais direto ao ponto:

Merchant paga $5-50 por novo usuário que se cadastra com cartão de crédito. 

O afiliado fraudulento cria milhares de cadastros falsos usando **cartões de crédito de uso único** (facilmente obtidos). 

O merchant não tem como saber que é cartão descartável. 

Dezenas a centenas de milhares de dólares extraídos assim.

**Gaming referral revenue from purchases — o mais sofisticado:**

1. Afiliado tem números de cartão de crédito roubados
2. Usa esses cartões para comprar produtos **e envia para o endereço real do dono do cartão**
3. Nenhum alerta de fraude é disparado — o endereço bate
4. A comissão é paga ao afiliado
5. Dias depois o dono do cartão recebe o produto, não reconhece a compra, disputa
6. O merchant estorna — mas o afiliado **já foi pago e sumiu**

O timing é a chave: o ciclo de pagamento de comissão é mais rápido que o ciclo de chargeback.

----

## Método Black Hat de Cartões de Crédito com limite

![[search_realizesolucoesfinanceiras_com_brcartoes_renner_2026_03_2.txt]]

Usar essa pesquisa de cartões de crédito com limite pra usar etc... 

