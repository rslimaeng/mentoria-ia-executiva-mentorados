# Framework PCTFL — Engenharia de Prompts

> Espelhado do workshop GPS (M4) adaptado pra contexto executivo.
>
> **Origem dos campos:** curso *Gestão com IA*, de **Adriano Couto** — `M2 Aula 1` traz os
> **4 Pilares** (PAPEL · CONTEXTO · OBJETIVO · FORMATO); `M2 Aula 2` traz `# RESTRIÇÕES`
> (o **L**) e `**Critérios:** [Como medir sucesso]` (o **CS**), em frameworks separados.
> **A consolidação numa sigla única é do Rafael.** Verificado em 2026-08-30 · ver
> `4-ativo-pedagogico/notas/couto--gestao-com-ia.md`.
> **Última sincronização:** 2026-08-31 (populado)

---

## O que é

PCTFL é um framework de 5 elementos pra estruturar prompts de qualidade. Cada letra é um eixo da clareza.

A versão corrente é **PCTFL+CS** — o sexto campo, **Critério de Sucesso**, é a camada que
separou amador de profissional nas turmas de 2026. Ver a linha CS na tabela.

| Letra | Significado | O que define | Pergunta-âncora |
|---|---|---|---|
| **P** | Papel | Quem a IA está sendo agora | "Atue como…" |
| **C** | Contexto | O cenário, restrições, audiência | "No contexto de…" |
| **T** | Tarefa | O que exatamente fazer | "Faça…" |
| **F** | Formato | Como apresentar a resposta | "Em formato de…" |
| **L** | Limitações | O que evitar / não fazer | "Não inclua… / use no máximo…" |
| **CS** | Critério de Sucesso | Quando a resposta é boa — o que o destinatário faz depois de ler | "Está bom quando…" |

**PCTFL é padrão de prompt, não framework de trabalho.** Ele diz *como escrever o pedido*.
Quem diz *como pensar o problema* é o IPO (ver [[ipo]]) ou os 7 Níveis (ver
[[7-niveis]]). A confusão entre os dois é comum e cara: quem usa PCTFL para pensar acaba
com um prompt lindo sobre a tarefa errada.

## Exemplo simples (executivo)

```
P — Atue como uma chefe de gabinete experiente.
C — Estou organizando um relatório mensal para um vereador
     sobre andamento de projetos em curso.
T — Resuma os 3 projetos descritos abaixo, destacando 
     status, próximos passos e bloqueios.
F — Formato: bullets curtos, 1 parágrafo por projeto, máximo 200 palavras total.
L — Não invente dados que não estão no input. Linguagem 
     formal, sem jargão técnico.
CS — Está bom quando o vereador decide sobre os 3 projetos sem
     precisar abrir os anexos.
```

---

## Campo a campo: o que entra, e o erro que aparece sempre

A tabela abaixo é a régua de correção. Em turma, quase todo prompt que "volta genérico"
tem o defeito numa destas seis linhas — e quase sempre no **C** ou no **CS**.

| Campo | O que colocar | O erro comum |
|---|---|---|
| **P** · Papel | A função **e a experiência** que mudam o vocabulário: "controller de uma rede de 12 lojas" | "Atue como um especialista". Especialista em quê, com quantos anos, falando com quem? Papel genérico não muda nada na resposta |
| **C** · Contexto | O que só você sabe: quem lê, o que já foi decidido, o que não pode mudar | Descrever o **assunto** em vez do **cenário**. Assunto a IA já tem; cenário só você tem |
| **T** · Tarefa | Um **verbo objetivo** e um alvo: "Compare", "Liste", "Reescreva" | "Me ajude com", "veja isso", "melhore". Verbo vago devolve resposta vaga |
| **F** · Formato | A forma exata da saída: quantas seções, que colunas, que tamanho | Deixar em branco e corrigir depois. Formato dito depois é retrabalho; dito antes é instrução |
| **L** · Limitações | O que **não** pode acontecer, incluindo o que fazer com o vazio | Deixar vazio. Campo em branco é lido como "pode tudo", e é onde nasce o número inventado |
| **CS** · Critério de sucesso | O que o **destinatário faz** depois de ler | Escrever um critério sobre o texto ("está bom quando estiver claro") em vez de sobre o efeito |

### O verbo objetivo

Regra do curso do Couto (`M2`), e é a correção mais barata que existe: **troque a palavra
genérica pelo verbo que diz a operação.**

| Em vez de | Escreva |
|---|---|
| "me ajude com" | **Liste** |
| "pense sobre" | **Compare** |
| "fale sobre" | **Resuma** |
| "melhore" | **Reescreva** |
| "o que você acha" | **Analise** |

### O CS é o campo que quase ninguém escreve certo

O erro não é esquecer o campo: é escrevê-lo sobre o **texto** em vez de sobre a **ação**.

| ❌ Critério sobre o texto | ✅ Critério sobre o efeito |
|---|---|
| "Está bom quando estiver claro e bem escrito" | "Está bom quando o gestor decide a prioridade da semana sem abrir a planilha" |
| "Está bom quando cobrir todos os pontos" | "Está bom quando eu consigo enviar sem reescrever nada" |
| "Está bom quando for profissional" | "Está bom quando em 3 idas e voltas o plano sai utilizável. Se gastei mais que 4, faltou contexto no começo" |

O teste: **o critério tem de ser conferível por alguém que não escreveu o prompt.**
"Claro" não é conferível. "Decide sem abrir a planilha" é.

---

## Quando os seis campos, quando três bastam

Prompt completo custa tempo de escrever. A régua de profundidade:

