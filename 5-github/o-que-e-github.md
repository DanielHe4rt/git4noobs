# O que é o GitHub?

Simplificado: _A rede social dos repositórios Git_ <br><br>
Até aqui falamos só do **Git**: a ferramenta que roda na sua máquina e versiona seus arquivos. O **GitHub** é outra coisa - é um **serviço web** que hospeda repositórios Git na nuvem e adiciona uma camada de colaboração em volta deles:

- Um lugar central para o time enviar (`push`) e buscar (`pull`) código - veja [Remote](../3-comandos/remote.md);
- **Pull Requests**: forma de propor e revisar alterações antes de irem para a branch principal;
- **Issues**: para acompanhar bugs, tarefas e ideias;
- Permissões: quem pode ler, escrever ou administrar cada repositório;
- Integrações como GitHub Actions (automação de testes, deploys, etc).

Ou seja: **Git é a ferramenta, GitHub é onde o time se encontra para usar essa ferramenta em conjunto.** Existem alternativas equivalentes, como GitLab, Bitbucket e Azure DevOps - os conceitos deste capítulo se aplicam a todas elas, apenas com nomes/telas diferentes.

## Repositório local vs repositório remoto

```
Sua máquina                         GitHub
┌─────────────────────┐            ┌─────────────────────┐
│ repositório local    │  push -->  │ repositório remoto    │
│ (git init / commits)  │ <-- pull  │ (origin)               │
└─────────────────────┘            └─────────────────────┘
```

Todo o trabalho de criar commits, branches, fazer merge, etc. continua sendo feito **localmente** com os comandos que você já aprendeu. O GitHub entra apenas no momento de **sincronizar** (`push`/`pull`/`fetch`) e no fluxo de revisão (**Pull Request**).

## Permissões básicas

Na prática, em um repositório de time você normalmente vai se encaixar em um destes cenários:

- **Você tem acesso de escrita ao repositório**: pode criar branches diretamente nele e abrir Pull Requests a partir delas.
- **Você não tem acesso de escrita** (ex: contribuindo para um projeto de outra pessoa/empresa): você precisa criar um **fork** - uma cópia do repositório na sua conta - e trabalhar nele. Veja o passo a passo em [Fork e Pull Request](fork-e-pull-request.md).

Ir para: [5.2. Fork e Pull Request](fork-e-pull-request.md)
