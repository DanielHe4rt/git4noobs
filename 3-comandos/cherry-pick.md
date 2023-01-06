# Cherry Pick

O git cherry pick é um comando poderoso do Git que permite ao usuário selecionar commits específicos para trazer ao branch desejado.

Imagine o seguinte caso, você está trabalhando na branch de cadastro de pessoas administradoras, e outra pessoa desenvolvedora do seu time está trabalhando em uma outra branch relacionada a cadastro de users.

Nesse trabalho, a outra pessoa acaba encontrando um problema que atinge vocês dois, e faz a correção, mas a task dele ainda está em andamento.

Sendo assim, você não pode fazer o merge, mas você precisa da correção.

O Cherry pick veio para nos ajudar nesse problema! No caso da task ainda estar em andamento, ele consegue pegar um commit e copia-lo de uma branch para a outra.

## Funcionamento

Para fazer essa copia basta você ter em mãos o id do commit da outra branch e rodar o comando: ``git cherry-pick {id do commit aqui}``

Exemplo: ``git cherry-pick f13bd3c3531f26e805c606729857f39987a2420f``

Claro, em alguns momentos você pode querer obter também um intervalo de commit, e o comando permite você fazer isso.

Nesse primeiro caso, temos o exemplo onde a gente copia todos os commits do id "A" até o id "B", incluindo o A: ``git cherry-pick A^..B``

No Segundo caso a gente ignora o primeiro commit "A", e pega todos, incluindo o "B": ``git cherry-pick A..B``

Se você quiser ver um exemplo prático sobre, você pode encontra nesse vídeo aqui: [Como pegar apenas um Commit de outra Branch - Cherry Pick](https://youtu.be/Wi1vdL57gd0)