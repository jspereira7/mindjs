

![[Pasted image 20250611171401.png]]

### Arquitetura completa
1. Coleta dos dados do tiktok ads via FiveTran
2. Criação da dataBase TikTokAds no bigQuery, todas as tabelas individuais são agregadas e armazenadas em uma nova dataBase dedicada ao TT ads, funciona como um datamart intermediario.
3. Coleta dos dados do RedTrack
4. Transformação e integração
	1. Feito um Join entre os dados do TikTok e do RedTrack. (Consolidar os dados do TikTok com os do redtrack)
5. DataBase temporaria dos ultimos 3d 
	1. Resultado do join é armazenado em uma nova dataBase com os dados combinados dos ultimos 3d.
6. Append e deduplicacão.
	- Esse conjunto de dados dos ultimos 3d é adicionado a base completa da operação, com um processo de desduplicacao. 

**Banco de Dados que vão Existir**
- DataBase TikTokAds (last3days)
- DataBase RedTrack (last3days)
- DataBase TikTokAds + RedTrack (last3days)
- DataBase DayOne Geral.

---
O que falta é juntar o ttk + rtk pelo utc e ad_id. 

Obs importantes: 
- Juntar os dados usando ad_id + horario, converter o horario pro fuso do UTC (RedTrack) pelo horario e ad_id, vamos fazer o match.

---

### DataSet direct_response_dev

[[schema]] -> tt_rtk_raw_lifetime.

**rtk_raw_last3d** = 
	tabela com os dados do rtk dos ultimos 3 dias (replacement)

**ttads_raw_last3d** = 
	tabela com os dados de todas as contas do tiktok ads (replacement)

**tt_rtk_replacment_last3d** = 
	tabela TikTokAds + Rtk, somente dos ultimos 3 dias (replacement). 

**tt_rtk_raw_lifetime** = 
	tabela TikTokAds + Rtk, armazenando os dados. 
  


#### To-do 

- [x] rtk_stg_last3d
- [x] ttads_stg_last3d
- [x] tt_rtk_stg_last3d
- [x] tt_rtk_raw_lifetime

