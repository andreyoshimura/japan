# tools/ — calculadoras

Esta pasta contém as calculadoras HTML que funcionam como **isca principal** do funil.
Especificação de cada uma em [`docs/ferramentas.md`](../docs/ferramentas.md).

## Onde colocar os arquivos que você já tem

Coloque os dois HTMLs prontos **direto nesta pasta**, na raiz de `tools/`:

```
tools/
├── calculadora-hora-extra-japao.html   ← coloque aqui
├── calculadora-gastos-japao.html       ← coloque aqui
├── calculadora-cambio-iene-real.html   ← a construir/portar
├── index.html                          ← (opcional) página que lista as calculadoras
└── assets/
    ├── css/    ← estilos compartilhados, quando houver
    ├── js/     ← funções compartilhadas (formatação de iene, gráfico de barra)
    └── img/
```

Pelo terminal, a partir da raiz do repositório:

```bash
cp /caminho/para/calculadora-hora-extra-japao.html tools/
cp /caminho/para/calculadora-gastos-japao.html     tools/
git add tools/ && git commit -m "Adiciona calculadoras de hora extra e de gastos"
```

Mantenha os nomes de arquivo como estão — eles já estão referenciados na documentação
e viram URL pública (`/tools/calculadora-hora-extra-japao.html`).

## Convenções

- **Nomenclatura:** `calculadora-<assunto>-japao.html`, minúsculas, hífens, sem acento
- **Arquivo único:** HTML/CSS/JS no mesmo arquivo enquanto não houver duplicação real.
  Só extraia para `assets/` quando o mesmo código existir em duas calculadoras.
- **Sem build, sem framework, sem dependência externa em runtime** — o arquivo precisa
  abrir direto no navegador e continuar funcionando com conexão ruim
- **Mobile-first** — o público acessa pelo celular
- **Nenhum dado sai do navegador.** Todo cálculo é local; não enviar valores salariais
  para servidor nenhum
- Afirmação legal na página ⇒ **fonte linkada** ao lado
- Link de afiliado na página ⇒ **aviso de afiliado visível** na mesma tela

## Testar localmente

```bash
python3 -m http.server 8000
# abre http://localhost:8000/tools/
```

## Ao adicionar uma calculadora nova

1. Arquivo aqui, seguindo a nomenclatura
2. Seção em [`docs/ferramentas.md`](../docs/ferramentas.md)
3. Entrada no [`CHANGELOG.md`](../CHANGELOG.md)
4. Checklist de [`docs/diretrizes-eticas.md`](../docs/diretrizes-eticas.md) antes de publicar
