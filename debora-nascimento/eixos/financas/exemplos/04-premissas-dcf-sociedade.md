---
tipo: exemplo-pratico
cenario: Premissas DCF — avaliação da cota de 25% do Restaurante CHR
uso: pra praticar IA no encontro 3 (Finanças)
formato_real: xlsx (será gerado em paralelo)
atualizado: 2026-06-30
---

# Premissas DCF — Avaliação da Sociedade

## Objetivo deste arquivo

Estrutura as **premissas econômicas** pra valuation por **Fluxo de Caixa Descontado (DCF)** da oferta de sociedade que a Débora recebeu: comprar **25% do Restaurante CHR** por **R$ 180.000**.

A pergunta que precisa ser respondida: **"Esses R$ 180k vão voltar pra mim em fluxo de lucro distribuído nos próximos 5 anos? Em quanto tempo? Vale mais do que CDB?"**

**Como Débora vai usar com IA:**

1. Anexa este arquivo + DRE (arquivo 02) e pede:
   - "Calcula VPL, TIR e payback descontado nos 3 cenários (base, estresse, otimista)."
   - "Constrói o fluxo de caixa projetado mês a mês pelos 60 meses."
   - "Compara o retorno com aplicar R$ 180k em CDB 110% CDI pelo mesmo período."
2. Pede sensibilidade: "Mantendo tudo igual, qual seria a TMA máxima em que o investimento ainda dá VPL positivo?"
3. Roda pergunta-chave: "Se o restaurante quebrar no ano 3, qual o tamanho do prejuízo?"

> **Disclaimer importante:** este DCF avalia **só o fluxo de distribuição de lucro**. Não inclui valor de saída (venda da cota depois). Pra inclusão de saída, premissa adicional de múltiplo de EBITDA na saída seria necessária — modelo simplificado pra PME.

---

## Conceitos-base (linguagem PME — sem WACC/CAPM)

| Termo | O que é, em linguagem direta |
|---|---|
| **VPL (Valor Presente Líquido)** | Soma de todos os lucros futuros que vou receber, **trazidos pra valor de hoje** (descontados pela TMA), menos o que paguei. Se VPL > 0, o investimento bate a TMA. Se VPL < 0, melhor não fazer. |
| **TIR (Taxa Interna de Retorno)** | A taxa de rentabilidade que o investimento entrega. Se TIR > TMA, é interessante. Se TIR < TMA, não compensa o risco. |
| **Payback descontado** | Em quantos meses o investimento volta inteiro, **considerando o valor do dinheiro no tempo**. Diferente do payback simples (que ignora o tempo). |
| **TMA (Taxa Mínima de Atratividade)** | A rentabilidade mínima que você exige pra topar o risco. Fórmula simples: TMA = retorno de aplicação segura (CDB) **+** prêmio pelo risco de empreender. |

> **Como calcular sua TMA na prática (PME):**
> - Quanto rende uma aplicação segura hoje? CDB 110% CDI ≈ 13% a.a.
> - Quanto a mais você exige pra trocar segurança por risco PME? 5 a 8% a.a.
> - TMA = 13% + 6% = **19% a.a.** (≈ 1,46% a.m.)

---

## Premissas do cenário-base

| Item | Valor |
|---|---|
| Cota oferecida | 25% do capital social |
| Valor pago pela cota (investimento inicial) | R$ 180.000 |
| Horizonte de avaliação | 5 anos (60 meses) |
| Lucro líquido mensal médio do restaurante (referência DRE) | R$ 36.598 |
| Lucro distribuível ao sócio minoritário (25%) | R$ 9.149/mês (teto) |
| **Lucro distribuível usado no cenário-base** | **R$ 7.000/mês** (conservador — desconta capital de giro e reinvestimento) |
| TMA (nominal) | 19% a.a. ≈ 1,46% a.m. |
| Inflação considerada | 4% a.a. |
| Crescimento real da receita projetado | 3% a.a. |
| Crescimento nominal anual da distribuição | (1,04 × 1,03) − 1 = **7,12% a.a.** |
| Distribuição mês 1 | R$ 7.000 |
| Distribuição mês 12 → mês 13 | aplica reajuste de 7,12% |

---

## Cenários

