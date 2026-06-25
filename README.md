# Mentoria IA Executiva — Mentorados

Repositório monorepo das páginas personalizadas dos mentorados da Mentoria IA Executiva (Rafael Lima).
Cada mentorado tem sua subpasta com material adaptado às áreas de interesse, ao nível de maturidade e aos casos reais discutidos nas sessões.

## Privacidade

Toda página de mentorado usa:
- `<meta name="robots" content="noindex, nofollow">`
- `_shared/robots.txt` com `Disallow: /`
- Index raiz vazio (apenas "área privada")

Links são compartilhados **diretamente** com cada mentorado via WhatsApp/email. Não são publicados em redes sociais. URLs com slug previsível (`/debora-nascimento/`) — privacidade vem da soma de obscurecimento + noindex + casos reais ficarem ao vivo (não na página).

## Estrutura

```
mentoria-ia-executiva-mentorados/
├── _shared/                          # design system + canonical + robots
│   ├── assets/                       # style.css, script.js, design-tokens.md
│   ├── canonical/                    # 7-niveis, pctfl, ipo (espelhados do vault)
│   └── robots.txt
├── _template-mentorado/              # clone-base pra criar novos mentorados
├── <slug-do-mentorado>/              # uma pasta por cliente ativo
├── index.html                        # landing vazia ("área privada")
└── README.md                         # este arquivo
```

## Mentorados ativos

- `debora-nascimento/` — Chefe de Gabinete · 5 áreas de desejo · v1 da mentoria personalizada

## Operação

- Repo conectado ao vault: `/Users/rafaellima/developer/9-meus-produtos/produtos-criados/produto-mentoria-ia-executiva/obsidian-mentoria-ia-executiva/`
- Cada mentorado tem ficha em `04-mentorados/<slug>/` com `00-pagina-mentorado.md` apontando pra subpasta deste repo
- Mudanças no design system (em `_shared/`) propagam automaticamente pra todos os mentorados

## Convenção de commit

| Prefixo | Quando usar |
|---|---|
| `sessao-N:` | Mudanças relacionadas a uma sessão específica |
| `prompt:` | Novo prompt no banco de algum mentorado |
| `caso:` | Caso novo adicionado à biblioteca pessoal |
| `chore:` | Ajuste no design system, estrutura, configuração |
| `novo:` | Início de novo mentorado (criação de pasta) |
