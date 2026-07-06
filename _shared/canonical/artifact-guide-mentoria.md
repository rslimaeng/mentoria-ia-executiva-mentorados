---
tipo: guia-canonico
uso: instruções pra alimentar prompts que geram Artifacts interativos no Claude.ai
finalidade: cada prompt do eixo termina pedindo Artifact vivo — não relatório estático — no visual do site da mentorada
atualizado: 2026-07-06
---

# Artifact Guide — Ferramentas Vivas para Mentoria IA Executiva

Padrão pra criar Artifacts INTERATIVOS no Claude.ai. Não é relatório estático — é ferramenta operacional. A mentorada digita valor, muda de cor, arrasta card, adiciona linha, imprime resultado.

## Princípio

> **Artifact vivo > Artifact bonito**
> A analise textual dá o raciocínio. O Artifact dá a ferramenta pra ela usar toda semana.

## Bloco pra colar no fim de qualquer prompt

Este é o sufixo padrão. Cada prompt específico substitui `[COMPONENTE_INTERATIVO]` pelo widget certo.

```
---

## Formato de entrega

1. Primeiro entregue a **análise textual completa** — raciocínio, tabelas, insights (do jeito que fez até aqui).
2. Depois **gere um Artifact HTML self-contained** com este perfil:

**Design tokens (obrigatórios — bate com o site da mentoria):**
- Paleta: cream `#fafaf7` (bg), warm `#f4f1ea` (bg-warm), white `#ffffff` (card), ink `#1f1d1a` (texto), teal `#2c5f70` (accent frio), terracota `#c2916b` (accent quente), verde `#5c7d5f` (positivo), amarelo `#c08a2a` (atenção), vermelho `#b54a3a` (crítico)
- Tipografia: Playfair Display (títulos serif) + Inter (corpo sans) via Google Fonts
- Bordas suaves 6-12px, sombras leves, letter-spacing wide em eyebrows uppercase

**Estrutura mínima do Artifact:**
- **Header** com eyebrow (nome do prompt) + título grande serif + subtítulo com contexto + botão "Imprimir" no canto (`window.print()`)
- **Corpo interativo**: [COMPONENTE_INTERATIVO]
- **Footer** pequeno: "Mentoria IA Executiva · Débora Nascimento · gerado com o [nome do Professor]"

**Interatividade (obrigatória):**
- Campos editáveis (input, textarea, contenteditable) onde faz sentido
- Cálculos ao vivo em JavaScript vanilla — sem framework, sem dependência externa
- Estado persistido em `localStorage` (opcional mas recomendado — sobrevive ao reload)
- Impressão A4 amigável com `@media print` (esconde botões, ajusta layout)

**Restrições técnicas:**
- HTML + CSS + JS vanilla no MESMO arquivo (self-contained, sem CDN)
- Sem dependência externa exceto Google Fonts
- Zero React/Vue/framework — Claude.ai renderiza `text/html` puro
- Responsivo (mobile-first, mas otimizado pra desktop)

**Restrições de conteúdo:**
- Zero jargão inventado — use os termos exatos que apareceram na análise textual
- Se algum campo depende de dado que a Débora não tem, deixe placeholder claro + tooltip explicando
```

## Componentes por tipo de artefato

Reference pra escolher `[COMPONENTE_INTERATIVO]` conforme o prompt.

### 1. Matriz 2×2 (SWOT / Impacto×Esforço / etc.)

- 4 quadrantes CSS grid com cor de fundo suave por quadrante
- Cada quadrante tem `<textarea>` ou lista `contenteditable` pra ela editar
- Se for priorização: cards arrastáveis com `draggable="true"` entre quadrantes
- Ícone / eyebrow por quadrante

### 2. Cinco Forças de Porter

- 5 cards em coluna (ou grid 2×3)
- Cada card com: nome da força, campo textarea pra descrição, **radio button Alta/Média/Baixa** que muda cor da borda
- Total: mini-diagnóstico "esta força pesa muito no seu negócio?"

### 3. Fluxo AS-IS (hierarquia PROC>SUBPROC>ATIV)

- Lista aninhada com indentação visual (borda esquerda por nível)
- Cada linha tem botão "+" pra adicionar subitem
- Botão "🚨 marcar como gargalo" que pinta a linha de warning
- Contador ao vivo: X etapas, Y gargalos marcados

### 4. POP (Procedimento Operacional Padrão)

- Documento formato A4 imprimível com 7 blocos obrigatórios em ordem (Objetivo · Escopo · Responsáveis · Materiais · Procedimento · Registros · Referências)
- Cada bloco = `contenteditable` com placeholder guia
- Numeração automática dos passos do Procedimento (JS regenera ao adicionar/remover linhas)
- **Cabeçalho** com nº do POP, versão, data, responsável (campos editáveis)

### 5. Dashboard KPI Semafórico

- Grid de 5 tiles
- Cada tile: nome do KPI + `<input type="number">` pra valor atual + campos verde/amarelo/vermelho + fórmula
- **Cor do tile muda AO VIVO conforme o valor entra em cada faixa**
- Badge Lagging/Leading destacado
- Área "regra de ação por cor" abaixo de cada tile

### 6. Fishbone / Espinha-de-peixe (6 categorias Hosotani)

- SVG horizontal com 6 diagonais (matéria-prima, equipamentos, pessoas, ambiente, procedimentos, informações)
- Cada categoria tem `<ul>` colateral onde ela adiciona causas
- Ao final: tabela ranking das 5 hipóteses mais prováveis com `<select>` de probabilidade Alta/Média/Baixa

### 7. Cinco Porquês (cascata guiada)

- 5 rounds visuais empilhados
- Cada round: pergunta pré-preenchida (baseada na resposta anterior) + `<textarea>` pra resposta
- Botão "Avançar pro próximo Porquê" só habilita quando a resposta tem 20+ chars
- No 5º Porquê: **campo "Contramediada"** destacado

### 8. Plano de Ação 5W2H

- Tabela editável (7 colunas: What / Why / Where / When / Who / How / How much)
- Botão "+ adicionar linha"
- Alerta visual se algum campo estiver vazio (borda vermelha)
- Botão "Copiar como texto" (JSON ou markdown)

## Componentes globais compartilhados

Todos os Artifacts devem ter:

- **Botão flutuante "🖨️ Imprimir"** canto superior direito → `window.print()`
- **`@media print`** que esconde botões, remove sombras, força margens A4
- **Meta viewport** responsivo
- **Google Fonts** carregado no head (Playfair Display + Inter)
- **Rodapé** com marca `Mentoria IA Executiva · Débora Nascimento · 2026`

## Regras de escopo

- Artifact NÃO substitui análise textual. Vem DEPOIS.
- Artifact NÃO decide por ela. É espaço de trabalho.
- Se a análise achou algo que Débora precisa confirmar em campo (dado real, opinião de sócio), o Artifact tem campo pra ela preencher e voltar.

## Como replicar pra outros eixos

Este padrão nasce em Gestão. Pra usar em Finanças, RH, Marketing, n8n:
1. Fork os componentes acima (matriz, tabela, dashboard) — servem em qualquer contexto
2. Adapte paleta se o eixo tiver cor própria (mantendo os tokens do site)
3. Cada prompt do eixo deve especificar QUAL componente interativo esperar
