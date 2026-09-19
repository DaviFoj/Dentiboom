# Instruções para Claude

Este arquivo define as convenções de colaboração de Claude no repositório Dentiboom. Instruções mais específicas em subdiretórios, se existirem, complementam ou substituem estas regras.

## Projeto

Dentiboom é um projeto de extensão em saúde bucal, planejado para experiências web e mobile com conteúdo educativo, vídeos em streaming, APK e armazenamento local SQLite.

Consulte primeiro:

1. `README.md`;
2. `docs/visao-geral.md`;
3. `docs/arquitetura.md`;
4. `docs/plano-mvp.md`;
5. `AGENTS.md`, que contém o contrato operacional comum dos agentes.

O contexto visual está no board [Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/). Se o Miro não estiver disponível, use apenas informações já verificadas no repositório e marque incertezas; não invente conteúdo do board.

## Estado e decisões

O projeto ainda está na fundação. Não existem aplicações web/mobile, API ou banco remoto. A stack permanece aberta até o time validar um vertical slice.

Não escolha framework, provedor de vídeo, backend ou serviço de infraestrutura como decisão definitiva sem documentar alternativas e consequências em `docs/decisoes/`.

## Comandos

```bash
pnpm install
pnpm docs:check
pnpm docs:format
```

Use a versão de Node indicada em `.nvmrc`. Antes de trabalhar, verifique `git status` e não sobrescreva alterações existentes.

## Regras de implementação

- Faça mudanças pequenas e focadas.
- Atualize a documentação junto com mudanças de escopo, arquitetura, comandos ou comportamento.
- Não faça commit, push, deploy ou alterações externas sem pedido explícito.
- Não adicione segredos, tokens, chaves ou dados pessoais.
- Preserve acessibilidade, baixo consumo de dados e tolerância a conectividade instável.
- Trate todo conteúdo odontológico como material educativo que exige revisão qualificada e não substitui atendimento profissional.

## Qualidade

Para mudanças de documentação/configuração, rode:

```bash
pnpm install --frozen-lockfile
pnpm docs:check
git diff --check
```

Para código novo, adicione e execute testes adequados antes de concluir.
