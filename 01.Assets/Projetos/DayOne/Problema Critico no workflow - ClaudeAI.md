🤔 **Sua estratégia tem um problema crítico!**

## ⚠️ **PROBLEMA COM APPEND + LIMPEZA FINAL**

Se o pipeline roda **várias vezes ao dia** com append, você terá:

```
Execução 1 (09:00): 1000 registros
Execução 2 (12:00): +1500 registros (500 novos + 1000 duplicados)
Execução 3 (15:00): +2000 registros (500 novos + 1500 duplicados)
Execução 4 (18:00): +2500 registros (500 novos + 2000 duplicados)
```

**Resultado**: Tabela cresce exponencialmente com duplicatas até a limpeza!

## 🚨 **PROBLEMAS CRÍTICOS DESTA ABORDAGEM**

1. **Performance degradada**: Tabela fica gigante entre limpezas
2. **Consumo de storage**: Desperdício de espaço em disco
3. **Dashboard lento**: Queries ficam lentas com milhões de duplicatas
4. **Risco de falha**: Se a limpeza falhar, tabela fica corrompida
5. **Janela de inconsistência**: Dashboard mostra dados duplicados entre execuções

## 💡 **ESTRATÉGIAS MELHORES PARA MÚLTIPLAS EXECUÇÕES**

### **Opção A: UPSERT (Recomendada)**

```sql
-- Sempre sobrescreve registros existentes
MERGE INTO tabela_consolidada AS target
USING tt_rtk_raw AS source
ON target.ad_id = source.ad_id AND target.datetime = source.datetime
WHEN MATCHED THEN UPDATE SET [campos...]
WHEN NOT MATCHED THEN INSERT [valores...]
```

### **Opção B: DELETE + INSERT por período**

```sql
-- Remove dados do período atual antes de inserir
DELETE FROM tabela_consolidada 
WHERE DATE(datetime) = CURRENT_DATE;

INSERT INTO tabela_consolidada 
SELECT DISTINCT * FROM tt_rtk_raw;
```

### **Opção C: Staging + Replace**

```sql
-- Cria tabela temp, depois substitui
CREATE TABLE tabela_consolidada_temp AS 
SELECT * FROM tabela_consolidada 
WHERE DATE(datetime) < CURRENT_DATE;

INSERT INTO tabela_consolidada_temp 
SELECT DISTINCT * FROM tt_rtk_raw;

DROP TABLE tabela_consolidada;
ALTER TABLE tabela_consolidada_temp RENAME TO tabela_consolidada;
```

**Qual dessas opções faz mais sentido? A Opção A (UPSERT) é geralmente a mais robusta para seu cenário.**