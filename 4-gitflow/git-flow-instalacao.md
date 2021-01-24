# Instalação do git-flow

Esse tutorial segue o [guia oficial](https://github.com/nvie/gitflow/wiki/Installation) do criador da extensão.

Para instalar a extensão, escolha abaixo o seu sistema operacional:

1. [Mac OS X](#mac-os)
2. [Linux](#linux)
3. [Windows](#windows)


<h1 id="mac-os">Mac OS X</h1>

Utilizando o Homebrew:

```
$ brew install git-flow
```

Utilizando MacPorts:

```
$ port install git-flow
```

Utilizando o wget:
```
$ wget --no-check-certificate -q -O - https://github.com/nvie/gitflow/raw/develop/contrib/gitflow-installer.sh | sudo bash
```

`wget: command not found`? Com o curl, são apenas duas linhas:
```
$ curl -L -O https://raw.github.com/nvie/gitflow/develop/contrib/gitflow-installer.sh
$ sudo bash gitflow-installer.sh
```

<h1 id="linux">Linux</h1>

Instalando no Ubuntu ou Debian:
```
$ apt-get install git-flow
```

Instalando no Archlinux:
```
$ yay -S gitflow-avh
```

Instalando no Fedora:
```
$ sudo dnf install gitflow
```

Instalando em outros Linux:
```
$ curl -OL https://raw.github.com/nvie/gitflow/develop/contrib/gitflow-installer.sh
$ chmod +x gitflow-installer.sh
$ sudo ./gitflow-installer.sh
```

<h1 id="windows">Windows</h1>

Para os usuários windows, o [Git for Windows](https://gitforwindows.org/) já inclui a extensão.

Caso não queira utilizar o Git for Windows, o Cygwin faz isso por você:

```
$ wget -q -O - --no-check-certificate https://raw.github.com/petervanderdoes/gitflow-avh/develop/contrib/gitflow-installer.sh install stable | bash
```