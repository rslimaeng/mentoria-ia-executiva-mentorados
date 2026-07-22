# Checklist de Anonimização · antes de colar no Claude

> **Responsabilidade LGPD é sua, não da IA.** Faça toda substituição num editor local (Notas · Sublime · Word) usando **Localizar e Substituir**. Guarde a chave de mapeamento fora do Claude.

---

## Antes de começar

- [ ] Abri a transcrição em editor local (não é web)
- [ ] Criei um arquivo separado no meu drive chamado `chave-anonimizacao-[reuniao-X].md` — vou guardar as substituições aqui
- [ ] Este arquivo de chave **nunca** vai pro Claude, é backup local

---

## Substituições · faça todas em ordem

### 1. Você
```
Débora / [primeiro nome dela] → [GESTORA]
```
Você também some. É o padrão.

### 2. Colegas / colaboradores
```
[Nome colega 1]  → COLABORADOR_A
[Nome colega 2]  → COLABORADOR_B
[Nome colega 3]  → COLABORADOR_C
...
```
Ordem pela primeira aparição no texto. **Consistente do começo ao fim** — se COLABORADOR_A é o Fulano no parágrafo 1, é o Fulano até o fim.

### 3. Órgão / instituição
```
[Nome da Câmara / prefeitura]     → [ORGÃO]
[Secretaria X]                    → [SETOR_1]
[Cargo do secretário / vereador]  → [FIGURA_1], [FIGURA_2]
```

### 4. Cidade / endereço
```
[Nome da cidade]                  → [CIDADE]
[Endereço específico]             → [LOCAL]
```

### 5. Dados sensíveis
```
Valores em R$ (que identificam)   → [VALOR_1], [VALOR_2]
Nº de processos administrativos   → [Nº_PROC]
Matrículas de servidor            → [MATRÍCULA]
CPF, RG, cartão                   → [DOC_1]
```

> **Regra:** só anonimiza se identificar. Números genéricos ("3 mesas de reunião", "45 minutos") podem ficar.

### 6. Datas específicas
```
"12/03/2027 às 14h"               → "semana X, período tarde"
"Reunião de 20/03"                → "próxima reunião"
"contrato de julho"               → "contrato recente"
```

### 7. Termos internos (jargão específico)
```
[Termo interno do gabinete que identifica X caso] → [CATEGORIA]
[Programa/projeto interno específico]             → [INICIATIVA]
```

---

## Teste de saída · antes de colar no Claude

Leia o texto **sem contexto** (como se você não conhecesse o gabinete). Faça essas 3 perguntas:

- [ ] Consigo identificar quem é a pessoa, órgão ou situação só lendo?  
      Se **sim** → anonimize mais.

- [ ] Existe algum dado numérico ou nome próprio que sobrevive?  
      Se **sim** → substitua.

- [ ] Alguém do gabinete lendo esta versão reconheceria uma pessoa específica?  
      Se **sim** → refaça.

Só depois dos 3 "não", vai pro Claude.

---

## Depois de terminar (fluxo reverso)

Depois que a ata executiva final voltar do Claude:

1. Baixe o texto final em `.txt` ou `.md`
2. Abra no editor local
3. Use a chave `chave-anonimizacao-[reuniao-X].md` pra fazer o caminho reverso (`COLABORADOR_A → nome real`)
4. Confira leitura completa
5. **Apague a transcrição bruta original** (a que tinha nomes reais)
6. Guarde só: (a) ata revertida final e (b) chave (offline, no seu drive)

---

## Regra de ouro

> **A IA não te protege. Você se protege.**  
> Anonimize antes. Reverta depois. Nunca peça pro Claude fazer isso por você.

---

*Mentoria IA Executiva · Débora Nascimento · S4 · Caso 3 · Gabinete*
