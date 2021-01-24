# Comandos do git-flow

## Inicialização

Para iniciar a extensão, rode o comando abaixo para iniciar o git-flow (se possível, faça isso assim que iniciar o git em qualquer repositório, para evitar quaisquer conflitos com nomenclaturas de branches):

```
$ git flow init
```

Você precisará responder algumas questões relativas às convenções de nomenclatura dos seus branches. É recomendado que sejam usados os valores padrões.

## Funcionalidades/features

Normalmente utilizada para desenvolver novas funcionalidades para as versões futuras.

### Começar uma nova funcionalidade:

```
$ git flow feature start MYFEATURE
```

Esse comando cria um novo branch da funcionalidade baseado no `develop` (normalmente, a branch onde se começam as features) e alterna para ele.

### Finalizar uma nova funcionalidade:

```
$ git flow feature finish MYFEATURE
```

Finaliza o desenvolvimento de uma funcionalidade. Esse comando mescla a `MYFEATURE` no `develop`, remove esse branch e volta para o `develop`.

### Publicar uma nova funcionalidade:

```
$ git flow feature publish MYFEATURE
```

Publica a branch da funcionalidade no seu servidor remoto (GitHub, GitLab, etc).

### Obter uma funcionalidade publicada

```
$ git flow feature pull MYFEATURE
```

Obtenha uma funcionalidade publicada por outro usuário e acompanhe as alterações remotas.