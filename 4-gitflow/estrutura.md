# Estrutura de um Git Flow

Quando você começa a estudar um tipo de GitFlow, a primeira coisa a se entender são as responsabilidades de cada tipo de branch.
Entenda o Gitflow como uma hierarquia a ser seguida, onde você não pode pular nenhum processo ou irá gerar algum tipo de conflito em certo ponto. <br>

Vamos analisar a lista de branches abaixo:

```
Master─────────────────────Hotfix
│
└──────Releases────────────Bugfix
       │
       └─────Develop───────Bugfix
             │
             └─────Features
                   │
                   └───────Tasks
```

Podemos ver as branches em cascata, que sempre partem de uma tarefa e vão subindo gradualmente até chegarem na branch principal (master). Tá, mas o que quer dizer cada uma dessas branchs? Segue a função de cada branch abaixo:

- Master - branch responsável pelo ambiente que roda em Produção

- Hotfix(es) - responsável por corrigir algum erro critico que impeça o cliente de executar alguma função em ambiente de produção.

- Releases - responsável por gerenciar e documentar todas as alterações feitas a cada deploy

- Bugfix(es) - responsável por corrigir bugs pequenos em ambiente de desenvolvimento (develop) ou homologação (release).

- Develop - branch onde sempre será criada e/ou mergeadas novas features

- Features - branchs responsáveis por desenvolver estórias do projeto

- Tasks - branch relacionada a uma feature (estória) descrevendo sempre um objetivo a ser trabalhado

Seguindo o projeto com esse fluxo, há maiores garantias de que ninguém no time irá atropelar ou perder código em merges falhos onde haverão conflitos.

Ir para: [4.3 Releases](releases.md)