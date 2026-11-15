# 02. Formulário instantâneo, WhatsApp e página de destino

Meta: lead que o corretor consegue converter em visita. Volume bruto de lead é vaidade.

## Formulário instantâneo — tipo "Maior intenção"

- Usar o tipo **Maior intenção** (tela de revisão antes de enviar). Espere menos volume e mais qualidade (estimativas de terceiros: 20–40% menos leads; não confirmado pela Meta).
- 3 a 5 perguntas, na ordem do esforço:
  1. Quer para **morar ou investir**?
  2. **Faixa de valor** do imóvel (faixas, não campo aberto).
  3. **Prazo** para decidir.
  4. **Forma de pagamento** (financiamento aprovado / à vista / ainda vou simular / outras opções que existam no seu mercado).
  5. **Canal preferido** (WhatsApp ou ligação) e melhor horário.
- Nome, e-mail e telefone preenchidos automaticamente; telefone com código do país e de área.
- **Política de privacidade** com link real e texto de finalidade (exigida pela maioria das leis de privacidade).
- Tela de agradecimento com **o que acontece em seguida e em quanto tempo** ("um consultor chama no WhatsApp em até X minutos") — e cumprir.
- O `lead_id` do formulário (15–17 dígitos) **deve ser guardado no seu CRM**: é a chave para devolver estágios à Meta.
- ⚠ conferir: quando este texto foi escrito, o conector oficial da Meta não criava formulário instantâneo; criar o formulário **à mão no Gerenciador**, a menos que a lista atual de ferramentas diga o contrário.
- Respeitar o horário: formulário que chega às 23h e só é respondido às 9h perde o lead. Considerar resposta automática honesta ("recebemos, retornamos às 9h").

## Clique para WhatsApp (CTWA)

- Exige conta do WhatsApp Business vinculada à Página e número verificado **antes de gastar**.
- Mensagem pré-preenchida que identifica o anúncio/imóvel ("Olá, vi o apartamento da Vila Verde").
- Métricas próprias: **custo por conversa iniciada → taxa de resposta (primeira resposta do lead) → custo por resposta → custo por visita**. Se as pessoas iniciam conversa e não respondem nem compram, o gargalo é o **atendimento**, não o anúncio.
- ⚠ Devolver conversões das conversas à Meta (API de Conversões para mensagens) exige a plataforma **oficial** do WhatsApp Business e o identificador `ctwa_clid`. **Não verificado:** se integrações de WhatsApp não oficiais usadas por alguns CRMs conseguem fechar essa atribuição. Até verificar, medir pelo que o CRM registra (origem + estágio), sem prometer otimização por conversão de WhatsApp.

## Velocidade e dono do lead

- Definir **prazo máximo do primeiro contato** e **um responsável nomeado** por turno. Lead barato que ninguém atende é o erro mais comum (e o mais caro).
- Medir o tempo até a primeira resposta humana/IA no CRM e cruzar com a taxa de visita.

## Página de destino (quando houver)

- A promessa do anúncio aparece **igual** na página; chamada para ação acima da dobra.
- Dados reais: metragem, tipologia, entrega, condições, preço ou faixa **que existe**; imagens ilustrativas sinalizadas.
- Números de registro profissional/licença onde o seu lugar exigir (ver `07-moradia-e-regras-locais.md`).
- Banner de cookies/consentimento **antes** de o pixel disparar, onde a lei de privacidade exigir.
- Eventos: `PageView`, `ViewContent`, evento próprio de visita engajada (30 s ou 60% de rolagem), clique no WhatsApp, envio de formulário — com **deduplicação por `event_id`** entre navegador e servidor.
