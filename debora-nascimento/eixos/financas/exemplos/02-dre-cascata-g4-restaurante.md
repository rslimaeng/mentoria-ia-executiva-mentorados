---
tipo: exemplo-pratico
cenario: DRE em cascata (método G4) — Restaurante CHR
uso: pra praticar IA no encontro 3 (Finanças)
formato_real: xlsx (será gerado em paralelo)
atualizado: 2026-06-30
---

# DRE em Cascata — Método G4 (Restaurante CHR)

## Objetivo deste arquivo

DRE estruturada em **12 grupos em cascata** seguindo o método **G4 (Julian Tonioli — Sistema G4 Educação)**. A diferença do método G4 pra DRE contábil tradicional é separar **despesas variáveis** de **despesas fixas** — o que permite calcular **Margem de Contribuição** antes do EBITDA.

**Como Débora vai usar com IA:**

1. Anexa o `.xlsx` e pede: "Calcula o ponto de equilíbrio operacional desse restaurante e diz quantos R$ de receita ele precisa pra cobrir só os custos fixos."
2. Pede análise vertical (% sobre receita líquida) e benchmarka contra mercado.
3. Cruza com o fluxo de caixa (arquivo 01) — entradas brutas devem casar com Receita Bruta da DRE; saídas operacionais devem casar com CMV + despesas.

> **Por que separar MC de EBITDA:** MC mostra **quanto sobra de cada R$ vendido** depois de pagar o que varia com a venda (matéria-prima, comissão, taxa cartão). EBITDA mostra o resultado operacional **depois** de pagar a estrutura fixa (aluguel, folha, energia). Decisões diferentes — MC orienta precificação de prato; EBITDA orienta tamanho de estrutura.

> **Conexão com a banda de forró da Débora:** mesma lógica vale. Cachê do show é receita; cachê dos músicos + frete + combustível = despesa variável; ensaio + aluguel de sala + assessoria = despesa fixa.

---

## DRE — mar, abr, mai/2026 (R$)

| # | Conta | Mar/2026 | Abr/2026 | Mai/2026 | Média 3M | % vertical |
|---|---|---:|---:|---:|---:|---:|
| 1 | **(=) Receita Bruta** | 261.840 | 288.420 | 273.180 | 274.480 | 100,0% |
| 2 | (−) Deduções (impostos sobre venda + descontos) | -15.710 | -17.305 | -16.391 | -16.469 | -6,0% |
| 3 | **(=) Receita Líquida** | 246.130 | 271.115 | 256.789 | 258.011 | 94,0% |
| 4 | (−) CMV (alimentos + bebidas + descartáveis) | -83.789 | -91.420 | -86.840 | -87.350 | -33,9% |
| 5 | **(=) Lucro Bruto** | 162.341 | 179.695 | 169.949 | 170.661 | 66,2% |
| 6 | (−) Despesas Variáveis | -22.180 | -24.840 | -23.510 | -23.510 | -9,1% |
| 6.1 | Taxa cartão (≈3% receita) | -7.855 | -8.653 | -8.195 | -8.234 | -3,2% |
| 6.2 | Comissão garçom (10% receita salão) | -10.470 | -11.537 | -10.927 | -10.978 | -4,3% |
| 6.3 | Taxa iFood/delivery | -2.620 | -2.880 | -2.730 | -2.743 | -1,1% |
| 6.4 | Marketing variável (% sobre receita) | -1.235 | -1.770 | -1.658 | -1.554 | -0,6% |
| 7 | **(=) Margem de Contribuição** | 140.161 | 154.855 | 146.439 | 147.151 | 57,0% |
| 8 | (−) Despesas Operacionais Fixas | -107.890 | -108.420 | -108.150 | -108.153 | -41,9% |
| 8.1 | Folha (cozinha + salão + encargos) | -52.600 | -53.180 | -52.840 | -52.873 | -20,5% |
| 8.2 | Aluguel | -18.000 | -18.000 | -18.000 | -18.000 | -7,0% |
| 8.3 | Energia (Enel) | -3.840 | -3.920 | -3.880 | -3.880 | -1,5% |
| 8.4 | Água (Cagece) | -1.180 | -1.220 | -1.190 | -1.197 | -0,5% |
| 8.5 | Gás (GLP) | -980 | -1.020 | -990 | -997 | -0,4% |
| 8.6 | Internet + telefonia | -480 | -480 | -480 | -480 | -0,2% |
| 8.7 | Contabilidade | -1.450 | -1.450 | -1.450 | -1.450 | -0,6% |
| 8.8 | Software (PDV + gestão + ERP) | -890 | -890 | -890 | -890 | -0,3% |
| 8.9 | Pró-labore sócios (A + B) | -16.000 | -16.000 | -16.000 | -16.000 | -6,2% |
| 8.10 | Outras despesas operacionais | -12.470 | -12.260 | -12.430 | -12.387 | -4,8% |
| 9 | **(=) EBITDA** | 32.271 | 46.435 | 38.289 | 38.998 | 15,1% |
| 10 | (−) Depreciação (equip. cozinha + mobiliário) | -2.400 | -2.400 | -2.400 | -2.400 | -0,9% |
| 11 | **(=) EBIT / Resultado Operacional** | 29.871 | 44.035 | 35.889 | 36.598 | 14,2% |
| 12 | (−) Imposto sobre lucro (no Simples já está no item 2) | 0 | 0 | 0 | 0 | 0,0% |
| 13 | **(=) Lucro Líquido** | 29.871 | 44.035 | 35.889 | **36.598** | **14,2%** |

