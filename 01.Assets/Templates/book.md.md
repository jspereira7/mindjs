<%*
Let autor = await tp.System.Prompt ("Qual o autor?")
Let ano = await tp.System.Prompt ("Ano de publicação?")
%>
# 📖 <% tp.file.title %>

**Autor:** <%* tR = autor %>  
**Ano:** <%* tR = ano %>  
**Criado em:** <% tp.date.now("YYYY-MM-DD HH:mm") %>

---
## Resumo
