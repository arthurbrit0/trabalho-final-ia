0) Primeiro alerta prático: grupo tem 6, mas o edital diz “máx. 5”

Vocês listaram 6 pessoas. A regra do professor diz máximo 5 integrantes. Sugestões práticas:

Confirmar com o professor se haverá exceção (mais seguro).

Se não houver: escolher 5 autores oficiais e o 6º pode ajudar como “colaborador” sem constar como integrante (mas isso é decisão do professor/critério da disciplina).

Alternativa: dividir em 2 grupos (geralmente inviável perto do prazo).

Não ignora isso — pode dar problema na avaliação.

1) Tema de segurança escolhido para vocês (bem “surveyável” com seus 10 papers)
Tema (recorte forte e atual)

Segurança de aplicações com LLMs: Prompt Injection (direto e indireto), ameaças híbridas e defesas em sistemas com RAG e agentes

Por que esse tema é bom:

OWASP coloca Prompt Injection como risco central em apps com LLMs (ótimo “gancho” de motivação e taxonomia).

OWASP-Top-10-for-LLMs-v2025

O ataque indireto (instruções escondidas em conteúdo externo) rompe fronteiras tradicionais de segurança e é altamente relevante para RAG/agentes.

2302.12173v2

Há evidências de escala/benchmark (HackAPrompt e Tensor Trust) para discutir avaliação e por que “prompt-only defense” falha.

2311.16119v3

2311.16119v3

2311.01011v1

Título sugerido (em português, estilo LNCS)

Opção A (direta):
“Prompt Injection em Aplicações com LLMs: Uma Revisão Sistemática, Taxonomia de Ameaças e Estratégias de Mitigação”

Opção B (com agentes/RAG):
“Segurança em Sistemas com LLMs, RAG e Agentes: Prompt Injection Direta/Indireta, Ameaças Híbridas e Defesas”

2) Como encaixar exatamente os 10 papers (papéis na narrativa)

Vocês já têm um “conjunto perfeito” para um survey curto (6–10 páginas):

(i) Fundamentos / visão geral / taxonomias

OWASP Top 10 for LLMs (2025) → taxonomia “industria”, linguagem de risco e exemplos.

OWASP-Top-10-for-LLMs-v2025

 

OWASP-Top-10-for-LLMs-v2025

Threat Landscape (Naik et al.) → panorama mais amplo de ataques (inclui RAG injection etc.).

Threat-Landscape-of-Adversarial…

 

Threat-Landscape-of-Adversarial…

MDPI review (Information 2026) → revisão sistemática recente e discussão do “problema estrutural” (instrução vs dado).

information-17-00054

 

information-17-00054

Prompt Injection 2.0 (Hybrid AI Threats) → conecta prompt injection com ameaças clássicas (XSS/SQLi/CSRF etc.), bom para “tendências futuras”.

2507.13169v1

 

2507.13169v1

(ii) Ataques (e como acontecem em apps reais)

Greshake et al. (Indirect Prompt Injection) → ataque indireto e implicações em apps com dados externos + APIs.

2302.12173v2

 

2302.12173v2

HOUYI / Liu et al. (Prompt Injection em LLM-integrated apps) → ataque em apps integrados e categorização de cenários (malicious instruction injection / data extraction / goal hijacking).

2306.05499v3

 

2311.16119v3

(iii) Avaliação / benchmarks (para seção “protocolos de avaliação”)

HackAPrompt → competição em larga escala; 600K+ prompts; e evidência de que defesas “só prompt” não resolvem.

2311.16119v3

2311.16119v3

 

2311.16119v3

Tensor Trust → dataset/benchmarks de prompt extraction e hijacking (jogo online).

2311.01011v1

 

2311.01011v1

(iv) Defesas (um paper “âncora” de mitigação)

Spotlighting (Hines et al.) → estratégia de defesa contra indirect injection e resultado forte (ASR baixo) como estudo de caso de mitigação. 

paper03

(v) Agentes (para conectar com “tool use”)

Kalliomäki (2025) → visão de agentes + segurança; útil para motivar o porquê de agentes ampliarem superfície de ataque. 

Kalliomäki_Aleksi_2025

3) Roteiro do trabalho do zero até “pronto para envio”

A ideia é transformar isso numa pipeline com artefatos intermediários que viram texto/figuras/tabelas.

Etapa 1 — Definir perguntas de pesquisa (RQs) e escopo (1 página no máximo)

Escolham 3–5 RQs. Sugestão (bem “survey”):

RQ1: Quais são os principais vetores de prompt injection em aplicações com LLMs (direto, indireto e híbrido)?

RQ2: Quais impactos/objetivos aparecem com mais frequência (exfiltração, goal hijacking, execução de ações via ferramentas, degradação/DoS)?

RQ3: Como os trabalhos avaliam ataques/defesas (métricas, datasets, setups)?

RQ4: Quais estratégias de mitigação existem e quais trade-offs (custo, falsa detecção, perda de utilidade)?

RQ5 (opcional): O que muda quando entra RAG e/ou agentes com ferramentas?

