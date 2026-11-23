# Texto Humanizado — Claude Skill (PT-BR)

Uma Skill para o Claude (Desktop, Web e Claude Code) que escreve, adapta e revisa textos em português eliminando os padrões mais comuns de escrita gerada por inteligência artificial.

## Por que essa Skill existe

Modelos de linguagem costumam repetir vícios fáceis de identificar: excesso de travessões, gerúndio no fim das frases, listas sempre com três itens, palavras pomposas e ritmo uniforme. Essa Skill transforma as observações do guia **WP:AISIGNS** (*Signs of AI writing*) da Wikipédia em regras práticas de escrita para o português do Brasil.

## Resultados nos testes (ZeroGPT)

Durante o desenvolvimento, o mesmo texto informativo sobre hidratação foi avaliado no detector ZeroGPT em três etapas:
- **Texto original gerado pelo ChatGPT:** 22,7% de probabilidade de IA
- **Skill v1.0 (apenas bloqueio de palavras proibidas):** 55,6% de probabilidade de IA
- **Skill v2.0 (regras de ritmo, sintaxe e variação):** 0% de probabilidade de IA

## O que a Skill corrige

- **Vocabulário:** remove jargões típicos de IA (como *crucial*, *mergulhar*, *tapeçaria*, *cenário*, *aprimorar*, *alavancar*) e substitui verbos formais (*utilizou*, *redigiu*, *atua como*) por formas simples (*usou*, *escreveu*, *é*).
- **Ritmo e sintaxe:** alterna frases curtas com frases longas, evita parágrafos simétricos e permite a repetição natural de substantivos em vez de forçar sinônimos difíceis.
- **Estrutura:** corta gerúndios reflexivos no fim das orações, paralelismos negativos (*"não é apenas X, mas Y"*), regra de três e conclusões moralizantes.
- **Limpeza:** elimina travessões em excesso, listas com negrito repetitivo e notas ou introduções de assistente.

## Como instalar

1. Baixe a pasta `texto-humanizado` (contendo o arquivo `SKILL.md`) deste repositório.
2. **No Claude Desktop / Web:** acesse *Personalizar > Habilidades* (ou digite `/skills`) e importe o arquivo `SKILL.md` ou a pasta compactada em `.zip`.
3. **No Claude Code:** copie a pasta `texto-humanizado` para o diretório `~/.claude/skills/` (global) ou `.claude/skills/` dentro do seu projeto.

## Como usar

Você pode chamar a Skill diretamente pelo comando ou pedir de forma natural:
- `/texto-humanizado Reescreva este e-mail para ficar mais direto.`
- `Deixe este texto sem cara de IA e mais natural.`

---

## English Summary

**Texto Humanizado** is an open-source Agent Skill (`SKILL.md`) designed for Brazilian Portuguese writing in Claude Desktop, Claude Web, and Claude Code. Based on Wikipedia's **WP:AISIGNS** (*Signs of AI writing*) field guide, it enforces sentence-length variation, natural word repetition, simple verbs, and strict removal of AI clichés, negative parallelisms, and chatbot disclaimers. In benchmark tests using ZeroGPT, it reduced AI detection scores from 22.7% (raw LLM output) to 0%.