| Situação | Campos | Por quê |
|---|---|---|
| Pergunta de uma vez só, resposta descartável | **T + F** | Escrever os seis para uma pergunta que você lê e joga fora custa mais que a resposta vale |
| Tarefa que você repete, resultado que alguém lê | **P C T F L CS** | É a que vira arquivo guardado. Vale escrever inteiro uma vez |
| Instrução permanente (projeto, assistente) | **P C L CS**, sem T | A tarefa muda a cada uso; o resto é fixo. Ver a peça `.sistema` do padrão de treinamentos |
| Decisão complexa, sem resposta única | **P C CS** + pedido de perspectivas | Aqui a IA não executa, ajuda a pensar. Ver *scaffolding* abaixo |

### Executar × pensar junto

Duas formas de uso, do curso do Couto (`M2`), e elas pedem prompts diferentes:

- **Descarregar a tarefa** — a IA executa o que você já sabe que quer. Tarefa repetitiva,
  análise, redação. É onde o PCTFL completo brilha.
- **Pensar junto** — a IA é parceira para você decidir melhor. Aqui o **T** deixa de ser
  "calcule" e vira "examine sob três perspectivas e aponte onde minha análise pode estar
  enviesada". O **CS** vira o critério da decisão, não do texto.

Quem usa o prompt de executar numa situação de pensar recebe uma resposta segura e inútil.

---

## Anti-padrões

Todos observados em turma, e nenhum é falta de esforço:

| Anti-padrão | Por que acontece | O conserto |
|---|---|---|
| **Prompt que cresce e piora** | A pessoa adiciona **detalhe** sobre o assunto, não **campo** | Corte pela metade e cheque os seis campos. Falta quase sempre C ou F |
| **Papel decorativo** | "Atue como especialista sênior" soa profissional e não muda o vocabulário | O papel só vale se mudar o que a resposta assume que você sabe |
| **Caçar a palavra mágica** | A crença de que existe um termo que destrava | Não existe termo. Existe informação que faltava |
| **Formato descoberto na terceira rodada** | Ninguém pensa no formato antes de ver a resposta errada | O F é o campo mais barato de escrever e o que mais economiza rodada |
| **Copiar o prompt de outra pessoa inteiro** | Funciona uma vez e não repete | O C é o campo que não transfere: o cenário é seu. Copie a estrutura, reescreva o C |
| **Guardar a resposta, não o prompt** | O resultado é o que impressiona | O pedido bom guardado vale mais que a resposta boa recebida |

---

## Validação de clareza: peça a crítica antes da resposta

Técnica do curso do Couto (`M2`), e é a que menos gente usa: **antes de executar, peça
que a IA critique o próprio prompt.** Ela aponta o campo que faltou, e a correção sai
antes de gastar a rodada.

```
Antes de executar, analise se o pedido abaixo está claro e tem
todas as informações necessárias. Se não estiver, diga o que
está faltando e sugira uma versão melhorada.

[cole aqui o seu PCTFL+CS]
```

Funciona melhor com o prompt já estruturado do que com o texto solto: com os seis campos
declarados, ela aponta *qual campo* está fraco, e não "poderia dar mais detalhes".

---

## Exemplos por área

### Gestão · relatório de rotina

```
P — Atue como analista de operações de uma rede com 12 lojas.
C — Segunda de manhã. Quem lê é o gestor da área, que decide o que priorizar
     na semana e não acompanha o dia a dia. O corte de produto descontinuado
     já foi decidido e não volta à discussão.
T — Compare o fechamento desta semana com o da anterior e liste os três
     números que mais mudaram.
F — Uma página. Três números, cada um com a variação e uma frase dizendo
     o que fazer com ele.
L — Sem gráfico (vai impresso em preto e branco). Não reabra o corte de produto.
CS — Está bom quando o gestor escolhe a prioridade da semana lendo só essa
     página, e não pede a planilha.
```

### Pessoas · descrição de vaga

```
P — Atue como uma pessoa de RH que já contratou para esta função antes.
C — Vaga de analista para uma equipe de 4 pessoas que hoje faz o trabalho
     no improviso. Quem lê o anúncio são candidatos de fora da área.
T — Reescreva a descrição abaixo separando o que é requisito real do que é
     desejável.
F — Duas listas nomeadas, no máximo 5 itens cada.
L — Nada de "proatividade" e "dinamismo": só requisito que dê para verificar
     numa entrevista.
CS — Está bom quando eu consigo eliminar um candidato apontando a linha
     exata que ele não cumpre.
```

### Finanças · leitura de número

```
P — Atue como controller acostumado a apresentar para sócio não financeiro.
C — Fechamento do mês de um restaurante com dois sócios. Um deles não lê
     demonstrativo e decide pelo saldo da conta.
T — Analise o resultado abaixo e aponte as duas linhas que explicam a maior
     parte da variação.
F — Duas linhas, cada uma com o número, a variação e a causa provável.
L — Sem sigla contábil. Se faltar dado para explicar uma linha, escreva
     "não consta" em vez de estimar.
CS — Está bom quando o sócio que não lê demonstrativo consegue repetir a
     explicação com as próprias palavras.
```

---

## Quando NÃO usar

- **Quando você não sabe o que quer.** PCTFL estrutura um pedido; ele não descobre o
  pedido. Se você não consegue escrever o T, o problema é anterior: use o [[ipo]] para
  abrir o processo antes.
- **Quando a tarefa decide sobre uma pessoa específica.** Avaliação, desligamento,
  promoção. O prompt bem escrito não torna a tarefa apropriada.
- **Quando você não consegue conferir o resultado.** Resultado que você não confere não é
  resultado, é opinião com boa formatação — e o CS existe justamente para expor isso: se
  você não consegue escrever o critério, escolha outra tarefa.
