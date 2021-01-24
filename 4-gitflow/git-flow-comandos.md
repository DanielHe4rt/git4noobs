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

## Versões/releases

Auxilia a preparação de uma nova versão de produção, e permite correções de bugs menores e a preparação de metadados de uma versão.

### Começar uma versão

```
$ git flow release start RELEASE [BASE]

# Você pode opcionalmente fornecer um hash sha-1 do commit [BASE] de onde começar a versão.
# O commit precisa estar no branch 'develop'.
```

Esse comando cria um novo branch da versão baseado no `develop` e alterna para ele.

É sensato publicar o branch da versão depois de criá-lo, para permitir commits por outros desenvolvedores. É semelhante à publicação de uma funcionalidade com o comando:

```
$ git flow release publish RELEASE

# Você também pode acompanhar uma versão remota com o comando:

$ git flow release track RELEASE
```

### Finalizar uma versão

```
$ git flow release finish RELEASE
```

Finaliza a versão. Esse comando mescla o branch da versão na `master`, etiqueta a versão com seu nome, mescla o branch da versão de volta no `develop` e remove o branch da versão.

## Hotfixes

Os hotfixes surgem da necessidade de agir imediatamente sobre uma situação indesejada na versão de produção ativa.

Pode ser criado a partir da tag correspondente no branch master que indica a versão em produção.

### Começar um hotfix

```
$ git flow hotfix start VERSION [BASENAME]
```

### Finalizar um hotfix

```
$ git flow hotfix finish VERSION
```

Ao finalizar um hotfix ele é mesclado tanto no develop quanto no master. 

Além disso, o merge no master é etiquetado.