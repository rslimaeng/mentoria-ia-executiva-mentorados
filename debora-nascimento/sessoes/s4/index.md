# S4 · Conversar com IA de verdade — Chat + intro Cowork

**Sessão 4 · Nova rota Claude · Módulo 1 de 5 · Base de uso**

> Você conheceu os fundamentos (M1-M4) e a ideia de organizar caixa (S3). Agora entra na primeira ferramenta a fundo: **Claude Chat**. E abre a porta pra segunda: **Cowork**. Sair daqui sabendo iniciar, conduzir e recuperar uma conversa produtiva com o Claude — e sabendo em quais casos escolher Chat vs Cowork — é o que destranca todas as próximas sessões.

Esta página HTML (`index.html`) traz o mesmo conteúdo em formato interativo (cards vivos, exemplos com prompt copiável, exercícios com checklist). Este `.md` é a fonte canônica de leitura — imprime em A4, mora no repositório, funciona sozinho.

---

## Contrato do módulo

**Você ganha**
- 1 mental model claro pra decidir Chat vs Cowork sem hesitar
- 1 caso executivo desenvolvido do zero (preparação de entrevista pra vaga gerencial na corretora)
- 3 exercícios prontos pra rodar essa semana (Banda de forró · Restaurante CHR · Gabinete anonimizado)

**Você se compromete com**
- 3 conversas em Chat na semana, uma por cenário, salvando os links
- 1 documento saído do Cowork (transferência de uma conversa pra edição lado-a-lado)
- Reportar de volta na S5: o que fluiu, onde travou

**Tempo**
- Leitura: ~12 min · Sessão ao vivo: 120 min · Casa: ~90 min distribuídos na semana

---

## Onde você está na nova rota

```
● S4 Chat + Cowork    ← você está aqui
○ S5 Artifacts
○ S6 Scheduled Tasks
○ S7 Projects
○ S8 Personalização (Skills · Connectors · Plugins)
```

A ordem é a progressão natural: primeiro aprende a *conversar* (S4). Depois aprende a pedir *entregável estruturado em vez de texto solto* (S5 Artifacts). Depois deixa a IA *trabalhar sem você estar acordada* (S6 Scheduled Tasks). Depois monta *assistentes com contexto persistente* que já sabem quem você é (S7 Projects). E por fim *personaliza* com Skills, Connectors e Plugins (S8).

Cada sessão herda a anterior. Chat é onde tudo começa.

---

## Você entra com · o que acontece · você sai com

| Entra | Acontece | Sai |
|---|---|---|
| Pergunta na cabeça que você não sabe formular em prompt. Vontade de usar Claude no dia a dia mas trava na hora de começar. | Você aprende PCTFL como abertura, faz 5-6 iterações comentadas, discorda do Claude quando ele generaliza, refina, e transfere a conversa pro Cowork pra editar o documento final lado a lado. | 1 documento executável real — no caso ao vivo, 3 perguntas prováveis de entrevista + esboço de resposta pra vaga da corretora. Em casa, 3 conversas salvas e 1 documento saído do Cowork. |

---

## Conceito — Chat × Cowork

### Claude Chat — onde você pensa com a IA

**O que é.** A interface conversacional em `claude.ai` e no app. Uma pergunta, uma resposta, você refina na próxima. Trocas curtas ou longas, sempre em formato de conversa.

**Mental model.** Chat é onde você **pensa com** o Claude. Não é onde você delega.

**Como funciona (5 pontos).**
1. Você abre uma conversa nova — ela nasce vazia, sem memória de conversas anteriores (a menos que você esteja num Project, que vem em S7).
2. Você escreve uma mensagem inicial — quanto mais contexto e limite (o PCTFL do M4), mais útil vem a resposta.
3. O Claude responde e você lê pensando "isso me serve?". Se não serve inteiro, refina — pede a versão B, discorda, adiciona um dado que faltou.
4. Você pode anexar arquivo (PDF, planilha, imagem) que ele analisa dentro da conversa.
5. Ao fim, você tem uma conversa inteira salva. Volta nela quando quiser.

**Use Chat quando**
- Precisa de resposta rápida (1-3 turnos)
- Está iterando, pensando em voz alta, buscando ângulo
- A tarefa termina na resposta — vai copiar o output pra outro lugar
- Anexou 1 arquivo e quer conversar em cima dele

**Não use Chat quando**
- Precisa que a IA edite um documento longo com você iterativamente (aí é Cowork)
- Vai gerar um entregável estruturado que você quer receber pronto (aí é Artifact, S5)
- Quer que rode toda semana automaticamente sem você abrir (aí é Scheduled Task, S6)

**Armadilha comum.** Sair do Chat com texto vago porque você aceitou a primeira resposta. Regra: se a primeira resposta veio genérica, é porque a *sua* pergunta veio genérica. Refina antes de reclamar do Claude.

