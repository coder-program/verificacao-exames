# Verificação de Exames

Análises integradas de exames laboratoriais (Junho 2026) — Deleon e Monique.

## Uso local

Abra `index.html` no navegador ou rode um servidor estático:

```bash
python -m http.server 8899
```

Acesse `http://localhost:8899`

## Deploy (Vercel)

1. Importe este repositório na [Vercel](https://vercel.com)
2. Framework: **Other** (site estático)
3. Root: `.` (raiz)

| Rota | Conteúdo |
|------|----------|
| `/` | Seleção Deleon / Monique |
| `/DELEON/` | Análise Deleon (PWA) |
| `/MONIQUE/` | Análise Monique (PWA) |

## PDFs — Monique

Laudos nas pastas (dentro de `MONIQUE/`):

| Pasta | Conteúdo |
|-------|----------|
| `laudos exames ac/` | Laudo AC completo (Lavoisier) |
| `laudos exames imagens/` | US tireoide, mamas e pelve |

A aba **Docs** no site aponta direto para esses arquivos — **não** duplicar em outra pasta.

- **GitHub:** PDFs fora do repo (`.gitignore`).
- **Vercel:** só as duas pastas acima sobem no deploy (`.vercelignore`).

Para publicar laudos novos na Vercel:

```bash
vercel --prod
```

Ou faça deploy pelo painel da Vercel a partir da pasta local (com os PDFs em `MONIQUE/laudos exames ac` e `MONIQUE/laudos exames imagens`).

> Laudos contêm dados sensíveis. Evite repo público com PDFs.
