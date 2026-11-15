# 06. Ler resultados e gerar relatórios que fazem sentido

Objetivo: relatório **que faz sentido** para quem decide, não "relatório de agência" ininteligível. Regra: quem lê não precisa saber o que é CPM.

## Princípios

1. **Resposta primeiro.** As 3 primeiras linhas dizem: *o que aconteceu, o que significa, o que fazer.*
2. **Tudo em dinheiro e em gente.** "Gastamos R$ 4.200 e isso gerou 38 contatos, 11 qualificados e 4 visitas; cada visita custou R$ 1.050." Não "CPM R$ 38, CTR 1,2%". Usar a moeda da empresa.
3. **Métricas de funil, em ordem:** gasto → leads → **qualificados** → **visitas** → propostas → vendas; custo de cada degrau; % de passagem entre degraus.
4. **Comparar com algo:** período anterior, mesma campanha, meta combinada. Número sem comparação não informa.
5. **Dizer o que NÃO sabemos:** amostra pequena, dados atrasados, leads sem origem, divergência Meta × CRM. Nunca esconder.
6. **Uma recomendação principal** (e até duas secundárias), com motivo, custo e risco. Nada de lista de 15 "oportunidades".
7. **Causa antes de culpa:** se o lead é barato e não vira visita, investigar atendimento/qualificação antes de culpar o criativo.
8. **Sem vaidade:** curtidas, alcance, CPM, CTR só aparecem como apoio de um diagnóstico específico (ex.: "o criativo cansou: frequência 5,1").
9. **Sem dado pessoal** (nome, telefone) no relatório.

## Modelo (resumo de 1 página + detalhe)

```
# Meta Ads — <período> — <empresa/empreendimento>

## Em 3 linhas
1. O que aconteceu: ...
2. O que significa: ...
3. O que recomendo: ... (decisão sua: sim/não)

## O funil em dinheiro
| Etapa | Qtd | Custo por unidade | vs. período anterior |
|---|---|---|---|
| Gasto | R$ | | |
| Leads | | R$ | |
| Qualificados | | R$ | |
| Visitas agendadas / feitas | | R$ | |
| Propostas / Vendas | | R$ | |
(Fonte: gasto = Meta; demais = CRM. Leads sem origem: N = X%.)

## O que funcionou e o que não
- Melhor anúncio/campanha por **custo por visita** (não por custo por lead), com amostra.
- Pior, e o que fazer (pausar / testar outro ângulo / consertar o atendimento).

## Atendimento (o gargalo escondido)
Tempo médio até a 1ª resposta; % de leads respondidos em ≤ X min; taxa lead → visita por faixa de tempo.

## Antes de concluir
Amostra, atraso de dados, divergências, o que ainda não dá para afirmar.

## Decisões pedidas
1) ... 2) ...  (cada uma vai ao protocolo de mudança)
```

## Como ler os números (cola)

| Sintoma | Causa provável | Verificar primeiro |
|---|---|---|
| Custo por lead baixo, quase nenhum qualificado | Formulário fácil demais / público amplo / Audience Network | Perguntas de qualificação; relatório por posicionamento |
| Muitas conversas no WhatsApp, poucas respostas | Atendimento lento ou mensagem desalinhada | Tempo da 1ª resposta; texto pré-preenchido |
| Custo por lead subiu de repente | Fadiga do criativo / sazonalidade / concorrência no leilão | Frequência; criativo; data da mudança |
| Visitas boas, vendas zero (ciclo curto demais para concluir) | Ainda é cedo | Janela de 90–180 dias; dizer "inconclusivo" |
| Painel da Meta ≠ CRM | Janela de atribuição / lead sem origem / duplicidade | Contar os sem origem; deduplicar |
| Remarketing "com ROAS ótimo" | Colheu quem já ia comprar | Separar da prospecção; teste de holdout |

## Amostra mínima (regra prática, ajustar)

- Não comparar anúncios com menos de ~30 leads cada nem com menos de 7 dias de entrega.
- Não decidir por "venda" em campanha com poucas vendas: usar qualificado/visita e dizer o intervalo de incerteza.
- Conclusão fraca vira "hipótese a testar", não "fato".

## Formatos de entrega

- **Chat/terminal:** resumo curto em português simples (sempre).
- **Relatório completo:** HTML/PDF de 1–2 páginas para o dono/sócios, a pedido. Gráfico só quando mostra tendência ou comparação de verdade; funil como barras horizontais em dinheiro.
- **Arquivo:** `meta-ads/relatorios/AAAA-MM-DD-<período>.md` dentro da pasta da própria empresa (criar a pasta só com aprovação).
- Idioma: o do dono, frases curtas, sem anglicismo desnecessário (explicar a sigla na primeira vez).
