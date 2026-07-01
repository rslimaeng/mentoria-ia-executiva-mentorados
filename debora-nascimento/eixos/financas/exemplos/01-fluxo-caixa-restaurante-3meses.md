---
tipo: exemplo-pratico
cenario: Fluxo de caixa diário — Restaurante CHR (Fortaleza)
uso: pra praticar IA no encontro 3 (Finanças)
formato_real: xlsx (será gerado em paralelo)
atualizado: 2026-06-30
---

# Fluxo de Caixa — Restaurante CHR

## Objetivo deste arquivo

Este é um fluxo de caixa diário de 90 dias (mar/2026 a mai/2026) de um restaurante meio-médio em Fortaleza. Os dados são FICTÍCIOS mas REALISTAS — refletem o padrão de movimento de uma casa que fatura entre R$ 200k–300k/mês.

**Como Débora vai usar com IA:**

1. Anexa o `.xlsx` num chat com Claude/ChatGPT e pede:
   - "Identifica as 3 categorias de saída que mais consomem caixa"
   - "Compara o ticket médio de dia útil vs. fim de semana"
   - "Aponta qualquer lançamento que pareça erro de classificação ou valor desproporcional"
2. Treina o olhar pra **achar anomalias** antes da IA — depois compara com o que a IA achou.
3. Cruza com a DRE (arquivo 02) — o saldo de entradas/saídas deve bater com receita bruta e despesas operacionais.

> **Dica de prompt pra Débora:** "Atua como controller financeiro de restaurante. Analisa esse fluxo de caixa e me devolve: (1) padrão de sazonalidade semanal, (2) categorias com maior peso, (3) lançamentos suspeitos com justificativa. Não inventa nada — se o dado não está claro, pergunta."

---

## Premissas do cenário

| Item | Valor |
|---|---|
| Faturamento mensal médio | R$ 270.000 |
| Dias úteis (seg–qui) | Receita R$ 6.000 – R$ 12.000/dia |
| Sexta a domingo | Receita R$ 14.000 – R$ 22.000/dia |
| Mix de recebimento | Cartão crédito 45% · Débito 22% · PIX 18% · iFood 10% · Dinheiro 5% |
| Aluguel mensal | R$ 18.000 (vence dia 5) |
| Folha quinzenal | Dia 15 e dia 30 — ~R$ 26.000 por quinzena |
| Impostos Simples | ~6% sobre faturamento (DAS dia 20) |
| Pró-labore sócios | R$ 8.000 cada (Sócio A e Sócio B), pago dia 10 |

---

## Amostra de lançamentos (30 linhas — extrato completo de 90 dias no .xlsx)

