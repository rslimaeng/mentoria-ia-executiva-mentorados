# Framework IPO — Input → Process → Output

> **Origem:** curso *Gestão com IA — O guia da Jornada*, de **Adriano Couto** (Couto Performance),
> `M3 ➔ Agentes Departamentais (Custom GPTs) / Aula 2 – Mapeando Seu Processo de Negócio`.
> Dele vêm o modelo IPO, a coluna **Exceção** e a regra dos **4–7 passos**.
> Verificado no material em 2026-08-30 · leitura em `4-ativo-pedagogico/notas/couto--gestao-com-ia.md`.
> *(Registro anterior creditava o AI Radar — estava errado.)*
> **Última sincronização:** 2026-08-31 (populado)

---

## A ideia

Todo trabalho (planilha, relatório, decisão, conversa) é uma máquina simples:

```
INPUT → PROCESS → OUTPUT
```

- **Input:** o que entra (dados, ferramentas, pessoas, restrições)
- **Process:** o que acontece com o input (regras, fórmulas, validações, decisões)
- **Output:** o que sai (planilha pronta, recomendação, mensagem, ação)

Antes de pedir pra IA fazer algo, você declara os 3 explicitamente. A clareza do prompt nasce da clareza do IPO.

**IPO é framework de trabalho, não padrão de prompt.** Ele diz *como pensar o processo*.
Quem diz *como escrever o pedido* é o [[pctfl]]. A ordem entre os dois importa e é
sempre a mesma: **primeiro o IPO, depois o PCTFL.** Quem inverte escreve um prompt bem
estruturado sobre um processo que ninguém abriu.

## Exemplo prático

**Tarefa:** atualizar planilha de gastos da banda a partir do extrato bancário.

| Eixo | Conteúdo |
|---|---|
| **Input** | Print do extrato do banco (últimos 7 dias) + planilha atual (Excel) |
| **Process** | Identificar entradas e saídas, classificar por categoria (caché, transporte, equipamento, obrigações), atualizar saldo |
| **Output** | Planilha atualizada com linhas novas + saldo recalculado + 1 frase de resumo |

## Por que importa

- Evita prompts vagos ("organiza isso aqui")
- Força a pensar o que você espera ANTES de pedir
- Reduz retrabalho (sai certo na 1ª tentativa)
- É reutilizável (mesmo IPO, dados novos)

---

## A tabela completa: seis campos, não três

Os três eixos são o nome do modelo. A tabela que se preenche na prática tem **seis
colunas**, e as três que faltam são as que separam um mapa que funciona de um desenho
bonito.

| Campo | O que colocar | O erro comum |
|---|---|---|
| **Área** | O nome específico do processo: "triagem de currículo para vaga operacional" | Só o setor. "RH" e "Financeiro" não são processos, são endereços |
| **Input** | O que aciona **e o formato exato** dos dados que chegam | "Uma solicitação". Solicitação como? E-mail, formulário, mensagem no grupo? O formato muda tudo |
| **Process** | **4 a 7 passos**, cada um com verbo **e critério de decisão** | Passo vago: "aprovar", "verificar", "analisar". Sem critério, a IA inventa um razoável |
| **Output** | O formato final **e o destinatário** | "Uma resposta". Resposta para quem, em que formato, entregue onde? |
| **Exceção** | A regra de escape para o que sai do fluxo normal | Deixar vazio. É o campo mais esquecido e o que mais custa: sem ele, a primeira situação inesperada trava ou inventa |
| **Recursos** | Dados, arquivos e acessos que o processo exige | Listar sistema que não tem acesso disponível. Recurso que você não consegue entregar não é recurso, é bloqueio |

### A regra dos 4 a 7 passos

Do curso do Couto: **use de 4 a 7 passos; se passar disso, divida em subprocessos.**

Não é estética. Abaixo de 4, o processo não foi aberto — continua sendo uma caixa preta
com nome novo. Acima de 7, ele deixa de ser um processo e vira dois ou três colados, e o
mapa passa a esconder exatamente as fronteiras onde as coisas quebram.

Quando um processo insiste em ter doze passos, quase sempre há uma **troca de dono** no
meio dele: o passo 6 é a entrega para outra pessoa. Esse é o corte natural.

### A coluna Exceção é o diferencial, e ela é do curso

**Crédito:** a coluna `Exceção` vem do material do Couto (`M3`). Ela chegou a ser
registrada no acervo como diferencial autoral contra o AI Canvas da StartSe — **é
diferencial, e não é nosso.**

O que ela resolve: todo processo real tem o caso que não estava previsto. Sem regra de
escape declarada, a IA faz uma de duas coisas, e as duas são ruins: trava, ou inventa uma
saída plausível que ninguém autorizou.

Exemplos de exceção bem escrita:

- "Se o cargo não estiver na tabela → responder *'cargo não previsto'* e parar"
- "Se o campo obrigatório vier vazio → solicitar reenvio, não estimar"
- "Se não houver resposta em 24h → escalar para o gestor da área"

O padrão das três: **condição observável → ação única.** Exceção que diz "usar bom senso"
não é exceção.

---

## O princípio crítico: verbo + critério

É o que separa o mapa que a IA executa do mapa que ela reinterpreta a cada vez.

| ❌ Intenção vaga | ✅ Instrução com critério |
|---|---|
| "Verificar currículo" | "Se o candidato atende os 3 requisitos não negociáveis → entrevistar; se atende parcialmente → segunda rodada; se não → arquivar" |
| "Aprovar a despesa" | "Se estiver abaixo de R$ 2.000 e tiver nota → aprovar; acima disso → encaminhar ao gestor" |
| "Classificar o chamado" | "Se citar sistema fora do ar → urgente; se citar dúvida de uso → normal; se não der para classificar → devolver perguntando" |

