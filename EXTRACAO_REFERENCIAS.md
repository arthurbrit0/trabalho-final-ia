# Extracao e referencias (10 PDFs)

Este arquivo consolida a resposta anterior (fichas e BibTeX) + a tabela de extracao SLR.

## Mapa de IDs e arquivos
- P1 = `2302.12173v2.pdf`
- P2 = `2306.05499v3.pdf`
- P3 = `2311.01011v1.pdf`
- P4 = `2311.16119v3.pdf`
- P5 = `2507.13169v1.pdf`
- P6 = `information-17-00054.pdf`
- P7 = `Kalliomaki_Aleksi_2025.pdf`
- P8 = `OWASP-Top-10-for-LLMs-v2025.pdf`
- P9 = `paper03.pdf`
- P10 = `Threat-Landscape-of-Adversarial-Attacks-on-Generative-AI-and-Large-Language-Models-(LLMs)-Exploring-Different-Types-of-Adversarial-Attacks-Associated-Risks-and-Mitigation-Strategies.pdf`

## Fichas resumidas (dados para citacao)
P1 - Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection (arXiv:2302.12173)
Authors: Kai Greshake; Christoph Endres; Sahar Abdelnabi; Thorsten Holz; Shailesh Mishra; Mario Fritz.
Tipo/escopo: estudo de ataque + taxonomia de prompt injection indireta em apps LLM-integrados.
Evidencias-chave: demonstra ataques em sistemas reais (Bing GPT-4 Chat, code completion) e apps sinteticos; impactos como roubo de dados, worming, contaminacao de ecossistemas; aponta falta de mitigacao efetiva.

P2 - Prompt Injection attack against LLM-integrated Applications (arXiv:2306.05499)
Authors: Yi Liu; Gelei Deng; Yuekang Li; Kailong Wang; Zihao Wang; Xiaofeng Wang; Tianwei Zhang; Yepang Liu; Haoyu Wang; Yan Zheng; Leo Yu Zhang; Yang Liu.
Tipo/escopo: tecnica de ataque black-box (HOUYI) para apps LLM-integrados.
Evidencias-chave: estudo inicial em 10 apps comerciais; HOUYI com 3 elementos; avaliado em 36 apps reais com 31 vulneraveis; 10 vendors confirmaram (inclui Notion); aponta roubo de prompt e uso arbitrario do LLM.

P3 - Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game (arXiv:2311.01011)
Authors: Sam Toyer; Olivia Watkins; Ethan Mendes; Justin Svegliato; Luke Bailey; Tiffany Wang; Isaac Ong; Karim Elmaaroufi; Pieter Abbeel; Trevor Darrell; Alan Ritter; Stuart Russell.
Tipo/escopo: dataset + benchmark de prompt injection.
Evidencias-chave: 126k ataques e 46k "defesas" gerados por humanos; benchmark para prompt extraction e prompt hijacking; ataques generalizam para apps reais; dataset em tensortrust.ai/paper.

P4 - Ignore This Title and HackAPrompt: Exposing Systemic Vulnerabilities of LLMs through a Global Scale Prompt Hacking Competition (arXiv:2311.16119)
Authors: Sander Schulhoff; Jeremy Pinto; Anaum Khan; Louis-Francois Bouchard; Chenglei Si; Svetlina Anati; Valen Tagliabue; Anson Liu Kost; Christopher Carnahan; Jordan Boyd-Graber.
Tipo/escopo: competicao global + dataset + taxonomia de prompt hacking.
Evidencias-chave: 600k+ prompts adversariais contra 3 LLMs; dataset grande e ontologia de tipos de ataques.

P5 - Prompt Injection 2.0: Hybrid AI Threats (arXiv:2507.13169)
Authors: Jeremy McHugh; Kristina Sekrst; Jon Cefalu.
Tipo/escopo: analise de ameacas hibridas em sistemas LLM/agentic.
Evidencias-chave: combina prompt injection com XSS/CSRF/SQLi; discute como agentes ampliam superficie; relata falhas de controles tradicionais; propoe isolamento de prompts, runtime security e separacao de privilegios.

