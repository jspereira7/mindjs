# 🧹 Dashboard de Limpeza do Cofre

> Revise cada seção abaixo e decida o destino de cada nota.

---

## 🕸️ 1. Notas Órfãs (sem nenhum link)
*Notas que ninguém referencia e não referenciam ninguém — candidatas a deletar.*
```dataview
TABLE file.ctime AS "Criada", file.mtime AS "Modificada"
FROM "" 
WHERE length(file.inlinks) = 0 
AND length(file.outlinks) = 0
AND file.name != "_Dashboard de Limpeza"
SORT file.mtime ASC
```

---

## 📭 2. Notas Vazias ou Muito Curtas
*Notas com menos de 3 linhas — provavelmente rascunhos abandonados.*
```dataview
TABLE file.size AS "Tamanho (bytes)", file.mtime AS "Última edição"
FROM ""
WHERE file.size < 300
AND file.name != "_Dashboard de Limpeza"
SORT file.size ASC
```

---

## 🧊 3. Notas Congeladas (sem edição há mais de 90 dias)
*Notas que você não toca há muito tempo.*
```dataview
TABLE file.mtime AS "Última edição", file.folder AS "Pasta"
FROM ""
WHERE date(today) - file.mtime > dur(90 days)
AND !contains(file.folder, "Daily Notes")
SORT file.mtime ASC
```

---

## 📥 4. Notas Presas na Inbox (00.Notes sem links de saída)
*Notas que deveriam ter sido processadas mas ficaram paradas.*
```dataview
TABLE file.ctime AS "Criada", file.mtime AS "Modificada"
FROM "00.Notes"
WHERE length(file.outlinks) = 0
SORT file.ctime ASC
```

---

## 📅 5. Daily Notes Antigas (mais de 60 dias)
*Diários antigos — você pode arquivar ou deletar com mais tranquilidade.*
```dataview
TABLE file.ctime AS "Data"
FROM "Daily Notes"
WHERE date(today) - file.ctime > dur(60 days)
SORT file.ctime ASC
```