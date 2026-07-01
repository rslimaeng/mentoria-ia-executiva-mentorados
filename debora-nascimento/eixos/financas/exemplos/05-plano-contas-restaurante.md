---
tipo: exemplo-pratico
cenario: Plano de contas (método G4) — Restaurante CHR / food service
uso: pra praticar IA no encontro 3 (Finanças)
formato_real: xlsx (será gerado em paralelo)
atualizado: 2026-06-30
---

# Plano de Contas — Restaurante CHR

## Objetivo deste arquivo

Plano de contas hierárquico adaptado ao **método G4** pra **food service** (restaurante, bar, food truck). É a **espinha dorsal** de tudo: sem plano de contas claro, DRE vira ficção e IA não consegue categorizar extrato bancário corretamente.

**Como Débora vai usar com IA:**

1. Anexa este arquivo + um extrato bancário bruto e pede:
   - "Classifica cada lançamento desse extrato usando ESTE plano de contas. Se um lançamento não couber, marque como 'a classificar' e me diga por quê."
   - "Identifica lançamentos que deveriam ter sido CMV mas foram como despesa fixa (erro comum)."
2. Pede sugestão: "Faltou alguma conta importante pra restaurante meio-médio? Sugere ajuste."
3. Pode replicar a mesma estrutura pra **banda de forró** dela — basta trocar nomenclatura (CMV vira "custo direto de show": cachê músicos, frete, hospedagem).

---

## Por que IA precisa de plano de contas

Sem plano de contas, IA tenta categorizar pelo nome do estabelecimento — e erra muito:
- "Carrefour" → IA chuta "supermercado pessoal", mas pode ser **CMV (hortifruti)** do restaurante.
- "Posto Shell" → IA chuta "combustível", mas pode ser **logística de delivery** ou **despesa pessoal** misturada (problema clássico).
- "PIX João Silva" → IA não tem como saber se é **fornecedor**, **funcionário** ou **sócio**.

**Com plano de contas + glossário de fornecedores conhecidos**, a IA acerta 85%+ na primeira passada. Sem isso, fica em 40%.

> **Dica de prompt master pra Débora:** "Você é um contador. Vou te passar (1) este plano de contas e (2) um extrato bancário. Sua tarefa: classificar cada lançamento na conta MAIS ESPECÍFICA possível. Se não tiver certeza, marca como 'a classificar' com sua melhor hipótese e por que ficou em dúvida. NÃO INVENTA conta que não existe no plano."

---

## Estrutura do plano de contas

### 1 — RECEITAS

| Código | Conta | Descrição |
|---|---|---|
| 1.1 | Venda balcão | Receita do salão (consumo no local) |
| 1.2 | Venda delivery próprio | Pedidos via WhatsApp/telefone com motoboy próprio |
| 1.3 | Venda iFood | Receita líquida do iFood (já descontada taxa marketplace) |
| 1.4 | Venda Rappi/99Food/outros | Outros marketplaces |
| 1.5 | Venda eventos | Aluguel de salão pra aniversário, casamento, confraternização |
| 1.6 | Venda buffet/catering externo | Eventos servidos fora do restaurante |
| 1.7 | Outras receitas | Estorno, achados, indenizações |

### 2 — DEDUÇÕES DA RECEITA

| Código | Conta | Descrição |
|---|---|---|
| 2.1 | Simples Nacional (DAS) | Imposto sobre faturamento |
| 2.2 | Devoluções e cancelamentos | Pedido cancelado, prato devolvido com estorno |
| 2.3 | Descontos concedidos | Cupom, voucher, cortesia formal |

### 3 — CMV (Custo da Mercadoria Vendida)

| Código | Conta | Descrição |
|---|---|---|
| 3.1 | Cárneas | Carnes bovina, suína, aves, peixes, frutos do mar |
| 3.2 | Hortifruti | Verduras, legumes, frutas, ervas |
| 3.3 | Mercearia / secos | Arroz, feijão, massas, farinhas, óleos, temperos |
| 3.4 | Laticínios | Leite, queijos, manteiga, iogurte |
| 3.5 | Bebidas | Refrigerante, sucos, água, cervejas, vinhos, destilados |
| 3.6 | Descartáveis | Embalagem delivery, guardanapo, palito, sacola |
| 3.7 | Padaria / panificação | Pães, massas frescas, sobremesas terceirizadas |
| 3.8 | Outros insumos | Gelo, café, açúcar, adoçante |

### 4 — DESPESAS VARIÁVEIS (variam com a venda)

| Código | Conta | Descrição |
|---|---|---|
| 4.1 | Taxa cartão | Taxa da adquirente (Cielo, Stone, Getnet) — débito + crédito |
| 4.2 | Comissão garçom | 10% sobre receita salão |
| 4.3 | Taxa iFood / marketplace fee | Comissão paga ao iFood (12–27% conforme plano) |
| 4.4 | Taxa motoboy terceirizado | Quando entrega não é própria |
| 4.5 | Marketing variável | Tráfego pago % sobre faturamento (Meta Ads, Google Ads) |
| 4.6 | Embalagem variável | Embalagem que escala com volume delivery |

### 5 — DESPESAS OPERACIONAIS FIXAS

