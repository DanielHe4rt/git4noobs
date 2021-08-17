# Tag

Este comando é utilizado para criar as versões do seu projeto.

O formato padrão para uma tag é Vx.y.z, sendo:

* v -> sigla para a palavra versão.
* x -> chamada de **Major**. Representa a versão principal do projeto.
* y -> chamada de **Minor**. Representa a adições de novas funcionalidades.
* z -> chamada de **Patchs**. Representa correções de bugs no sistema.

## Opções

### Gerar tag non-annontated

```sh
git tag v1.0.0
```

Cria uma tag `non-annontated` **possui** referencia direta ao commmit que ela foi gerada.

---

### Gerar tag annotated

```sh
git tag -a v1.0.0
```

Cria uma tag `annotated` **não possui** referencia direta ao commmit que ela foi gerada, possuindo uma mensagem propria.

---

### Apagar uma tag

```sh
git tag -d v1.0.0
```

Apaga a tag no seu git local.

Ir para: [3.8. Rebase](rebase.md)