### Claude Cowork — onde você edita junto com a IA

**O que é.** Um modo de trabalho em que Claude e você editam um documento (ou código, ou análise) lado a lado, no mesmo painel. Você não faz "pergunta e resposta" — você trabalha *dentro* do artefato.

**Mental model.** Cowork é sobre trabalhar *no* documento junto, não sobre conversar melhor.

**Como funciona (5 pontos).**
1. Você abre o Cowork com um documento em branco ou colando texto existente.
2. Peça: "Reescreve este parágrafo em tom mais executivo" — Claude edita o parágrafo *ali*, você vê a mudança na hora.
3. Você discorda, edita você mesma no painel. Ele lê e continua dali.
4. Peça mais transformações — "adiciona um bullet sobre risco cambial", "corta o penúltimo parágrafo".
5. Ao fim, você tem o documento final pronto pra copiar/exportar.

**Use Cowork quando**
- Já tem uma versão base (email longo, POP, JD, relatório) e quer iterar em cima
- Precisa de várias transformações no mesmo texto ao longo de 20-30 min
- Quer ver a edição acontecendo, não descrita numa resposta longa

**Não use Cowork quando**
- Só quer pensar/discutir sem um documento na mesa (aí é Chat)
- Precisa gerar 1 entregável de uma vez em formato estruturado (aí é Artifact, S5)

**Armadilha comum.** Começar direto no Cowork sem antes ter uma versão base ou uma direção clara. Cowork brilha com matéria-prima. Sem matéria-prima, vira Chat mais lento.

### Regra de decisão em 10 segundos

> Pergunta que faço: *"Eu já tenho um documento na mesa que quero mexer?"*
> Se **sim** → Cowork.
> Se **não, quero pensar/decidir** → Chat.

---

## Rafael executa ao vivo — Corretora de Seguros

**Cenário.** A Débora está em transição de carreira e quer preparar-se pra uma entrevista de gerente comercial numa corretora de seguros. Ela nunca trabalhou em corretora. Tem 4 dias até a entrevista. Vamos usar Chat pra levantar as 3 perguntas mais prováveis + Cowork pra montar o esboço de resposta pra cada uma.

**Prompt inicial** (PCTFL — retomada do M4):

> **Papel:** Você é uma head de RH de corretora de seguros de médio porte com 15 anos de experiência conduzindo entrevistas de gerente comercial.
>
> **Contexto:** Vou entrevistar candidata pra gerente comercial. O perfil dela é: gestora administrativa (chefe de gabinete de câmara municipal por 8 anos), pré-1 em IA mas em ascensão. Nunca trabalhou em corretora. Tem visão de gestão de pessoas e processos, mas pouco vocabulário técnico de seguros.
>
> **Tarefa:** Liste as 3 perguntas mais prováveis que vão cair nessa entrevista e a intenção real por trás de cada uma — o que a entrevistadora quer *descobrir* (não o que ela literalmente pergunta).
>
> **Formato:** Tabela markdown 3 linhas. Colunas: Pergunta · Intenção real · O que uma resposta *ruim* revela sobre a candidata.
>
> **Limite:** Nada de perguntas óbvias de "me fale sobre você". Vá pras que separam finalistas.

**Iteração 2** (Claude entregou 3 perguntas boas mas em corretora *grande*, e a nossa é média). Correção:

> Refaz. As 3 perguntas vindas assumiram corretora grande com estrutura comercial madura. A corretora dessa vaga tem 50 funcionários e o gerente comercial responde ao dono. Ajusta.

**Iteração 3** (Uma das perguntas ficou sobre CRM e a Débora não sabe qual CRM eles usam. Reforço:)

> Uma das perguntas assume que ela sabe qual CRM eles usam. Reescreve pressupondo que ela vai pra entrevista *sem* saber o stack técnico deles — pergunta que ela consegue responder mesmo sem essa informação prévia.

**Iteração 4** (Bom. Agora peço a resposta em rascunho:)

> Boa. Agora, pra cada pergunta, esboça 1 resposta em ~4 linhas usando a lente **STAR** (Situação · Tarefa · Ação · Resultado) — mas ancorada na experiência dela de chefe de gabinete. Se faltar dado que só ela sabe, marca `[DÉBORA PREENCHE]`.

**Passagem pro Cowork.** Nesse ponto, o Chat tem 4 mensagens de rica iteração. Copio o output final (tabela + 3 esboços) pro Cowork. Ali, no painel:

> Reescreve o esboço da pergunta 2 em tom mais executivo e menos operacional. Preserva a estrutura STAR mas troca "consegui organizar" por verbos de decisão. E adiciona 1 linha final de "aprendizado que levo pra corretora".

