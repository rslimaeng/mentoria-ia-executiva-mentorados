---
caso: briefing-matinal
sessao: S4 · Chat + Cowork
ferramenta: Cowork + connectors
tempo: 30-40 min pra montar · 3 min por dia pra rodar
arquivo: nenhum (requer connectors ativos)
---

# Prompt · Briefing matinal cruzando suas fontes

> A ideia é simples: em vez de você abrir 6 abas todo dia de manhã (WhatsApp de trabalho, e-mail, planilhas, agenda, dashboard), o Claude no Cowork abre pra você e te entrega 1 texto priorizado — o que precisa da sua atenção hoje.
>
> Requer setup inicial (30-40 min) porque envolve conectar suas ferramentas. Depois disso, é 3 min por dia.

---

## Antes de começar · setup

Sem esse setup, o resto não funciona.

1. **Baixe o [Claude Desktop](https://claude.com/download)** — o Chat na web não tem Cowork
2. **Instale o [Claude in Chrome](https://claude.com/chrome)** — pra ele conseguir ler abas do navegador (dashboards, sistema interno)
3. **Ative os [connectors](https://claude.com/connectors)** que fazem sentido pra você. Sugestões pra rotina executiva:
   - **Google Drive** — se seus documentos vivem lá
   - **Gmail** — se você quer que ele leia e-mails
   - **Google Calendar** — pra ele saber sua agenda
4. **Abra o Claude Desktop → Cowork** — nova sessão

---

## Prompt inicial (pra usar TODA manhã)

Depois que o setup estiver pronto, esse é o prompt que você cola todo dia de manhã. Adapte à sua rotina.

```
Papel: Você é minha assistente de manhã. Meu tempo de leitura é 5 minutos. Seu trabalho é me entregar 1 texto que responde "o que preciso saber ANTES de qualquer reunião hoje".

Contexto:
- Hoje é [DATA — o Claude puxa automaticamente]
- Minha agenda de hoje: [ele lê do Google Calendar]
- Ferramentas conectadas: [Gmail, Drive, Calendar — o que estiver ativo]

Tarefa: Monta meu briefing de manhã com essa estrutura:

## URGENTE hoje
E-mails ou mensagens dos últimos 15h que:
- Pedem resposta minha antes do fim do dia
- Vieram de [PESSOAS-CHAVE — ex.: prefeito, vereadores, chefe direto]
- Contêm palavra-chave: [prazo, urgente, decisão, orçamento]

## Reuniões de hoje
Pra cada reunião, me dá:
- Título e horário
- Quem participa (só nome e cargo, sem lista longa)
- Documentos anexados ou linkados no convite
- Se tem uma decisão a ser tomada, qual é

## Pendências da semana
- O que eu tinha marcado pra fazer hoje/amanhã e ainda não fechei
- Prazos que vencem nos próximos 3 dias

## Não-urgente mas relevante
- 2-3 e-mails/mensagens que não são urgentes mas eu ia querer saber (contexto, não ação)

Formato: Uma única página. Bullets curtos. Máximo 5 min de leitura. Se algo pedir mais contexto, me dá o link pra clicar.

Limite: Nada de newsletter, promoção, sistema de tarefas ("você tem 3 tarefas pendentes"). Só o que envolve DECISÃO ou RESPOSTA minha.
```

---

## Prompt 2 · Aprofundar num item urgente

Depois do briefing, você geralmente identifica 1-2 itens que precisam mais contexto.

```
Do item [X] em "URGENTE hoje", me traz o histórico completo. Toda a thread de e-mail. Quem já respondeu, o que foi decidido antes, o que ficou em aberto. Se tiver documentos anexados, resume o que dizem em 2 linhas cada.
```

---

## Prompt 3 · Preparar 1 reunião cara-a-cara

Se você tem reunião importante hoje, peça um mini-briefing só pra ela.

```
A reunião das [HORA] com [PESSOA/GRUPO] é a mais importante do dia. Me prepara em 5 min:
1. Contexto — do que se trata (últimos 3 e-mails/mensagens sobre o tema)
2. Posição das partes — quem quer o quê
3. Se tem histórico de decisão prévia, qual foi
4. 3 perguntas que eu deveria fazer
5. 1 risco que eu não quero esquecer de mencionar
```

---

## Prompt 4 · Encerre com "o que salvar pra amanhã"

Antes de fechar, o Claude registra o que ficou solto — pra ele lembrar amanhã.

```
Antes de eu fechar: me lista o que ficou em aberto hoje que eu preciso retomar amanhã. Isso vira o "pendente" do briefing de amanhã.
```

---

## Checklist antes de fechar

- [ ] Briefing cabe em 1 tela (não precisa scrollar muito)
- [ ] Você sabe qual é a decisão mais importante do dia
- [ ] Você tem UM item que vai fechar antes do meio-dia
- [ ] Anotou o que foi útil e o que foi ruído (pra melhorar o prompt amanhã)

---

## Truques

**Ajuste o prompt na 1ª semana.** No 1º dia ele vai errar — trazer coisa demais, coisa de menos, ou coisa que você não pediu. Todo dia, ajuste 1 linha do prompt. Em 7 dias vira ferramenta afiada.

**Palavras-chave são o filtro real.** "Urgente" é subjetivo — cada organização tem palavras que sinalizam urgência: "OSC pediu", "ofício", "cobrança", "recurso", "prazo legal". Liste as suas.

**Cowork não é telepatia — ele lê o que você conectou.** Se um sistema importante fica fora dos connectors, o briefing não vai ver. Isso é limite real da ferramenta.

**Guarde o prompt final num arquivo.** Depois de ajustar por 2 semanas, salve como `briefing-matinal-v1.md` num lugar acessível. Você vai querer reusar.

---

## Se você não tem Claude Desktop ainda

Faça uma versão light no Chat comum: cola 3-4 e-mails importantes no chat + agenda do dia + peça o briefing. É pior que o Cowork automatizado, mas já ajuda a experimentar a mecânica antes de investir no setup.

---

*Base: adaptação de [Build a daily briefing across your tools · Anthropic](https://claude.com/resources/use-cases/build-a-daily-briefing-across-your-tools). Curadoria: Rafael Lima · Mentoria IA Executiva.*
