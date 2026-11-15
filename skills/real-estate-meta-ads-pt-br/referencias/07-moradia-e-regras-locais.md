# 07. Categoria Moradia e regras locais — conferir ANTES de publicar

⚠ Este arquivo foi escrito com pesquisa de 15/11/2026. **As políticas da Meta e as regras de cada país mudam: conferir a versão vigente** (e, em dúvida, consultar advogado ou o órgão de registro profissional) antes de afirmar algo ao cliente.

> **Nota do autor:** este projeto é escrito por um corretor que atua no **Brasil**. Os exemplos, alguns detalhes e a leitura de que a categoria é "opcional fora de EUA, Canadá e Europa" refletem o **mercado brasileiro** e podem ser específicos dele. Se você atua em outro país, confira como a Meta aplica a regra aí e adapte.

## 1. Categoria especial Moradia (Housing) da Meta

### O que a documentação da Meta dizia (lida em 15/11/2026)

- A página da Marketing API sobre categorias especiais (`.../audiences/special-ad-category`) diz que a categoria é **obrigatória** quando o anúncio atinge **Estados Unidos (desde 2019), Canadá (desde 2020) ou Europa (desde 2021)** — e em qualquer outro mercado em que a Meta aplique a mesma regra.
- Para **anunciante fora dessas regiões que atinge só público fora delas**, o campo continua existindo (precisa ser preenchido), mas pode ir **`NONE`**: declarar Moradia é opcional nesse caso.
- A página geral da Meta sobre anúncios de imóveis diz: "Advertisers must specify `HOUSING` as a `special_ad_category` for ad campaigns that market housing" — **sem citar país**. As duas páginas não dizem exatamente a mesma coisa; por isso a regra precisa ser reconferida.
- Não foi encontrada página da Central de Ajuda específica para outros países. ⚠ **reconferir antes de publicar e sempre que a Meta mudar a política.** ⚠ conferir quais países a Meta considera "Europa".

### Quando declarar Moradia

| Situação | Moradia |
|---|---|
| O anúncio atinge EUA, Canadá ou Europa (mesmo parte do público, ex.: investidor ou expatriado que mora lá) | **Obrigatória** |
| A Meta pede (na revisão do anúncio, no fluxo do Gerenciador ou numa reprovação) | **Declarar**, seguir o pedido e avisar o dono |
| Anunciante fora dessas regiões, público só fora delas | **Opcional** segundo a documentação acima (pode ir `NONE`). A decisão é do anunciante; registrar a decisão e a data |

### O que a declaração restringe (conforme documentado quando este texto foi escrito)

- Idade fixa 18–65+; sem segmentação por gênero.
- Sem lookalike (público semelhante).
- Sem segmentação por CEP/código postal ou bairro; raio mínimo em torno do local.
- Sem exclusões detalhadas; público detalhado restrito.
- Certificação de não discriminação.

Sem declarar (onde é opcional), lookalike, idade/gênero, público detalhado e bairro/CEP **ficam disponíveis**. ⚠ conferir a lista atual na tela.

### Vale sempre, declarada ou não

**A política de não discriminação da Meta e a lei.** Nunca segmentar nem excluir por raça, religião, origem, sexo/gênero, estado civil, deficiência ou qualquer outra característica protegida. Segmentar por **localização e interesse legítimo ligado ao imóvel** é diferente de excluir grupo protegido.

## 2. Regras locais de publicidade, registro profissional e privacidade — confira as do seu lugar

Esta skill não lista leis de um país: elas variam por país, estado e cidade, e mudam. Antes de publicar, descubra o que vale para você. Perguntas típicas:

- **Registro profissional:** o número de registro/licença da imobiliária ou do corretor precisa aparecer no anúncio, e com que tamanho?
- **Lançamento / na planta:** é preciso registro, licença ou aprovação antes de anunciar ou aceitar reserva? O número precisa aparecer na peça?
- **Defesa do consumidor e normas de publicidade:** a oferta anunciada vincula? O que conta como enganoso (preço "a partir de", metragem, vaga, prazo de entrega, render, "últimas unidades")? Existe código de autorregulamentação publicitária?
- **Leis de privacidade** (por exemplo GDPR, LGPD, CCPA): base legal e finalidade para formulário, público de lista de clientes e CAPI; política de privacidade; consentimento de cookies antes do pixel; direitos do titular.
- **Regras contra discriminação** em anúncios de moradia, além da política da Meta.

Em dúvida, consultar advogado ou o órgão de registro profissional. Não afirmar ao cliente uma regra que você não conferiu.

## 3. Privacidade (mínimo geral)

- Finalidade e **política de privacidade** no formulário.
- **Base legal** para subir lista de clientes do CRM como público e para enviar dados pela CAPI.
- Consentimento de cookies antes do pixel, onde exigido.
- Telefone/e-mail enviados à Meta **com hash**. Nada de dado pessoal em relatório.

## 4. Checklist rápido por peça

- [ ] Números de registro/licença visíveis onde exigido
- [ ] Lançamento: registro/licença exigido no seu lugar obtido e exibido, se exigido
- [ ] Preço/metragem/prazo/vagas = contrato/memorial oficial
- [ ] Ilustração sinalizada; nenhuma imagem de IA passada como real
- [ ] Sem escassez/urgência/depoimento inventados; sem rentabilidade garantida
- [ ] Público não discrimina nenhum grupo protegido
- [ ] Países atingidos conferidos: EUA, Canadá ou Europa? → declarar Moradia
- [ ] Formulário com privacidade; pixel com consentimento onde exigido
- [ ] Imóvel ainda disponível hoje
