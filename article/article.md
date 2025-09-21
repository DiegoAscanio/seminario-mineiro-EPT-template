---
title: "Título do Artigo"
subtitle: "Subtítulo (opcional)"
author:
  - "Nome Sobrenome¹"
  - "Outro Nome²"
date: 21 setembro 2025
lang: pt-BR

# Citações e bibliografia (ABNT)
csl: https://www.zotero.org/styles/associacao-brasileira-de-normas-tecnicas-ufrgs
bibliography: references.bib          # opcional; pode usar só o bloco 'references:' abaixo
citeproc: true
link-citations: true
reference-section-title: "Referências"

# Aparência (LaTeX/PDF)
documentclass: scrartcl
fontsize: 12pt
linestretch: 1.5
papersize: a4
geometry:
  - left=3cm
  - right=2cm
  - top=3cm
  - bottom=2cm
indent: true
toc: true
toc-title: "Sumário"
toc-depth: 2
abstract-title: "Resumo"

# Palavras-chave ficam também nos metadados (além de impressas abaixo do Resumo)
keywords:
  - palavra-chave 1
  - palavra-chave 2
  - palavra-chave 3

# Exemplos embutidos de referências (use estes ou troque pelo seu .bib)
references:
  - id: silva2020
    author:
      - family: Silva
        given: João P.
    issued:
      - year: 2020
    title: Introdução à Pesquisa Científica
    publisher: Editora Acadêmica
    type: book
    publisher-place: São Paulo
  - id: souza2022
    author:
      - family: Souza
        given: Maria A.
      - family: Pereira
        given: Carlos H.
    issued:
      - year: 2022
    title: "Modelagem e otimização em sistemas discretos"
    container-title: Revista Brasileira de Pesquisa Operacional
    volume: 42
    issue: 3
    page: 123-145
    type: article-journal
    DOI: 10.1234/rbpo.v42i3.2022
  - id: abnt6023
    author:
      - family: ABNT
        literal: Associação Brasileira de Normas Técnicas
    issued:
      - year: 2018
    title: NBR 6023 — Informações e documentação — Referências — Elaboração
    type: standard
---

## Resumo

Escreva aqui um **resumo** conciso (150–250 palavras) apresentando o tema, objetivo(s), método(s), resultado(s) principais e conclusão(ões). O resumo deve ser **informativo** e autossuficiente, sem citações extensas nem abreviações não definidas.

**Palavras-chave:** palavra-chave 1; palavra-chave 2; palavra-chave 3.

### Abstract (opcional)

Short version of the abstract in English (if required by the venue).  
**Keywords:** keyword 1; keyword 2; keyword 3.

# Introdução

Contextualize o problema, a motivação e os objetivos do estudo. Apresente brevemente a lacuna na literatura e contribuições do artigo. Cite trabalhos relevantes no fluxo do texto, por exemplo, segundo @silva2020, a estruturação do projeto influencia a qualidade dos resultados; estudos recentes reforçam esse ponto [@souza2022].

# Referencial teórico (ou Revisão de literatura)

Organize os conceitos, definições e trabalhos relacionados. Use citações **narrativas** (ex.: *Silva (2020) discute…*) ou **parentéticas** (ex.: *… já observado (SILVA, 2020)*), conforme o estilo ABNT aplicado automaticamente pelo CSL.

# Metodologia

Descreva o delineamento do estudo, materiais e métodos, escopo, critérios de inclusão/exclusão, instrumentos, procedimentos e forma de análise dos dados. Detalhe o suficiente para permitir **reprodutibilidade**.

# Resultados

Apresente os resultados de forma clara, com **tabelas** e **figuras** quando necessário.

| Métrica        | Grupo A | Grupo B |
|----------------|---------|---------|
| Acurácia (%)   | 92,3    | 88,7    |
| Tempo (s)      | 12,4    | 10,9    |

: Tabela 1 – Desempenho comparativo

*Fonte: elaboração própria.*

![Exemplo de figura com legenda.](images/Eleanor_Roosevelt_and_Human_Rights_Declaration.jpeg)

*Figura 1 – Fluxo resumido do método. Fonte: elaboração própria.*

# Discussão

Interprete os achados à luz da literatura, a plausibilidade dos resultados, limitações do estudo e implicações práticas/teóricas. Compare com trabalhos anteriores (e.g., ver @souza2022).

# Conclusão

Resuma as respostas aos objetivos, destaque contribuições e trabalhos futuros. Evite intro