Escopo explícito (para não virar 30 páginas):

Foco em prompt injection e adjacências (jailbreak, prompt leaking, tool misuse, RAG injection).

Fora do escopo: training-time poisoning, DP, etc. (podem citar como relacionado).

Produto dessa etapa: 1 parágrafo “Objetivo e contribuições do survey”.

Etapa 2 — Fazer a Revisão Sistemática (A1) de forma “auditável”

Mesmo com papers já escolhidos, vocês precisam escrever o método. Não inventem números.

Checklist A1 (o que deve aparecer no artigo):

Bases (ex.: arXiv, ACM DL, IEEE Xplore, ACL Anthology, Google Scholar).

String(s) de busca (2–4 strings).

Filtros (anos, idioma, tipo de doc).

Critérios de inclusão/exclusão.

Triagem (quantos retornaram → quantos selecionados).

Lista final (seus 10 + justificativa de inclusão).

Template pronto para vocês colarem no artigo (preencher com seus dados reais):

“Realizamos uma busca nas bases X, Y e Z em (data). Utilizamos as strings S1–S3, com filtros de ano (2023–2026) e termos relacionados a prompt injection/LLM-integrated apps/agents/RAG. Foram recuperados N registros; após remoção de duplicatas (D) e triagem por título/resumo, restaram K; após leitura completa e aplicação dos critérios de exclusão, selecionamos 10 estudos primários.”

Sugestão prática: montar uma planilha (Google Sheets) com colunas:

ID, referência, ano, tipo (ataque/defesa/benchmark/revisão), alvo (chatbot/app/RAG/agente), vetor (direto/indireto/híbrido), objetivo, métrica, principais achados, limitações.

Etapa 3 — Extrair dados dos 10 papers (isso vira tabelas do artigo)

Façam uma “ficha de extração” por paper (10–15 min cada, dá para dividir).

Campos mínimos para cada paper:

Tipo: ataque / defesa / benchmark / survey / diretriz.

Cenário: LLM standalone vs LLM-integrated app vs RAG vs agente.

Vetor de ataque: direto / indireto / híbrido.

Objetivo do atacante: exfiltração (prompt/data), goal hijacking, tool/action hijack, DoS/token waste, etc.

Como avalia: dataset, métrica (ASR, taxa de extração, taxa de jailbreak, custo/latência, etc).

Mitigação proposta (se houver) e limitações.

Tabela 1 sugerida (no artigo): “Resumo dos estudos incluídos”
Tabela 2 sugerida: “Taxonomia unificada (vetor × objetivo × superfície)”

Etapa 4 — Criar a taxonomia do survey (sua “contribuição central”)

Vocês não precisam inventar do nada: podem unificar OWASP + Greshake + Prompt Injection 2.0 + HackAPrompt.

Taxonomia sugerida (simples e forte)

Eixo A — Vetor

Direto: instrução maliciosa no input do usuário (chat, formulário, etc.).

OWASP-Top-10-for-LLMs-v2025

Indireto: instrução escondida em conteúdo externo (web/page, docs, e-mail, RAG retrieval).

Threat-Landscape-of-Adversarial…

Híbrido: mistura prompt injection com vetores clássicos (ex.: injeção em HTML/JS + pipeline LLM; ou exploração de fluxo de ferramenta).

2507.13169v1

Eixo B — Superfície

Chatbot / assistente

Aplicação integrada (LLM como componente)

RAG (retrieval + contexto)

Agentes com ferramentas (tool use; ações)

Eixo C — Objetivo/Impacto

Prompt leaking / prompt extraction

Data exfiltration

Goal hijacking

Tool/action hijacking (agente executa ação indevida)

DoS / token waste

Desinformação/manipulação (resumo confiante de fonte não confiável)

Dica de redação: expliquem que a raiz do problema é que LLMs não têm separação “nativa” perfeita entre instrução e dado, o que favorece a classe de ataques de injeção (use uma citação do review).

information-17-00054

Figura autoral recomendada (1 figura vale ouro no vídeo e no paper):
Um diagrama de pipeline:
Usuário → App → (RAG retriever → documentos) → Montagem do prompt → LLM → (ferramentas/APIs) → resposta
E marcar em vermelho onde entra direto, indireto e híbrido.

4) Como escrever o Artigo LNCS (A2) sem travar
Estrutura mínima (com as seções que o professor quer + extras recomendadas)

Sugestão de sumário (6–10 páginas fica ótimo):

Introdução

Metodologia da Revisão Sistemática (Atividade 1 dentro do artigo)

Fundamentos e Superfície de Ataque em Apps com LLMs (RAG e Agentes)

Taxonomia Proposta

Famílias de Ataques e Evidências Empíricas

Estratégias de Mitigação e Trade-offs

Protocolos de Avaliação (benchmarks, métricas, setups)

Desafios Abertos e Tendências

Conclusão

Referências

Esqueleto LNCS (para vocês colarem no Overleaf)

No Overleaf: criar projeto → “Springer LNCS” → adaptar para PT-BR.
No preâmbulo, vocês podem usar:

