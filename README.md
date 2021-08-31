# De "Pessoa que Programa" para "Programador"

  A ideia não é ser uma lista exaustiva, mas sim um guia de boas práticas que serão úteis mesmo se você quiser ser apenas "alguém que programa".

## Porque eu falo "pessoa que programa"?

  Segundo o [Uncle Bob](https://www.youtube.com/playlist?list=PLo61EKto8ZPHUOld83z0pwpzdlioliu6j) para ser um profissional precisamos "professar" alguma coisa, mas é fácil ver por aí um monte de gambiarras e códigos mal escritos.
  
  Existem [lugares dedicados](https://www.reddit.com/r/ProgrammerHumor/) a fazer graça disso.
  
  Assim como não chamamos uma pessoa que faz um castelo de areia de arquiteto ou engenheiro, podemos chamar alguém de que não tem cuidado com o código de programador?

  Muitas pessoas não querem se tornar programadoras, e isso não é um problema!
  Mas assim como você olha chefs no youtube para aprender receitas novas e maneiras melhores de cozinhar, aprender com programadores profissionais vai te ensinar muita coisa e deixar, seja lá o que for fazer, muito melhor.

## Não leve tudo o que vou colocar abaixo como verdades

> **Primeiro é preciso conhecer as regras para depois quebrá-las.**
>
> &mdash; *David B. Agus*

## Assuntos

### GIT

O Git serve para que você possa ter todas as alterações feitas em cada arquivo e dentro do projeto em uma linha do tempo onde você possa "rebobinar" o arquivo até qualquer versão que desejar.

GIT é padrão da indústria e será muito difícil fugir dele. Vale a pena aprender mesmo caso não vá usar ele.

#### Boas práticas para trabalhar com mais pessoas

- Bloqueie a main/master contra commits. Na master só PR!
- Uma branch "develop" é algo interessante para ir jogando e puxando as alterações.
  - Só jogue nessa branch código que funciona!
  - Prefira PR menores, se já está funcionando está na hora de fazer um PR.
- Cada feature diferente deveria ficar em uma branch separada.
  - Se mais pessoas estão trabalhando na mesma feature, cuidado com os conflitos de merge.
  - Uma branch adicional para jogar e puxar as alterações pode ajudar a evitar conflitos de merge.

#### Padrões de Commits

- Commits precisam ter uma mensagem significativa relacionado ao que está sendo alterado.
- Prefira commits *atômicos*:
  - Terminou uma função? Comite!
  - Terminou um teste? Comite!
  - Refatorou uma nomenclatura? Comite!
  - É só uma linha? Não importa! Comite!
  - Commits menores são melhores de se verificar e manter controle.
    - Também são mais fáceis de escrever uma boa mensagem significativa.
- Coisas a não fazer:
  - "Pequenas mudanças" ou "aasddasfdfdsfsfa" não. Simplesmente não.
  - Commit de 9999 linhas não.
    - Primeiro: tem gente esperando enquanto você cria esse monstro.
    - Segundo: provavelmente você pode quebrar isso em pedacinhos menores e ir comitando pedaço a pedaço.
- Convenções de commits:
  - [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/)
  - [Gitmoji](https://gitmoji.dev/)
  - Usar os dois, ou nenhum:
    - Mais importante é o ***time*** ter uma convenção, seja ela qual for e seguir ela.

### Testes

#### porque fazer
#### soft vs hard (software)

### Tive problemas, e agora?

#### Leia os erros
#### Leia a documentação
#### Stackoverflow guidelines

### Clean Code

#### Nomes descritivos
#### Regra do escoteiro
#### Overenginering
#### Não abstrair de mais
#### Numeros Magicos

#### "Siglas"

##### DRY
##### KISS
##### SOLID
##### YAGNI

## Senti falta de alguma coisa ou acho que existem erros

Só deixar um [PR](https://www.youtube.com/watch?v=U-Y_Mtdyo74&ab_channel=WillianJustenCursos) ou abrir uma [issue](https://www.youtube.com/watch?v=WpA2NXdfkNQ&ab_channel=DevSuperior)!
