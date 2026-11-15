# Contributing · Como contribuir

[English](#english) · [Português (Brasil)](#português-brasil)

---

## English

Thank you for helping. This project is small and opinionated: honest ads, decisions based on data, and no change to anyone's ad account without confirmation. Contributions should keep it that way.

### How to propose a change

1. Open an issue first for anything larger than a typo (use the templates: outdated content / policy error, or improvement proposal).
2. Fork, create a branch, make the change.
3. **Change both languages** (`skills/real-estate-meta-ads/` and `skills/real-estate-meta-ads-pt-br/`). If you can only write one, say so in the pull request and a maintainer or another contributor will translate.
4. Keep file numbers and topics aligned between the two versions.
5. Add a line to `CHANGELOG.md` under "Unreleased".
6. Open the pull request using the template.

### Honesty and anti-hype rules

- No promises of results ("doubles your leads", "guaranteed ROI").
- No invented numbers. Every figure (thresholds, percentages, requirements) needs a source or must be labeled as a rule of thumb.
- Separate **confirmed in official documentation** from **inference** and **not verified**. Keep the `⚠ check` / `⚠ conferir` marks until someone verifies the point, and add the date of verification.
- Do not add country-specific laws to the skill. It stays general; local rules are described as questions to check (see `07`).
- Do not weaken the safety rules: everything created paused, confirmation per item, no tokens in files/URLs/chat, read-only first.
- No disparaging other projects. Describe what you used, not what you think of them.

### Citing official sources

- Prefer Meta's own pages: Meta Business Help Center, Meta for Developers (Marketing API, Conversions API, Commerce/catalog, WhatsApp Business Platform), Meta Advertising Standards.
- Cite the page title, the URL and the **date you read it** (e.g. "Marketing API — Special Ad Categories, read 2026-11-15").
- Quote the shortest sentence that supports the claim, in the original language.
- Third-party articles may support a warning, never a rule. Label them as third-party.

### "No private data" test (required before every pull request)

The skill must never contain real company names, people's names, ad account IDs, emails, phone numbers, local file paths or tokens. Run this from the repository root and review every hit:

```bash
grep -rniE '@[a-z0-9.-]+\.[a-z]{2,}|act_[0-9]{5,}|EAA[A-Za-z0-9]{10,}|[/]Users[/]|[/]home[/]|\+?[0-9]{2,3}[ -]?\(?[0-9]{2,3}\)?[ -]?[0-9]{4,5}-?[0-9]{4}' --exclude-dir=.git .
```

Also search for the names of your own company, clients, CRM and colleagues. Use neutral examples (`ACME`, `Green Park`, `$4,200`).

### Reporting an error in a Meta policy

Meta changes policies often, so this is the most useful kind of report.

1. Open an issue with the **"Outdated content / Meta policy error"** template.
2. Say which file and line, what the skill says, what Meta says now, the official link and the date you read it.
3. If you saw the behavior in Ads Manager (e.g. Housing forced on a catalog campaign), describe it **without** account IDs or screenshots showing personal data.

---

## Português (Brasil)

Obrigado por ajudar. Este projeto é pequeno e tem posição clara: anúncio honesto, decisão com dado e nenhuma mudança na conta de anúncios de ninguém sem confirmação. As contribuições devem manter isso.

### Como propor uma mudança

1. Abra uma issue antes de qualquer coisa maior que erro de digitação (use os modelos: conteúdo desatualizado / erro de política, ou proposta de melhoria).
2. Faça o fork, crie uma branch, faça a mudança.
3. **Mude os dois idiomas** (`skills/real-estate-meta-ads/` e `skills/real-estate-meta-ads-pt-br/`). Se só conseguir escrever em um, diga no pull request e alguém traduz.
4. Mantenha os números dos arquivos e os assuntos alinhados entre as duas versões.
5. Acrescente uma linha no `CHANGELOG.md` em "Unreleased".
6. Abra o pull request usando o modelo.

### Regras de honestidade (sem exagero)

- Sem promessa de resultado ("dobra seus leads", "ROI garantido").
- Sem número inventado. Todo número (limites, percentuais, requisitos) precisa de fonte ou deve ser marcado como regra prática.
- Separar **confirmado em documentação oficial**, **inferência** e **não verificado**. Manter as marcas `⚠ conferir` / `⚠ check` até alguém verificar, e acrescentar a data da verificação.
- Não acrescentar leis de um país na skill. Ela continua geral; regras locais aparecem como perguntas a conferir (ver `07`).
- Não enfraquecer as regras de segurança: tudo criado pausado, confirmação por item, nada de token em arquivo/URL/chat, leitura primeiro.
- Sem falar mal de outros projetos. Descreva o que aproveitou, não o que acha deles.

### Como citar fonte oficial

- Preferir as páginas da própria Meta: Central de Ajuda para Empresas, Meta for Developers (Marketing API, API de Conversões, Commerce/catálogo, WhatsApp Business Platform), Padrões de Publicidade da Meta.
- Citar o título da página, a URL e a **data em que leu** (ex.: "Marketing API — Special Ad Categories, lida em 15/11/2026").
- Citar a frase mais curta que sustenta a afirmação, no idioma original.
- Artigo de terceiros pode sustentar um alerta, nunca uma regra. Marcar como terceiro.

### Teste "sem dado privado" (obrigatório antes de todo pull request)

A skill nunca pode ter nome real de empresa ou de pessoa, ID de conta de anúncios, e-mail, telefone, caminho de arquivo local ou token. Rode o comando da seção em inglês acima na raiz do repositório e revise cada resultado. Procure também o nome da sua empresa, dos seus clientes, do seu CRM e dos colegas. Use exemplos neutros (`ACME`, `Vila Verde`, `R$ 4.200`).

### Como reportar erro em política da Meta

A Meta muda políticas com frequência; este é o tipo de relato mais útil.

1. Abra uma issue com o modelo **"Outdated content / Meta policy error"**.
2. Diga o arquivo e a linha, o que a skill diz, o que a Meta diz hoje, o link oficial e a data em que leu.
3. Se viu o comportamento no Gerenciador (ex.: Moradia forçada numa campanha de catálogo), descreva **sem** ID de conta e sem captura de tela com dado pessoal.
