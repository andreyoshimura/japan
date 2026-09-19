# Changelog

Formato baseado em [Keep a Changelog](https://keepachangelog.com/pt-BR/1.1.0/).
Datas em AAAA-MM-DD.

---

## [Não publicado] — estado atual

### Adicionado

- Estrutura inicial do repositório: `docs/`, `tools/`, `automations/n8n/`, `content/`, `assets/`
- `README.md` — problema, público-alvo, funil e mapa do repositório
- `docs/roadmap.md` — fases 0 a 5, vertical de previdência e escopo da V2
- `docs/monetizacao.md` — Wise, Rakuten/Amazon, camada Mercari e princípios
- `docs/ferramentas.md` — especificação das três calculadoras
- `docs/verticais-avaliadas.md` — decisões de descarte com justificativa
- `docs/diretrizes-eticas.md` — regras de conteúdo e checklist de publicação
- `tools/README.md` — onde colocar os HTMLs e convenções técnicas
- `automations/README.md` e `content/README.md` — convenções das pastas

### Construído fora do repositório (a mover para `tools/`)

- `calculadora-hora-extra-japao.html` — adicionais de zangyo segundo a lei japonesa,
  comparados ao valor pago pela empreiteira
- `calculadora-gastos-japao.html` — distribuição do salário com gráfico de barra e
  indicador de sobra real no fim do mês

### Decidido

- Marketplace próprio: **descartado** (Mercari dominante; Leilão.JP/Loja.jp como caso de estudo)
- App de emprego: **descartado** (mercado saturado + conflito de interesse com a
  calculadora de hora extra)
- Criptomoedas: **não é pilar** (risco reputacional e erro irreversível de transação)
- Mercari tratado como camada de facilitação, não como concorrente
- Previdência (acordo Brasil–Japão / Dattai Ichiji-kin): **aprovada** como vertical
  de alta prioridade futura
- Assistente de IA da V2 nunca pede, recebe ou armazena documento de identidade

---

## Próximos passos

Em ordem de execução:

1. **Mover as calculadoras prontas para `tools/`** e commitar
2. Revisar os percentuais de zangyo na fonte oficial e linkar a fonte na página
3. Construir/portar a **calculadora de câmbio iene ↔ real** (spread + tarifa)
4. Publicar as calculadoras (GitHub Pages ou hospedagem própria) e definir domínio
5. Adicionar aviso de afiliado visível e formulário de captura
6. Criar o workflow n8n `captura-lead-calculadora` + política de privacidade
7. Estruturar os capítulos do e-book em `content/ebook/capitulos/`
8. Escrever a sequência de boas-vindas (educativa, sem oferta nas primeiras mensagens)
9. Ativar o programa de afiliado de remessa
10. Fechar as fontes da vertical de previdência antes de qualquer publicação

### Pendências de verificação factual

Itens que **não vão ao ar** sem fonte citável (ver `docs/diretrizes-eticas.md`):

- 68% da comunidade envia dinheiro ao Brasil regularmente
- Mercari: 40%+ de participação de mercado e ~23 milhões de usuários ativos
- Percentuais de adicional de hora extra (art. 37 da Lei de Normas do Trabalho)
- Vigência e alcance do acordo previdenciário Brasil–Japão
