# Verticais avaliadas

Registro das direções consideradas e **descartadas**, com a justificativa. O objetivo
é evitar que a mesma ideia seja reavaliada do zero daqui a seis meses — e deixar
explícito **o que teria que mudar** para a decisão ser revista.

Formato: contexto → análise → decisão → o que mudaria a decisão.

---

## ❌ Marketplace próprio ("OLX do Japão")

**Contexto:** criar uma plataforma de compra e venda entre brasileiros no Japão.

**Análise:**

- O concorrente histórico **Leilão.JP / Loja.jp** serve como caso de estudo: existiu,
  atendeu a comunidade e não se sustentou como plataforma dominante.
- O mercado hoje é **dominado pelo Mercari**: mais de 40% de participação no
  C2C japonês e cerca de 23 milhões de usuários ativos, empresa de capital aberto.
  *(Números a confirmar com fonte citável antes de qualquer uso público.)*
- Marketplace é negócio de **liquidez**: sem massa crítica dos dois lados, não há
  produto. Competir por liquidez contra um incumbente listado em bolsa exige capital
  e tempo que este projeto não tem.
- O público já está no Mercari. O atrito dele não é falta de plataforma — é **idioma**.

**Decisão:** descartado como produto. O Mercari vira **camada de facilitação**
(código de convite, guia de segurança, futuro assistente de tradução de anúncios),
não alvo de concorrência. Ver [monetizacao.md](monetizacao.md).

**O que mudaria a decisão:** uma retirada do Mercari do segmento, ou uma barreira
regulatória que exclua estrangeiros da plataforma. Nenhum dos dois está no horizonte.

---

## ❌ App de emprego

**Contexto:** aplicativo para conectar brasileiros a vagas em fábricas e empreiteiras.

**Análise:**

- Mercado saturado, com players estabelecidos: **WORK JAPAN**, **JP Empregos**, **JJobs**,
  além das próprias empreiteiras, que já recrutam por conta própria e por indicação.
- O canal real de contratação nesse segmento é **indicação pessoal** e grupos de
  mensagem — não um app.
- Monetização dependeria de vender para empreiteiras, o que colocaria o projeto do
  lado do empregador. Isso **conflita diretamente** com a calculadora de hora extra,
  que existe para proteger o trabalhador. Conflito de interesse estrutural.

**Decisão:** descartado. O conflito de interesse é o motivo mais forte, acima da
saturação de mercado.

**O que mudaria a decisão:** nada no modelo atual. Uma camada de *informação* sobre
direitos trabalhistas (não intermediação de vagas) continua dentro do escopo.

---

## ⚠️ Criptomoedas — não recomendado como pilar

**Contexto:** usar cripto/stablecoins como via de remessa ou como tema de conteúdo.

**Análise:**

- **Risco de erro irreversível:** endereço errado, rede errada ou golpe de suporte
  significam perda total, sem estorno. O público é justamente o que menos pode
  absorver esse tipo de perda.
- **Risco reputacional:** a comunidade é alvo frequente de fraudes financeiras.
  Associar o projeto a cripto entrega ao leitor exatamente o sinal que o faria
  desconfiar — e destruiria o ativo principal, que é a confiança da lista.
- **Complexidade fiscal:** tributação de cripto no Japão e no Brasil é hostil ao
  usuário comum e criaria responsabilidade que o projeto não pode assumir.
- O ganho de custo frente a uma fintech regulada não compensa o risco assumido.

**Decisão:** não é pilar do projeto e não entra no funil de remessa. Conteúdo
**defensivo** ("como reconhecer golpes de investimento em cripto na comunidade") é
aceitável e alinhado com a missão.

**O que mudaria a decisão:** um trilho regulado, com reversibilidade e cobertura
de suporte em português — em outras palavras, uma fintech. Que é o que já se recomenda.

---

## ✅ Aposentadoria / Previdência — alta prioridade futura

Única vertical avaliada que foi **aprovada** para expansão. Detalhes e pré-requisitos
no [roadmap](roadmap.md#vertical-de-alta-prioridade-para-o-futuro-aposentadoria--previdência).

Resumo: o acordo bilateral Brasil–Japão (em vigor desde 2012) permite somar tempo de
contribuição INSS + Nenkin; muitos pedem o resgate parcial (**Dattai Ichiji-kin**) sem
saber que isso encerra o vínculo de forma irreversível. Impacto alto, concorrência de
conteúdo baixa, e exige revisão especializada antes de publicar.

---

## Critérios usados na avaliação

Toda vertical nova é testada contra estas cinco perguntas:

1. **Resolve uma dor que o público já sente?** (não uma que precisa ser criada)
2. **Dá para competir?** (incumbente dominante = não entrar de frente)
3. **Há conflito de interesse com o conteúdo educativo?** (se sim, não entra)
4. **O erro do usuário é reversível?** (se não, o cuidado exigido sobe muito)
5. **Constrói ou consome a confiança da base de leads?**
