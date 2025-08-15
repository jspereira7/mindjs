## Transform. 

### Limpeza de Dados 

- Remover linhas com valores nulos ou invalidos. 
- Corrigir tipos de dados (String para data)
----
### Conversão 

Converter data para timestamp e etc... 

### Criação de tabelas derivadas

- Juntar dados de diferentes fontes
- Agregar dados por dia 

---
### Criar campos calculados 

Como:
- CTR ou etc... 
----
### Ferramentas para transformar dados

SQL, dataBuild Tool, apache pyspark, Stored procedurres no proprio dataWare house.

----
### Porque é importante transformar dados ? 

Sem transformação os dados são somente um monte de numeros soltos, a transformação dá sentido e estrutura, permitindo: 

- Criar dashboards
- Fazer analises reais e tomar melhores decisões
- Automatizar relatorios

---

### Resumo 

Pense no ELT assim: 

- Extract -> Extraia todos os dados que precisa
- Load -> Armazene tudo dentro do wareHouse
- Transform -> Use somente o que importa do jeito certo.

-----

### Processo de Transform - WorkFlow

1. Definir o objetivo da transformação
2. Limpeza e padronização (Remover Valores Nulos) 
3. Corrigir Formatos
4. Eliminar duplicatas (ex: via ROW_NUMBER() ou DISTINCT)
5. Modelagem dos dados (Agregar dados por periodo, juntar diferentes fontes)
6. Criação de Métricas de Negócio, como: (ROAS, CTR, CPL)

#### Checklist 

- Criar SQL de limpeza  -> Salvar como staging table
- Criar SQL de agregações/joins -> Salvar como model table

