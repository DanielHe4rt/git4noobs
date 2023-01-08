# Config

Simplificado: _Configurações gerais_ <br><br>
Para uma boa usabilidade e um bom rendimento o **config** e uma forma de deixar suas configurações padrões do jeito que você deseja.

Imagine você e um amigo querem criar um novo projeto e precisão utiliza o git, com isso e possivel criar uma configuração na sua maquina ou no seu repositorio local do git que assine todos os commits feito por você com o seu nome tendo assim uma melhor visualização de quem fez aquele respectivo commit.

Adicionando o seu **nome** e **e-mail** nas configurações global para que o git assine os commits automaticamente.
```
$ git config --global user.name "Seu Nome"

$ git config --global user.email "Seu Email"
```

Listando todas as configurações existentes:
```
git config --list
```

Ir para: [3.3. Commit](commit.md)