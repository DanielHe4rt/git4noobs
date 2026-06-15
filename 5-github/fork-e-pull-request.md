# Fork e Pull Request

Simplificado: _A forma organizada de propor mudanças em um projeto_ <br><br>
Esse é provavelmente o fluxo mais importante para trabalhar em equipe no GitHub. A ideia central é: **ninguém commita direto na branch principal (`main`)**. Toda alteração passa por uma branch própria e por uma revisão antes de ser integrada.

## Cenário 1: você tem acesso de escrita ao repositório

```bash
# 1. Atualize sua main local
git switch main
git pull

# 2. Crie uma branch para a sua tarefa
git switch -c feature/cadastro-de-clientes

# 3. Trabalhe normalmente: edite, adicione, commite
git add .
git commit -m "Adiciona formulário de cadastro de clientes"

# 4. Envie sua branch para o GitHub
git push -u origin feature/cadastro-de-clientes
```

Depois do push, o GitHub mostra um botão **"Compare & pull request"**. Ao clicar:

1. Escolha a branch de destino (geralmente `main`) e a branch de origem (`feature/cadastro-de-clientes`);
2. Escreva um título e uma descrição explicando **o que** foi feito e **por quê** - isso ajuda quem for revisar;
3. Adicione revisores (colegas de time);
4. Clique em **Create pull request**.

A partir daí, qualquer novo `git push` na mesma branch atualiza automaticamente o Pull Request (PR).

## Cenário 2: Fork (você não tem acesso de escrita)

Muito comum em projetos open source ou ao contribuir com um repositório de outra organização (foi exatamente assim que este material chegou até você: via fork 🙂).

```bash
# 1. No GitHub, clique em "Fork" no repositório original.
#    Isso cria uma cópia em https://github.com/SEU_USUARIO/projeto

# 2. Clone o SEU fork (não o original)
git clone https://github.com/SEU_USUARIO/projeto.git
cd projeto

# 3. Adicione o repositório original como "upstream"
git remote add upstream https://github.com/dono-original/projeto.git

# 4. Crie sua branch, trabalhe e suba para o SEU fork (origin)
git switch -c feature/melhoria-na-documentacao
git add .
git commit -m "Adiciona seção sobre GitHub"
git push -u origin feature/melhoria-na-documentacao
```

5. No GitHub, abra o Pull Request do seu fork (`SEU_USUARIO/projeto:feature/melhoria-na-documentacao`) para o repositório original (`dono-original/projeto:main`).

Para manter seu fork atualizado com o projeto original ao longo do tempo:

```bash
git switch main
git fetch upstream
git merge upstream/main
git push origin main
```

## Boas práticas de branch e PR

- **Nomes de branch descritivos**: `feature/...`, `fix/...`, `hotfix/...`, `docs/...` - facilita identificar o objetivo só pelo nome (veja também [GitFlow](../4-gitflow/o-que-e-gitflow.md));
- **PRs pequenos e focados**: um PR que faz "uma coisa" é muito mais fácil (e rápido) de revisar do que um PR gigante que mistura várias alterações;
- **Descreva o "porquê"**, não só o "o quê" - o código já mostra o que mudou, a descrição do PR explica o motivo;
- **Não force push em branches que outros já estão revisando** sem avisar - isso pode reescrever o histórico que o revisor já viu (veja [Push](../3-comandos/push.md)).

Ir para: [5.3. Resolvendo conflitos](resolvendo-conflitos.md)
