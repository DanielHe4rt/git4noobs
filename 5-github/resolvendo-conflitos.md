# Resolvendo conflitos

Simplificado: _Quando duas pessoas alteram a mesma linha e o Git não sabe qual manter_ <br><br>
Conflito de merge é, sem dúvidas, o momento que mais gera pânico em quem está começando. A boa notícia: **é normal**, acontece com todo mundo, e o Git nunca apaga código sozinho - ele só pausa e pede para você decidir.

## Por que acontece?

Um conflito surge quando o Git tenta juntar (`merge`, `pull` ou `rebase`) duas branches que alteraram **a mesma região do mesmo arquivo** de formas diferentes. O Git consegue juntar automaticamente alterações em partes diferentes de um arquivo (ou em arquivos diferentes) - o problema é só quando as duas versões "disputam" a mesma linha.

## Como aparece

Ao rodar `git merge` (ou `git pull`, que faz merge por trás dos panos):

```
$ git merge feature/cadastro-de-clientes
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
```

O Git **não cancela nada** - ele marca os trechos conflitantes diretamente no arquivo:

```html
<<<<<<< HEAD
<h1>Bem-vindo ao sistema</h1>
=======
<h1>Bem-vindo(a) ao nosso sistema!</h1>
>>>>>>> feature/cadastro-de-clientes
```

- O que está entre `<<<<<<< HEAD` e `=======` é a versão da branch em que você está (destino do merge);
- O que está entre `=======` e `>>>>>>> nome-da-branch` é a versão que está sendo trazida.

## Passo a passo para resolver

1. Abra o(s) arquivo(s) listados como conflito (`git status` mostra todos eles em "Unmerged paths");
2. Decida o que ficar: a versão de cima, a de baixo, uma combinação das duas, ou algo totalmente novo;
3. **Apague as marcações** `<<<<<<<`, `=======` e `>>>>>>>` - deixe apenas o código final;
4. Marque o arquivo como resolvido:

```bash
git add index.html
```

5. Finalize o merge com um commit (o Git já sugere uma mensagem padrão):

```bash
git commit
```

Se o conflito aconteceu durante um `git pull`, depois de resolver e commitar, finalize enviando suas alterações:

```bash
git push
```

## Em ferramentas visuais

O VSCode (e a maioria dos editores modernos) detecta automaticamente os arquivos em conflito e mostra botões como **"Accept Current Change"**, **"Accept Incoming Change"**, **"Accept Both Changes"** ou **"Compare Changes"** acima de cada trecho conflitante - você raramente precisa editar as marcações `<<<<<<<` manualmente.

## E se eu quiser desistir e voltar pro estado anterior?

```bash
git merge --abort
```

Isso cancela o merge em andamento e devolve seus arquivos para como estavam antes de você tentar o merge - sem perder nenhum commit já feito.

## Conflitos em Pull Requests

A lógica é exatamente a mesma, só muda onde você resolve: o GitHub avisa "This branch has conflicts that must be resolved" no próprio PR. Você resolve **localmente** (atualizando sua branch com a `main` via `git pull origin main` ou `git merge main`, resolvendo como descrito acima, e fazendo `git push`), e o PR atualiza automaticamente.

## Como evitar conflitos grandes

- Mantenha sua branch **atualizada com a main com frequência** (`git pull` / `git merge main` diariamente, não só no final);
- PRs pequenos e de vida curta diminuem a chance (e o tamanho) dos conflitos;
- Combine com o time quem está trabalhando em quais arquivos/áreas do código.

Ir para: [5.4. Code Review](code-review.md)
