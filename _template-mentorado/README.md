# Template Mentorado

Clone-base pra criar um novo mentorado no monorepo.

## Como criar um novo mentorado

1. **Duplicar esta pasta** com o slug do mentorado:
   ```bash
   cp -r _template-mentorado/ <slug-do-mentorado>/
   ```

2. **Editar `index.html`**: substituir `{{Mentorado}}` pelo nome dela/dele em todos os arquivos. Macete:
   ```bash
   find <slug-do-mentorado>/ -name "*.html" -exec sed -i '' 's/{{Mentorado}}/Nome Completo/g' {} +
   ```

3. **Adaptar M1–M4** conforme o perfil e nível do mentorado (veja `00-perfil.md` no vault).

4. **Criar banco de prompts custom** em `banco-de-prompts/` mapeado às áreas de desejo do mentorado.

5. **Manter privacidade**: `<meta name="robots" content="noindex, nofollow">` em todas as páginas. Não publicar links em redes sociais.

6. **Atualizar `00-pagina-mentorado.md`** no vault com o estado da página.

7. **Convenção de commit**: `sessao-N: <descrição>`, `prompt: <novo prompt>`, `caso: <caso novo>`, `chore: <ajuste técnico>`.

## Estrutura

```
_template-mentorado/
├── index.html                     # home do mentorado
├── m1-fundamentos/index.html      # adaptado do workshop GPS
├── m2-delegacao/index.html        # adaptado
├── m3-ipo/index.html              # adaptado
├── m4-prompts/index.html          # adaptado
├── banco-de-prompts/index.html    # 100% custom
├── sessoes/                       # uma página por sessão (s1.html, s2.html...)
└── README.md                      # este arquivo
```

## Princípios

- **Casos pessoais** (dados sensíveis, planilhas reais) NÃO entram na página estática — resolvem-se AO VIVO na sessão com Claude
- **Página cresce sessão a sessão** — banco expande, casos aparecem, biblioteca vira página
- **Design system compartilhado** em `_shared/` — não duplicar CSS por mentorado
