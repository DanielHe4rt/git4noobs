# Padronização de Commits

Em um projeto, tudo é arquitetado da melhor forma para todos terem o mesmo padrão de código e isso é relevante não só na parte de código. Pensando em uma maior facilidade para identificação de um trecho de código, elaboraremos um padrão de mensagens de commits.

## O que queremos evitar?

Commits com uma mensagem não colaborativa, ou não informativa podem confundir e atrasar a localização de certos trechos de código. Commits como:

- Fix de crud
- Feature completa
- Agora vai
- Deus abençoe funcionou

Vemos mensagens que podem conter um grande conteúdo de informações porém não temos nada que faça isso ter uma indexação e destaque sobre o que foi feito.

## Como podemos melhorar?

Colocar palavras chaves para iniciar a mensagem indicando o que foi feito de uma maneira geral. Palavras chaves como **Adiciona**, **Corrige**, **Remove** ou **Atualiza** indicariam melhor integração de um commit. Explicar minimamente o que está sendo commitado. Entenda nos exemplos abaixo:

- Adiciona novo CRUD de usuários
- Adiciona flag de administrador
- Corrige integração com API do Twitter
- Remove cards do dashboard
- Atualiza campos de registro

## Quando devemos commitar?

Commits não devem ser feito apenas quando vocês terminam algo, mas também devem ser feitas para trackear o progresso do que está sendo escrito. Padronizar e separar entre commits inteligentes, mostrando que você finalizou alguma parte da tarefa.

No exemplo abaixo iremos separar o back-end do front-end para entender como melhorar:

- Adiciona campos no formulário do login
- Atualiza novos campos a API de login

Em vez de fazer um único commit com vários arquivos indicando uma única task, você pode fazer algo mais elaborado pra conseguir identificar melhor o que foi está sendo feito.

Ir para: [Conclusão](../conclusao.md)