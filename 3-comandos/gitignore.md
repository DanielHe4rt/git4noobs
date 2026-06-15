# .gitignore

Simplificado: _Lista de "não me siga"_ <br><br>
Todo projeto tem arquivos que **não devem** ir para o repositório: senhas, chaves de API, pastas de dependências (`node_modules`, `vendor`), arquivos de build, configurações pessoais do seu editor, logs, etc.

Se você rodar um `git add .` sem cuidado, todos esses arquivos entram no commit e acabam no histórico do projeto - inclusive em repositórios públicos no GitHub, o que pode expor senhas e chaves de acesso.

Para evitar isso, criamos um arquivo chamado **.gitignore** na raiz do projeto, listando o que o Git deve ignorar.

```
$ touch .gitignore
```

Dentro dele, cada linha representa um padrão de arquivo ou pasta a ser ignorado:

```gitignore
# Dependências
node_modules/
vendor/

# Variáveis de ambiente e segredos
.env
.env.*
*.pem

# Build
dist/
build/

# Logs
*.log

# Configurações do editor/IDE
.vscode/
.idea/
```

## Pontos importantes

- O `.gitignore` só funciona para arquivos **ainda não rastreados** pelo Git. Se um arquivo já foi commitado antes de entrar no `.gitignore`, ele continuará sendo monitorado - é necessário remover do controle de versão com:

```bash
git rm --cached caminho/do/arquivo
```

- Existem modelos prontos de `.gitignore` para praticamente toda linguagem/framework no site [gitignore.io](https://www.toptal.com/developers/gitignore) ou no repositório oficial [github/gitignore](https://github.com/github/gitignore).
- **Nunca** suba arquivos `.env`, credenciais, tokens ou chaves privadas para o repositório, mesmo que ele seja privado.

Ir para: [3.5. Commit](commit.md)
