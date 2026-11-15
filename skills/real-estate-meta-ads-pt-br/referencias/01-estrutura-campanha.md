# 01. Estrutura de campanha e funil por degraus de intenção

Ideia adaptada (reescrita) do método de "intent ladder" de skills públicas, traduzida para imóvel. Cada degrau tem **público próprio, mensagem própria e exclusão dos degraus acima**.

## Degraus

| Degrau | Quem é | Mensagem | Objetivo |
|---|---|---|---|
| 0 Frio | Nunca nos viu | Mostrar o imóvel/região com fato (planta, metragem, localização, condição real) | Levar à página/formulário |
| 1 Viu o vídeo (≥ 50%) | Interessou-se | Aprofundar: diferenciais reais, vídeo do local | Levar à página do empreendimento/imóvel |
| 2 Visitou a página | Navegou | Prova (obra, entrega, referências) e convite concreto | Formulário ou WhatsApp |
| 3 Engajou de verdade | ≥ 30 s na página ou 60% de rolagem (evento próprio, ex.: `EngagedVisit`) | Convite direto para falar/visitar | Lead |
| 4 Clicou no WhatsApp/abriu o formulário e não terminou | Quase lead | Facilitar: "tire a dúvida em 2 minutos" | Lead |
| 5 Lead | No seu CRM | **Sai dos anúncios de captação** | Atendimento humano/IA |
| 6 Qualificado → Visita → Proposta → Venda | Funil do CRM | Fora de toda captação (venda fechada nunca vê anúncio do mesmo imóvel) | Medir e devolver à Meta |

Públicos mutuamente exclusivos: quem avança sai do degrau anterior. Quem comprou sai de tudo.

## Divisão de verba (ponto de partida, não dogma)

- Prospecção (0–1): ~65–75% · Reengajamento (2–4): ~15–25% · Fechamento (visita/proposta pendente): ~5–10%.
- Verba pequena demais para três camadas? Começar só com **prospecção + remarketing de visitantes da página**. Não fatiar a verba abaixo do que dá volume mínimo para aprendizado.
- Remarketing parece barato porque pega gente que já ia comprar. **Separar prospecção de remarketing nos relatórios** e não creditar ao remarketing a venda que ele só colheu.

## Funis diferentes (não misturar)

| Tipo | Particularidade |
|---|---|
| Lançamento / na planta | Pode exigir registro ou licença antes de anunciar, conforme o lugar (ver `07-moradia-e-regras-locais.md`); ciclo longo; capta lista de interessados |
| Revenda / pronto | Ciclo mais curto; imóvel específico; estoque muda — pausar o anúncio do imóvel vendido no mesmo dia |
| Locação | Ticket menor, volume alto; qualificação por renda/garantia; métrica própria |
| Captação de proprietário | Público e mensagem outros (quem quer vender/alugar o seu) |

## Convenção de nomes

`<MARCA> | <tipo> | <empreendimento/região> | <objetivo> | <degrau> | AAAA-MM`
Ex.: `ACME | Lançamento | Vila Verde | Lead-Form | D0 | 2026-11`. Mesma lógica em conjunto e anúncio (`<ângulo>_<formato>_v<n>`).

## Objetivo da campanha

- **Leads** (formulário instantâneo do tipo "maior intenção") ou **Mensagens/WhatsApp**. Não usar Tráfego nem Engajamento "porque tem pouca conversão": isso traz quem clica e curte, não quem compra.
- Otimizar pelo **evento mais fundo que ainda tenha volume** (ver `04-rastreamento-crm.md`): em geral *pré-qualificado* no começo, depois *qualificado* ou *visita agendada* quando houver volume; raramente *venda* (a Meta pede ~200 leads/mês e o evento em até 28 dias; venda de imóvel quase nunca cabe). ⚠ conferir os requisitos atuais.
- Posicionamentos: começar no Automático, mas **conferir a Audience Network** (costuma gastar verba com lead ruim); desligar se o relatório mostrar isso.
- Cuidado com o Advantage+ esticando idade/localização além do que o imóvel atende. Conferir o público real alcançado.

## Público

- Raio/bairros do imóvel e a região de quem realmente compra ali; lookalike de **clientes que visitaram/compraram** (não de "todos os leads").
- Lookalike, idade/gênero e público detalhado **não ficam disponíveis** quando a categoria Moradia é declarada (ver `07-moradia-e-regras-locais.md`). Decidir a categoria antes de desenhar a estrutura.
- Evitar o público "ideal" de 1–10 milhões: para imobiliária regional é grande demais.
- Subir lista de clientes do CRM como público exige base legal pelas leis de privacidade que se aplicam a você (ver `07-moradia-e-regras-locais.md`).
- Declarada ou não, **nunca segmentar nem excluir por critério discriminatório** (a política da Meta vale sempre).
- ⚠ conferir: as exclusões de segmentação detalhada foram informadas como removidas pela Meta em jan/2026 — confirmar o estado atual na tela.

## Rotina (anti-mexe-demais)

- **Dia 0:** estrutura, rastreio testado, tudo pausado até o ok.
- **Dias 1–3:** não mexer (aprendizado). Só olhar entrega e erros.
- **Dia 4+:** decidir pela tabela abaixo, com amostra mínima.
- Registrar toda mudança num `log-mudancas.md` (data, o quê, antes, depois, por quê).

| Situação (com amostra suficiente) | Ação |
|---|---|
| Custo por qualificado/visita bom e estável | Manter; escalar a verba em passos pequenos (≤ 20% por vez) |
| Lead barato, ninguém atende/qualifica | **Não é o anúncio**: auditar atendimento e formulário |
| Criativo caro e sem lead qualificado depois do mínimo | Pausar o criativo, não a campanha |
| Pouca entrega | Revisar público, verba e rejeições antes de culpar o criativo |
| Dados insuficientes | Dizer "ainda não dá para concluir" e quanto falta |

Ordem de teste: **gancho → ângulo → formato → oferta → público**, um de cada vez; grade 3×2×2 (3 conceitos × 2 ganchos × 2 textos) quando houver verba.
