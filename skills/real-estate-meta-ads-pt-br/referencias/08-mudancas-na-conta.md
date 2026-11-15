# 08. Mudanças na conta — protocolo Confirmar → Executar → Conferir

Vale para TODA alteração: criar, ativar, pausar, verba, público, anúncio, formulário, regras automáticas, aplicar sugestão da Meta. Sem exceção, mesmo que digam "pode fazer tudo".

## 1. Confirmar (antes)

```
## Mudança proposta
Conta: <nome> (<ID, sem expor dado pessoal>)
Onde: campanha / conjunto / anúncio
O que é: <português simples>
Antes: <estado lido AGORA na tela ou pela API, não de memória>
Depois: <novo estado>
Efeito no gasto: <ex.: R$ 50/dia → R$ 60/dia ≈ +R$ 300/mês>
Risco: baixo / médio / alto
Como desfazer: <passo exato>
```

- Mostrar **o impacto antes de pedir o ok**.
- Lote: ≤ ~50 itens por confirmação, listados um a um. Pausar e excluir são confirmações separadas. **Excluir só se pedido explicitamente** — preferir pausar. (Vale também para qualquer ferramenta com `delete`.)
- Aumento de verba: **no máximo 2× por vez** e nunca acima do teto combinado. Autorização genérica ("pode ajustar a verba") **não vale**: verba é sempre por campanha.

## 2. Executar

- Tudo criado nasce **PAUSADO**. **Criar e ativar nunca no mesmo passo**: ativar é nova confirmação.
- Não mexer em conjunto nos **3 primeiros dias** (aprendizado) nem oscilar verba.
- Antes de otimizar, **ler os últimos 3 dias do `log-mudancas.md`** (não desfazer o que acabou de ser feito).
- Registrar em `meta-ads/log-mudancas.md` da empresa: data/hora, o quê, antes, depois, motivo, como desfazer.
- **Modo navegador:** uma mudança por vez; ler a tela antes e depois; não acionar diálogo de confirmação do navegador sem avisar.
- **Conector oficial da Meta:** começar só com ferramentas de leitura. Para escrita, criar pausado e conferir depois o status real e a aprovação dos anúncios. Se a conta oferecer regras de proteção (bloquear ativação, limitar verba), sugerir ligá-las.
- Se pixel/CAPI estiverem quebrados: **parar** e consertar antes de criar campanha.

## 3. Conferir (depois)

- Reler a tela/API: o estado é mesmo o proposto? Anúncios aprovados? Status PAUSADO/ATIVO como combinado?
- Dizer ao dono o que ficou, o que não foi feito e como desfazer.

## Segurança de acesso

- **Nunca token de acesso da Meta em arquivo `.env`, em URL ou colado no chat.** Preferir o login OAuth do conector oficial.
- **Começar só com leitura.** Uma reportagem (Digiday) citou contas de anúncio restringidas depois de usar o Claude Code com o conector da Meta, sem causa confirmada. ⚠ não verificado por este projeto.
- Não instalar pacotes/scripts de terceiros que escrevam na conta sem revisá-los (quem guarda o token, o que podem fazer, se há simulação/teto de gasto/registro).
- Aviso de política da Meta ou conta restrita: parar e avisar o dono; não insistir.
