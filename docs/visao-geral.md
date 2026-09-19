# Visão geral

## Contexto

O Dentiboom é um projeto de extensão em saúde bucal. A proposta inicial é aproximar informação odontológica confiável do público por meio de uma experiência digital simples, com suporte a web, mobile e conteúdo audiovisual.

Esta visão foi consolidada a partir do board do Miro [Saúde Bucal — Arquitetura e Projeto](https://miro.com/app/board/uXjVHmbV2ho=/), cuja descrição aponta para um MVP web/mobile, distribuição de APK, streaming de vídeos, SQLite local, preocupação com alto tráfego em tiers gratuitos, responsabilidades da equipe e pesquisa odontológica.

## Problema a resolver

Pessoas precisam encontrar, entender e revisitar orientações de saúde bucal em um formato acessível e adequado ao uso cotidiano no celular. O projeto deve reduzir a distância entre conteúdo educativo revisado e a prática de aprendizagem do usuário.

## Público inicial

O público exato ainda precisa ser priorizado com o time. Até essa validação, a documentação considera como hipóteses:

- pessoas buscando educação básica em saúde bucal;
- estudantes ou participantes de ações de extensão;
- educadores e profissionais que apoiem a curadoria do conteúdo.

Essas hipóteses não substituem pesquisa com usuários.

## Objetivos do MVP

- apresentar uma sequência curta de conteúdos educativos;
- permitir assistir a vídeos com carregamento compatível com conexões móveis;
- manter parte do estado local para reduzir dependência de conectividade;
- entregar uma primeira experiência Android distribuível por APK;
- medir uso suficiente para aprender quais conteúdos e fluxos têm valor.

## Fora do MVP, salvo decisão posterior

- diagnóstico ou recomendação clínica individual;
- substituição de consulta ou atendimento odontológico;
- marketplace, teleatendimento ou prontuário;
- gamificação complexa antes de validar o fluxo de aprendizagem;
- arquitetura distribuída de alta complexidade sem evidência de necessidade.

## Princípios

1. **Educação antes de complexidade:** cada funcionalidade deve melhorar compreensão, acesso ou continuidade do aprendizado.
2. **Segurança e responsabilidade:** conteúdo de saúde precisa de revisão, fonte e linguagem cuidadosa.
3. **Mobile primeiro:** conexão, armazenamento e tamanho dos arquivos importam.
4. **Decisões explícitas:** o que ainda é hipótese deve permanecer marcado como hipótese.
5. **Evolução incremental:** validar um fluxo completo antes de expandir a plataforma.

## Critérios de sucesso iniciais

- uma pessoa consegue encontrar e concluir um conteúdo sem ajuda;
- o vídeo inicia em uma conexão móvel realista;
- o progresso local é preservado após fechar e reabrir o aplicativo;
- o time consegue publicar uma atualização de conteúdo sem alterar o aplicativo inteiro;
- uma rodada de testes produz evidências para priorizar a próxima iteração.
