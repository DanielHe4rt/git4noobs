# Remote

Simplificado: _O "endereço" do repositório na nuvem_ <br><br>
Tudo que vimos até agora aconteceu **apenas na sua máquina**. Mas o Git é um sistema distribuído: o mesmo repositório pode existir em vários lugares - na sua máquina, na do seu colega, e em um servidor compartilhado como GitHub, GitLab ou Bitbucket.

Um **remote** é justamente uma referência para uma dessas outras cópias do repositório. Quando você clona um projeto (veja [Clone](clone.md)), o Git já cria automaticamente um remote chamado `origin`, apontando para a URL de onde você clonou.

## Listando os remotes configurados

```bash
$ git remote -v
origin  https://github.com/usuario/nome-do-repositorio.git (fetch)
origin  https://github.com/usuario/nome-do-repositorio.git (push)
```

## Adicionando um novo remote

Útil quando você criou o repositório localmente com `git init` e agora quer conectá-lo a um repositório vazio criado no GitHub:

```bash
git remote add origin https://github.com/usuario/nome-do-repositorio.git
```

## Trabalhando com forks: origin vs upstream

Uma situação muito comum em times e em projetos open source: você faz um **fork** (sua cópia) de um repositório, clona o **seu fork**, mas também precisa acompanhar as atualizações do repositório **original**. Para isso, é comum adicionar um segundo remote chamado `upstream`:

```bash
$ git remote -v
origin    https://github.com/seu-usuario/projeto.git (fetch)
origin    https://github.com/seu-usuario/projeto.git (push)

$ git remote add upstream https://github.com/dono-original/projeto.git
$ git remote -v
origin    https://github.com/seu-usuario/projeto.git (fetch)
origin    https://github.com/seu-usuario/projeto.git (push)
upstream  https://github.com/dono-original/projeto.git (fetch)
upstream  https://github.com/dono-original/projeto.git (push)
```

Assim você pode usar `git fetch upstream` / `git merge upstream/main` para trazer as novidades do projeto original para o seu fork, sem perder a referência de onde enviar (`push`) as suas próprias alterações (`origin`). Esse fluxo é detalhado em [Fork e Pull Request](../5-github/fork-e-pull-request.md).

## Removendo ou renomeando um remote

```bash
git remote remove upstream
git remote rename origin upstream
```

Ir para: [3.13. Push](push.md)
