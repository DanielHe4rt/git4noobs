# Code Review

Simplificado: _Um colega lê seu código antes dele entrar no projeto_ <br><br>
Code review é a etapa em que outra pessoa do time analisa as alterações de um Pull Request antes de aprová-lo. O objetivo não é "achar erro de quem escreveu", mas sim:

- Pegar bugs e casos esquecidos antes de chegarem em produção;
- Manter um padrão de código consistente no projeto;
- Compartilhar conhecimento - todo mundo entende um pouco do que está sendo feito;
- Ter um segundo olhar antes de mudanças irreversíveis (ex: alterações em banco de dados).

## Como funciona no GitHub

Na aba **"Files changed"** de um Pull Request, qualquer revisor pode:

- Comentar em uma linha específica do código;
- Sugerir uma alteração de código diretamente (`Suggest change`), que o autor pode aceitar com um clique;
- Marcar a revisão como:
  - **Comment**: apenas comentários, sem bloquear o PR;
  - **Approve**: aprova as alterações - dependendo das regras do repositório, isso libera o merge;
  - **Request changes**: pede ajustes antes de aprovar - o autor faz novos commits/push na mesma branch e o PR atualiza.

## Dando feedback (como revisor)

- Seja específico: "essa função pode lançar erro se `lista` vier vazia, já tratamos isso?" é mais útil que "ajustar tratamento de erro";
- Separe o que é **bloqueante** (precisa mudar antes do merge) do que é **sugestão/opinião** - muitos times usam prefixos como `nit:` (nitpick, não bloqueante) para isso;
- Elogie o que está bom também - review não é só apontar problema.

## Recebendo feedback (como autor)

- Não é pessoal - o objetivo é o código ficar melhor;
- Se não concordar com um comentário, explique seu raciocínio em vez de simplesmente ignorar ou aceitar sem entender;
- Depois de ajustar, responda os comentários (o GitHub permite marcar como "resolved") e dê push - o PR atualiza automaticamente.

## Fazendo merge do Pull Request

Depois de aprovado (e com os conflitos resolvidos, veja [Resolvendo conflitos](resolvendo-conflitos.md)), o GitHub oferece três formas de integrar o PR na branch principal:

- **Create a merge commit**: mantém todos os commits da branch + cria um commit de merge. Histórico completo, porém mais "poluído";
- **Squash and merge**: junta todos os commits do PR em **um único commit** na `main`. Histórico mais limpo, ótimo quando a branch tem muitos commits de "WIP", "ajuste", "fix typo";
- **Rebase and merge**: reaplica os commits da branch sobre a `main`, sem criar commit de merge. Mantém histórico linear, mas reescreve os hashes dos commits.

A escolha costuma ser **uma convenção do time** (geralmente combinada com a estratégia de [GitFlow](../4-gitflow/o-que-e-gitflow.md) adotada no projeto) - o importante é manter consistência.

Depois do merge, é seguro apagar a branch (o próprio GitHub oferece o botão "Delete branch"):

```bash
git switch main
git pull
git branch -d feature/cadastro-de-clientes        # apaga local
git push origin --delete feature/cadastro-de-clientes  # apaga remota (se ainda existir)
```

Ir para: [Conclusão](../conclusao.md)
