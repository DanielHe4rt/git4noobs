# Clone

Simplificado: _Baixar uma cópia completa de um repositório_ <br><br>
Até agora vimos o `git init`, que cria um repositório **novo e vazio**. Mas no dia a dia, o mais comum é você entrar em um projeto que **já existe** - seja no trabalho, em um projeto open source, ou em um repositório que você acabou de dar fork no GitHub.

Para isso usamos o comando **git clone**, passando a URL do repositório:

```bash
git clone https://github.com/usuario/nome-do-repositorio.git
```

Isso vai:

1. Criar uma pasta com o nome do repositório;
2. Baixar todo o histórico de commits, branches e tags;
3. Configurar automaticamente o repositório remoto chamado `origin`, apontando para a URL clonada (veremos mais sobre isso em [Remote](remote.md)).

Se quiser clonar em uma pasta com outro nome:

```bash
git clone https://github.com/usuario/nome-do-repositorio.git meu-projeto
```

## HTTPS vs SSH

Você vai notar que o GitHub oferece duas URLs para clonar:

```bash
# HTTPS - pede usuário/token (ou abre o navegador) ao fazer push
git clone https://github.com/usuario/nome-do-repositorio.git

# SSH - usa uma chave configurada na sua máquina, sem pedir senha depois
git clone git@github.com:usuario/nome-do-repositorio.git
```

No começo, HTTPS costuma ser mais simples. Conforme você for fazer `push` com frequência, vale configurar uma chave SSH para não precisar autenticar a cada envio.

Ir para: [3.2. Config](config.md)