P6 - Prompt Injection Attacks in Large Language Models and AI Agent Systems: A Comprehensive Review of Vulnerabilities, Attack Vectors, and Defense Mechanisms (Information 2026, 17, 54; DOI: 10.3390/info17010054)
Authors: Saidakhror Gulyamov; Said Gulyamov; Andrey Rodionov; Rustam Khursanov; Kambariddin Mekhmonov; Djakhongir Babaev; Akmaljon Rakhimjonov.
Tipo/escopo: review sistematico (2023-2025) com 45 fontes.
Evidencias-chave: taxonomia de ataques diretos/indiretos; menciona MCP e agentes (tool poisoning, credential theft); cita incidentes (CVE-2025-53773, exposicao de chaves); RAG poisoning com 90% usando 5 docs; propoe PALADIN (defense-in-depth).

P7 - Large Language Model (LLM) Agents: Applications and Security (Aalto University, 2025, bachelor thesis)
Author: Aleksi Kalliomaki.
Tipo/escopo: tese de graduacao sobre aplicacoes e seguranca de agentes LLM.
Evidencias-chave: mapeia aplicacoes por industria (medicina e engenharia em destaque); discute riscos (prompt injection, data poisoning, model extraction) e defesas; aponta multi-agent systems como direcao promissora.

P8 - OWASP Top 10 for LLM Applications 2025 (Version 2025, Nov 18 2024)
Tipo/escopo: taxonomia industrial de riscos para apps com LLMs.
Top 10: LLM01 Prompt Injection; LLM02 Sensitive Information Disclosure; LLM03 Supply Chain; LLM04 Data and Model Poisoning; LLM05 Improper Output Handling; LLM06 Excessive Agency; LLM07 System Prompt Leakage; LLM08 Vector and Embedding Weaknesses; LLM09 Misinformation; LLM10 Unbounded Consumption.

