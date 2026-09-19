# Renda Extra Japão — projeto de conteúdo e ferramentas para brasileiros dekasseguis

Projeto de renda extra automatizada voltado para brasileiros dekasseguis no Japão,
combinando **conteúdo educativo gratuito** com **afiliados de remessa internacional**.

O repositório reúne as calculadoras interativas (isca principal do funil), a
documentação de estratégia e, futuramente, as automações (n8n), os templates de
e-mail e o conteúdo do e-book.

---

## O problema que o projeto resolve

A comunidade brasileira no Japão ganha bem em iene, mas tem **pouco controle
financeiro** e **desconhece alternativas mais baratas ao Banco do Brasil** para
enviar dinheiro ao Brasil.

Três lacunas concretas:

1. **Remessa cara por hábito.** O Banco do Brasil é usado por confiança e
   familiaridade, não por ser a opção mais barata. A diferença entre o câmbio do
   banco e o câmbio comercial raramente é visível para quem envia.
2. **Falta de visibilidade sobre o próprio salário.** Muitos trabalhadores de
   fábrica não conferem se as horas extras foram pagas segundo a lei japonesa
   (Zangyo) nem sabem para onde vai o salário no fim do mês.
3. **Urgência real de contexto.** As regras de visto no Japão vêm ficando mais
   rígidas (renda, idioma, histórico fiscal), o que torna organização financeira
   e regularidade fiscal um assunto prático, não teórico.

> Nota de conteúdo: essa urgência é **real e documentável**, e é exatamente por
> isso que ela nunca deve ser inflada. Ver [Diretrizes éticas](docs/diretrizes-eticas.md).

## Público-alvo

| Dimensão | Perfil |
|---|---|
| Quem | Brasileiros dekasseguis no Japão, majoritariamente trabalhadores de fábrica |
| Idade | 25–45 anos |
| Onde | Região de Tokai (Aichi, Shizuoka, Mie) — sobretudo Hamamatsu, Toyota e Nagoya |
| Comportamento | ~68% enviam dinheiro ao Brasil regularmente *(dado a confirmar com fonte citável)* |
| Barreira | Usam o Banco do Brasil por hábito/confiança, não por custo |
| Sensibilidade | Público frequentemente alvo de golpes — desconfia (com razão) de pressão comercial |

## Como o projeto funciona (funil)

```
Tráfego orgânico
      │
      ▼
Calculadora interativa  ← isca principal (/tools)
      │
      ▼
Captura de contato via n8n (e-mail / WhatsApp)
      │
      ▼
Sequência automatizada de e-mails
(conteúdo apoiado em IA, baseado no e-book
 "Como brasileiros no Japão podem guardar dinheiro")
      │
      ▼
CTA de afiliado  →  Conversão
      │
      ▼
Base de leads (ativo de longo prazo)
```

O ativo que importa no longo prazo é a **base de leads**, não a conversão pontual.
Cada decisão de conteúdo é avaliada por: *isso aumenta a confiança da lista?*

## Estrutura do repositório

```
.
├── README.md                  ← este arquivo
├── CHANGELOG.md               ← o que já existe vs. próximo passo
├── docs/                      ← estratégia e decisões
│   ├── roadmap.md
│   ├── monetizacao.md
│   ├── ferramentas.md
│   ├── verticais-avaliadas.md
│   └── diretrizes-eticas.md
├── tools/                     ← calculadoras HTML (as iscas do funil)
│   ├── README.md
│   └── assets/                ← CSS/JS/ícones compartilhados entre calculadoras
├── automations/
│   └── n8n/
│       ├── workflows/         ← exports .json dos fluxos do n8n
│       └── credenciais-exemplo/
├── content/
│   ├── ebook/                 ← manuscrito do e-book, por capítulo
│   ├── emails/sequencias/     ← templates das sequências de e-mail
│   └── blog/                  ← artigos de tráfego orgânico
└── assets/img/                ← imagens de apoio (diagramas, capturas)
```

Onde colocar as calculadoras que já estão prontas: **[`tools/`](tools/README.md)**
(instruções de nomenclatura no README daquela pasta).

## Documentação

- [Roadmap](docs/roadmap.md) — fases, estado atual e próximos passos
- [Monetização](docs/monetizacao.md) — fontes de receita por prioridade
- [Ferramentas](docs/ferramentas.md) — especificação de cada calculadora
- [Verticais avaliadas](docs/verticais-avaliadas.md) — o que foi descartado e por quê
- [Diretrizes éticas](docs/diretrizes-eticas.md) — regras inegociáveis de conteúdo

## Transparência

Este projeto usa **links de afiliado**. Isso é declarado de forma visível em toda
página, e-mail e ferramenta que os contenha — nunca em letra miúda. Nenhum conteúdo
educativo é condicionado ao uso de um link. Ver [Diretrizes éticas](docs/diretrizes-eticas.md).

## Status

Em construção. Estado detalhado no [CHANGELOG](CHANGELOG.md).
