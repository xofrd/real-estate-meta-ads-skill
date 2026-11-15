# 05. Auditoria da conta — checklist pontuado para lead imobiliário

Formato inspirado em auditorias pontuadas públicas, reescrito para lead de ticket alto. Cada item: **OK / Atenção / Falha / Ganho rápido**. Nota por bloco de 0 a 100 e nota geral ponderada. **Ler a conta antes de opinar; nunca auditar de memória.**

## Bloco A — Rastreamento e sinal (peso 30%)
- [ ] Pixel disparando nos eventos certos; deduplicação por `event_id` (navegador × servidor)
- [ ] CAPI ativa; EMQ ≥ 8 nos eventos de lead
- [ ] Domínio verificado; prioridade de eventos conferida (Lead acima de compra)
- [ ] Estágios do CRM (qualificado/visita/venda) chegando à Meta ≥ 1×/dia
- [ ] `lead_id` e UTMs guardados no CRM; % de leads sem origem
- [ ] Banner de consentimento antes do pixel, onde exigido
- [ ] Atraso dos dados explicado nos relatórios

## Bloco B — Funil e qualidade do lead (peso 30%)
- [ ] "Qualificado" definido por escrito
- [ ] Formulário de maior intenção com 3–5 perguntas de qualificação
- [ ] Tempo até a primeira resposta e responsável por turno
- [ ] Taxa lead → qualificado → visita por campanha (não só custo por lead)
- [ ] CTWA: custo por conversa, taxa de resposta, custo por resposta
- [ ] Remarketing separado de prospecção nos relatórios

## Bloco C — Estrutura (peso 20%)
- [ ] % de conjuntos em *Aprendizado limitado* (meta ≤ 30%)
- [ ] Verba diária ≥ ~5× o custo-alvo por evento otimizado
- [ ] Públicos exclusivos entre degraus; clientes e imóveis vendidos excluídos
- [ ] Audience Network/posicionamentos conferidos
- [ ] Nomes padronizados; UTM em todos os anúncios
- [ ] Imóvel vendido/indisponível com anúncio pausado
- [ ] Decisão sobre a categoria Moradia registrada e correta para os países atingidos

## Bloco D — Criativo e regras (peso 20%)
- [ ] 3+ conceitos ativos; fadiga/frequência sob controle
- [ ] Peças sem escassez/urgência falsa, sem imagem gerada passada por real
- [ ] Números de registro/licença visíveis onde o seu lugar exigir; preço/metragem conferidos
- [ ] Política de privacidade no formulário

## Saída da auditoria

1. **Nota geral e por bloco**, numa tabela de 4 linhas.
2. **Os 3 maiores vazamentos de dinheiro** (estimados em dinheiro por mês, dizendo a incerteza).
3. **Ganhos rápidos** (≤ 1 hora cada, risco baixo).
4. **O que não deu para verificar** e por quê.
5. Plano em ordem de impacto; qualquer mudança vai pelo protocolo `08-mudancas-na-conta.md`.

## Rotina

- **Semanal (15 min):** gasto, leads, qualificados, visitas, tempo de resposta; anomalias; nada de mexer nos primeiros 3 dias de um conjunto novo.
- **Mensal:** relatório completo (`06-relatorios.md`), auditoria rápida dos blocos A e B.
- **Trimestral:** reavaliar a definição de qualificado, o funil e a verba por tipo de imóvel.
