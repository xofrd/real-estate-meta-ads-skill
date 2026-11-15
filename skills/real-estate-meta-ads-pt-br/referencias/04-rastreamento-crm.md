# 04. Rastreamento: do anúncio à venda, passando pelo seu CRM

Problema central (nenhuma skill pública avaliada resolve): a venda de imóvel leva 90–180 dias e a atribuição da Meta é de cerca de 7 dias. O caminho é **devolver para a Meta os estágios do funil** (Conversion Leads) e **medir a verdade no CRM**.

## 1. Definir "qualificado" (obrigatório antes de analisar)

Definição padrão em três degraus — adapte ao seu negócio e deixe por escrito:

| Estágio | Regra | O que vira para a Meta |
|---|---|---|
| **Lead sem resposta** ("bad lead") | Entrou e **nunca respondeu** ao primeiro contato (prazo a combinar, ex.: 7 dias) | Sinal negativo: a Meta aprende o que NÃO é bom (⚠ ver abaixo) |
| **Lead pré-qualificado** | **Respondeu** + **aceitou o acompanhamento** (curadoria de imóveis) + fala dos imóveis que está buscando | Evento positivo de volume (bom para otimizar) |
| **Lead qualificado** | Depois de analisar o que busca e o **financeiro** (renda, entrada, financiamento etc.) **e ainda ativo**; provável de agendar visita | Evento positivo de maior valor |

Regras de borda a decidir: quanto tempo o lead "sem resposta" espera até virar bad lead; o que é "ainda ativo" (ex.: respondeu nos últimos X dias); se a definição muda entre lançamento, revenda e locação.

Sem essa definição aplicada nos dados, a análise para: **"bloqueado: lead sem estágio no CRM"**.

## 2. Estágios e eventos

`lead` → (`sem resposta` | `pré-qualificado`) → `qualificado` → `visita agendada` → `visita feita` → `proposta` → `venda`.

- **Devolver o "bad lead" à Meta:** enviar o estágio sem resposta pelo mesmo canal (CAPI/integração de CRM). ⚠ **Não verificado:** se a documentação do Conversion Leads aceita evento negativo/"lead perdido" para treino. Se não aceitar, o sinal é indireto: a Meta aprende pelo contraste entre quem avançou e quem ficou parado, então **todo estágio positivo precisa chegar com o `lead_id`**. Não prometer o efeito antes de testar.
- Otimizar primeiro por **pré-qualificado** (responde + aceita acompanhamento): é rápido e tem volume, cabe nos requisitos da Meta. Passar para **qualificado** ou **visita agendada** quando houver volume; não otimizar por **venda** (a Meta pede ~200 leads/mês, o estágio-alvo em até 28 dias e conversão entre ~1% e 40%; venda de imóvel costuma passar de 28 dias e ficar abaixo de 1%). **Enviar a venda mesmo assim**, para medir. ⚠ conferir os requisitos atuais.
- Enviar **no mínimo 2, de preferência 3+** estágios à Meta (integração de CRM/Conversion Leads via CAPI), ao menos **1 vez por dia**, sempre no **mesmo pixel/conjunto de dados**.
- Guardar no CRM, por lead: `lead_id` (formulário), UTMs (campanha/conjunto/anúncio), `ctwa_clid`/origem do clique no WhatsApp (se disponível), data de cada estágio.
- ⚠ conferir: o treinamento leva 1–2 meses, segundo o que foi lido, e só funciona com formulário instantâneo. Verificar esses requisitos na documentação atual antes de prometer (a política muda).

## 3. Qualidade do sinal (CAPI)

- **Deduplicação por `event_id`** entre pixel e servidor.
- Meta de **EMQ (qualidade de correspondência de eventos) ≥ 8**. Parâmetros: e-mail e telefone **com hash**, `fbc`, `fbp`, `external_id`.
- Domínio verificado e prioridade de eventos conferida. Para imobiliária, **Lead (e estágios) pesa mais que Purchase** — o contrário do que as skills de e-commerce ensinam.
- Atraso de dados: eventos do CRM chegam depois; avisar nos relatórios que os últimos dias estão incompletos.

## 4. Origem sem perda

- Todo lead com origem: campanha/anúncio/formulário/WhatsApp/orgânico. **Contar à parte os leads sem origem** (quantos, % do total) e nunca esconder.
- Lead duplicado: deduplicar por telefone normalizado antes de contar. Registrar os rejeitados.
- Cruzar sempre: **gasto (Meta) × leads (CRM) × visitas × vendas (CRM)**. Quando o painel da Meta e o CRM divergirem, vale o CRM, explicando a diferença.

## 5. Privacidade no rastreio

- Base legal e finalidade para usar dados em público/CAPI, conforme as leis de privacidade que se aplicam a você (ex.: GDPR, LGPD, CCPA); política de privacidade acessível no formulário.
- Consentimento de cookies antes do pixel, onde for exigido.
- **Não enriquecer lead por raspagem de busca ou de IA** (risco de privacidade).
- Dado pessoal (telefone, e-mail) nunca em relatório, log ou URL.

## 6. Perguntas em aberto

- Integrações de WhatsApp não oficiais podem **não** permitir CAPI de conversas: não verificado.
- Mapear onde o seu CRM guarda `lead_id` e UTMs antes de prometer o envio de estágios.
