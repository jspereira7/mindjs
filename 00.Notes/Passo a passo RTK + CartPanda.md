
# 1) Config Dominio no RTK (Opicional)

Esse passo é basicamente adicionar um dominio personalizado no redtrack, bem easy, provavelmente o cara já fez isso. 

- https://help.redtrack.io/knowledgebase/kb/conversion-tracking/adding-custom-domain/

Custom tracking domain basicamente.

----
# 2) Offer Source

Offer sources/Brands → New From Template → Search for CartPanda → Add → fill in the mandatory fields → copy the postback URL → Save:

![[Pasted image 20260227212316.png]]

CartPanda só envia postback pra compra aprovada. 

**Config importante:** 

![[Pasted image 20260227215039.png]]

Copiar link do postback final. 

https://zxjz1.ttrk.io/postback?status=approved&fname={first_name}&lname={last_name}&phone={phone_number}&email={email}&contentid={product_id}&product={product_name}&clickid={cid}&sum={total_price}
# 3) Criar Offer

Aqui iremos criar a offer, inserindo o link do checkout da cart panda, e adicionando os parametros que iremos enviar. 

Ou seja o clickid.

**Deixar status de conversão como approved.

# 4 ) Criar o Traffic Channel 

Adicionar link do postback anterior: 
- https://zxjz1.ttrk.io/postback?status=approved&fname={first_name}&lname={last_name}&phone={phone_number}&email={email}&contentid={product_id}&product={product_name}&clickid={cid}&sum={total_price}

https://zxjz1.ttrk.io/postback?status=approved&clickid={cid}&sum={total_price}




## Veja também

- [[Traffic Brokering - How to Make Money with Affiliates]]
- [[Funis de Email.]]
- [[Estratégia pra levantar caixa]]