\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[brazil]{babel}
\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{url}


E manter o \begin{abstract}...\end{abstract} mas escrever como Resumo (no texto).

Como produzir texto rápido sem perder qualidade

Introdução: 4 parágrafos

Contexto (LLMs em apps)

Problema (prompt injection como ameaça relevante; citar OWASP)

OWASP-Top-10-for-LLMs-v2025

Por que é difícil (instrução vs dado; citar review)

information-17-00054

Contribuições do survey + organização do artigo

Seção de ataques: organizem por (direto / indireto / híbrido) e dentro por objetivo (exfiltração, goal hijack, tool hijack, DoS).

Apoiem “indireto” com Greshake.

2302.12173v2

Apoiem “ataque em apps integrados” com HOUYI e as categorias de ameaça que eles usam.

2306.05499v3

Seção de avaliação: destaquem HackAPrompt (escala) e Tensor Trust (benchmark estruturado).

2311.16119v3

2311.01011v1

Seção de defesas: pelo menos 2 camadas:

“Prompt/guardrails” (e explicar limites — HackAPrompt indica que prompt-based defense não resolve sozinho).

2311.16119v3

“Arquitetura/isolamento/políticas” (defesa-in-depth)

um estudo concreto: Spotlighting reduz ASR de ataques indiretos (bom para mostrar resultado).

5) Como montar os Slides (A3) e o vídeo (até 20 min)
Estrutura de slides (12 slides, objetivo “claro e completo”)

Título + autores + UFC / disciplina

Motivação: por que segurança em LLMs importa (OWASP + apps reais)

OWASP-Top-10-for-LLMs-v2025

Conceito: prompt injection (direto vs indireto) + 1 exemplo simples

Pipeline de app com LLM (figura autoral)

Taxonomia proposta (3 eixos)

Ataques diretos: padrões e objetivos (ex.: HackAPrompt como evidência)

2311.16119v3

Ataques indiretos: por que são perigosos (Greshake)

2302.12173v2

Ameaças híbridas (Prompt Injection 2.0)

2507.13169v1

Benchmarks e avaliação (HackAPrompt + Tensor Trust)

2311.01011v1

Defesas: camadas + Spotlighting (resultado)

Desafios abertos e tendências (agentes, ferramentas, RAG poisoning etc.)

Conclusão + takeaways + referências-chave

Roteiro do vídeo (divisão sugerida)

1 pessoa abre (1–2 min): motivação + objetivo + RQs

2 pessoas (6–8 min): taxonomia + ataques diretos/indiretos

1 pessoa (4–5 min): híbridos + agentes

1 pessoa (4–5 min): defesas + avaliação

1 pessoa fecha (1–2 min): desafios + conclusão

Observação: se o grupo ficar oficialmente com 5 pessoas, distribuam as falas por 5.

6) README e empacotamento do .zip (entrega final)
Estrutura do .zip (como o professor pede)

A1_ArtigoResumo.pdf

A2_LinkVideo.txt (URL do vídeo não listado)

A3_Slides.pdf (recomendado)

README.txt

Template de README (copiar e preencher)

Tema: Prompt Injection e segurança em aplicações com LLMs (RAG e agentes)
Integrantes: (máx. 5 — ajustar)
Conteúdo do .zip: descreve cada arquivo em 1 linha
Como avaliar rapidamente: “Abrir A1_ArtigoResumo.pdf; ver Seção 2 (Metodologia da Revisão Sistemática); depois assistir vídeo pelo link; slides em A3.”
Uso de IA: “Ferramentas de IA foram usadas para organizar a estrutura do texto, sugerir taxonomias e revisar gramática; todo conteúdo foi revisado e validado pelo grupo, e todas as fontes foram citadas.”

7) Distribuição de tarefas (para vocês realmente finalizarem)

Uma divisão eficiente (ajusta nomes depois conforme “máx. 5”):

Editor principal (Overleaf + LNCS + coesão)

Metodologia SLR + PRISMA + tabela dos estudos

Ataques diretos/indiretos (Greshake + HOUYI + OWASP)

Benchmarks/avaliação (HackAPrompt + Tensor Trust)

Defesas + tendências (Spotlighting + Prompt Injection 2.0 + Agentes)

Regra de ouro: 1 pessoa “fecha” o texto final para manter consistência de estilo.

8) Checklist de qualidade antes de exportar PDF (pontos que dão nota)

 O artigo tem todas as seções mínimas (Título, Autores, Abstract/Resumo, Introdução, Trabalhos Relacionados, Conclusão, Bibliografia).

 Existe seção explícita de Revisão Sistemática (bases, strings, filtros, triagem, lista final).

 Tem pelo menos 1 figura autoral (pipeline + pontos de ataque).

 Tem pelo menos 2 tabelas (estudos incluídos + taxonomia/mitigações).

 Discussão crítica: trade-offs e limitações (ex.: por que defesas “só prompt” falham).

2311.16119v3

 Referências consistentes (BibTeX), sem links quebrados.

 README declara uso de IA e não há trechos “copiados” sem citação.