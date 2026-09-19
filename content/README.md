# content/ — e-book, e-mails e artigos

Todo o conteúdo editorial do projeto, em Markdown, versionado.

```
content/
├── ebook/                ← "Como brasileiros no Japão podem guardar dinheiro"
│   └── capitulos/        ← um arquivo por capítulo: 01-nome-do-capitulo.md
├── emails/
│   ├── sequencias/       ← uma pasta por sequência
│   │   ├── boas-vindas/  ← 01-*.md, 02-*.md ... na ordem de envio
│   │   └── remessa/
│   └── snippets/         ← blocos reutilizáveis (rodapé, aviso de afiliado)
└── blog/                 ← artigos de tráfego orgânico
```

## Convenções

- Um arquivo por peça, numerado quando a ordem importa: `01-titulo-curto.md`
- Frontmatter no topo de cada arquivo:

```yaml
---
titulo: Quanto custa de verdade mandar dinheiro pelo banco
status: rascunho        # rascunho | revisao | publicado
revisao_humana: false   # obrigatório ser true antes de publicar
fontes:
  - url: https://exemplo.gov.br/...
    consultado_em: 2026-09-19
---
```

- **Nenhum texto vai ao ar com `revisao_humana: false`.** Vale especialmente para
  conteúdo apoiado em IA.
- Toda afirmação factual entra em `fontes`, com data de consulta.
- Antes de publicar, rodar o checklist de
  [`docs/diretrizes-eticas.md`](../docs/diretrizes-eticas.md).
- E-mail nunca usa assunto enganoso e sempre traz descadastro visível.
