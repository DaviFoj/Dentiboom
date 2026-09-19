# Como contribuir

## Antes de começar

1. Instale Node.js conforme `.nvmrc`.
2. Instale as dependências com `pnpm install`.
3. Leia o [README](README.md), a [visão geral](docs/visao-geral.md) e o [plano do MVP](docs/plano-mvp.md).
4. Consulte o board [Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/) para o contexto visual.

## Fluxo de trabalho

- Crie uma branch curta a partir de `main`.
- Mantenha cada mudança focada e documente decisões que alterem escopo, dados, arquitetura ou operação.
- Rode `pnpm docs:check` antes de abrir um pull request.
- Atualize a documentação quando o comportamento ou a decisão registrada mudar.

## Convenções iniciais

- Escreva documentação em português claro, preservando nomes técnicos em inglês quando forem termos da ferramenta.
- Prefira decisões pequenas e reversíveis durante a fase de descoberta.
- Não coloque segredos, tokens, chaves de API ou dados pessoais no repositório.
- Conteúdo de saúde deve ser revisado por uma pessoa qualificada antes de ser publicado para usuários finais.

## Pull requests

Descreva o problema, a solução, os riscos e como a mudança foi validada. Para alterações de produto, inclua o impacto no MVP e a documentação correspondente.
