# Dentiboom

Projeto de extensão em saúde bucal, com experiência web e mobile para distribuir conteúdo educativo de forma simples, acessível e preparada para crescer.

> Status: fundação do repositório — setembro de 2026.

## Visão do produto

O Dentiboom nasce para organizar e entregar conteúdo de educação em saúde bucal, combinando pesquisa odontológica, vídeos e uma experiência que funcione bem em dispositivos móveis. A visão inicial e as restrições técnicas foram levantadas no board do Miro:

[Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/)

O board é a referência visual do projeto. Este repositório concentra decisões versionadas, documentação executável e o código que será criado a partir delas.

## Escopo inicial

- MVP web e mobile.
- Distribuição de aplicativo Android por APK nas primeiras etapas.
- Conteúdo em vídeo com reprodução por streaming.
- Persistência local em SQLite no dispositivo móvel, quando fizer sentido para uso offline e cache.
- Infraestrutura dimensionada com cuidado para tiers gratuitos e possibilidade de alto tráfego.
- Conteúdo baseado em pesquisa odontológica e revisão do time.

O escopo acima é uma direção de trabalho, não uma especificação fechada. Decisões que exigem validação — como framework, provedor de vídeo, backend, autenticação, sincronização e publicação em lojas — permanecem explícitas na documentação para evitar premissas escondidas.

## Estado atual

O projeto está na etapa de preparação. Já foram criados:

- estrutura inicial de documentação em `docs/`;
- decisão arquitetural inicial registrada em `docs/decisoes/`;
- configuração de Node.js e pnpm para tarefas do repositório;
- formatação automatizada com Prettier;
- validação de documentação no GitHub Actions.

Ainda não há aplicação web, aplicativo mobile, API ou banco de dados implementados.

## Ambiente de desenvolvimento

Requisitos:

- Node.js `18.19.1` ou superior compatível com o projeto;
- pnpm `9` ou superior;
- Git.

Instalação:

```bash
pnpm install
```

Verificação da documentação:

```bash
pnpm docs:check
```

Formatação:

```bash
pnpm docs:format
```

## Estrutura

```text
.
├── docs/
│   ├── arquitetura.md
│   ├── plano-mvp.md
│   ├── visao-geral.md
│   └── decisoes/
│       └── 0001-escopo-e-estado-inicial.md
├── .editorconfig
├── .gitignore
├── .nvmrc
├── AGENTS.md
├── CLAUDE.md
├── CONTRIBUTING.md
├── package.json
└── README.md
```

## Documentação

- [Visão geral](docs/visao-geral.md): problema, público, objetivos e critérios de sucesso.
- [Arquitetura](docs/arquitetura.md): componentes previstos, fluxos e pontos ainda em decisão.
- [Plano do MVP](docs/plano-mvp.md): entregas em ordem de prioridade e critérios de aceite.
- [ADR 0001](docs/decisoes/0001-escopo-e-estado-inicial.md): por que o repositório começa com uma fundação neutra.
- [Como contribuir](CONTRIBUTING.md): fluxo local, documentação e convenções.
- [AGENTS.md](AGENTS.md): instruções gerais para agentes de desenvolvimento.
- [CLAUDE.md](CLAUDE.md): instruções específicas para Claude, alinhadas ao contrato do repositório.

## Próximos passos

1. Validar com o time o público prioritário e o primeiro fluxo de aprendizagem.
2. Transformar o escopo do MVP em histórias e critérios de aceite.
3. Escolher a stack web/mobile e os serviços de backend, vídeo e distribuição.
4. Criar um vertical slice pequeno: abrir conteúdo, assistir a um vídeo e registrar o progresso localmente.
5. Testar a solução com usuários e revisar as decisões técnicas antes de ampliar a infraestrutura.

## Licença

Licença ainda não definida. Não distribua o conteúdo ou o código publicamente como se houvesse uma licença permissiva até essa decisão ser registrada.
