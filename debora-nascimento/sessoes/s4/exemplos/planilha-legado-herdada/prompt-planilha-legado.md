---
caso: planilha-legado-herdada
sessao: S4 · Chat + Cowork
ferramenta: Chat + upload xlsx + file creation
tempo: 35-45 min · 6-7 turnos
arquivo: planilha-legado-mock.xlsx
---

# Prompt · Herdei essa planilha, o que ela faz?

> Alguém saiu da equipe. Deixou uma planilha viva que "todo mundo usa". Fórmulas em cima de fórmulas, abas conectadas em jeitos que ninguém documentou, valores que mudam sozinhos quando você mexe em outra coisa. E agora você precisa ESTENDER essa planilha sem quebrar tudo.
>
> Esse é um dos usos mais valiosos do Claude no dia a dia executivo.

---

## Antes de começar

1. Baixe [planilha-legado-mock.xlsx](planilha-legado-mock.xlsx) — planilha fictícia de acompanhamento trimestral de equipe, com fórmulas, aba Legend, cell comments e conexões entre abas. É complexa de propósito.
2. Abra [claude.ai/new](https://claude.ai/new)
3. Anexe a planilha (clip ou arrasta)
4. **Habilite File Creation** nas configurações da conversa — assim o Claude pode devolver uma versão nova do arquivo, não só texto explicando

---

## Prompt inicial · PCTFL

```
Papel: Você é uma analista financeira sênior que se especializou em auditar e estender modelos herdados. Já viu de tudo — de planilhas com 40 abas até modelos que quebram se você mexer numa célula errada.

Contexto: Herdei essa planilha de acompanhamento trimestral. A pessoa que criou saiu. Preciso entender como ela funciona ANTES de mexer, porque semana que vem preciso adicionar o Q3 e o Q4 desse ano.

A planilha tem uma aba "Legend" com algumas notas e alguns cell comments espalhados. Não é o suficiente.

Tarefa: Faz 3 coisas, nessa ordem:
1. Explica como as abas se conectam entre si — o que puxa de onde, o que é hardcoded, o que é fórmula
2. Explica as fórmulas complexas (as que têm cell comment E as que não têm)
3. Marca o que NÃO está documentado mas eu deveria saber pra estender sem quebrar — armadilhas invisíveis

Formato: 
- Seção 1: Mapa das abas em texto (não desenho)
- Seção 2: Cada fórmula complexa numerada, com célula de origem + o que ela faz + por que é assim
- Seção 3: Lista de armadilhas — cada uma com o que quebra se eu ignorar

Limite: Se algo não é claro, marca "🚩 não consegui entender" — prefiro saber que você não sabe do que ler suposição. Não me diga "essa fórmula parece calcular X" — se não tem certeza, marca a incerteza.
```

---

## Prompt 2 · Peça pra anotar a planilha

Depois que o Claude te mostrou o mapa, peça pra ele DEVOLVER a planilha com anotações — não só descrever.

```
Boa. Agora me devolve a planilha com:
1. Cell comments novos nas fórmulas complexas que você identificou (que ainda não tinham)
2. Uma aba nova chamada "Mapa" com o resumo das conexões entre abas
3. Formatação condicional (dá bar de dados) nas colunas de margem e crescimento, pra eu ver a tendência de bater o olho

Preserva TUDO que já está lá — só adiciona.
```

---

## Prompt 3 · Antes de estender, teste sua compreensão

Este passo é o que separa "usar IA como calculadora" de "usar IA pra aprender".

```
Antes de eu estender pra Q3 e Q4, me faz um quiz de 3 perguntas sobre essa planilha. Perguntas que testam se eu entendi mesmo — não decoreba. Perguntas do tipo "se eu mudar a célula X, o que acontece na aba Y?".

Espera minha resposta antes de continuar.
```

Responda. Se errar, o Claude vai explicar. Errar aqui é ouro — é onde você aprende sem quebrar o arquivo real.

---

## Prompt 4 · Estenda com padrão preservado

Agora sim.

```
Estende a planilha adicionando Q3 e Q4 de 2026. Regras:
1. Segue exatamente o padrão que já está lá — mesmas fórmulas, mesmas conexões, mesmo estilo de nome
2. Mantém a lógica de sazonalidade que existe entre trimestres
3. Nas células novas que têm fórmula complexa, adiciona comment explicando (mesmo padrão dos comments que já existem)
4. Se tiver que tomar alguma decisão de forecast, me pergunta antes — não assume

Me devolve a planilha estendida.
```

---

## Prompt 5 · Transfira pro Cowork · valide num par de olhos

Se você quer usar Cowork pra abrir a planilha lado a lado e navegar clicando:

```
Abre a planilha nova. Vou apontar uma célula do Q3 que eu quero entender melhor. Me explica o que ela puxa e por quê, em texto simples que eu poderia contar pra meu chefe.
```

---

## Checklist antes de fechar

- [ ] Você entende como as abas se conectam (consegue desenhar num guardanapo)
- [ ] Você sabe pelo menos 1 armadilha da planilha que não estava documentada
- [ ] Você acertou o quiz (se errou, entendeu por quê)
- [ ] A versão estendida abre no Excel/Sheets sem erro de fórmula
- [ ] Você guardou a versão original antes de sobrescrever

---

## Truques

**Nunca sobrescreva o original.** Salve como `planilha-Q3-Q4-v1.xlsx`. Se algo quebrar, você volta.

**Peça pra IA marcar o que ela NÃO entendeu.** É o oposto do reflexo dela. Ela quer entregar. Você quer saber onde ela chutou.

**Faça o quiz.** Mesmo que pareça bobo. É o momento em que você aprende a planilha, não só a lê.

**Cell comments valem ouro em planilhas herdadas.** Quem herdar depois vai agradecer — inclusive você daqui a 6 meses quando esquecer.

---

*Base: adaptação de [Understand and extend an inherited spreadsheet · Anthropic](https://claude.com/resources/use-cases/understand-and-extend-an-inherited-spreadsheet). Curadoria: Rafael Lima · Mentoria IA Executiva.*
