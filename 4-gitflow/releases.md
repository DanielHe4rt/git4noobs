# Releases

O que é uma release? Uma release é o compilado de alterações feitas no sistema onde é atribuido uma tag de versionamento. Quando aparecem os numeros "1.2.15" em softwares, geralmente cada um desses digitos quer te dizer algo.

- O primeiro digito é para o breaking change release, mais conhecido como que altera toda estrutura do projeto.
- O segundo digito será para releases de projeto (compilado de novas features)
- O terceiro digito será para correção de bugfixes e alterações não agendadas referentes a release.

Quando é lançado um sistema pela primeira vez, é dado como versão 1.0.0 e a cada deploy de novas features é incrementado o segundo digito. Exemplo fictício abaixo:

```
Release: 1.2.0 (Release)
- Sistema de comentários nos posts de blog
- Sistema de comentário para usuários anonimos
- Alterações no fluxo de cadastro
Release: 1.1.2 (Bugfix)
- Correção de conflito de usuários com posts
Release: 1.1.1 (Bugfix)
- Correção de comentários duplicados em posts
Release: 1.1.0 (Release)
- Correções de bugs relacionado a login de novos dispositivos
- Sistema de Blog para usuário
Release: 1.0.0 (Breaking Change)
- Lançamento do sistema
```

Ir para: [4.4 Exemplos de GitFlow](exemplos.md)