P9 - Defending Against Indirect Prompt Injection Attacks With Spotlighting (CAMLIS'24, CEUR-WS)
Authors: Keegan Hines; Gary Lopez; Matthew Hall; Federico Zarfati; Yonatan Zunger; Emre Kiciman.
Tipo/escopo: defesa para prompt injection indireta (spotlighting).
Evidencias-chave: spotlighting sinaliza proveniencia do input; reduz ASR de >50% para <2% em modelos GPT, com impacto minimo na tarefa.

P10 - Threat Landscape of Adversarial Attacks on Generative AI and LLMs: Exploring Different Types of Adversarial Attacks, Associated Risks, and Mitigation Strategies
Authors: Ishita Naik; Dishita Naik; Nitin Naik.
Tipo/escopo: survey amplo de ataques adversariais, riscos e mitigacoes.
Evidencias-chave: cobre prompt injection, data poisoning, RAG attacks, model inversion/extraction, excessive agency; compara ataques a LLMs vs ataques ciberneticos convencionais. Ano inferido por metadata (2025).

## Tabela de extracao SLR (para artigo)
| ID | Referencia curta | Tipo | Cenario/Alvo | Vetor | Objetivo/Impacto | Evidencia/Avaliacao | Achados principais | Limitacoes/Notas |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| P1 | Greshake et al. 2023 (arXiv:2302.12173) | Ataque + taxonomia | Apps LLM-integrados; retrieval externo | Indirect prompt injection | Override de instrucoes; data theft; worming; contaminacao; misuse de APIs | Demonstra ataques em Bing GPT-4 Chat, code completion e apps sinteticos | Indireta permite exploracao remota via dados recuperados; mitigacoes fracas | Sem metricas quantitativas no abstract |
| P2 | Liu et al. 2025 (arXiv:2306.05499) | Ataque (HOUYI) | Apps LLM-integrados (comerciais) | Prompt injection black-box | Prompt theft; uso arbitrario do LLM; override | 10 apps no piloto; 36 apps testados com 31 vulneraveis; 10 vendors confirmaram | HOUYI melhora efetividade e revela impactos severos | Metricas detalhadas nao aparecem no abstract |
| P3 | Toyer et al. 2023 (arXiv:2311.01011) | Dataset + benchmark | LLMs instrucao-following; generalizacao para apps | Prompt injection (extraction/hijacking) | Subverter intent; extrair prompt; hijack | 126k ataques e 46k defesas; benchmark; modelos vulneraveis | Dataset grande e interpretavel; ataques generalizam | Ambiente de jogo difere de apps reais |
| P4 | Schulhoff et al. 2024 (arXiv:2311.16119) | Competicao + dataset + taxonomia | LLMs interativos (chatbots) | Prompt hacking (injection/jailbreak) | Forcar desvio de instrucoes | 600k+ prompts contra 3 LLMs | Recurso global em larga escala; ontologia de ataques | Detalhes de metricas nao no abstract |
| P5 | McHugh et al. 2025 (arXiv:2507.13169) | Analise de ameacas | Sistemas agentic; apps enterprise | Prompt injection + XSS/CSRF/SQLi (hibrido) | Compromisso de sistema; exfiltracao; ataques coordenados | Analise conceitual; cita falhas de controles tradicionais | Enfatiza ataques hibridos e necessidade de isolamento/runtime security | Pouca evid. empirica no abstract |
| P6 | Gulyamov et al. 2026 (Information 17:54) | Review sistematico | LLMs + AI agents + RAG | Direto/indireto; tool poisoning; RAG poisoning | Vulnerabilidades e incidentes de seguranca | 45 fontes; menciona 90% sucesso com 5 docs em RAG; PALADIN | Prompt injection como vulnerabilidade estrutural; defense-in-depth | Review (nao experimental) |
| P7 | Kalliomaki 2025 (thesis) | Tese (survey) | Agentes LLM em industrias | Riscos: prompt injection, data poisoning, model extraction | Analise de aplicacoes e riscos | Classificacao de papers por area; sintese de defesas | Medicina e engenharia destacam-se; multi-agent systems promissor | Nao eh artigo revisado por pares; sem experimento |
| P8 | OWASP 2024 (Top 10 2025) | Diretriz/taxonomia | Aplicacoes com LLMs | LLM01-LLM10 | Mapear riscos e mitigacoes | Documento de referencia | Define Top 10 (prompt injection, excessive agency, etc.) | Sem avaliacao empirica |
| P9 | Hines et al. 2024 (CAMLIS) | Defesa (spotlighting) | Prompts multi-fonte; XPIA | Indirect prompt injection | Reduz ASR; separa origem | ASR cai de >50% para <2% em modelos GPT | Defesa simples e eficaz com baixo impacto | Detalhes de datasets/tarefas nao no abstract |
| P10 | Naik et al. 2025 | Survey | Generative AI + LLMs | Varios (prompt injection, poisoning, RAG, etc.) | Mapear ataques, riscos, mitigacoes | Revisao narrativa | Comparacao com ataques convencionais; panorama amplo | Ano/venue nao explicitos na capa |

## BibTeX (ajustado para LNCS)
```bibtex
@article{greshake2023indirect,
  title = {Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection},
  author = {Greshake, Kai and Endres, Christoph and Abdelnabi, Sahar and Holz, Thorsten and Mishra, Shailesh and Fritz, Mario},
  year = {2023},
  eprint = {2302.12173},
  archivePrefix = {arXiv},
  primaryClass = {cs.CR}
}

@article{liu2025prompt,
  title = {Prompt Injection attack against LLM-integrated Applications},
  author = {Liu, Yi and Deng, Gelei and Li, Yuekang and Wang, Kailong and Wang, Zihao and Wang, Xiaofeng and Zhang, Tianwei and Liu, Yepang and Wang, Haoyu and Zheng, Yan and Zhang, Leo Yu and Liu, Yang},
  year = {2025},
  eprint = {2306.05499},
  archivePrefix = {arXiv},
  primaryClass = {cs.CR}
}

@article{toyer2023tensortrust,
  title = {Tensor Trust: Interpretable Prompt Injection Attacks from an Online Game},
  author = {Toyer, Sam and Watkins, Olivia and Mendes, Ethan and Svegliato, Justin and Bailey, Luke and Wang, Tiffany and Ong, Isaac and Elmaaroufi, Karim and Abbeel, Pieter and Darrell, Trevor and Ritter, Alan and Russell, Stuart},
  year = {2023},
  eprint = {2311.01011},
  archivePrefix = {arXiv},
  primaryClass = {cs.LG}
}

@article{schulhoff2024hackaprompt,
  title = {Ignore This Title and HackAPrompt: Exposing Systemic Vulnerabilities of LLMs through a Global Scale Prompt Hacking Competition},
  author = {Schulhoff, Sander and Pinto, Jeremy and Khan, Anaum and Bouchard, Louis-Fran\\c{c}ois and Si, Chenglei and Anati, Svetlina and Tagliabue, Valen and Kost, Anson Liu and Carnahan, Christopher and Boyd-Graber, Jordan},
  year = {2024},
  eprint = {2311.16119},
  archivePrefix = {arXiv},
  primaryClass = {cs.CR}
}

@article{mchugh2025promptinjection2,
  title = {Prompt Injection 2.0: Hybrid AI Threats},
  author = {McHugh, Jeremy and {\\v{S}}ekrst, Kristina and Cefalu, Jon},
  year = {2025},
  eprint = {2507.13169},
  archivePrefix = {arXiv},
  primaryClass = {cs.CR}
}

@article{gulyamov2026review,
  title = {Prompt Injection Attacks in Large Language Models and AI Agent Systems: A Comprehensive Review of Vulnerabilities, Attack Vectors, and Defense Mechanisms},
  author = {Gulyamov, Saidakhror and Gulyamov, Said and Rodionov, Andrey and Khursanov, Rustam and Mekhmonov, Kambariddin and Babaev, Djakhongir and Rakhimjonov, Akmaljon},
  journal = {Information},
  year = {2026},
  volume = {17},
  pages = {54},
  doi = {10.3390/info17010054}
}

@thesis{kalliomaki2025llmagents,
  title = {Large Language Model (LLM) Agents: Applications and Security},
  author = {Kallioma{\\\"a}ki, Aleksi},
  year = {2025},
  school = {Aalto University},
  type = {Bachelor's thesis}
}

@misc{owasp2024top10llm,
  title = {OWASP Top 10 for LLM Applications 2025},
  author = {{OWASP}},
  year = {2024},
  note = {Version 2025, Nov 18 2024}
}

@inproceedings{hines2024spotlighting,
  title = {Defending Against Indirect Prompt Injection Attacks With Spotlighting},
  author = {Hines, Keegan and Lopez, Gary and Hall, Matthew and Zarfati, Federico and Zunger, Yonatan and K{\\i}c{\\i}man, Emre},
  booktitle = {CAMLIS'24: Conference on Applied Machine Learning for Information Security},
  year = {2024},
  publisher = {CEUR Workshop Proceedings},
  note = {Arlington, VA, October 24--25, 2024}
}

@misc{naik2025threatlandscape,
  title = {Threat Landscape of Adversarial Attacks on Generative AI and Large Language Models (LLMs): Exploring Different Types of Adversarial Attacks, Associated Risks, and Mitigation Strategies},
  author = {Naik, Ishita and Naik, Dishita and Naik, Nitin},
  year = {2025},
  note = {Year inferred from PDF metadata; venue not stated in front matter}
}
```

## Pendencias para checagem rapida (se quiser refinar)
- Confirmar venue/ano exato do P10 (o PDF nao explicita na capa).
- Se quiser DOI/URL oficial do OWASP Top 10 2025, adicionar no BibTeX.
