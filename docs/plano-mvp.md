# Plano do MVP

## Estratégia

Construir um vertical slice pequeno que percorra catálogo → conteúdo → vídeo → progresso local. Cada etapa deve gerar aprendizado de produto e reduzir uma incerteza técnica.

## Fases

### Fase 0 — alinhamento

- definir público prioritário e cenário de uso;
- selecionar o primeiro conjunto de conteúdos;
- confirmar responsáveis por conteúdo, produto e tecnologia;
- transformar as hipóteses em histórias de usuário.

**Saída:** backlog priorizado e critérios de aceite.

### Fase 1 — prova de experiência

- tela inicial e catálogo;
- detalhe de um conteúdo;
- reprodução de um vídeo de teste;
- estado de carregamento, erro e retomada;
- registro de progresso local.

**Saída:** fluxo navegável em web e/ou mobile para teste interno.

### Fase 2 — fundação técnica

- contrato de dados do catálogo;
- SQLite local no mobile;
- estratégia de sincronização ou decisão explícita de não sincronizar no primeiro corte;
- pipeline de build do APK;
- ambiente de desenvolvimento reproduzível.

**Saída:** build instalável e fluxo validado em dispositivo real.

### Fase 3 — validação

- teste com usuários representativos;
- revisão odontológica e editorial;
- medição de início/conclusão de conteúdo e falhas de reprodução;
- revisão de custos e limites do provedor escolhido.

**Saída:** decisão de continuar, ajustar ou reduzir o escopo.

## Critérios de aceite do primeiro vertical slice

- o catálogo apresenta ao menos um conteúdo publicado;
- o usuário consegue iniciar e pausar um vídeo;
- o aplicativo recupera o progresso depois de ser encerrado;
- falha de rede não apaga o estado local;
- o APK pode ser gerado a partir de instruções documentadas;
- o conteúdo exibe fonte/revisão e não promete diagnóstico individual.

## Riscos e mitigação

| Risco                       | Sinal de alerta                         | Mitigação                                                  |
| --------------------------- | --------------------------------------- | ---------------------------------------------------------- |
| stack escolhida cedo demais | retrabalho entre web e mobile           | comparar um vertical slice antes de fechar a arquitetura   |
| custo de vídeo              | tráfego cresce mais rápido que usuários | estimar minutos assistidos e testar limites desde o início |
| conteúdo sem revisão        | afirmações divergentes ou absolutas     | fluxo de aprovação com responsável identificado            |
| offline complexo            | conflitos de sincronização              | começar com progresso local simples e contrato explícito   |
| escopo amplo                | muitas telas sem fluxo completo         | priorizar um caminho ponta a ponta                         |
