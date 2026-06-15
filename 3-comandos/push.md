# Push

Simplificado: _Enviar seus commits para o repositório remoto_ <br><br>
Tudo que você faz com `git commit` fica guardado **localmente**, na sua máquina. Para que seu time (ou o GitHub) veja essas alterações, você precisa **enviá-las** para o remote com o comando `git push`.

```bash
git push origin main
```

Isso envia os commits da sua branch `main` local para a branch `main` do remote `origin`.

## Primeiro push de uma branch nova

Quando você cria uma branch nova localmente (com `git switch -c minha-feature`) e faz commits nela, essa branch ainda **não existe** no remote. No primeiro push, use `-u` (ou `--set-upstream`) para vincular sua branch local à branch remota:

```bash
git push -u origin minha-feature
```

A partir daí, basta `git push` (sem mais nada) que o Git já sabe para onde enviar.

## Erros comuns

### "rejected... (fetch first)" / "non-fast-forward"

```
! [rejected]        main -> main (fetch first)
error: failed to push some refs
```

Isso significa que o remote tem commits que você ainda não tem localmente (alguém do time fez push antes de você). A solução **não é forçar o push**, e sim trazer as alterações primeiro:

```bash
git pull
# resolva eventuais conflitos (veja resolvendo-conflitos.md)
git push
```

### Nunca use `git push --force` em branches compartilhadas

```bash
git push --force origin main
```

Esse comando **sobrescreve o histórico remoto**, podendo apagar commits dos seus colegas sem aviso. Use apenas em branches pessoais (ex: sua própria branch de feature, antes de abrir o Pull Request) e, mesmo assim, prefira `git push --force-with-lease`, que falha caso alguém tenha enviado algo novo que você ainda não viu.

Ir para: [3.14. Pull](pull.md)
