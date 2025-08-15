![[Pasted image 20250618162518.png]]

![[Pasted image 20250611164958.png]]

Esse é o pipeline que precisamos implementar. 

Vamos usar a IA para entender os conceitos principais. 

---

**O que é replacement ?** 

- Replacement = substituir.

- Sempre que é feito o sync, os dados da tabela são apagados, e inseridos novamente. 

----

**O que é join ?** 

Após a coleta, o n8n une os dados (TT + RedTrack) referente aos mesmos dias. 

É criado uma tabela com os dados combinados dos ultimos 2 ou 3 dias.

---

**O que é essa tabela final com os dados prontos para serem consumidos ?** 

Essa tabela é onde os dados prontos já tratados e removido os duplicados são armazenados. 

---

**O que é append ?** 

**Append = Acresentar** 

Esse processo é sobre acresentar dados novos aos que você já tem. 

Exemplo: Imagine que você tem uma planilha de estoque de frutas, onde é guardado todas as frutas que vc tem na sua loja.

E hoje chega frutas novas para vc colocar no estoque, o append seria voce inserindo uma linha nova na tabela que voce tem, com os dados antigos...

Você está acresentando as novas frutas que chegaram, ao estoque que voce já tinha antes. 

![[Pasted image 20250618171954.png]]


----

**O que é deduplicação ?** 

**Deduplicação é como remover dados antigos.**

**Exemplo:** Se voce inseriu os dados de hoje, mas sem querer inseriu os dados de ontem denovo junto com os dados de hoje.

Agora você tem duas linhas iguais, o processo de deduplicar é remover as linhas duplicadas, que são exatamente iguais, mantendo somente a versão correta. 

----

**Append mais deduplicação:** 

1. **Append:** O sistema recebe os dados novos e insere ao historico.
2. **Deduplicação:** Antes de salvar tudo, ele verifica se já não tem linhas iguais, e remove o que está duplicado. 


----

**Precisamos entender como funciona e se dá pra criar uma nova tabela com base nos resultados de selects que fizemos.**

## Plano de execução

### Criar fluxo no n8n para o RedTrack.

Inserir os dados em uma tabela staging do RedTrack (armazenando os dados crus)

Na tabela staging ele só faz o append, adiciona as linhas novamente.

E adicionar um processo / query de replacement, pra sempre substituir os dados da tabela. 

Isso que precisamos fazer.

### Fazer o Join (RedTrack  + TikTokAds)

1) Crie outro fluxo no n8n chamado "Join TT + RTK"
2) Adicione 2 nós BigQuery:
	1) Nó para puxar os dados dos ultimos 3 dias de bigquery_tiktok_ads
	2) Outro nó para puxar os dados dos ultimos 3 dias de bigquery_redtrack
3) Adicione um nó function para fazer o join manualmente (unindo pelo ad_id e data)
4) Armazenar esses dados em uma tabela temporaria chamada tiktok_redtrack_joined



A base do tiktokads staging vai sempre puxar das contas de 0 até 60. 


Limpar a base do redtrack staging.

Tabelas que precisam criar. 
- tiktok_ads_staging
- red_track_staging_tiktok = puxar só 
- red_track_staging_google = futuramente 
- rtk_

---

Hmm entendi, talvez o que me atrapalhe entrar no flow tambem é que minha mente fica querendo fazer outras coisas, ao inves de fazer o que é importante. 

Ela tem outras coisas na frente, talvez só vir no obsidian e escrever um pouco, me ajude a descarregar o que tenho na mente. 

Fazendo assim minha mente ficar limpa. 

Escrever tambem me ajuda a deixar as ideias mais claras, porque textos são editaveis, então posso descarregar as coisas aqui, e depois editar o texto, deixando a ideia mais clara. 



