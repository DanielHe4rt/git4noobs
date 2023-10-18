# Add

O comando `git add` é um dos comandos fundamentais do Git e é usado para adicionar alterações do seu diretório de trabalho ao índice (também chamado de "staging area"). Em outras palavras, ele prepara as alterações para serem incluídas no próximo commit.

Aqui estão algumas formas comuns de usar o `git add`:

1. **Adicionar um arquivo específico**:
    
    ```bash
    git add nome_do_arquivo.txt
    ```
    
    Isso adiciona apenas as alterações feitas em `nome_do_arquivo.txt` ao índice.
    
2. **Adicionar vários arquivos**:
    
    ```bash
    git add arquivo1.txt arquivo2.txt
    ```
    
3. **Adicionar todos os arquivos e subdiretórios**:
    
    ```bash
    git add .
    ```
    
    Isso adicionará todas as alterações feitas em todos os arquivos e diretórios ao índice.
    
4. **Adicionar todos os arquivos modificados**:
    
    ```bash
    git add -u
    ```
    
    Isso adicionará ao índice todas as alterações feitas em arquivos já rastreados, incluindo exclusões. Arquivos novos (não rastreados anteriormente) não serão incluídos.
    
5. **Adicionar todos os arquivos (modificados e não rastreados)**:
    
    ```bash
    git add -A
    ```
    
    Essa opção combina a funcionalidade de `git add .` e `git add -u`. Ela adiciona todas as alterações feitas em todos os arquivos, sejam eles novos ou já rastreados.
    
6. **Adicionar arquivos interativamente**:
    
    ```bash
    git add -i
    ```
    
    Esse comando lança um modo interativo que permite escolher quais alterações adicionar ao índice.
    

Uma vez que as alterações são adicionadas ao índice usando `git add`, elas estão prontas para serem "commitadas" ao repositório com o comando `git commit`. Lembre-se de que o `git add` não altera o repositório até que um `git commit` seja executado. Ele simplesmente prepara as alterações, permitindo que você crie commits mais limpos e organizados.

Ir para [3.3. Commits](commit.md)