Cowork edita *o esboço da pergunta 2* na hora. Débora lê, discorda de uma frase, edita manualmente ali. Peço mais uma passada nas 3, e o documento final sai pronto pra impressão.

**Output final** (o que sai da mão dela): 1 documento com 3 perguntas + 3 esboços de resposta em formato STAR + gaps marcados `[DÉBORA PREENCHE]` — que ela vai completar com dados reais (números do gabinete, projetos que conduziu).

**O que ela viu acontecer neste caso**
- Como PCTFL abre uma conversa boa desde o primeiro turno
- Como discordar (iteração 2 e 3) faz o Claude corrigir premissa errada
- Quando um caso deixa Chat e entra em Cowork (quando você tem uma base pra iterar dentro)
- Que a IA marca lacunas em vez de inventar dado (`[DÉBORA PREENCHE]`) — anti-alucinação em prática

---

## Você exercita — 3 casos

Cada exercício é feito ao vivo com a Rafael acompanhando. Ela conduz, você digita.

### Exercício 1 — Banda de forró (fácil)

**Cenário.** A banda da família precisa organizar o financeiro do ano que vem. Hoje mora tudo na cabeça de um dos irmãos.

**Objetivo.** Sair com um esboço de estrutura de controle financeiro 2027 — categorias, ritmo de conferência, quem faz o quê.

**Passos.**
1. Abrir Claude Chat, conversa nova
2. Escrever prompt inicial com PCTFL (Papel: sócio financeiro sênior; Contexto: banda de forró familiar com 6 membros, ~R$ 15k/mês em shows; Tarefa: propor estrutura de controle 2027; Formato: 4 blocos)
3. Iterar 3-4 vezes: pedir alternativa, discordar de algo genérico, adicionar dado que faltou
4. Copiar output final pra Cowork e refinar 1 parte

**Como você sabe que deu certo.** Você sai com um documento de 1 página que consegue mostrar pro irmão que hoje cuida do dinheiro e ele topa começar em janeiro. Se ele lê e diz "isso é o que eu já faço mas melhor organizado" — deu certo.

**Prompt-base copiável** (você adapta antes de rodar):

```
Papel: Você é um sócio financeiro sênior que já organizou o caixa
de 5 bandas independentes e 2 pequenos negócios de eventos.

Contexto: Sou parte de uma banda de forró familiar com 6 integrantes.
Hoje o financeiro mora informal na cabeça de 1 irmão. Faturamento
médio ~R$ 15.000/mês, ~4 shows por mês, custos variáveis (transporte,
som, cachê de músicos convidados) que variam muito.

Tarefa: Proponha uma estrutura de controle financeiro pra 2027 em 4
blocos: (1) categorias de entrada e saída, (2) ritmo de conferência
(diário, semanal, mensal), (3) responsabilidades por membro, (4)
indicadores mínimos que a família olha junto no fim do mês.

Formato: Blocos com título + 3-5 bullets curtos por bloco.
Limite: Nada de ERP nem software pago no primeiro ano.
```

### Exercício 2 — Restaurante CHR (médio)

**Cenário.** O caso didático do restaurante CHR (mesmo cenário fictício das sessões S3 Finanças e S4 Gestão publicadas no site). 20 lançamentos do caixa da semana passada precisam ser categorizados pra virar DRE.

**Objetivo.** Sair sabendo pedir categorização estruturada em Chat e transferir pro Cowork pra ajustar linha a linha.

**Passos.**
1. Abrir Claude Chat, colar os 20 lançamentos (formato: data, descrição, valor)
2. Prompt: "Categoriza esses lançamentos em Receita (dividida por origem), Custos Variáveis, Custos Fixos, Despesas Operacionais. Formato: tabela markdown."
3. Discordar de 2-3 categorizações que ficaram estranhas (ex.: "aluguel de fritadeira" — é fixo ou variável?)
4. Transferir a tabela pro Cowork e editar as linhas discordantes ali

**Como você sabe que deu certo.** Você sai com a tabela final de 20 linhas categorizadas, 100% revisadas por você (não deixou nenhuma "ok" sem olhar), e consegue explicar em 30 segundos por que 3 delas ficaram na categoria escolhida.

**Prompt-base copiável** (você cola os 20 lançamentos onde tem `[COLAR AQUI]`):

```
Papel: Você é um controller com experiência em restaurantes de pequeno
porte que já ajudou 20+ operações a organizarem DRE mensal.

Contexto: Vou colar 20 lançamentos do caixa da semana passada de um
restaurante fictício de treinamento (CHR). O restaurante tem ~40 lugares
e ticket médio ~R$ 65.

Tarefa: Categorize CADA lançamento em 1 de 4 grupos: Receita (subdivida
por: salão, delivery, evento fechado), Custos Variáveis, Custos Fixos,
Despesas Operacionais. Quando uma linha for ambígua, marque `⚠️`
e explique em 1 linha por que ficou ambígua.

Formato: Tabela markdown. Colunas: Data · Descrição · Valor · Categoria · Nota.

Limite: Não invente lançamentos. Se ficou ambíguo, marque, não chuta.

Lançamentos:
[COLAR AQUI]
```

