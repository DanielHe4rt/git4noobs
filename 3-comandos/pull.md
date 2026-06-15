# Pull

Simplificado: _Trazer as novidades do remote para o seu projeto local_ <br><br>
Enquanto você trabalha, seus colegas também estão commitando e fazendo `push` de alterações. O comando `git pull` serve para **atualizar sua branch local** com tudo que já foi enviado ao remote.

```bash
git pull origin main
```

Na prática, `git pull` é a combinação de dois comandos que você já conhece:

```bash
git fetch origin   # baixa as novidades do remote (sem alterar seus arquivos)
git merge origin/main  # mescla essas novidades na sua branch atual
```

Veja [Fetch](fetch.md) para entender melhor a primeira parte.

## Quando rodar `git pull`?

- **Antes de começar a trabalhar**, para garantir que você está partindo do código mais atualizado;
- **Antes de criar uma branch nova**, para que ela já nasça a partir da versão mais recente da `main`;
- **Antes de dar `git push`**, caso o remote tenha recebido alterações novas desde a última vez que você sincronizou (veja [Push](push.md)).

## Pull pode gerar conflitos

Como o `pull` faz um `merge` por debaixo dos panos, se você e um colega alteraram a **mesma linha do mesmo arquivo**, o Git vai pedir para você resolver o conflito manualmente antes de continuar. Isso é normal e faz parte do trabalho em equipe - veja o passo a passo em [Resolvendo conflitos](../5-github/resolvendo-conflitos.md).

## git pull --rebase

Uma alternativa ao merge automático do `pull` é pedir para o Git **reaplicar seus commits locais por cima** das novidades baixadas, mantendo o histórico mais linear (sem um commit de merge extra):

```bash
git pull --rebase origin main
```

Útil em times que preferem um histórico de commits mais "limpo", mas exige mais atenção ao resolver conflitos (veja [Rebase](rebase.md)).

Ir para: [3.15. Fetch](fetch.md)
