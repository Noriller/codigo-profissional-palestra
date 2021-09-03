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

*Soft*ware, macio, maleável. Diferente de *hard*ware (e também de *firm*ware), que são duros, firmes.

Software deveria ser fácil de mexer, modificar. Poder alterar deveria ser tão simples quanto fazer pela primeira vez.

#### Porque testar

Testes normalmente são quebrados em testes exploratórios, testes ponta-a-ponta, testes de integração e testes unitários.
De certa forma também é possível incluir a "análise estática", em outras palavras: Tipagem Estática.

Alguns, como o Uncle Bob talvez favoreçam mais os testes unitário, outros como o [Kent C. Dodds](https://sergioamjr.medium.com/escreva-testes-n%C3%A3o-muitos-mas-mais-de-integra%C3%A7%C3%A3o-7ebebf225516) favorecem mais os de integração. Independente disso, todos dizem a mesma coisa: **TESTE**!

#### Tipos de Testes

Embora você mexer em alguma coisa e ir ver lá se funcionou ou não é um teste, não é algo confiável.

E se o que você alterou acabou quebrando algo em um lugar que você não abriu depois?

"Testes manuais" demoram tempo, não são possiveis de serem replicados e cobrem muito pouco.

##### Tipagem Estática

Linguagens que oferecem a tipagem estática possuem uma camada adicional de segurança, pois antes mesmo de rodar o código já é possivel pegar erros como que não existe uma propriedade ou método em um objeto ou que o retorno é de um tipo diferente do esperado.

##### Testes Unitários

São os testes que cobrem apenas a menor fração possível do código, seja uma função, método ou classe.

São também os mais rápidos de rodar e mais baratos de realizar.

##### Testes de Integração

Testes de integração cobrem a ligação entre as menores frações. Duas funções podem funcionar perfeitamente sozinhas, mas pode haver uma quebra quando uma chama a outra.

O exemplo mais comum é o do guarda chuva, o botão funciona, a tela se abre, a haste se estica... mas na hora que tentamos abrir o guarda chuva "em produção" tudo funciona como deveria... exceto que você fica só com a guarda e haste na mão enquanto a tela sai voando (mas a tela está aberta como deveria).

Neste ponto é bom ver a visão que está na [Testing Library](https://testing-library.com/):

> Quanto mais seus testes se assemelharem à maneira como o software é usado, mais confiança eles podem lhe dar.
>
> &mdash; *Kent C. Dodds*

##### Testes Ponta-A-Ponta

São os testes que cobrem de ponta a ponta.

Eles não precisam cobrir todos os caminhos possíveis, especialmente se há uma cobertura disso dos outros testes. Eles normalmente correm nos caminhos mais importantes testando o fluxo da aplicação como um todo.

São os mais caros, lentos e mais voláteis, mas são parte importante da suíte de testes.

##### Testes Exploratórios

Estes normalmente são feitos de forma a testar os limites da aplicação.

Entre outros: testes de penetração, testes de mutação, testes de carga, etc.

#### TDD

É uma disciplina onde você escreve os testes **ANTES** de escrever o código.

Dessa forma o teste já nasce testado e, normalmente, acaba gerando um código mais desacoplado, melhorando a qualidade do próprio código.

Para saber mais veja [aqui](wiki/As_Tres_Leis_do_TDD.md)

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
#### Refatorar

#### "Siglas"

##### DRY
##### KISS
##### SOLID
##### YAGNI

## Senti falta de alguma coisa ou acho que existem erros

Só deixar um [PR](https://www.youtube.com/watch?v=U-Y_Mtdyo74&ab_channel=WillianJustenCursos) ou abrir uma [issue](https://www.youtube.com/watch?v=WpA2NXdfkNQ&ab_channel=DevSuperior)!
