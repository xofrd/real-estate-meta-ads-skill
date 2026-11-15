# 09. Catálogo de imóveis (Facebook, Instagram, WhatsApp)

Pesquisa de 15/11/2026 na documentação oficial da Meta. Separar sempre **confirmado em documentação oficial** de **inferência**. Reconferir antes de investir tempo: a Meta muda isso com frequência.

## O que é o catálogo de imóveis

- Catálogo do tipo **imóveis (`home_listings`)** no Gerenciador de Comércio. O tipo **não pode ser alterado** depois de criado. Um catálogo só para todos os imóveis.
- Alimentado por **feed em XML** (raiz `<listings>`, vários `<listing>`), CSV ou TSV, **por URL com agendamento** (por hora, dia ou semana). Um plugin do site que gere o XML serve, se o formato bater com os campos abaixo.

## Campos do feed

| Obrigatórios para anúncio | Opcionais úteis |
|---|---|
| `home_listing_id`, `name`, `availability`, `address` (`addr1`, `city`, `region`, `country`, `postal_code`), `latitude`, `longitude`, `neighborhood`, `price`, `image`, `url` | `description`, `num_beds`, `num_baths`, `year_built`, `property_type` (apartment, condo, house, land, townhouse, other…), `listing_type` (for_sale_by_agent, for_rent_by_agent, new_construction…) |

- `availability`: for_sale, for_rent, sale_pending, recently_sold, off_market, available_soon.
- `price`: valor + código ISO de 3 letras da moeda, ex.: `850000 BRL` (ou USD, EUR, GBP…).
- **Nomes dos campos em inglês**; o texto dos valores pode estar em qualquer idioma.
- **Imóvel vendido sai do feed ou muda `availability` no mesmo dia** (anúncio de imóvel vendido queima verba e reputação).
- Imagem para Instagram: a etiqueta `INSTAGRAM_STANDARD_PREFERRED` escolhe a foto usada lá.

## Facebook e Instagram (confirmado em documentação)

- Anúncios de catálogo ("anúncios com mídia de produto"): **carrossel, coleção, imagem ou vídeo único**. Instagram: Feed, Stories e Explorar (em Stories, coleção/mapa/vídeo do catálogo não aparecem).
- Objetivo clássico: `PRODUCT_CATALOG_SALES`. Com Leads/Tráfego/Engajamento, o **local de conversão é Site ou App** (o clique vai à página do imóvel). Existe também anúncio de catálogo com **formulário de lead**.
- Para **lead qualificado**, combinar: anúncio de catálogo → página do imóvel com formulário/WhatsApp, e/ou o anúncio de catálogo com formulário. Medir como em `04-rastreamento-crm.md`.
- Disponibilidade por país: a documentação lida não traz lista de países nem restrição para esses anúncios, mas também não afirma disponibilidade em todos. **Testar com campanha pausada e catálogo pequeno** antes de subir tudo.

## Categoria Moradia com catálogo

- Página geral de anúncios de imóveis da Meta: "Advertisers must specify `HOUSING` as a `special_ad_category` for ad campaigns that market housing" — **sem citar país**.
- Página da categoria especial: fora dos EUA, Canadá e Europa, o campo existe mas pode ir `NONE` (ver `07-moradia-e-regras-locais.md`).
- **Não confirmado:** se o Gerenciador força/sugere Moradia ao escolher catálogo de imóveis, e se a revisão automática pausa anúncio de imóvel marcado `NONE`. **Primeiro teste a fazer** (campanha pausada). Se a Meta exigir, declarar e avisar o dono: perde-se lookalike, idade/gênero e bairro/CEP naquela campanha.

## WhatsApp — o que dá e o que não dá

**Confirmado em documentação oficial (lida em 15/11/2026)**
- API (Cloud API): mensagens de catálogo e de vários produtos exigem **catálogo de e-commerce** (tipos "Produtos" e "Serviços"). **O catálogo de imóveis (`home_listings`) não é citado em nenhum ponto** da documentação do WhatsApp. Um catálogo por conta.
- App WhatsApp Business: catálogo de produto/serviço **cadastrado à mão**; cada item passa por análise.
- ⚠ conferir: as ferramentas de pedido estavam previstas para sair do app em 15/11/2026 (o cliente ainda vê o catálogo).
- Política: imóvel **não está** entre os itens restritos; são proibidos terreno em área de conservação ecológica, discriminação em classificados de moradia e conteúdo sem item à venda.

**Inferência (não testada)**
- O catálogo de imóveis do Facebook/Instagram **provavelmente não aparece para conectar ao WhatsApp**. O caminho seria um **catálogo de e-commerce separado** com imóveis cadastrados como "produtos" (à mão no app, ou por feed próprio). Risco de reprovação na análise: não descartado.

**Alternativas oficiais mais seguras**
1. **Anúncio clique-para-WhatsApp** (imagem, vídeo, carrossel) com saudação automática que pode ter botão "ver catálogo".
2. Anúncio de catálogo → página do imóvel (`url` do feed) → botão de WhatsApp com mensagem pré-preenchida citando o imóvel.
3. Na conversa, o atendimento envia o **link do imóvel** (página do site) em vez de item de catálogo.
4. Só vale mexer em catálogo de e-commerce no WhatsApp se o teste mostrar ganho real; começar pelos itens 1–3.

## Próximos passos (modelo)

- [ ] Identificar a origem do feed (plugin do site, exportação do CRM) e conferir se o XML traz os campos obrigatórios acima (principalmente `latitude`, `longitude`, `neighborhood`, `postal_code` e `price` com o código da moeda).
- [ ] Criar um catálogo `home_listings` pequeno e testar o feed por URL (com aprovação do dono, protocolo `08-mudancas-na-conta.md`).
- [ ] Campanha de catálogo **pausada** para ver se a Meta exige Moradia.
- [ ] Decidir sobre WhatsApp só depois de rodar 1–3.
