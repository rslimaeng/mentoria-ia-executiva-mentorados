---
tipo: exemplo-pratico
cenario: Margem de Contribuição dos 5 pratos âncora — Restaurante CHR
uso: pra praticar IA no encontro 3 (Finanças)
formato_real: xlsx (será gerado em paralelo)
atualizado: 2026-06-30
---

# Margem de Contribuição — 5 Pratos Âncora

## Objetivo deste arquivo

Análise de **Margem de Contribuição unitária** dos 5 pratos mais vendidos do Restaurante CHR. Permite responder: **"Qual prato dá mais lucro real depois de descontar o que varia com a venda?"**

**Como Débora vai usar com IA:**

1. Anexa o `.xlsx` e pede: "Rankeia os pratos por MC total mensal e por MC %. São rankings diferentes? Qual usar pra decisão de cardápio?"
2. Pede simulação: "Se eu aumentar 5% no preço do prato com menor MC%, mantendo o mesmo volume, qual o impacto no lucro mensal?"
3. Testa: "Se o restaurante quiser bater R$ 50k de MC só com esses 5 pratos, preciso aumentar volume de quanto em cada um?"

---

## Conceito: MC ≠ Lucro

**Margem de Contribuição (MC)** é o que sobra do preço de venda DEPOIS de descontar **só o que varia com a venda**:
- Custo direto (ficha técnica — ingredientes)
- Comissão do garçom (10%)
- Taxa do cartão (3% média)

Ainda **não** desconta aluguel, folha, energia — esses são fixos, vão pra DRE depois.

**Por que isso importa:**
- **MC unitária alta + volume baixo** = prato premium (margem boa, mas vende pouco)
- **MC unitária baixa + volume alto** = prato chamariz (margem apertada, mas movimenta)
- Decisão de cardápio nunca é só pelo "mais lucrativo" — é pela **MC total mensal** (unitária × volume).

> **Regra G4:** o ideal é ter no cardápio uma combinação dos 4 quadrantes (alta MC% / alta MC R$ / alto giro / baixo giro). Carta toda no mesmo quadrante quebra o negócio.

---

## Cálculo da MC unitária

Fórmula:
```
MC unitária = Preço venda − Custo direto − (Preço × 10% comissão) − (Preço × 3% cartão)
            = Preço × (1 − 13%) − Custo direto
            = Preço × 0,87 − Custo direto
```

---

## Tabela dos 5 pratos

| # | Prato | Preço venda R$ | Custo direto R$ | Comissão 10% R$ | Taxa cartão 3% R$ | MC unitária R$ | MC % | Volume/mês | MC total R$/mês |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|
| 1 | Filé à parmegiana | 58,00 | 18,00 | 5,80 | 1,74 | **32,46** | **56,0%** | 240 | **7.790,40** |
| 2 | Camarão na moranga | 78,00 | 32,00 | 7,80 | 2,34 | **35,86** | **46,0%** | 110 | **3.944,60** |
| 3 | Picanha na chapa | 92,00 | 41,00 | 9,20 | 2,76 | **39,04** | **42,4%** | 180 | **7.027,20** |
| 4 | Risoto de frutos do mar | 65,00 | 28,00 | 6,50 | 1,95 | **28,55** | **43,9%** | 95 | **2.712,25** |
| 5 | Hambúrguer da casa | 42,00 | 14,00 | 4,20 | 1,26 | **22,54** | **53,7%** | 320 | **7.212,80** |
|  | **TOTAL** | — | — | — | — | — | — | **945** | **R$ 28.687,25** |

---

## Ranking — duas leituras possíveis

### Ranking 1: por MC unitária absoluta (R$)
1. Picanha na chapa — R$ 39,04/prato
2. Camarão na moranga — R$ 35,86/prato
3. Filé à parmegiana — R$ 32,46/prato
4. Risoto de frutos do mar — R$ 28,55/prato
5. Hambúrguer da casa — R$ 22,54/prato

> **Leitura:** se o restaurante quer **upselling** (sugerir prato mais lucrativo por venda), a picanha é a rainha.

### Ranking 2: por MC % (eficiência da margem)
1. Filé à parmegiana — 56,0%
2. Hambúrguer da casa — 53,7%
3. Camarão na moranga — 46,0%
4. Risoto de frutos do mar — 43,9%
5. Picanha na chapa — 42,4%

> **Leitura:** se o restaurante quer **proteger margem** (qual prato sofre menos com aumento de custo de insumo), filé e hambúrguer são os mais robustos.

### Ranking 3: por MC total mensal (R$ que cada prato gera)
1. **Filé à parmegiana** — R$ 7.790,40/mês  ←  campeão de MC total
2. Hambúrguer da casa — R$ 7.212,80/mês
3. Picanha na chapa — R$ 7.027,20/mês
4. Camarão na moranga — R$ 3.944,60/mês
5. Risoto de frutos do mar — R$ 2.712,25/mês

> **Leitura:** este é o ranking **mais importante pra decisão de cardápio**. Se for tirar um prato da carta, candidato natural é o risoto (menor MC total mensal). Mas atenção: ele pode ser o prato que segura um nicho de cliente específico — análise quantitativa não decide sozinha.

---

## Insights cruzados

| Insight | Implicação |
|---|---|
| Hambúrguer vende 320/mês com MC% de 53,7% | Prato âncora — chamariz com margem boa. Mantém. |
| Picanha tem maior MC unitária mas MC% mediana | Cobrar mais ou negociar fornecedor de carne. |
| Risoto tem MC total mensal mais baixa | Avaliar reposicionar receita ou substituir por prato de maior giro. |
| Filé é o mais equilibrado (alto MC% + alto volume) | Provavelmente o "carro-chefe" da casa — destacar no cardápio. |
| Camarão tem MC% baixa por causa do custo do camarão | Sazonalidade de preço — renegociar safra. |

---

## Conexão com os outros arquivos

- **MC dos 5 pratos = R$ 28.687/mês** — isso é só o "topo do iceberg". O cardápio inteiro do restaurante gera os **R$ 147.151 de MC** consolidados na DRE (arquivo 02). Ou seja, esses 5 pratos = **~19% da MC total**.
- **Atenção:** se a Débora rodar IA pra "calcular MC do restaurante", a resposta dela vai ser a DRE consolidada, não estes 5 pratos isolados. São níveis de análise diferentes — prato a prato (gestão de cardápio) vs. consolidado (gestão do negócio).

---

## Pergunta pra Débora levar pro encontro

> Se você fosse sócia de 25%, qual seria sua **primeira recomendação operacional** olhando essa tabela de MC? Justifique com número.
