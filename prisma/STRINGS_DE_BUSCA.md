# Strings de Busca por Base de Dados

> **Tema:** Prompt Injection em LLMs e Sistemas Agênticos
> **Período:** 2023-2026

---

## 1. arXiv (arxiv.org)

**URL:** https://arxiv.org/search/advanced

> **ATENÇÃO:** O arXiv NÃO aceita operadores booleanos complexos. Faça buscas separadas e some os resultados.

**Busca 1:**
```
"prompt injection" AND "large language model"
```

**Busca 2:**
```
"prompt injection" AND LLM
```

**Busca 3:**
```
jailbreak AND "large language model"
```

**Busca 4 (opcional):**
```
"indirect prompt injection"
```

**Configurações:**
- Field: All fields
- Include cross-list: ✓ Yes
- Subject: Computer Science
- Date: From 2023-01-01 To 2026-12-31

**Como registrar:** Some os resultados das buscas (removendo duplicatas óbvias) e anote o total.

**Exportar:** Selecione os papers → Export BibTeX (ou use Zotero Connector)

---

## 2. Google Scholar (scholar.google.com)

**URL:** https://scholar.google.com/

**String (copiar na barra de busca):**
```
("prompt injection" OR jailbreak) ("large language model" OR LLM) security attack
```

**String alternativa (mais específica):**
```
"prompt injection" "LLM" OR "large language model" vulnerability defense
```

**Configurações:**
- Clicar em "Desde 2023" no menu lateral
- Ordenar por relevância (padrão)
- **IMPORTANTE:** Limitar aos primeiros 100 resultados (declarar isso no artigo)

**Exportar:** Use a extensão Zotero Connector no navegador (clica no ícone da pasta)

---

## 3. IEEE Xplore (ieeexplore.ieee.org)

**URL:** https://ieeexplore.ieee.org/search/advanced

**String (usar o Command Search):**
```
("prompt injection" OR "jailbreak" OR "adversarial prompt") AND ("large language model" OR "LLM" OR "generative AI" OR "agent")
```

**Ou no formulário Advanced Search:**
- Field 1: "prompt injection" [All Metadata] OR "jailbreak" [All Metadata]
- AND
- Field 2: "large language model" [All Metadata] OR "LLM" [All Metadata]

**Filtros:**
- Year: 2023-2026
- Content Type: Conferences, Journals, Early Access

**Exportar:** Selecionar todos → Export → BibTeX

---

## 4. ACM Digital Library (dl.acm.org)

**URL:** https://dl.acm.org/search/advanced

**String (no campo de busca avançada):**
```
[[All: "prompt injection"] OR [All: "jailbreak"]] AND [[All: "large language model"] OR [All: "LLM"] OR [All: "language model agent"]]
```

**String simplificada (busca básica):**
```
"prompt injection" "large language model" security
```

**Filtros:**
- Publication Date: Custom range → 2023 to 2026
- Content Type: Research Article, Short Paper

**Exportar:** Select All → Export Citations → BibTeX

---

## 5. Semantic Scholar (semanticscholar.org)

**URL:** https://www.semanticscholar.org/

**String (copiar na barra de busca):**
```
prompt injection attack large language model security
```

**String alternativa:**
```
jailbreak LLM vulnerability defense
```

**Filtros (menu lateral):**
- Year: 2023-2026
- Fields of Study: Computer Science
- Publication Type: Conference Paper, Journal Article

**Exportar:** Selecionar papers → Cite → BibTeX

---

## 6. Busca complementar: Snowballing

Após ter os 10 papers principais, faça:

1. **Backward snowballing:** Olhe as referências dos 10 papers e verifique se alguma é relevante
2. **Forward snowballing:** No Google Scholar, clique em "Citado por" para ver quem citou seus papers

Registre papers encontrados por snowballing separadamente (isso vai na caixa "Other methods" do PRISMA).

---

## Resumo das Strings

| Base | String Principal |
|------|------------------|
| arXiv | `("prompt injection" OR "jailbreak") AND ("LLM" OR "large language model")` |
| Google Scholar | `("prompt injection" OR jailbreak) ("large language model" OR LLM) security` |
| IEEE Xplore | `("prompt injection" OR "jailbreak") AND ("large language model" OR "LLM")` |
| ACM DL | `"prompt injection" "large language model" security` |
| Semantic Scholar | `prompt injection attack large language model security` |

---

## Checklist antes de começar

- [ ] Instalar Zotero + Zotero Connector no navegador
- [ ] Criar coleção "Revisão - Prompt Injection LLMs" no Zotero
- [ ] Abrir a planilha LOG_BUSCA.csv para registrar
- [ ] Ter os critérios de inclusão/exclusão em mãos (CRITERIOS.md)
