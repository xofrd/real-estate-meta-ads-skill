# real-estate-meta-ads-skill

[English](README.md) · **Português (Brasil)**

Uma skill do Claude para anúncios Meta (Facebook e Instagram) de **imóveis de ticket alto**: imobiliárias, corretores e incorporadoras que vendem ou alugam imóveis, em qualquer país.

É um método de trabalho, não um software. Ensina o Claude a estruturar campanhas, escrever anúncios honestos de imóvel, rastrear o lead do anúncio até a visita e a venda no seu CRM, auditar a conta, escrever relatórios que o dono consegue ler, lidar com a categoria especial Moradia (Housing) da Meta, usar catálogo de imóveis e só mudar algo na conta depois de confirmação explícita.

Sem promessa de resultado. Anúncio amplifica o que já funciona; não conserta oferta fraca nem atendimento lento.

## Para quem é

- Imobiliárias, corretores e equipes de marketing que compram anúncios da Meta por conta própria.
- Agências ou autônomos que atendem clientes do mercado imobiliário e querem um método mais rigoroso e honesto.
- Quem tem venda longa (meses), de valor alto e que depende de visita — o método pode servir a outras vendas consultivas, mas foi escrito para imóvel.

**Não** foi feito para e-commerce, otimização de ROAS ou volume de lead barato.

## O que tem dentro

```
skills/
  real-estate-meta-ads/          inglês
    SKILL.md
    references/01..09-*.md
  real-estate-meta-ads-pt-br/    português do Brasil (mesmo conteúdo)
    SKILL.md
    referencias/01..09-*.md
```

| # | Assunto |
|---|---|
| 01 | Estrutura de campanha: degraus de intenção, divisão de verba, funis por tipo de imóvel, nomes, rotina |
| 02 | Formulário instantâneo de maior intenção, clique-para-WhatsApp, página de destino, velocidade de atendimento |
| 03 | Criativos e textos honestos; promessas proibidas |
| 04 | Rastreio até o CRM: estágios do lead (sem resposta → pré-qualificado → qualificado), Conversion Leads, CAPI |
| 05 | Auditoria pontuada da conta (4 blocos) |
| 06 | Relatórios em dinheiro e em gente, não em CPM/CTR |
| 07 | Categoria Moradia por país; regras locais de publicidade, registro profissional e privacidade (genéricas) |
| 08 | Protocolo de mudança: Confirmar → Executar → Conferir; tudo criado pausado; segurança de acesso |
| 09 | Catálogo de imóveis (feed `home_listings`) para Facebook/Instagram; o que o WhatsApp aceita e o que não |

## Instalação

Instale **uma** versão de idioma (as duas têm os mesmos gatilhos e competiriam).

```bash
git clone <url-do-repositorio>
cp -r real-estate-meta-ads-skill/skills/real-estate-meta-ads-pt-br ~/.claude/skills/
# ou, em inglês:
cp -r real-estate-meta-ads-skill/skills/real-estate-meta-ads ~/.claude/skills/
```

Para um só projeto, copie a pasta para `.claude/skills/` dentro do projeto. Outros apps do Claude que aceitam skills podem aceitar a pasta como ZIP; confira a documentação do seu app.

O Claude carrega a skill quando a conversa é sobre anúncios Meta/Facebook/Instagram, formulário de lead, anúncio de imóvel, pixel/CAPI, auditoria ou relatório de anúncios.

### Conectar à sua conta de anúncios da Meta (opcional)

A skill funciona sem conexão (colando ou exportando relatórios em CSV). Para o Claude ler a conta:

1. No **claude.ai** (navegador): Configurações → Conectores → adicionar conector personalizado com a URL `https://mcp.facebook.com/ads` e autorizar com o Facebook (conta com acesso à conta de anúncios).
2. Reabrir o Claude Code: as ferramentas devem aparecer com o nome do conector.
3. A liberação pode ser conta a conta; pode aparecer `is_ads_mcp_enabled: false`.

Notas da nossa configuração (⚠ pode ter mudado): o OAuth iniciado pelo terminal do Claude Code falhou com `redirect_uris are not registered`; adicionar o conector pelo claude.ai era o caminho esperado. O conector pede várias permissões, inclusive `ads_management` (escrita). Uma reportagem (Digiday) citou contas de anúncio restringidas depois de usar o Claude Code com o conector, sem causa confirmada. **Comece só com leitura.**

Nunca coloque token de acesso da Meta em arquivo, URL ou chat. Ver [SECURITY.md](SECURITY.md).

## Exemplos

