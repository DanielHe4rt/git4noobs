# Merge

Simplificado: _Fusão de duas branches_ <br><br>
Quando algum desenvolvedor falar de **merge**, quer dizer que houve uma fusão ou junção de códigos em uma única branch. Tá, mas como assim?<br>
Vamos continuar na nossa situação hipotética dos commits acima, já que temos duas branches nesse repositório. Iremos criar um merge da branch **implementacao-css** para a branch **main**. Em outras palavras, vamos juntar todas as alterações feitas na branch **implementacao-css** dentro da branch **main**, mantendo a nossa main com todo o conteúdo.

```
$ git switch main
$ git merge implementacao-css
Updating 9b61048..ab4a625
Fast-forward
 main.css | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 main.css
```

![imagem listando as branches](/images/merge1.png)

Podemos ver que a main agora possui as funcionalidades da implementação-css sem precisar mexer em nada relacionado a ela, e em questão de organização você sabe onde e quando foi feito as alterações.

## E se houver conflito?

No exemplo acima o Git conseguiu juntar tudo automaticamente (fast-forward) porque a **main** não tinha recebido nenhum commit novo desde que a branch **implementacao-css** foi criada. Mas se as duas branches alterarem a **mesma linha do mesmo arquivo**, o Git não vai saber qual versão manter e vai te avisar de um **conflito de merge**. Esse é exatamente o tipo de situação que costuma assustar quem está começando — e tem um capítulo dedicado a isso em [Resolvendo conflitos](../5-github/resolvendo-conflitos.md).

Ir para: [3.6. Status](status.md)