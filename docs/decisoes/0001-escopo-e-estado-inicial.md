# ADR 0001 — Escopo e estado inicial do projeto

- **Status:** aceito como ponto de partida
- **Data:** 2026-09-18
- **Fonte:** board do Miro [Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/)

## Contexto

O repositório começou vazio, sem aplicação ou stack definida. O board de referência descreve uma iniciativa de saúde bucal com MVP web/mobile, APK, vídeos em streaming, SQLite local, preocupação com alto tráfego em tiers gratuitos, responsabilidades da equipe, pesquisa odontológica e decisões técnicas.

## Decisão

Começar com uma fundação neutra e versionada:

- README orientado a produto e execução;
- documentação separada para visão, arquitetura e plano do MVP;
- decisões técnicas registradas como ADRs;
- Node.js/pnpm apenas para tooling do repositório nesta etapa;
- nenhum framework web/mobile ou provedor de infraestrutura será tratado como definitivo antes de um vertical slice.

## Motivos

- evita transformar hipóteses do board em decisões irreversíveis;
- permite que produto, conteúdo e tecnologia alinhem o primeiro fluxo;
- deixa rastreável o que já foi decidido e o que ainda precisa de validação;
- prepara automação de qualidade sem introduzir dependências de runtime prematuramente.

## Consequências

Há menos código executável no início, mas o time ganha clareza sobre escopo e critérios de escolha. A próxima decisão relevante deve fechar a stack do vertical slice e incluir evidência de custo, experiência mobile e manutenção.

## Limitação da fonte

O Miro confirmou o board e sua descrição. A consulta automatizada ao conteúdo interno do board estava temporariamente indisponível durante a preparação; por isso, esta ADR usa apenas informações verificadas no nome e na descrição do board e mantém os demais itens como hipóteses a validar.
