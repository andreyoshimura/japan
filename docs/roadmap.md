# Roadmap

Documento vivo. Atualizado em 2026-09-19.

O roadmap é organizado por **fases do funil**, não por trimestres: cada fase só
faz sentido se a anterior estiver funcionando. A ordem importa mais que a data.

---

## Fase 0 — Base do repositório *(em andamento)*

Objetivo: ter um lugar único e versionado para ferramentas, conteúdo e decisões.

- [x] Estrutura de pastas e documentação de estratégia
- [ ] Calculadoras HTML existentes movidas para `tools/`
- [ ] Publicação estática das calculadoras (GitHub Pages ou hospedagem própria)
- [ ] Domínio definido e apontado

## Fase 1 — Isca funcionando

Objetivo: uma calculadora pública que resolva um problema real sozinha, mesmo
para quem nunca deixar o contato.

- [ ] `calculadora-hora-extra-japao.html` publicada e revisada quanto à lei vigente
- [ ] `calculadora-gastos-japao.html` publicada
- [ ] **Calculadora de câmbio iene↔real** (a construir/portar) — comparação entre
      banco tradicional e câmbio comercial justo
- [ ] Aviso de afiliado visível em todas as calculadoras
- [ ] Versão mobile verificada (o público acessa majoritariamente pelo celular)

## Fase 2 — Captura e automação

Objetivo: transformar uso da ferramenta em lista própria.

- [ ] Formulário de captura (e-mail e/ou WhatsApp) integrado às calculadoras
- [ ] Workflow n8n de captura → normalização → armazenamento
- [ ] Política de privacidade e consentimento explícito (LGPD + APPI japonesa)
- [ ] Double opt-in e caminho de descadastro em um clique

## Fase 3 — Conteúdo e sequência de e-mails

Objetivo: entregar valor antes de qualquer CTA comercial.

- [ ] E-book "Como brasileiros no Japão podem guardar dinheiro" — estrutura por capítulo
- [ ] Sequência de boas-vindas (educativa, sem oferta nas primeiras mensagens)
- [ ] Sequência específica de remessa, com comparação de custos verificável
- [ ] Revisão humana obrigatória de todo texto apoiado em IA (ver diretrizes éticas)

## Fase 4 — Monetização ativa

Objetivo: converter confiança acumulada, sem queimá-la.

- [ ] Programa de afiliado de remessa aprovado e link ativo
- [ ] Rakuten Affiliate / Amazon Associados em conteúdo de apoio
- [ ] Camada Mercari: código de convite + guia de segurança
- [ ] Painel simples de acompanhamento (tráfego → leads → cliques → conversões)

## Fase 5 — Tráfego orgânico sustentado

- [ ] Artigos de blog para as buscas de maior intenção (remessa, zangyo, nenkin)
- [ ] Conteúdo em vídeo curto reaproveitando as calculadoras
- [ ] Presença em comunidades regionais (Hamamatsu, Toyota, Nagoya) sem spam

---

## Vertical de alta prioridade para o futuro: aposentadoria / previdência

Existe **acordo bilateral Brasil–Japão de previdência social, em vigor desde 2012**,
que permite somar tempo de contribuição (INSS + Nenkin) para fins de aposentadoria.

O problema: muitos brasileiros pedem o **resgate parcial (Dattai Ichiji-kin)** ao
deixar o Japão sem saber que isso **encerra o vínculo de forma irreversível** para
o período resgatado — trocando anos de contribuição por um pagamento único.

Por que é prioridade:

- Impacto alto e permanente na vida da pessoa (decisão sem volta)
- Concorrência baixa de conteúdo acessível em português sobre o tema
- Alinhamento perfeito com a tese do projeto: informação que economiza dinheiro
- Conecta com o contexto de visto (histórico fiscal e contributivo regular)

O que é preciso antes de publicar:

- [ ] Levantamento das fontes oficiais (acordo, Japan Pension Service, INSS/Gov.br)
- [ ] Revisão por alguém com conhecimento previdenciário — o tema admite erro caro
- [ ] Delimitação clara de escopo: o conteúdo **informa**, não presta consultoria
- [ ] Simulador de decisão (resgatar vs. manter) apenas depois das fontes fechadas

## Versão 2 — Assistente de suporte via IA

Assistente para ajudar no cadastro em fintechs de remessa, implantado em 3 fases:

1. **FAQ fixo** — respostas escritas e revisadas por humano, sem geração dinâmica
2. **IA dinâmica** — respostas geradas com base restrita ao conteúdo aprovado
3. **Suporte humano monitorado** — escalonamento para pessoa, com registro

**Regra de segurança inegociável:** o assistente **nunca pede, recebe ou armazena
documentos de identidade do usuário** (zairyu card, passaporte, CPF, my number,
comprovantes). Se o usuário enviar mesmo assim, o conteúdo é descartado sem
persistência e o usuário é orientado a nunca reenviar. Essa regra vale em todas as
três fases e não depende de configuração — ela é parte do projeto do sistema.

## Fora de escopo (por decisão, não por falta de tempo)

Marketplace próprio, app de emprego e criptomoedas como pilar.
Justificativas em [verticais-avaliadas.md](verticais-avaliadas.md).
