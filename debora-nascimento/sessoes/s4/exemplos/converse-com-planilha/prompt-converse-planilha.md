---
caso: converse-com-planilha
sessao: S4 · Chat + Cowork
ferramenta: Chat + upload de arquivo
tempo: 25-35 min · 5-6 turnos
arquivo: planilha-produtividade-mock.xlsx
---

# Prompt · Converse com sua planilha antes de decidir

> Você tem uma planilha. Antes de fazer o gráfico bonito e apresentar pra chefia, você conversa com ela junto do Claude — pede pra ele te mostrar o que salta aos olhos, o que é armadilha, o que você não devia dizer sem checar.

---

## Antes de começar

1. Baixe [planilha-produtividade-mock.xlsx](planilha-produtividade-mock.xlsx) — dados fictícios de uma equipe pra você praticar
2. Abra [claude.ai/new](https://claude.ai/new)
3. Clique no clip de anexo (ou arrasta a planilha pra dentro da conversa)
4. **Aguarde** o Claude confirmar que leu a planilha antes de mandar o próximo prompt

---

## Prompt inicial · PCTFL

```
Papel: Você é um analista de gestão sênior que ajuda executivas a lerem planilhas antes de apresentar.

Contexto: Anexei uma planilha com dados de uma equipe fictícia — 30 colaboradores, medidos ao longo de 6 meses em horas trabalhadas, entregas concluídas, satisfação autorreportada e faltas. Vou apresentar isso numa reunião com minha chefia e preciso saber o que os dados estão dizendo antes de montar slides.

Tarefa: Me mostra o que essa planilha está me dizendo. Especificamente:
1. As 3 relações mais fortes entre as variáveis (ex.: horas × satisfação, entregas × faltas)
2. Anomalias — pessoas ou meses que fogem do padrão
3. Uma leitura honesta: o que dá pra afirmar com esses dados, e o que precisaria de mais análise antes de virar afirmação

Formato: Estruturado em 3 seções (Relações, Anomalias, Leitura honesta). Cada relação com o número (correlação ou % de variação). Cada anomalia com o dado bruto que sustenta.

Limite: Nada de "os dados sugerem que talvez possa haver uma tendência" — se não dá pra afirmar, diga. Se dá, diga com o número. Não invente narrativa causal (X causa Y) — mostra só correlação e me deixa julgar a causa.
```

---

## Prompt 2 · Peça o gráfico da relação mais interessante

Depois que o Claude te devolveu as 3 relações, escolhe UMA e peça pra ver.

```
Da relação [X × Y], me monta um gráfico de dispersão. Marca em cor diferente os pontos que estão >2 desvios padrão da média. Legenda simples — vou botar num slide.
```

---

## Prompt 3 · Force o "e se eu estivesse errada?"

Este é o prompt que separa análise de bajulação.

```
Se alguém da chefia me perguntar "isso que você tá mostrando não seria explicado por [FATOR ALTERNATIVO — ex.: mês de férias, mudança de escritório]?", como eu respondo? O que os dados dessa planilha permitem afirmar contra essa objeção?
```

---

## Prompt 4 · Peça o parágrafo de conclusão

Só depois de ter pensado. Não antes.

```
Escreve pra mim 1 parágrafo (~4 linhas) que eu poderia colocar como conclusão do slide sobre [RELAÇÃO ESCOLHIDA]. Tom executivo — nada de "os dados aparentam sugerir". Onde eu deveria hedgear, marca com colchete: [HEDGE aqui].
```

---

## Prompt 5 · Transfira pro Cowork

Se você quiser polir esse parágrafo com contexto do seu deck real, transfere pro Cowork. Cole o parágrafo lá e:

```
Reescreve esse parágrafo pra caber num slide de deck executivo. Regras:
- Máximo 3 linhas
- Verbo forte no início
- Sem "eu acho" ou "os dados sugerem"
- Preserva o hedge onde estiver
```

---

## Checklist antes de fechar

- [ ] Salvou o gráfico que o Claude gerou (screenshot ou download)
- [ ] Anotou UMA leitura que você levaria pra chefia
- [ ] Marcou UM ponto que ainda precisa ser checado antes de apresentar
- [ ] Sabe explicar em 30s como você chegou nessa leitura

---

## Truques

**Nunca aceite a primeira leitura sem perguntar "e se eu estivesse errada".** Toda planilha permite mais de uma narrativa. O Claude te dá a mais óbvia primeiro.

**Peça o número, não o adjetivo.** "Correlação forte" não te ajuda. "Correlação 0.72" te ajuda.

**Correlação ≠ causa.** O Claude sabe disso, mas às vezes usa linguagem sugestiva. Fique atenta.

---

*Base: adaptação de [Chart your data in conversation with Claude · Anthropic](https://claude.com/resources/use-cases/chart-your-data-before-you-commit). Curadoria: Rafael Lima · Mentoria IA Executiva.*
