# Tag

Este comando é utilizado para criar as versões do seu projeto.

O formato padrão para uma tag é Vx.y.z, sendo:

* v -> sigla para a palavra versão.
* x -> chamada de **Major**. Representa a versão principal do projeto.
* y -> chamada de **Minor**. Representa a adições de novas funcionalidades.
* z -> chamada de **Patchs**. Representa correções de bugs no sistema.

## Opções

### Gerar tag lightweight (non-annotated)

```sh
git tag v1.0.0
```

Cria uma tag `lightweight`, que é apenas um **ponteiro/referência direta** para o commit atual, sem nenhuma informação extra (sem autor, data ou mensagem própria).

---

### Gerar tag annotated

```sh
git tag -a v1.0.0 -m "Versão 1.0.0"
```

Cria uma tag `annotated`, que também aponta para o commit, mas é armazenada como um objeto completo no Git, guardando **mensagem própria, autor e data**. Por isso é a forma recomendada para marcar versões/releases.

---

### Apagar uma tag

```sh
git tag -d v1.0.0
```

Apaga a tag no seu git local.

Ir para: [3.9. Rebase](rebase.md)
