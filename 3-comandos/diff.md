# Diff

Passamos por todo esse processo de criar commits e entender branches, creio que tenha ficado bem claro que há um fluxo a ser seguido. Mas como vamos saber o que exatamente foi alterado nos arquivos?<br>
O comando **git diff nomearquivo.ext** consegue resolver esse problema e para entendermos melhor, iremos fazer algumas alterações no nosso projeto:

- Altere o arquivo **main.css** adicionando e editando as linhas descritas abaixo;
- Utilize o comando **"git diff main.css"** para ver as alterações criadas.

```css
/*
   Arquivo: ./main.css
*/
body {
  background-color: mediumpurple;
  color: red;
}
p {
  color: blue;
}
```

```
$ git diff main.css
diff --git a/main.css b/main.css
index 85d348e..2cfe522 100644
--- a/main.css
+++ b/main.css
@@ -1,4 +1,8 @@
 body{
     background-color:mediumpurple;
-    color:white;
+    color:red;
+}
+
+p{
+    color:blue;
 }
```

Agora vamos para uma breve interpretação do retorno acima:

- Ele está comparando com o último commit feito no mesmo arquivo;
- O sinal "+" significa tudo que foi ADICIONADO ao documento;
- O sinal "-" significa tudo que foi REMOVIDO do document.

Uma coisa interessante de saber é que se você adicionar o arquivo com o **"git add"** e tentar usar o **"git diff"** no mesmo arquivo, você não verá as alterações pois elas já estão prontas para serem commitadas.

Ir para: [3.7. Tag](tag.md) 