| Código | Conta | Descrição |
|---|---|---|
| 5.1 | Folha cozinha | Chef, cozinheiros, auxiliares, lavadores |
| 5.2 | Folha salão | Garçons (base CLT), recepção, caixa |
| 5.3 | Encargos sociais (INSS + FGTS) | Quando fora do Simples; em Simples já está em 2.1 |
| 5.4 | Aluguel | Aluguel mensal do imóvel |
| 5.5 | Energia elétrica | Enel |
| 5.6 | Água | Cagece |
| 5.7 | Gás (GLP) | Recarga de botijões + gás encanado |
| 5.8 | Internet + telefonia | Wi-Fi, telefone fixo, celular corporativo |
| 5.9 | Contabilidade | Honorários mensais do contador |
| 5.10 | Software (PDV + ERP + gestão) | Goomer, Consumer, Conta Azul, Omie, etc. |
| 5.11 | Pró-labore sócios | Retirada mensal dos sócios A e B |
| 5.12 | Segurança | Vigilância, alarme monitorado, câmeras |
| 5.13 | Limpeza | Material + diarista (se terceirizado) |

### 6 — OUTRAS DESPESAS OPERACIONAIS

| Código | Conta | Descrição |
|---|---|---|
| 6.1 | Manutenção predial | Pintura, telhado, fachada, hidráulica |
| 6.2 | Manutenção equipamentos cozinha | Geladeira, fogão industrial, forno, fritadeira |
| 6.3 | Treinamento de equipe | Curso, palestra, capacitação |
| 6.4 | Uniformes | Aventais, camisetas, calçados de segurança |
| 6.5 | EPI | Luvas, máscaras, touca, redes |
| 6.6 | Material de escritório | Papel, caneta, impressora |
| 6.7 | Despesas com viagem (compras) | Viagem pra mercado atacado, feira de fornecedor |
| 6.8 | Outras despesas administrativas | Cartório, taxas, certidões, alvarás |

### 7 — DEPRECIAÇÃO

| Código | Conta | Descrição |
|---|---|---|
| 7.1 | Depreciação equipamentos de cozinha | 10 anos linear |
| 7.2 | Depreciação mobiliário | Mesas, cadeiras, decoração — 10 anos |
| 7.3 | Depreciação utensílios | Pratos, talheres, copos — 5 anos |
| 7.4 | Depreciação benfeitorias | Reforma do imóvel alugado — prazo do contrato |

### 8 — IMPOSTOS SOBRE LUCRO (só se fora do Simples)

| Código | Conta | Descrição |
|---|---|---|
| 8.1 | IRPJ | Imposto de renda pessoa jurídica |
| 8.2 | CSLL | Contribuição social sobre lucro líquido |

> **Restaurante CHR está no Simples** — então tudo de imposto fica em 2.1 (DAS). Contas 8.1 e 8.2 ficam zeradas. Plano mantém a estrutura caso migre pra Lucro Presumido.

### 9 — INVESTIMENTOS (CAPEX — não vai pra DRE, vai pro Balanço)

| Código | Conta | Descrição |
|---|---|---|
| 9.1 | Equipamentos novos | Compra de fogão, geladeira, equipamento novo |
| 9.2 | Reforma e benfeitorias | Reforma do salão, pintura grande, fachada nova |
| 9.3 | Investimento em marketing institucional | Branding, sinalização permanente, site |

> **Cuidado:** despesa de R$ 28.500 com "reforma fachada" no fluxo de caixa (arquivo 01) **NÃO É despesa operacional** — vai pra 9.2 e entra na DRE só via depreciação. Lançar como despesa direta distorce EBITDA em ~R$ 28k no mês.

---

## Glossário de fornecedores conhecidos (Restaurante CHR)

| Nome no extrato | Conta no plano |
|---|---|
| BOI FORTE AÇOUGUE | 3.1 Cárneas |
| CEASA / CENTRAL ABASTECIMENTO | 3.2 Hortifruti |
| DIST NORTE BEBIDAS | 3.5 Bebidas |
| EMBALAGENS SUL | 3.6 Descartáveis |
| ENEL CE | 5.5 Energia |
| CAGECE | 5.6 Água |
| GLP ULTRAGAZ | 5.7 Gás |
| IMOBILIARIA X | 5.4 Aluguel |
| ESCRITORIO CONTABIL Y | 5.9 Contabilidade |
| GOOMER / CONTA AZUL | 5.10 Software |
| META PLATAFORMS / META ADS | 4.5 Marketing variável |
| IFOOD COM AGENCIA | 4.3 Taxa iFood |
| CIELO / STONE / GETNET | 4.1 Taxa cartão |

---

## Checklist pra Débora antes de jogar pra IA

- [ ] Plano de contas atualizado nos últimos 6 meses?
- [ ] Glossário de fornecedores cobre 80%+ do volume?
- [ ] Cada conta tem **regra clara** de quando entra (evita "conta lixo")?
- [ ] Existe conta "**a classificar**" pra IA jogar o que não souber? (CRÍTICO — sem isso ela chuta.)
- [ ] Investimento (CAPEX) está separado de despesa (OPEX)?
- [ ] Pró-labore separado de folha?
- [ ] Impostos sobre venda separados de impostos sobre lucro?

---

## Conexão com os outros arquivos

- **Fluxo de caixa (arquivo 01):** cada lançamento daquele extrato precisa estar classificado numa conta DESTE plano. Se "Reforma fachada" foi pra "Despesa fixa" no fluxo, está **errado** — deveria ir pra **9.2 (CAPEX)**.
- **DRE (arquivo 02):** estrutura dos 12 grupos da DRE em cascata é o **agrupamento** das contas deste plano. Grupo 4 (CMV) = soma de 3.1 a 3.8. Grupo 6 (Variáveis) = soma de 4.1 a 4.6. Etc.
- **Plano de contas mal feito = DRE bonita mas falsa.** É o erro mais comum em PME e o que mais distorce análise de IA.
