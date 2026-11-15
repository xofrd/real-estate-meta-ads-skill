---
name: real-estate-meta-ads-pt-br
description: Anúncios Meta (Facebook e Instagram) para imobiliária e corretor de ticket alto em qualquer país, em português do Brasil — funil por degraus de intenção, formulário instantâneo de maior intenção e clique-para-WhatsApp, criativos honestos, rastreio do lead do anúncio até a visita e a venda no seu CRM (CAPI / Conversion Leads), auditoria pontuada, relatórios que o dono entende (custo por lead qualificado e por visita, não CPM/CTR soltos), categoria especial Moradia (Housing) por país, catálogo de imóveis e mudança na conta só com confirmação. Use SEMPRE que o assunto for Meta Ads, Facebook Ads, Instagram Ads, Gerenciador de Anúncios, anúncio de lead, formulário instantâneo, anúncio de imóvel, lançamento, locação, pixel, CAPI, público, criativo, "o anúncio traz lead ruim", "quanto gastei no Meta", "audita minha conta Meta", relatório de anúncios, catálogo de imóveis, ou pedir para criar, pausar ou alterar algo numa conta de anúncios da Meta.
---

# Meta Ads para imobiliária — método de trabalho

Quase todas as skills públicas de Meta Ads são de e-commerce ou infoproduto (ROAS, urgência, "bold claims"). Imóvel é outro negócio: **ticket alto, venda consultiva de 90 a 180 dias, e o lead só vale se virar visita**. Esta skill reescreve boas ideias públicas (degraus de intenção, rotina por dia, protocolo de mudança) para esse caso. Nenhum texto foi copiado de outros projetos (ver README do repositório, "Trabalhos anteriores").

## Regras que valem sempre

1. **Dinheiro e visita são a métrica, não clique.** CTR, CPM, curtida e até custo por lead são meios. A pergunta é: *quanto custou cada lead QUALIFICADO, cada VISITA e cada VENDA?* Funil de qualidade padrão (adapte e deixe o seu por escrito): **lead sem resposta ("bad lead") → pré-qualificado (respondeu + aceitou o acompanhamento + fala dos imóveis que busca) → qualificado (financeiro analisado e ainda ativo)**. Detalhes em `referencias/04-rastreamento-crm.md`. Os bad leads voltam à Meta como sinal, onde a plataforma permitir.
2. **Anúncio amplifica o que já funciona.** Oferta fraca, atendimento lento ou página ruim não se consertam com segmentação. Diagnosticar o funil inteiro (anúncio → formulário/WhatsApp → primeira resposta → visita) antes de mexer no anúncio.
3. **Honestidade total na peça.** Nunca inventar escassez ("últimas unidades", "só hoje"), prazo, desconto, depoimento, número ou "a partir de" que não exista. Nunca imagem de imóvel gerada por IA apresentada como real. Checklist em `referencias/07-moradia-e-regras-locais.md`.
4. **A categoria especial Moradia (Housing) depende de onde o anúncio roda.** Obrigatória quando o anúncio atinge EUA, Canadá ou Europa, e sempre que a Meta pedir; a documentação da Meta (lida em 15/11/2026) diz que ela pode ir `NONE` para anunciante fora dessas regiões que atinge só público fora delas. ⚠ Reconferir antes de cada campanha nova. A política de não discriminação da Meta vale sempre, declarada ou não. A decisão é do anunciante; registrar. Detalhes em `referencias/07-moradia-e-regras-locais.md`.
5. **Nenhuma mudança na conta sem o ok do dono, item a item.** Tudo novo nasce **PAUSADO**. Protocolo em `referencias/08-mudancas-na-conta.md`.
6. **Dado antes de opinião, amostra antes de conclusão.** Sempre dizer o tamanho da amostra e o que ela NÃO permite concluir. Não ranquear campanha com pouco volume.
7. **A verdade das vendas é o CRM**, não o painel da Meta (a atribuição da Meta é em janela curta; a venda de imóvel demora meses).
8. **Uma empresa por pasta de trabalho.** Os dados de cada empresa (relatórios, registro de mudanças) ficam numa pasta própria, ex.: `meta-ads/` dentro do projeto daquela empresa. Criar pasta só com aprovação do dono.
9. **Relatório que o dono entende** (`referencias/06-relatorios.md`): resposta primeiro, em dinheiro e em gente, sem jargão, com o que fazer. Nunca "relatório de agência".

## Triagem — o que a pessoa quer?

| Pedido | Ler |
|---|---|
| Montar/rever estrutura de campanha, funil, público, verba | `referencias/01-estrutura-campanha.md` |
| Formulário instantâneo, clique para WhatsApp, página de destino | `referencias/02-formularios-e-whatsapp.md` |
| Escrever/rever anúncio, vídeo, imagem, texto | `referencias/03-criativos-e-texto.md` |
| De onde vem o lead que visita/compra, CAPI, Conversion Leads, pixel | `referencias/04-rastreamento-crm.md` |
| "Audita a conta", "por que o lead é ruim", rotina semanal | `referencias/05-auditoria.md` |
| Ler resultados, gerar relatório (semanal, mensal, por empreendimento) | `referencias/06-relatorios.md` |
| Antes de publicar qualquer peça: Moradia, registro profissional, regras locais, privacidade | `referencias/07-moradia-e-regras-locais.md` |
| Qualquer alteração na conta | `referencias/08-mudancas-na-conta.md` |
| Catálogo de imóveis (feed XML), anúncios de catálogo, catálogo no WhatsApp | `referencias/09-catalogo-imoveis.md` |

Ler só o arquivo do assunto. Pedido que cruza vários ("monta a campanha do zero"): ordem 07 → 04 → 01 → 02 → 03, parando ao fim de cada etapa para o ok.

## Como a conta é acessada

- **Conector oficial da Meta (MCP, `https://mcp.facebook.com/ads`)**, adicionado como conector no claude.ai e autorizado por OAuth (login do Facebook). Se as ferramentas dele estiverem disponíveis, usar **primeiro só as de leitura**. O conector pede várias permissões, inclusive `ads_management` (escrita): toda escrita é mudança e segue `referencias/08-mudancas-na-conta.md`.
- **Modo navegador:** ler telas e relatórios do Gerenciador de Anúncios por uma ferramenta de automação de navegador; exportar CSV.
- **Modo exportação:** o dono exporta o relatório (CSV) e você analisa com os critérios de `referencias/06-relatorios.md`.
- **Nunca token de acesso da Meta em arquivo, URL ou chat.** Preferir o OAuth do conector oficial. Sem scripts ou pacotes de terceiros que escrevam na conta, a menos que o dono decida o contrário depois de revisá-los.

## Ao terminar uma etapa

Resumo curto em português simples: o que foi feito, o que **não** foi feito, o que depende de decisão e, se algo mudou na conta, como desfazer.
