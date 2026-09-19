# automations/ — n8n e integrações

Automação do funil: captura de contato nas calculadoras → normalização → base de leads
→ sequência de e-mails.

```
automations/
└── n8n/
    ├── workflows/            ← exports .json dos fluxos (versionados)
    │   ├── captura-lead-calculadora.json   (a criar)
    │   ├── sequencia-boas-vindas.json      (a criar)
    │   └── sincroniza-base-leads.json      (a criar)
    └── credenciais-exemplo/  ← .env.example e templates SEM segredo real
```

## Regras

- **Nenhuma credencial no repositório.** Exportar workflow do n8n sempre pela opção
  que não inclui credenciais; conferir o JSON antes de commitar.
- `credenciais-exemplo/` guarda apenas nomes de variáveis e formato esperado.
- Todo workflow que toca dado pessoal respeita
  [`docs/diretrizes-eticas.md`](../docs/diretrizes-eticas.md): consentimento explícito,
  finalidade declarada, descadastro em um clique, nenhum documento de identidade.
- Nome do arquivo = nome do workflow no n8n, em kebab-case.
- Mudança relevante de fluxo → entrada no [`CHANGELOG.md`](../CHANGELOG.md).

## Fluxos previstos

| Workflow | O que faz | Estado |
|---|---|---|
| `captura-lead-calculadora` | Recebe webhook da calculadora, valida, grava lead | a criar |
| `sequencia-boas-vindas` | Dispara a sequência educativa pós-cadastro | a criar |
| `sincroniza-base-leads` | Mantém a base consistente e processa descadastros | a criar |
