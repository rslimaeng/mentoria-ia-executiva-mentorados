# Design Tokens — Mentoria IA Executiva (mentorados)

> Referência rápida do design system reaproveitado do workshop GPS. Tokens em variáveis CSS (definidas em `style.css`).
> Anti-padrões e princípios visuais ao final.

## Paleta

| Token | Valor | Uso |
|---|---|---|
| `--bg` | `#fafaf7` | Fundo padrão (cream quase-branco) |
| `--bg-warm` | `#f4f1ea` | Fundo alternado, headers de tabela |
| `--bg-card` | `#ffffff` | Cards e blocos isolados |
| `--ink` | `#1f1d1a` | Texto principal (quase-preto quente) |
| `--ink-soft` | `#5a5247` | Texto secundário |
| `--ink-muted` | `#8f8678` | Texto sutil, captions |
| `--accent` | `#2c5f70` | **Teal** — cor primária |
| `--accent-dark` | `#1d4250` | Teal escuro (hover) |
| `--accent-warm` | `#c2916b` | **Terracota** — destaque |
| `--accent-warm-dark` | `#8f6a4d` | Terracota escuro (eyebrows) |
| `--border` | `#e6dfd2` | Bordas padrão |
| `--border-strong` | `#d4c8b0` | Bordas presentes (tabelas) |

## Tipografia

| Família | Google Fonts | Uso | Pesos |
|---|---|---|---|
| **Playfair Display** | serif | h1, h2, h3, eyebrow de seção | 400, 600, 700 |
| **Inter** | sans | corpo, labels, UI | 400, 500, 600 |
| **SF Mono** | mono (sistema) | código, números tabulares | — |

Import via Google Fonts:
```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
```

## Componentes

### Eyebrow
Inter 11px UPPERCASE, letter-spacing .2em, terracota-escuro. Marcador de seção/contexto.

### Module Card
Top line teal 3px que escala 0→1 no hover. Shadow sutil. Padding 24-28px.

### Callout
Border-left 3px teal, bg warm, radius 0 6px 6px 0. Padding 18-22px. Title uppercase Inter 12px.

### Tabela
Header bg-warm + Inter 12px UPPERCASE. Zebra stripe no hover. Border-bottom var(--border).

### Scroll reveal
IntersectionObserver + opacity/translateY animation. Em `script.js`.

## Anti-padrões (não fazer)

- ❌ Sem gradients de fundo
- ❌ Sem glassmorphism / backdrop blur exagerado
- ❌ Sem emojis na UI (só na documentação/legends)
- ❌ Sem border-radius 12px+ (perde seriedade)
- ❌ Sem box-shadow uniforme em todos os cards (sombras direcionais)
- ❌ Sem mais de 1 cor de destaque por seção

## Privacidade
- Toda página de mentorado: `<meta name="robots" content="noindex, nofollow">`
- `_shared/robots.txt` com `Disallow: /`
- Index raiz vazio (área privada)

---

*v1.0 · 2026-06-25 · base extraída do workshop GPS Engenharia*
