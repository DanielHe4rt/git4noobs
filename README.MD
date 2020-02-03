# Git4Noobs

Aula de Git de um jeito simples ao profissional para iniciantes.

## 1. Sobre o projeto

A ideia é ensinar para os usuários iniciantes que o Git não é nenhum "monstro" de se aprender e também ensinar como usar num ambiente onde há mais de um desenvolvedor atuando no projeto sem desorganizar ou perder algum traço de código no processo. 

## 2. Pré-requisitos 

Bom, só precisamos que você tenha o Git instalado na sua máquina. Aqui vai como você pode baixar:


- ### 2.1 Linux (Base Debian)
    Apenas execute o comando abaixo no seu terminal e a magica vai estar feita: 
    ```
    sudo apt install git 
    ```
- ### 2.2 Windows
    Vá até o site [Git SCM](https://git-scm.com/downloads) e faça download da versão mais atualizada e siga os passos do instalador.<br>
    Ao terminar o download você terá o app Git Bash instalado no seu Windows pronto para uso.

## 3. O que é git?

### 3.1 Primeiro Exemplo
Git é um sistema de controle de versão de arquivos. Através deles podemos desenvolver projetos na qual diversas pessoas podem contribuir simultaneamente no mesmo, editando e criando novos arquivos e permitindo que os mesmos possam existir sem o risco de suas alterações serem sobrescritas.

### 3.2 Segundo Exemplo
Git é um sistema de controle de versões distribuído, usado principalmente no desenvolvimento de software, mas pode ser usado para registrar o histórico de edições de qualquer tipo de arquivo. Cada diretório de trabalho do Git é um repositório com um histórico completo e habilidade total de acompanhamento das revisões, não dependente de acesso a uma rede ou a um servidor central. 

## 4. Glosário

### 4.1 - Repositório
Simplificado: *Pasta do Projeto* <br><br>
Isso ai mesmo que você está lendo. Repositório é a pasta raiz do seu projeto e não é nenhum tipo de item mágico lvl 99 que você só consegue depois de zerar algum jogo.<br><br>
Crie uma pasta vazia e digite o comando **git init**:

```shell script
$ mkdir git4noobs
$ cd git4noobs
$ git init

Initialized empty Git repository in ~/git4noobs/.git/
```
Simples, não é mesmo?!

### 4.2 - Commit
Simplificado: *Registro de um diário* <br><br>
Um dos problemas mais mundanos no desenvolvimento de software, é que com o dado tempo de um projeto em andamento, as pessoas começam a esquecer o quê e o porquê estão fazendo aquilo.
Enquanto você trabalha em um projeto, você pode editar e salvar arquivos no seu repositório quantas vezes você quiser. E em certo ponto, você decidir **commitar** suas alterações para o seu repositório.   

Vamos dar um exemplo abaixo (no CLI e exemplo visual):
* Crie um arquivo na raiz do seu projeto (Repositório) chamado index.html e adicione algum conteúdo a ele
* Logo após adicione o arquivo criado a lista de alterações com o comando git add nomearquivo
* Crie um novo registro (commit) repositório
```
echo "Hello Rocket Devs" > index.html 
git add index.html
git commit -m "inserção de index.html"
```
![x](./images/commit1.png)

Em um certo ponto, você percebe que cometeu algum erro ao subir essa alteração no seu projeto. Agora você tem duas opções: reverter ou sobrescrever.<br>
Nesse caso, eu irei sobrescrever a alteração para manter o registro anterior no nosso repositório com os passos abaixo:
* Altere o texto da sua index.html para "Hello He4rt Devs"
* Salve o arquivo e adicione a lista de alterações com o comand git add nomearquivo
* Crie um novo registro (commit) no seu repositório com uma descrição usando o comando git commit -m "alteração index.html"
```
echo "Hello He4rt Devs" > index.html 
git add index.html
git commit -m "alteração de index.html"
```
![x](./images/commit2.png)
Após fazer a alteração, podemos ver que foi adicionado outro registro em nosso repositório, uma nova entrada na qual está marcada as alterações mais recentes e com os registros anteriores guardados e documentados igualmente.

Um commit significa a adição/alteração/remoção de um ou mais arquivos dentro do seu repositório.

### 4.3 - Branch
Simplificado: *Universo Paralelo* <br><br>
Podemos dizer que a branch é um universo ou uma realidade alternativa onde em algum ponto irá se juntar com a realidade principal. Achou esse exemplo estranho? Então deixa eu te mostrar uns exemplos.<br><br>
Pense em um cenário onde seu time encontra um problema que precisa ser resolvido, porém nem sempre há apenas uma única solução para finalizar essa tarefa, certo? É ai que a branch entra para ajudar nessa organização entre os devs.<br>
Continuando nesse cenário hipotético, os desenvolvedores irão criar uma nova vertente do código partindo da branch **master** (branch princial gerada a partir do primeiro commit), assim criando a branch solucao-a.
```
$ git checkout -b implementacao-css
Switched to a new branch 'implementacao-css'

$ git branch
  master
* implementacao-css
``` 
![x](./images/branches1.png)

Podemos ver que agora estamos em um outro universo diferente do principal (master) e toda e qualquer alteração feita nessa nova branch não afetará nenhuma outra dentro do projeto.<br><br>
Tá, mas o que eu faço com essa branch? A ideia é você ter liberdade para criar coisas novas sem alterar onde está tudo funcionando (master).<br>
Vamos fazer algumas alterações no nosso projeto dentro dessa nova branch:
* Crie um novo arquivo na raiz do projeto chamado main.css
* Commite esse arquivo com a mensagem "criação de arquivo main.css"

```
touch main.css 
git add main.css
git commit -m "criação de arquivo main.css"
```
Após isso iremos fazer outro commit para adicionar uma regra css simples a esse arquivo. Apenas entre no arquivo criado e adicione alguma regra a tag body:
```css
./main.css

body{
    background-color:mediumpurple;
    color:white;
}
```
Salve o arquivo arquivo alterado com os mesmos comandos feitos anteriormente e faça mais um commit:
```
git add main.css
git commit -m "adicionando regras para o main.css"
```

Podemos ver na imagem abaixo que há duas linhas de tempo diferentes que não se conflitaram (até momento) e podem ser alteradas ninguém atropelar o código de nenhum dos outros desenvolvedores do projeto, evitando conflitos e sempre mantendo tudo que é feito documentado dentro do repositório.

![imagem listando as branches](images/branches2.png) 

### 4.4 - Merge
Simplificado: *Fusão de permanente duas branches* <br><br>

## x. Materiais utilizados

* [Wikipedia](https://pt.wikipedia.org/wiki/Git) - Git
* [Tableless](https://tableless.com.br/tudo-que-voce-queria-saber-sobre-git-e-github-mas-tinha-vergonha-de-perguntar/) - Tudo que você queria saber sobre Git e GitHub, mas tinha vergonha de perguntar
* [Medium](https://medium.com/faun/learn-git-in-13-words-part-1-of-3-45e83db145fd) - Aprenda Git em 13 palavras (Inglês)

## Autores

* **Daniel Reis (danielhe4rt)** - *Back-end Developer && He4rt Developers Leader* - [Portfólio](https://danielheart.dev) - [Twitter](https://twitter.com/danielhe4rt)
* **Anna Campelo (Annerland)** - *Front-end Developer && Melhor pessoa* - [Portfólio](https://github.com/AnnaCampelo) - [Twitter](https://twitter.com/danielhe4rt)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
