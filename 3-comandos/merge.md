# Merge

Simplificado: _Fusão de duas branches_ <br><br>
Quando algum desenvolvedor falar de **merge**, quer dizer que houve uma fusão ou junção de códigos em uma única branch. Tá, mas como assim?<br>
Vamos continuar na nossa situação hipotética dos commits acima, já que temos duas branches nesse repositório. Iremos criar um merge da branch **implementacao-css** para a branch **master**. Em outras palavras, vamos juntar todas as alterações feitas na branch **implementacao-css** dentro da branch **master**, mantendo a nossa master com todo o conteúdo.

```
$ git checkout master
$ git merge implementacao-css
Updating 9b61048..ab4a625
Fast-forward
 main.css | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 main.css
```

![imagem listando as branches](/images/merge1.png)

Podemos ver que a master agora possui as funcionalidades da implementação-css sem precisar mexer em nada relacionado a ela, e em questão de organização você sabe onde e quando foi feito as alterações.

Ir para: [3.5. Status](status.md)