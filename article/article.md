---
header-includes:
  - |
    ```{=latex}
    % thanks (como no \author) para mostrar instituição do autor
    % como nota de rodapé
    \makeatletter
    \renewcommand\thefootnote{\arabic{footnote}}
    \makeatother

    \usepackage{caption}

    \usepackage{float}
    \usepackage{graphicx}
    \usepackage{setspace}
    % Ambiente Fonte: centralizado, espaçamento 1, itálico, sem espaço extra
    \newenvironment{Fonte}
      {\par\begin{center}\begingroup\setstretch{1}\normalsize}
      {\par\endgroup\end{center}}

    % cabeçalhos e rodapés
    \usepackage{fancyhdr}
    \pagestyle{fancy}
    \fancyhf{} % limpa cabeçalho/rodapé

    % Cabeçalho à esquerda (2 linhas)
    \fancyhead[C]{%
      \begin{tabular}[t]{@{}l@{}}
        II Seminário Mineiro da Educação Profissional e Tecnológica  - 25 a 27 de setembro de 2025
      \end{tabular}
    }

    % Rodapé central (2 linhas), sem número de página
    \fancyfoot[C]{%
      \begin{tabular}[t]{@{}c@{}}
        Mestrado Profissional em Educação Profissional e Tecnológica – ProfEPT CEFET-MG
      \end{tabular}
    }

    % sem linhas de regra no topo/rodapé
    \renewcommand{\headrulewidth}{0pt}
    \renewcommand{\footrulewidth}{0pt}

    % Alinhamento com a largura do texto
    \fancyheadoffset{0pt}
    \fancyfootoffset{0pt}

    % numero de página no canto inferior direito
    \fancyfoot[R]{\thepage}

    % Garante que a página "plain" (ex.: após \maketitle) use o mesmo estilo
    \fancypagestyle{plain}{%
      \fancyhf{}
      \renewcommand{\headrulewidth}{0pt}
      \renewcommand{\footrulewidth}{0pt}
    }

    % título
    
    \usepackage{titling}
    % Sobe o bloco de título para "colar" no topo da página:
    %\setlength{\droptitle}{-6em} % ajuste fino: -4em a -10em conforme sua margem
    % Imagem acima do título:

    % --- Título com logo acima (ajuste seu includegraphics como já usa) ---
    \pretitle{%
      \begin{center}
      \vspace*{-1.5cm}%
      \includegraphics[width=\textwidth]{images/logo.png}\\[0.75\baselineskip]
      \Large
    }

    ```
title: "\"Título do Artigo\""
subtitle: "Subtítulo (opcional)"
author:
  - "\\normalsize \\href{mailto:author1@inst1.edu}{Nome Sobrenome Primeiro Autor}\\thanks{Instituição do Primeiro Autor – ex.: CEFET-MG}"
  - "\\normalsize \\href{mailto:author2@inst2.edu}{Nome Sobrenome Segundo Autor}\\thanks{Instituição do Segundo Autor – ex.: UEMG}"
  - "\\normalsize \\href{mailto:author3@inst3.edu}{Nome Sobrenome Terceiro Autor}\\thanks{Instituição do Terceiro Autor – ex.: UEMG}"
date: ""
lang: pt-BR

# Citações e bibliografia (ABNT)
csl: https://www.zotero.org/styles/associacao-brasileira-de-normas-tecnicas
bibliography: references.bib          # opcional; pode usar só o bloco 'references:' abaixo
citeproc: true
link-citations: true
reference-section-title: "Referências"

# Aparência (LaTeX/PDF)
documentclass: article
fontsize: 12pt
linestretch: 1.5
papersize: a4
geometry:
  - left=2cm
  - right=2cm
  - top=1cm
  - bottom=1cm
  - includehead
  - includefoot
  - headheight=28pt   # altura do cabeçalho
  - headsep=15pt      # espaço entre cabeçalho e texto
  - footskip=15pt     # distância do rodapé ao texto
  - heightrounded
indent: false
toc: false 
toc-title: "Sumário"
toc-depth: 2

# Numeração de seções
numbersections: false

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

\vspace{-\baselineskip}

**Resumo**

Escreva aqui um **resumo** conciso (150–250 palavras) apresentando o tema, objetivo(s), método(s), resultado(s) principais e conclusão(ões). O resumo deve ser **informativo** e autossuficiente, sem citações extensas nem abreviações não definidas.

**Palavras-chave:** palavra-chave 1; palavra-chave 2; palavra-chave 3.

**Abstract (opcional)**

Short version of the abstract in English (if required by the venue).  
**Keywords:** keyword 1; keyword 2; keyword 3.

\newpage

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

: Desempenho comparativo.

::: fonte
Fonte: [@souza2022].
:::

<!-- para adicionar figuras, use a sintaxe abaixo -->

![Exemplo de Imagem](images/Eleanor_Roosevelt_and_Human_Rights_Declaration.jpeg){#fig:exemplo width=60% placement=H}

::: fonte
Fonte: [@silva2020].
:::


# Discussão

Interprete os achados à luz da literatura, a plausibilidade dos resultados, limitações do estudo e implicações práticas/teóricas. Compare com trabalhos anteriores (e.g., ver @souza2022).

# Conclusão

Resuma as respostas aos objetivos, destaque contribuições e trabalhos futuros.

