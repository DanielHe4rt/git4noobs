# Commit

Simplificado: _Registro de um diário_ <br><br>
Um dos problemas mais mundanos no desenvolvimento de software, é que com o dado tempo de um projeto em andamento, as pessoas começam a esquecer o quê e o porquê estão fazendo aquilo.
Enquanto você trabalha em um projeto, você pode editar e salvar arquivos no seu repositório quantas vezes você quiser. E em certo ponto, você decidir **commitar** suas alterações para o seu repositório.

Vamos dar um exemplo abaixo (no CLI e exemplo visual):

- Crie um arquivo na raiz do seu projeto (Repositório) chamado `index.html` e adicione algum conteúdo a ele
- Logo após adicione o arquivo criado a lista de alterações com o comando `git add nomearquivo`
- Crie um novo registro (commit) repositório

```
echo "Hello Rocket Devs" > index.html
git add index.html
git commit -m "inserção de index.html"
```

![x](/images/commit1.png)

Em um certo ponto, você percebe que cometeu algum erro ao subir essa alteração no seu projeto. Agora você tem duas opções: reverter ou sobrescrever.<br>
Nesse caso, iremos sobrescrever a alteração para manter o registro anterior no nosso repositório com os passos abaixo:

- Altere o texto da sua index.html para "Hello He4rt Devs"
- Salve o arquivo e adicione a lista de alterações com o comand `git add nomearquivo`
- Crie um novo registro (commit) no seu repositório com uma descrição usando o comando `git commit -m "alteração index.html"`

```
echo "Hello He4rt Devs" > index.html
git add index.html
git commit -m "alteração de index.html"
```

![x](/images/commit2.png)

Após fazer a alteração, podemos ver que foi adicionado outro registro em nosso repositório, uma nova entrada na qual está marcada as alterações mais recentes e com os registros anteriores guardados e documentados igualmente.

Um commit significa a adição/alteração/remoção de um ou mais arquivos dentro do seu repositório.

Ir para: [3.3. Branch](branch.md)