### Exercício 3 — Gabinete anonimizado (desafio)

**Cenário.** Você teve 3 reuniões chatas na semana no gabinete e sabe que ficaram decisões pendentes que ninguém escreveu. Quer transformar o áudio/nota bruta em uma lista limpa de decisões + responsáveis + prazos.

**Objetivo.** Sair sabendo (a) anonimizar corretamente antes de colar em IA, (b) pedir extração estruturada, (c) usar Cowork pra editar a lista final.

**Passos.**
1. Pegar notas ou transcrição de 1 dessas reuniões
2. **Anonimizar antes** (regra LGPD da mentoria): trocar nomes por `COLABORADOR_A`, `COLABORADOR_B`, etc.; empresa por `[ORGÃO]`; qualquer dado sensível por `[DADO_SENSÍVEL]`
3. Abrir Chat, colar o texto anonimizado, prompt: extrair decisões, responsáveis (usando os pseudônimos), prazos, riscos
4. Discordar de 1 extração que ficou vaga
5. Transferir pro Cowork e refinar 1 decisão em texto executivo pra você mesma se lembrar do porquê

**Como você sabe que deu certo.** Você sai com uma lista limpa de decisões da reunião *sem* dado sensível colado no Claude. Reabre 3 dias depois e entende o que ficou combinado.

**Prompt-base copiável** (você anonimiza *antes* de colar):

```
Papel: Você é uma chefe de gabinete sênior com 15 anos de experiência
transformando reuniões operacionais em atas executivas.

Contexto: Vou colar uma transcrição anonimizada de uma reunião de 45 min
de um órgão público. Nomes e dados sensíveis já foram substituídos por
pseudônimos (COLABORADOR_A, [ORGÃO], [DADO_SENSÍVEL]).

Tarefa: Extraia (1) as 5 decisões mais concretas tomadas, (2) responsável
por cada uma (use os pseudônimos exatamente como aparecem), (3) prazo
explícito ou marcador `⚠️ PRAZO NÃO DEFINIDO`, (4) 3 riscos que ficaram
implícitos e ninguém verbalizou.

Formato: 4 blocos em ordem. Bloco decisões em tabela.

Limite: NÃO invente decisão que não está na transcrição. Se uma coisa
ficou meia-boca, escreve "decisão parcial: [texto]" — não completa.

Transcrição:
[COLAR AQUI TEXTO ANONIMIZADO]
```

---

## Casa da semana

**Mínimo (compromisso da sessão).** 3 conversas em Claude Chat durante a semana, 1 por cenário (Banda, CHR, Gabinete). Salvar os links. Anotar em 1 linha por conversa: *"o que fluiu / o que travou"*.

**Desafio.** 1 das 3 conversas termina em documento saído do Cowork. Salvar o documento final. Reportar na S5: *"a Cowork ajudou ou atrapalhou nesse caso? Por quê?"*.

**Não faz sentido pular a casa.** A S5 (Artifacts) parte do princípio que você já sabe conduzir conversa. Se você não praticou Chat na semana, S5 vai frustrar.

---

## Antes de sair deste módulo

**Reflita 3 minutos.**
1. Das 3 conversas que você planeja fazer, qual é a que você tem *mais* medo de começar? Por quê?
2. Em qual das 3 é mais importante você usar Cowork depois do Chat? Por quê?
3. Se algo na conversa te trouxer dado sensível (nome, número, algo do gabinete), qual seu ritual de anonimização antes de continuar? (Se não tem ritual, esse é o momento de criar.)

**Principais pontos pra levar.**
- Chat = pensar junto. Cowork = editar junto.
- PCTFL não é ritual chato — é o que separa resposta útil de resposta genérica.
- Discordar do Claude quando ele generaliza é parte do trabalho, não falha da IA.
- Anonimizar *antes* de colar. Sempre.

**Ponte pra S5.** Nesta semana você vai perceber que muita coisa boa da conversa sai como *texto solto* — bom pra ler, ruim pra reusar. Na S5 você aprende a pedir **Artifacts** — documentos, planilhas, HTMLs — que saem prontos pra usar, em vez de texto pra você reformatar depois.

---

*Mentoria IA Executiva · Débora Nascimento · Sessão 4 · Nova rota Claude*
*Curadoria e condução: Rafael Lima — [@iacomrafael](https://www.instagram.com/iacomrafael/)*
