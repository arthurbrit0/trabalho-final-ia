# Guia Prático PRISMA - Passo a Passo

## Arquivos criados

```
prisma/
├── LOG_BUSCA.csv         → Registrar cada busca que você fizer
├── TRIAGEM.csv           → Registrar decisão de cada paper
├── PRISMA_CONTAGEM.csv   → Calcular os números do PRISMA
├── CRITERIOS.md          → Critérios de inclusão/exclusão
├── STRINGS_DE_BUSCA.md   → Strings prontas para cada base
└── README.md             → Este guia
```

---

## PASSO 1: Preparação (10 min)

1. **Instale o Zotero:** https://www.zotero.org/download/
2. **Instale o Zotero Connector** no seu navegador
3. **Abra o Zotero** e crie uma coleção chamada "PRISMA - Prompt Injection"
4. **Abra LOG_BUSCA.csv** no Google Sheets ou Excel

---

## PASSO 2: Fazer as buscas (30-60 min)

Para CADA base de dados:

### 2.1 - arXiv
1. Acesse: https://arxiv.org/search/advanced
2. Cole a string do arquivo `STRINGS_DE_BUSCA.md`
3. Configure os filtros (2023-2026, cs.CR/cs.CL/cs.AI)
4. **Anote o número de resultados** no LOG_BUSCA.csv
5. Exporte em BibTeX e importe no Zotero

### 2.2 - Google Scholar
1. Acesse: https://scholar.google.com/
2. Cole a string
3. Filtre "Desde 2023"
4. **Anote o número aproximado** (ex: "~250, usamos top 100")
5. Use o Zotero Connector para salvar os primeiros 100

### 2.3 - IEEE Xplore
1. Acesse: https://ieeexplore.ieee.org/search/advanced
2. Cole a string no Command Search
3. Filtre: 2023-2026, Conferences + Journals
4. **Anote o número de resultados**
5. Exporte BibTeX → Importe no Zotero

### 2.4 - ACM DL
1. Acesse: https://dl.acm.org/search/advanced
2. Cole a string
3. Filtre: 2023-2026, Research Article
4. **Anote o número de resultados**
5. Exporte BibTeX → Importe no Zotero

### 2.5 - Semantic Scholar
1. Acesse: https://www.semanticscholar.org/
2. Cole a string
3. Filtre: 2023-2026, Computer Science
4. **Anote o número de resultados**
5. Exporte BibTeX → Importe no Zotero

---

## PASSO 3: Deduplicação no Zotero (10 min)

1. No Zotero, clique na sua coleção
2. Vá em **Edit → Duplicate Items** (ou veja a pasta "Duplicate Items" na biblioteca)
3. Para cada duplicata: selecione → clique direito → **Merge Items**
4. **Anote quantas duplicatas você removeu**
 35
---

## PASSO 4: Triagem por título/resumo (1-2 horas)

1. Abra `TRIAGEM.csv`
2. Para cada paper no Zotero:
   - Leia o **título** e o **abstract**
   - Decida: INCLUIR ou EXCLUIR
   - Se excluir, anote o código do motivo (E1, E2, E3, etc. - veja CRITERIOS.md)
3. **Conte quantos você excluiu** nesta fase

---

## PASSO 5: Leitura de texto completo (2-4 horas)

Para os papers que passaram na triagem de título/resumo:

1. Tente obter o PDF (Zotero geralmente baixa automaticamente)
2. Se não conseguir o PDF: marque "Não" em "Texto Completo Disponível" e anote o motivo
3. Leia o texto completo
4. Decida: INCLUIR ou EXCLUIR
5. Se excluir, anote o código do motivo

**Objetivo:** Chegar aos seus 10 papers finais

---

## PASSO 6: Preencher os números do PRISMA

Abra `PRISMA_CONTAGEM.csv` e preencha:

```
Exemplo (substitua pelos seus números reais):

A = 172  (soma de todas as bases)
B = 0    (snowballing, se tiver)
C = 28   (duplicatas removidas no Zotero)
D = 0    (removidos por outros motivos)
E = 144  (A + B - C - D = 172 + 0 - 28 - 0)
F = 97   (excluídos por título/resumo)
G = 47   (E - F = 144 - 97)
H = 2    (PDFs não obtidos)
I = 45   (G - H = 47 - 2)
J = 35   (excluídos após leitura completa)
K = 10   (I - J = 45 - 35) ← DEVE DAR 10!
```

---

## PASSO 7: Gerar o diagrama PRISMA (15 min)

1. Acesse: https://www.prisma-statement.org/prisma-2020-flow-diagram
2. Escolha o template:
   - Se só usou bases de dados: "Identification of studies via databases and registers"
   - Se fez snowballing também: "via databases/registers + other methods"
3. Preencha os números A-K nos campos correspondentes
4. Clique em **Download** → escolha **PDF**
5. Salve como `prisma.pdf`

---

## PASSO 8: Colocar no LaTeX (5 min)

1. Crie a pasta `figures/` no seu projeto (se não existir)
2. Coloque o `prisma.pdf` dentro de `figures/`
3. No seu arquivo `.tex`, substitua o placeholder atual por:

```latex
\begin{figure}[t]
  \centering
  \includegraphics[width=0.95\textwidth]{figures/prisma.pdf}
  \caption{Fluxograma PRISMA 2020 do processo de identificação, triagem e seleção dos estudos.}
  \label{fig:prisma}
\end{figure}
```

---

## Checklist Final

- [ ] LOG_BUSCA.csv preenchido com todas as buscas
- [ ] TRIAGEM.csv com todos os papers avaliados
- [ ] PRISMA_CONTAGEM.csv com os números fechando
- [ ] Diagrama PRISMA gerado (prisma.pdf)
- [ ] Figura incluída no LaTeX
- [ ] Números do texto do artigo atualizados

---

## Dúvidas comuns

**P: E se os números não "fecharem" em 10?**
R: Revise seus critérios. Talvez precise incluir ou excluir mais papers. Os 10 papers da Tabela 1 do seu artigo são o ponto de chegada.

**P: Posso fazer isso com menos papers nas bases?**
R: Sim, mas um PRISMA com poucos resultados (ex: só 15 papers no total) parece pouco sistemático. Idealmente, você quer pelo menos 50-100 resultados iniciais.

**P: E se eu já tenho os 10 papers escolhidos "na mão"?**
R: Você ainda precisa documentar de onde eles vieram. Faça as buscas e verifique se seus 10 papers aparecem nos resultados. Se não aparecerem, ajuste as strings.

**P: Preciso fazer isso sozinho?**
R: Idealmente, 2 pessoas fazem a triagem independentemente e comparam. Mas para trabalho de disciplina, 1 pessoa é aceitável - só declare isso no artigo.
