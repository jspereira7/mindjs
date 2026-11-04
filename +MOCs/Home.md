---
type: moc
tags:
  - moc
summary: Ponto de entrada do vault. Links para todos os MOCs temáticos, dashboards e listas de trabalho.
created: 2026-11-04
updated: 2026-11-04
---
# Home

Ponto de entrada do vault. Comece por aqui e desça para o MOC do tema.

## Temas

- [[MOC - Tipologia Junguiana]] — funções cognitivas, Beebe, Octagram, Socionics, como tipar
- [[MOC - Tipos e Autoconhecimento]] — ENTP, ESTP, ISTP, Ego Hacking, testes e perfis
- [[MOC - Modelos Mentais]] — sistemas, vieses, decisão e estratégia
- [[MOC - TDAH e Funções Executivas]] — Barkley, Hallowell, estratégias práticas
- [[MOC - Relacionamentos e Masculinidade]] — atração, SMV, enquadre, aparência
- [[MOC - Produtividade e Planejamento]] — GTD, hábitos, planos, aprendizado
- [[MOC - Negócios, Marketing e Finanças]] — finanças, marketing, projetos de tráfego
- [[MOC - IA e Tecnologia]] — prompts, automação, scraping, ferramentas
- [[MOC - Livros e Cursos]] — anotações de livros e cursos

## MOCs que já existiam

- [[MOC - ENTP Owner - Course.]]
- [[Moc Livro The Manual]]

## Dashboards

- [[Livros.base]]
- [[Modelos Mentais.base]]
- [[Banco de notas base.base]]
- [[Dashboard de Limpeza de Notas]]

## Notas recentes

```dataview
TABLE file.mtime AS "Modificada"
FROM "00.Notes"
WHERE file.ext = "md"
SORT file.mtime DESC
LIMIT 10
```

## Fila de conexão: notas sem nenhum link de entrada

Notas que nenhum outro arquivo aponta. Ao ligar uma delas a um MOC ela sai desta lista.

```dataview
LIST
FROM "00.Notes"
WHERE file.ext = "md" AND length(file.inlinks) = 0
SORT file.mtime DESC
LIMIT 30
```