- "Audita minha conta de anúncios da Meta pela qualidade do lead." → auditoria pontuada, os 3 maiores vazamentos de dinheiro, o que não deu para verificar.
- "Aqui está o CSV do mês passado. Escreve o relatório para o dono." → relatório de uma página: o que aconteceu, o que significa, uma recomendação, funil em dinheiro.
- "Escreve três anúncios para um apartamento de 2 dormitórios de revenda perto do metrô." → texto específico e honesto, com grade de teste e checklist antes de publicar.
- "Queremos atingir investidores que moram em Portugal. Precisa da categoria Moradia?" → sim (Europa), e o que isso restringe.
- "Pausa o anúncio da unidade vendida." → bloco de confirmação (antes, depois, efeito no gasto, como desfazer) e nada é feito até você dizer sim.
- "Nosso feed XML de imóveis pode virar catálogo para Instagram e WhatsApp?" → campos obrigatórios, o que é confirmado, o que é inferência, plano de teste pausado.

## Situação e limitações

- **Escrita no Brasil.** O autor é corretor de imóveis no Brasil. Alguns detalhes são específicos ou característicos do mercado brasileiro (por exemplo, como a categoria especial Moradia se aplica quando você anuncia só dentro do Brasil, vendas centradas em WhatsApp, formatos de moeda e número como `205,65`). Se você atua em outro país, trate essas partes como exemplo e confira as regras locais.

- **Versão 0.1.0.** Escrita a partir do dia a dia de uma imobiliária. **Ainda não testada em escala** nem em muitos países e tipos de conta.
- **A Meta muda políticas, produtos e requisitos com frequência.** Tudo o que tem data de 15/11/2026 e toda marcação `⚠ conferir` deve ser reconferido na documentação atual da Meta antes de você confiar.
- **Não é aconselhamento jurídico.** A skill, de propósito, não lista leis de país. Confira as regras de publicidade, registro profissional, defesa do consumidor e privacidade de onde você atua (leis de privacidade como GDPR, LGPD ou CCPA aparecem só como exemplo).
- Perguntas em aberto, não verificadas: se o Conversion Leads aceita evento negativo de "bad lead" para treino; se o Gerenciador força a categoria Moradia em campanha de catálogo de imóveis fora das regiões obrigatórias; se integrações de WhatsApp não oficiais conseguem devolver conversões de conversa à Meta.
- Sem vínculo, endosso ou patrocínio da Meta ou da Anthropic. Os nomes de produtos pertencem aos donos.

## Trabalhos anteriores e método

Em 15/11/2026 lemos 14 skills e servidores MCP públicos de Meta Ads para ver o que já existia. A maioria era de e-commerce ou infoproduto; nenhum cobria lead qualificado de ciclo longo, Conversion Leads com estágios do CRM nem regras do mercado imobiliário. Não publicamos notas: elas refletiam um caso de uso e um avaliador, não a qualidade geral desses projetos. Os nomes são os registrados na época; links e situação não foram reconferidos para esta versão.

**Nada foi copiado.** Onde aproveitamos uma ideia, ela foi reescrita com nossas palavras para imóvel. `hoodini/meta-ads` não tinha arquivo de licença na época da avaliação, então só ideias foram usadas, nunca texto.

| Projeto (nome na avaliação) | O que aproveitamos |
|---|---|
| MCP oficial da Meta (`mcp.facebook.com/ads`) | Conexão recomendada; leitura primeiro |
| hoodini/meta-ads | Ideias reescritas: degraus de intenção, rotina por dia, clique-para-WhatsApp, protocolo de escrita na conta |
| Adspirer Lead Gen Machine | Ideia de ranquear por lead qualificado, não por lead |
| thatrebeccarae/facebook-ads | Formato de auditoria pontuada |
| attainmentlabs (MCP) | Ideias de segurança: simulação, teto de gasto, registro de mudanças |
| dengineproblem | Ideia de manter histórico de ações (repositório indisponível na época) |
| Pipeboard | Não usado (acesso de terceiro ao token) |
| openclaudia, arnabbagxd, dvorkinguy, kostja94, Rioja, Varnan-Tech, claude-office-skills | Avaliados; nada usado aqui |

## Como contribuir

Correções são muito bem-vindas, principalmente quando a Meta muda uma política. Leia o [CONTRIBUTING.md](CONTRIBUTING.md): citar fonte oficial, sem exagero, sem dado privado. Conduta: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Mudanças: [CHANGELOG.md](CHANGELOG.md).

## Licença

[MIT](LICENSE).