| Cenário | Distribuição ano 1 (R$/mês) | Crescimento real a.a. | Inflação | Cresc. nominal a.a. | TMA |
|---|---:|---:|---:|---:|---:|
| **Estresse** | 5.000 | 0% | 4% | 4,00% | 22% |
| **Base** | 7.000 | 3% | 4% | 7,12% | 19% |
| **Otimista** | 9.000 | 5% | 4% | 9,20% | 17% |

> **Por que mudar a TMA por cenário:** quanto pior o cenário, **mais exigente** você fica — quer mais retorno pelo mesmo risco. No estresse, exige 22% porque o risco percebido subiu.

---

## Fluxo de caixa esperado (resumo anual — cenário base)

| Ano | Distribuição anual (R$) | Fator desconto (TMA 19%) | Valor presente (R$) |
|---|---:|---:|---:|
| 0 (hoje) | -180.000 (investimento) | 1,000 | -180.000 |
| 1 | 7.000 × 12 = 84.000 | 0,840 | 70.560 |
| 2 | 89.984 (cresce 7,12%) | 0,706 | 63.529 |
| 3 | 96.395 | 0,593 | 57.162 |
| 4 | 103.262 | 0,499 | 51.528 |
| 5 | 110.624 | 0,419 | 46.351 |
| **VPL** | — | — | **+R$ 109.130** |

> **Leitura cenário base:** VPL positivo (~R$ 109k) significa que, mesmo descontando pela TMA de 19%, o investimento bate a expectativa em R$ 109k. **TIR projetada ≈ 47% a.a.** — bem acima da TMA. **Payback descontado ≈ 33 meses.**

---

## Sensibilidades — perguntas pra IA rodar

1. **TMA de equilíbrio:** qual TMA faz VPL = 0 no cenário base? (Resposta esperada: ~47% a.a., que é a TIR.)
2. **Quebra do lucro:** se a distribuição cair pra R$ 4.500/mês (estresse forte), o VPL ainda é positivo?
3. **Lock-in:** e se Débora não puder sair antes de 3 anos? Recalcular payback considerando isso.
4. **Cenário de quebra:** se o restaurante fechar no ano 3, qual a TIR retroativa? (Resposta esperada: provavelmente negativa, ~-25% a.a.)

---

## Comparação com alternativa segura

| Alternativa | Aplicação inicial | Rendimento 5 anos (líquido IR) | Valor final | TIR efetiva |
|---|---:|---:|---:|---:|
| CDB 110% CDI (13% a.a.) | R$ 180.000 | + R$ 156.840 | R$ 336.840 | ~13% a.a. |
| Sociedade CHR (cenário base) | R$ 180.000 | + R$ 304.265 distribuídos (sem valor de saída) | R$ 484.265 fluxo | ~47% a.a. |
| Sociedade CHR (cenário estresse) | R$ 180.000 | + R$ 180.000 ~ distribuídos | R$ 360.000 fluxo | ~14% a.a. |

> **Leitura final:** no cenário base, sociedade ganha do CDB com folga. No estresse, empata com CDB — ou seja, **assume risco PME sem ser compensada por isso**. Decisão deve depender de quão provável é cada cenário.

---

## Premissas que precisam ser validadas com os sócios atuais ANTES de fechar

1. **Distribuição realmente é mensal?** Ou anual? Frequência muda VPL.
2. **Existe acordo de sócios?** Cláusula de saída, tag along, drag along?
3. **Como é apurado o lucro distribuível?** Há reserva obrigatória de capital de giro?
4. **Existe dívida no balanço?** DRE positiva com endividamento alto distorce análise.
5. **Capital social registrado bate com R$ 720k (180k ÷ 25%)?** Ou o valuation é informal?
6. **Sócios atuais têm pró-labore + distribuição?** Quanto cada conta vai influenciar Débora?
7. **CNPJ tem certidões negativas?** Dívida tributária oculta vira problema dos novos sócios.

---

## Conexão com os outros arquivos

- **DRE (arquivo 02):** Lucro líquido médio R$ 36.598/mês × 25% = **R$ 9.149/mês teto**. Premissa-base usa R$ 7.000 (conservadora, ~76% do teto).
- **Fluxo de caixa (arquivo 01):** saldo positivo de R$ 110.620 nos 3 meses confirma capacidade real de distribuir — mas atenção ao investimento em reforma de R$ 28k que aparece em mar/2026: é despesa pontual ou virou padrão?
- **Plano de contas (arquivo 05):** classificação correta separa o que é lucro distribuível do que é reinvestimento — sem plano de contas claro, distribuição vira chute.
