# Extensão git-flow
Caso você, assim como eu, tenha dificuldade de lidar com merges e branches diretamente pelos comandos nativos do git, saiba que existe uma extensão que foi feita para você. 

O [git-flow](https://github.com/nvie/gitflow) é um conjunto de extensões para o git no terminal, e funciona da seguinte forma:

```
# Ao invés de rodar nativamente os comandos:

$ git checkout -b new-branch => cria a nova branch e trabalha nela
$ git checkout develop => muda para a branch de desenvolvimento
$ git merge new-branch => realiza o merge com a branch trabalhada

# Você pode simplesmente rodar o comando:
$ git flow feature start my-feature => cria uma branch chamada feature/my-feature
$ git flow feature finish my-feature => muda para a branch develop e realiza o merge automaticamente
```

Podemos dessa forma ver que essa extensão realmente facilita algumas coisas (algumas delas que não são tão complicadas, mas ainda assim tornam nosso dia a dia mais produtivo).

Caso você tenha interesse em utilizar essa extensão, veja o [tutorial de instalação](git-flow-instalacao.md) e o [tutorial de comandos](git-flow-comandos.md).


Ir para: [4.6 Padrão de Commits](padrao-commit.md)