# Arquitetura inicial

## Status da decisão

Esta é uma arquitetura de trabalho. O board do Miro define os temas — web/mobile, APK, streaming, SQLite local e infraestrutura econômica — mas não fecha todos os provedores ou frameworks. A implementação deve validar as escolhas com um vertical slice antes de ampliar a solução.

## Visão de alto nível

```text
┌──────────────┐       ┌──────────────────┐
│ Web           │──────▶│                  │
└──────────────┘       │ API / conteúdo   │──────▶ Persistência remota
                       │                  │
┌──────────────┐       └────────┬─────────┘
│ Mobile / APK │──────▶         │
└──────┬───────┘                │
       │                        ▼
       │                 Streaming de vídeo
       ▼
 SQLite local / cache
```

Os nomes dos componentes são papéis arquiteturais, não escolhas de tecnologia.

## Componentes previstos

### Clientes web e mobile

Responsáveis por navegação, acessibilidade, reprodução de conteúdo, progresso e estados de carregamento/erro. O mobile precisa tratar armazenamento local, atualização de conteúdo e conectividade intermitente.

### API e catálogo de conteúdo

Deve expor metadados de conteúdos, módulos, vídeos e progresso. A API não deve transportar o arquivo de vídeo diretamente se um serviço de distribuição especializado atender melhor ao caso.

### Streaming de vídeo

O conteúdo audiovisual deve ser entregue por streaming adaptado ao dispositivo e à rede. O provedor, o formato, a proteção de conteúdo e os custos ainda precisam ser comparados.

### Persistência local

SQLite é a direção registrada no board para o dispositivo móvel. O modelo deve começar pequeno: catálogo sincronizado, estado de progresso e preferências necessárias ao MVP. Cache local não deve ser tratado como fonte definitiva sem uma estratégia de sincronização clara.

### Infraestrutura

O objetivo inicial é operar com baixo custo e permitir crescimento gradual. Antes de escolher serviços, medir tamanho de mídia, volume esperado, leitura/escrita, distribuição geográfica e limites dos tiers gratuitos.

## Fluxo principal do MVP

1. O usuário abre a aplicação e consulta o catálogo.
2. O cliente carrega os metadados disponíveis e mostra o estado de conectividade.
3. O usuário abre um conteúdo e inicia o vídeo.
4. O cliente registra progresso localmente.
5. Quando houver mecanismo de sincronização, o progresso é enviado à API de forma idempotente.
6. O usuário retoma o conteúdo a partir do último estado conhecido.

## Decisões ainda abertas

| Tema            | Pergunta                                                      | Critério de escolha                                    |
| --------------- | ------------------------------------------------------------- | ------------------------------------------------------ |
| Web             | Qual framework atende acessibilidade e velocidade de entrega? | produtividade, SEO se necessário e manutenção          |
| Mobile          | Qual caminho gera o APK e permite SQLite local?               | experiência offline, comunidade e build reproduzível   |
| Backend         | API própria, BaaS ou combinação?                              | custo, limites, segurança e portabilidade              |
| Vídeo           | Onde armazenar e distribuir os vídeos?                        | custo por tráfego, qualidade adaptativa e simplicidade |
| Conteúdo        | Como versionar e revisar material?                            | autoria, aprovação, fontes e publicação segura         |
| Identidade      | O MVP precisa de conta?                                       | valor real para progresso, privacidade e fricção       |
| Observabilidade | Quais eventos medir?                                          | aprendizado do produto sem coletar dados excessivos    |

## Requisitos não funcionais iniciais

- acessibilidade desde o primeiro fluxo;
- mensagens de erro úteis e recuperação após falhas de rede;
- coleta mínima de dados pessoais;
- logs e métricas sem conteúdo sensível;
- builds reproduzíveis e instruções locais documentadas;
- conteúdo de saúde revisado antes de publicação.