> **Atenção contábil:** restaurante no Simples Nacional já paga imposto **sobre faturamento** (linha 2), não sobre lucro. Por isso linha 12 zerada. Em Lucro Presumido ou Real, a linha 12 entraria.

---

## Indicadores derivados (média 3 meses)

| Indicador | Valor | Benchmark mercado | Status |
|---|---:|---|---|
| Margem Bruta | 66,2% | 60–70% (casual food) | OK |
| Margem de Contribuição | 57,0% | 50–60% | OK |
| Margem EBITDA | 15,1% | 12–18% | OK |
| Margem Líquida | 14,2% | 8–15% | OK / um pouco alta — checar se faltou despesa |
| CMV / Receita Bruta | 31,8% | 28–35% | OK |
| Folha / Receita Bruta | 19,3% (s/ pró-labore) | 18–25% | OK |
| **Ponto de equilíbrio (break-even)** | **R$ 189.742/mês** | — | Receita atual está 44% acima |

**Como ler o ponto de equilíbrio:** acima de R$ 189.742 de receita bruta, cada R$ vendido vira lucro. Abaixo disso, o restaurante opera no vermelho. Margem de segurança atual: ~30%.

---

## Pontos de atenção pra discussão com a IA

1. **Margem líquida 14,2% é alta pra setor** — confirmar se não está faltando despesa lançada (verificar contra fluxo de caixa).
2. **Pró-labore + folha total = 26% da receita** — espaço pra otimização ou ponto de risco se vendas caírem.
3. **Marketing 0,6% é baixo** — investimento mínimo, pode estar limitando crescimento.
4. **Crescimento mar→abr: +10%** — vale isolar se foi calendário (mais finais de semana) ou tração real.

---

## Conexão com os outros arquivos

- **Arquivo 01 (Fluxo de Caixa):** Receita Bruta acumulada 3M = R$ 823.440 (DRE) vs. R$ 810.420 (caixa). Diferença de R$ 13k = receita de cartão crédito de mai ainda não compensada em mai (D+30) — **comportamento esperado**, não erro.
- **Arquivo 03 (MC dos 5 pratos):** linha 7 (MC consolidada) é a soma do que cada prato individualmente contribui.
- **Arquivo 04 (DCF):** Lucro Líquido médio R$ 36.598/mês × 25% (cota oferecida) = **R$ 9.149/mês** seria o teto de distribuição — mas premissa-base usa R$ 7.000 (mais conservador, descontando reinvestimento e capital de giro).