| Data | Categoria | Subcategoria | Descrição | Entrada R$ | Saída R$ | Saldo |
|---|---|---|---|---|---|---|
| 02/03/2026 | Receita | Cartão crédito | Vendas do dia (seg) | 3.840,00 | — | 3.840,00 |
| 02/03/2026 | Receita | PIX | Vendas do dia (seg) | 1.520,00 | — | 5.360,00 |
| 02/03/2026 | Receita | Dinheiro | Vendas do dia (seg) | 380,00 | — | 5.740,00 |
| 02/03/2026 | Fornecedor | Hortifruti | Feira semanal — Ceasa | — | 1.240,00 | 4.500,00 |
| 03/03/2026 | Receita | Cartão crédito | Vendas do dia (ter) | 2.980,00 | — | 7.480,00 |
| 03/03/2026 | Receita | iFood | Repasse semanal | 1.180,00 | — | 8.660,00 |
| 03/03/2026 | Fornecedor | Cárneas | Açougue Boi Forte | — | 2.840,00 | 5.820,00 |
| 05/03/2026 | Despesa fixa | Aluguel | Aluguel mar/2026 | — | 18.000,00 | -12.180,00 |
| 06/03/2026 | Receita | Cartão crédito | Vendas do dia (sex) | 8.450,00 | — | -3.730,00 |
| 06/03/2026 | Receita | Cartão débito | Vendas do dia (sex) | 4.120,00 | — | 390,00 |
| 06/03/2026 | Receita | PIX | Vendas do dia (sex) | 3.640,00 | — | 4.030,00 |
| 07/03/2026 | Receita | Cartão crédito | Vendas do dia (sáb) | 11.280,00 | — | 15.310,00 |
| 07/03/2026 | Receita | Cartão débito | Vendas do dia (sáb) | 5.840,00 | — | 21.150,00 |
| 07/03/2026 | Despesa variável | Comissão | Comissão garçom (sáb) | — | 1.712,00 | 19.438,00 |
| 08/03/2026 | Fornecedor | Bebidas | Distribuidora Norte | — | 4.180,00 | 15.258,00 |
| 10/03/2026 | Sócios | Pró-labore | Sócio A — mar/2026 | — | 8.000,00 | 7.258,00 |
| 10/03/2026 | Sócios | Pró-labore | Sócio B — mar/2026 | — | 8.000,00 | -742,00 |
| 12/03/2026 | Despesa fixa | Energia | Enel — fev/2026 | — | 3.840,00 | -4.582,00 |
| 13/03/2026 | Despesa fixa | Gás | Recarga GLP | — | 980,00 | -5.562,00 |
| 14/03/2026 | Fornecedor | Descartáveis | Embalagens Sul | — | 1.420,00 | -6.982,00 |
| 14/03/2026 | Fornecedor | Descartáveis | Embalagens Sul | — | 1.420,00 | -8.402,00 |
| 15/03/2026 | Despesa fixa | Folha | Folha 1ª quinzena | — | 26.180,00 | -34.582,00 |
| 17/03/2026 | Despesa variável | Marketing | Tráfego pago — Meta Ads | — | 1.200,00 | -33.382,00 |
| 18/03/2026 | Fornecedor | Hortifruti | Feira semanal | — | 1.380,00 | -32.002,00 |
| 19/03/2026 | Despesa variável | Taxa cartão | Adquirente — taxa mar | — | 4.260,00 | -27.742,00 |
| 20/03/2026 | Imposto | DAS Simples | DAS competência fev | — | 14.820,00 | -12.922,00 |
| 21/03/2026 | Fornecedor | Manutenção | Reforma fachada — entrada | — | 28.500,00 | 15.578,00 |
| 22/03/2026 | Receita | Cartão crédito | Vendas do dia (dom) | 9.840,00 | — | 25.418,00 |
| 28/03/2026 | Receita | Eventos | Aluguel do salão — aniversário | 4.500,00 | — | 29.918,00 |
| 30/03/2026 | Despesa fixa | Folha | Folha 2ª quinzena | — | 26.420,00 | 3.498,00 |

> **Nota:** o dataset completo dos 90 dias (~640 lançamentos) vai estar no `.xlsx`. Esta amostra é só pra Débora ver o padrão.

---

## Estrutura de categorias (resumo de 90 dias)

| Categoria | Total entradas | Total saídas | Saldo |
|---|---|---|---|
| Receita | R$ 810.420 | — | +810.420 |
| CMV (Fornecedor cárneas + hortifruti + bebidas + descartáveis) | — | R$ 259.300 | -259.300 |
| Despesas variáveis (taxa cartão, comissão, marketing, iFood fee) | — | R$ 78.420 | -78.420 |
| Despesas fixas (aluguel, energia, água, gás, internet, software, contábil) | — | R$ 78.840 | -78.840 |
| Folha (cozinha + salão) | — | R$ 158.120 | -158.120 |
| Sócios (pró-labore) | — | R$ 48.000 | -48.000 |
| Impostos (Simples) | — | R$ 48.620 | -48.620 |
| Investimento (reforma fachada) | — | R$ 28.500 | -28.500 |
| **TOTAL** | **R$ 810.420** | **R$ 699.800** | **+R$ 110.620** |

---

## Observações pra análise

- **Sazonalidade semanal:** sexta a domingo concentra ~58% do faturamento. Terça e quarta são os dias mais fracos.
- **Sazonalidade mensal:** abril (mês com mais finais de semana) ficou ~8% acima da média.
- **CMV médio:** ~32% da receita (dentro do benchmark de food service casual).
- **Folha:** ~22% (alta — possível ponto de atenção em otimização de escalas).

> **Anomalias plantadas pra Débora achar:** este fluxo tem 2 lançamentos estranhos. Não conta pra ela — deixa ela achar.
