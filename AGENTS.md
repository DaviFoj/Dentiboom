# Instruções para agentes

Estas instruções valem para todo o repositório Dentiboom. Se existir outro `AGENTS.md` em um subdiretório, as instruções mais específicas daquele diretório prevalecem.

## Contexto do projeto

O Dentiboom é um projeto de extensão em saúde bucal com experiência web e mobile. A direção inicial contempla conteúdo educativo, vídeos em streaming, distribuição de APK, SQLite local e operação cuidadosa em tiers gratuitos.

A referência visual do produto é o board [Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/). O README e a documentação em `docs/` são a referência versionada do repositório.

## Estado atual

O repositório está na fase de fundação. Ainda não há aplicação web, aplicativo mobile, API ou banco remoto implementados. A stack definitiva permanece em aberto até a escolha e validação de um vertical slice.

Não transforme hipóteses em decisões definitivas. Quando uma escolha técnica for necessária, registre o contexto, as alternativas e a consequência em um ADR dentro de `docs/decisoes/`.

## Ambiente

- Use a versão de Node indicada em `.nvmrc`.
- Instale dependências com `pnpm install`.
- Valide a documentação com `pnpm docs:check`.
- Formate a documentação com `pnpm docs:format`.
- Não adicione frameworks de web/mobile ou serviços de infraestrutura sem uma decisão explícita do projeto.

## Fluxo de trabalho

1. Leia `README.md`, `docs/visao-geral.md`, `docs/arquitetura.md` e `docs/plano-mvp.md` antes de alterar o escopo.
2. Verifique `git status` e preserve alterações existentes do usuário.
3. Faça mudanças pequenas, focadas e reversíveis.
4. Atualize a documentação quando alterar comportamento, arquitetura, escopo ou comandos.
5. Rode as validações relevantes antes de finalizar.
6. Não faça commit, push, publicação ou alteração externa sem solicitação explícita.

## Regras de produto e conteúdo

- O produto é educativo e não substitui consulta, diagnóstico ou tratamento odontológico.
- Conteúdo de saúde deve ter fonte e revisão de pessoa qualificada antes de publicação.
- Evite coletar dados pessoais desnecessários.
- Considere acessibilidade, conectividade móvel e recuperação após falhas de rede desde o início.
- Não coloque segredos, tokens, chaves de API ou dados pessoais no repositório.

## Estilo

- Escreva documentação em português claro.
- Preserve termos técnicos em inglês quando forem nomes oficiais de ferramentas ou APIs.
- Prefira nomes descritivos e mudanças compatíveis com a estrutura existente.
- Use Prettier para Markdown e mantenha os arquivos UTF-8 com final de linha LF.

## Validação mínima

Antes de concluir uma mudança de documentação ou configuração, execute:

```bash
pnpm install --frozen-lockfile
pnpm docs:check
git diff --check
```

Se a mudança adicionar código, inclua também os testes e verificações específicos desse código.
