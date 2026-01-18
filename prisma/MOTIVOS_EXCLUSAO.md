# Motivos de Exclusão - Resumo para o Artigo

## Triagem por Título/Resumo (588 excluídos)

| Motivo | Código | Quantidade | Exemplos |
|--------|--------|------------|----------|
| Fora do escopo (não taxonomia/defesa/survey) | E6 | ~450 | Papers sobre ataques específicos sem contribuição taxonômica |
| Sobre LLM mas não segurança | E2 | ~80 | Papers de performance, fine-tuning, NLP genérico |
| Sem relação com LLM | E1 | ~30 | Segurança tradicional, redes, outros domínios |
| Sem metodologia/opinativo | E3 | ~20 | Blogs, tutoriais, opinião sem método |
| Idioma não suportado | E7 | ~8 | Papers em chinês, russo |

## Triagem por Texto Completo (39 excluídos)

| Motivo | Código | Quantidade | Justificativa |
|--------|--------|------------|---------------|
| Escopo muito específico | E6 | 25 | Focam em um único tipo de ataque sem visão geral |
| Sem contribuição para taxonomia | E6 | 8 | Replicam taxonomias existentes sem avanço |
| Metodologia fraca | E3 | 4 | Avaliação insuficiente ou sem reprodutibilidade |
| Texto incompleto | E5 | 2 | Versões preliminares sem detalhes |

## Reports Não Obtidos (3)

- 2 papers com paywall sem versão preprint
- 1 link quebrado/paper removido

---

## Texto sugerido para o artigo

> A triagem por título e resumo excluiu 588 registros, principalmente por estarem fora do escopo definido (E6: ~78%), abordarem LLMs sem foco em segurança (E2: ~14%), ou não terem relação com LLMs (E1: ~5%). Na avaliação de texto completo, 39 reports foram excluídos por focarem em ataques específicos sem contribuição taxonômica ou por metodologia insuficiente. Três reports não puderam ser obtidos (paywall ou indisponibilidade).

---

## Os 10 Estudos Incluídos

### Via Bases de Dados (4)
1. **Greshake et al. (2023)** - Indirect Prompt Injection - Primeiro estudo sistemático de PI indireto
2. **Liu et al. (2025)** - HOUYI - Framework de teste em 36 apps comerciais
3. **Naik et al. (2025)** - Threat Landscape - Panorama amplo de ataques em GenAI
4. **Gulyamov et al. (2026)** - Comprehensive Review - Revisão mais recente e abrangente

### Via Snowballing / Busca Manual (6)
5. **OWASP (2025)** - Top 10 for LLM Applications - Diretriz de referência da indústria
6. **Toyer et al. (2023)** - Tensor Trust - Benchmark com 126k ataques
7. **Schulhoff et al. (2024)** - HackAPrompt - Competição com 600k+ prompts
8. **Hines et al. (2024)** - Spotlighting - Defesa com redução de ASR para <2%
9. **McHugh et al. (2025)** - Prompt Injection 2.0 - Ameaças híbridas (PI + XSS/CSRF)
10. **Kalliomäki (2025)** - Tese sobre Agents - Aplicações e riscos de agentes LLM
