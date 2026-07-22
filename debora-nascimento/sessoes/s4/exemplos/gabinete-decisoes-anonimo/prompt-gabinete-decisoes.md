# Prompt · Extrair decisões de reunião do gabinete · Anonimizado

> **Pré-requisito:** rodar antes o `checklist-anonimizacao.md`. Nada entra no Claude com nome real, matrícula ou identificador único.

---

## Turno 1 · Extração estruturada

```
Papel: Você é uma chefe de gabinete sênior com 15 anos de experiência
transformando reuniões operacionais em atas executivas.

Contexto: Vou colar uma transcrição anonimizada de uma reunião de 45 min
de um órgão público. Nomes e dados sensíveis já foram substituídos por
pseudônimos (COLABORADOR_A, [ORGÃO], [DADO_SENSÍVEL]).

Tarefa: Extraia:
(1) as 5 decisões mais concretas tomadas
(2) responsável por cada uma (use os pseudônimos exatamente como aparecem)
(3) prazo explícito ou marcador ⚠️ PRAZO NÃO DEFINIDO
(4) 3 riscos que ficaram implícitos e ninguém verbalizou.

Formato: 4 blocos em ordem. Bloco decisões em tabela markdown.

Limite: NÃO invente decisão que não está na transcrição. Se ficou meia-boca,
escreve "decisão parcial: [texto]" — não completa. Nunca sugira dado que
a transcrição não trouxer.

Transcrição:
[COLAR AQUI TEXTO ANONIMIZADO]
```

---

## Passe pro Cowork · 3 refinamentos

Copie a saída completa. Cole num Cowork novo. Peça 1 refinamento por vez:

### Refinamento 1 · Explicar por que
```
Pra cada decisão, adiciona 1 linha curta de contexto — "por que essa decisão
saiu agora", baseado no que estava na transcrição. Não invente, use só o
que apareceu.
```

### Refinamento 2 · Sugerir prazos ausentes
```
Onde tá ⚠️ PRAZO NÃO DEFINIDO, sugira 1 prazo razoável baseado na urgência
aparente. Marca como [SUGERIDO — VOCÊ CONFIRMA].
```

### Refinamento 3 · Decisão vs Encaminhamento
```
Marca as que são decisão fechada vs as que são "encaminhamento" (foi
discutido, alguém vai analisar, volta depois). São coisas diferentes que
costumam ser tratadas iguais.
```

---

## Antes de dar por terminada

- [ ] Cada decisão tem responsável (pseudônimo)
- [ ] Cada decisão tem prazo (explícito ou sugerido)
- [ ] 3 riscos implícitos aparecem — se só vieram 1-2, peça mais
- [ ] Decisão × encaminhamento estão marcados diferente
- [ ] Nenhuma linha do Claude tem dado que não estava na transcrição

---

## Depois do Cowork · fluxo reverso (offline)

1. Baixe a versão final (Cowork → exportar `.txt` ou `.md`)
2. Abra no editor local
3. Use a chave `chave-anonimizacao-[reuniao-X].md` pra reverter (`COLABORADOR_A → nome real`)
4. Ata pronta pra circular internamente
5. **Apague a transcrição bruta original** (a que tinha nomes reais)

---

*Mentoria IA Executiva · Débora Nascimento · S4 · Caso 3 · Gabinete*
