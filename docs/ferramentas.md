# Ferramentas (calculadoras)

As calculadoras são a **isca principal** do funil: cada uma resolve um problema
concreto sozinha, sem exigir cadastro. O cadastro é oferecido depois do resultado,
nunca antes.

Arquivos ficam em [`/tools`](../tools/README.md).

---

## 1. Calculadora de hora extra — Zangyo

**Arquivo:** `tools/calculadora-hora-extra-japao.html` · **Estado:** pronta

**O que faz:** calcula os adicionais de hora extra segundo a lei trabalhista
japonesa e **compara com o valor efetivamente pago pela empreiteira**, revelando
diferenças não pagas.

**Por que funciona como isca:** o resultado é um número em ienes que a pessoa pode
conferir no próprio holerite. É verificável, pessoal e imediato.

**Base legal (a confirmar e citar na página):** Lei de Normas do Trabalho do Japão
(労働基準法), art. 37 — adicionais sobre o salário-hora base:

| Situação | Adicional legal mínimo |
|---|---|
| Hora extra além da jornada legal (8h/dia, 40h/semana) | +25% |
| Hora extra acima de 60h no mês | +50% |
| Trabalho noturno (22h–5h) | +25% |
| Trabalho em dia de folga legal (休日) | +35% |
| Noturno + hora extra (acumulado) | +50% |

> **Pendência de verificação:** antes da publicação, cada percentual acima deve ser
> conferido na fonte oficial vigente e a página deve linkar essa fonte. A regra de
> +50% acima de 60h/mês passou a valer para pequenas e médias empresas em abril de
> 2023 — confirmar redação atual. Ver [diretrizes-eticas.md](diretrizes-eticas.md).

**Pontos de atenção de produto:**

- O público trabalha via empreiteira (派遣/請負); o salário-hora base nem sempre é
  óbvio no holerite. A interface precisa explicar **onde olhar**.
- A calculadora aponta uma **diferença**, não uma acusação. O texto de saída deve
  dizer "verifique com a empresa" e não "você está sendo roubado" — inclusive porque
  há casos legítimos de cálculo diferente (jornada variável, acordos 36協定).
- Encaminhamento responsável: mencionar que o órgão competente para reclamação é o
  escritório de inspeção do trabalho (労働基準監督署).

**CTA natural:** e-mail com "o que fazer quando a diferença aparece" → base de leads.

---

## 2. Calculadora de gastos mensais

**Arquivo:** `tools/calculadora-gastos-japao.html` · **Estado:** pronta

**O que faz:** mostra a distribuição do salário entre moradia, alimentação, celular,
carro, lazer e remessa, com **gráfico de barra** e **indicador de sobra real** no
fim do mês.

**Por que funciona como isca:** ataca a lacuna de controle financeiro diretamente.
O "quanto sobra de verdade" costuma ser uma surpresa.

**Pontos de atenção de produto:**

- As categorias refletem o custo de vida real do público (carro é praticamente
  obrigatório fora dos grandes centros; celular e seguro pesam mais do que se espera).
- A saída deve terminar em **uma ação possível**, não em julgamento. Ex.: a categoria
  com maior potencial de corte aponta para o conteúdo correspondente.
- Ponte direta para a calculadora de câmbio: a linha "remessa" é onde a economia
  aparece sem exigir mudança de estilo de vida.

---

## 3. Calculadora de câmbio iene ↔ real *(a construir / portar)*

**Arquivo previsto:** `tools/calculadora-cambio-iene-real.html` · **Estado:** pendente

**O que faz:** compara o custo total de enviar um valor em ienes ao Brasil por
**banco tradicional** versus **câmbio comercial justo**, separando os dois
componentes do custo:

1. **Spread cambial** — diferença entre a taxa aplicada e a taxa comercial
2. **Tarifa fixa** — valor cobrado por operação

A soma dos dois é o custo real. É comum que a opção "sem tarifa" seja a mais cara
por causa do spread — e mostrar isso é o núcleo do valor da ferramenta.

**Requisitos:**

- Entrada: valor em ienes e destino (conta no Brasil)
- Saída: quanto chega em reais em cada opção + diferença em ienes e em reais
- Exibir a taxa de referência usada e **a data/hora** da cotação
- Aviso claro: valores são estimativa; a taxa final é a do momento da operação
- Aviso de afiliado na mesma tela do resultado

**Decisões abertas:**

- Fonte da cotação comercial (API pública vs. valor atualizado manualmente).
  Enquanto não houver fonte automática confiável, usar valor fixo **com data visível**
  é preferível a um número sem procedência.
- Tarifas dos bancos mudam: manter uma tabela de referência versionada neste repo,
  com data de última conferência, em vez de números soltos no HTML.

---

## Padrões comuns a todas as calculadoras

**Técnico**

- HTML/CSS/JS puros, sem build e sem framework — arquivo único abre no navegador
- Mobile-first: o público usa celular
- Sem dependência externa em tempo de execução (evita quebra e rastreamento)
- Todo cálculo roda no navegador; **nenhum dado financeiro é enviado ao servidor**
- Acessível com teclado e legível com fonte grande

**Conteúdo**

- Português simples; termos em japonês sempre com explicação (ex.: "zangyo — hora extra")
- Toda afirmação legal com fonte linkada
- Aviso de afiliado visível onde houver link de afiliado
- Resultado primeiro; oferta de cadastro depois, sem bloquear a ferramenta

**Ao adicionar uma calculadora nova**

1. Arquivo em `tools/`, nomenclatura `calculadora-<assunto>-japao.html`
2. Seção neste documento com objetivo, base factual e pendências
3. Entrada no [CHANGELOG](../CHANGELOG.md)