**A pergunta que revela o passo vago:** *duas pessoas diferentes, lendo este passo,
fariam a mesma coisa?* Se a resposta é não, o critério está na sua cabeça e não no papel
— e a IA vai preencher com o critério dela.

---

## Casos por área

### Gestão · resposta a chamado interno

| Campo | Conteúdo |
|---|---|
| **Área** | Triagem e resposta a chamado de suporte administrativo |
| **Input** | E-mail na caixa compartilhada, texto livre, com ou sem anexo |
| **Process** | 1. Classificar (urgente / normal / dúvida) pelo critério da tabela · 2. Se urgente → localizar o responsável na escala da semana · 3. Redigir a resposta usando o modelo da categoria · 4. Registrar número do chamado na planilha · 5. Confirmar envio |
| **Output** | E-mail respondido no tom formal, com número do chamado no assunto, para quem abriu |
| **Exceção** | Se o e-mail citar cliente externo → não responder, encaminhar ao comercial |
| **Recursos** | Tabela de critérios, escala da semana, modelos por categoria |

### Finanças · fechamento mensal simples

| Campo | Conteúdo |
|---|---|
| **Área** | Fechamento mensal de caixa de uma operação com dois sócios |
| **Input** | Extrato bancário do mês (PDF) e planilha de lançamentos (Excel) |
| **Process** | 1. Conferir se todo lançamento do extrato existe na planilha · 2. Classificar o que faltar pelo plano de contas · 3. Recalcular saldo · 4. Apontar as duas linhas de maior variação contra o mês anterior · 5. Escrever uma frase por linha apontada |
| **Output** | Planilha atualizada e um resumo de uma página, para o sócio que não lê demonstrativo |
| **Exceção** | Se um lançamento não couber em nenhuma conta do plano → listar em "a classificar" e não forçar categoria |
| **Recursos** | Plano de contas, planilha do mês anterior |

---

## Exercício · abra um processo seu

Escolha um processo que você repete **toda semana** e preencha os seis campos. Vale mais
um processo pequeno e completo do que um grande pela metade.

1. **Nomeie a área** com o processo, não com o setor. Se você escreveu uma palavra só, ainda não é o nome.
2. **Descreva o input pelo formato**, não pelo assunto. "Planilha exportada do sistema, uma aba, cabeçalho na linha 3" é input; "os dados de venda" não é.
3. **Escreva de 4 a 7 passos.** Cada um com verbo e critério. Se passar de 7, corte onde o dono muda.
4. **Diga o output e o destinatário.** Sem destinatário, o formato não tem como ser decidido.
5. **Escreva uma exceção real.** Lembre da última vez que o processo travou: aquilo é a exceção.
6. **Liste os recursos que você consegue entregar hoje.** O que depende de acesso que você não tem vira um passo separado de "conseguir acesso", e não entra neste mapa.

**Está bom quando** outra pessoa da sua área consegue executar o processo lendo só a
tabela, sem te perguntar nada. Esse é o mesmo teste que a IA aplica: ela não pergunta, ela
preenche.

### Se travar

- **Não sei qual processo escolher** → o que você fez na segunda passada e também tinha feito na segunda anterior.
- **Meu processo tem só dois passos** → provavelmente você descreveu o resultado, não o caminho. O que acontece entre receber e entregar?
- **Meu processo tem quinze passos** → procure onde a responsabilidade muda de mão. Ali é a fronteira entre dois processos.

**Não conta como processo mapeado:** uma tabela em que a coluna Process diz "analisar os
dados e gerar o relatório". Isso é o nome da caixa preta, escrito dentro dela.

---

## O que fazer com o IPO depois de preenchido

Ele não é o entregável. Ele é o **insumo de três coisas**, e é por isso que vale a hora
gasta:

| Vira | Como |
|---|---|
| **Um prompt bom** | O IPO preenchido tem quase todos os campos do [[pctfl]]: o Input vira o C, o Process vira o T, o Output vira o F, a Exceção vira o L. Falta só o P e o CS |
| **A instrução de um assistente permanente** | Área e Recursos viram a identidade; Process vira o fluxo obrigatório; Exceção e Output viram as diretrizes |
| **A escolha do que entra na base de conhecimento** | Ver o filtro abaixo |

### O filtro do que entra na base

Do curso do Couto (`M3`), para escolher os arquivos que alimentam um assistente:

> **Preciso?** o arquivo aborda exatamente uma etapa do processo mapeado?
> **Suficiente?** sozinho, ele entrega a informação completa?
> **Necessário?** sem ele, a resposta sai errada ou incompleta?
>
> **Só inclua se as três respostas forem sim. Máximo 15 arquivos.**

O que **nunca** entra: e-mail antigo, apresentação longa, documento genérico, e o
"arquivo por garantia" — aquele que você não consegue explicar por que incluiu.

---

## Quando NÃO usar

- **Processo que roda uma vez por ano.** O custo de mapear não volta.
- **Trabalho que é decisão, não fluxo.** Se o valor está no julgamento e não na sequência, o IPO achata justamente o que importa.
- **Processo de outra pessoa, mapeado por você.** Vira palpite com cara de diagnóstico, e chega na mão dela como cobrança. Quem quer o mapa da área pede que cada um faça o seu.
