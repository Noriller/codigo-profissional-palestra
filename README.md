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

Pegue os melhores Youtubers/Streamers/Professores de programação. 

Não importa o que eles mostram durante seus vídeos, eles também erram. E erram muito.

Você também vai errar e ter problemas. E isso é OK.

#### Leia os erros

Antes de se desesperar, leia a mensagem de erro.

Ela vai te dar informações úteis para você entender qual foi o problema e as vezes até o que falta ou o que você precisa fazer.

Ainda não funcionou? Copie e pesquise o erro, com certeza alguém já teve o mesmo problema.

#### Leia a documentação

> Horas de debugging te salvam minutos de ler documentação.

Leia a documentação. Não estou dizendo pra ler de cabo a rabo só por ler, mas se está usando uma [API](#api) (ou no mínimo se usa bastante) é interessante saber como ela funciona até para conseguir tirar mais dela ou usar ela de maneira melhor.

##### API

Quando falamos API, muitas vezes já pensamos em uma API pública tipo a [PokéAPI](https://pokeapi.co/), mas API é um termo muito mais amplo.

Aqui estou me referindo de API no sentido de interface mesmo. Quando chamamos o método de uma linguagem ou de um package, aquilo também é uma API.

#### StackOverflow - Como fazer uma boa pergunta?

[Acho importante mostrar a versão inglesa das guidelines do StackOverflow, porque são bem completas.](https://stackoverflow.com/help/how-to-ask)

Mas segue um resumo:

* Procure e faça sua pesquisa
* Escreva um título que resuma seu problema
  * Faça de conta que está falando com um colega ocupado
  * Gramática e pontuação são importantes
* Introduza o problema antes de qualquer código
  * Coloque código o suficiente para que outros possam reproduzir o problema
  * Se possível, crie em um playground algo que reproduza seu problema. 
  * Não poste imagens de código, data e erros. Copie o texto.
* Inclua todas as tags relevantes
* Leia o que escreveu: faz sentido? consegue reproduzir?
* Poste a questão e responda ao feedback

Adicionalmente quero colocar, porque é algo que vejo muito:

**Não chegue perguntando "quem pode me ajudar com XXXX?", já deixe sua pergunta!**

Muita gente em muitos fóruns e similares já vem perguntando quem pode ajudar com uma tecnologia, mas esperam alguém responder "sim", "qual o problema" para finalmente falar o problema.

Não faça isso! Se a pessoa depois não sabe como resolver, fica ruim pra todo mundo. 

Por outro lado, outra pessoa pode não ter confiança de ajudar algo que não sabe, mas já passou pelo problema e sabe como resolver.

E ainda: é uma baita perda de tempo!

Use o guia do StackOverflow, faça sua boa pergunta de cara e espere alguém te ajudar.

### Clean Code

Aqui é onde acontecem os "maiores pecados". 

Programadores não fazem código para máquinas, mas primeiramente para pessoas.

Vou repetir:

#### **PROGRAMADORES NÃO FAZEM CÓDIGO PARA MÁQUINAS, MAS PRIMEIRAMENTE PARA PESSOAS.**

Fazer o código funcionar é a parte mais fácil.

Mais do que isso, é preciso salientar que nós, programadores, passamos mais tempo LENDO código do que ESCREVENDO. (E por uma margem MUITO grande.)

Por isso, se o cógido não for legível ou se não for possível entender o que está acontecendo... pode funcionar, mas é inútil se eu não conseguir entender e mudar quando for preciso.


#### Regra do Escoteiro

> Toda vez que mexer em um código, deixe ele um pouco mais limpo do que quando encontrou.

#### Nomes descritivos

Faz tempo que as linguagens limitavam o nome das variáveis e funções. 

Hoje, mesmo as que limitam são generosas o suficiente para não ter como desculpa nomes como: `nm_ac (nome_alguma_coisa)`.

Os editores de código ajudam a completar, então mesmo se algo tenha o nome: `nomeSuperDescritivoMasSuperLongo`, mesmo colocando `superde` eles já encontram o nome certo e completo.

Outro ponto... não MENTIR! Se uma função se chamar `pegarNumeros` e a função em si pega e transforma... isso é uma mentira. Alguém pode querer os dados "crus" e vai ter problema porque ela faz alguma coisa inesperada.

#### Sobre o tamanho de funções, classes, métodos

Existe apenas duas regras:

1. Funções devem ser pequenas.
2. E ainda menores do que está pensando.

#### Sobre overenginering e não abstrair de mais

Não tente fazer algo genérico de cara, você vai quebrar a cara e vai acabar não usando a abstração em nenhum outro lugar.

Primeiro você faz funcionar para um caso, daí quando precisar você abstrai para usar em outros.

Mas CUIDADO! Um monte de `ifs` não fazem uma boa abstração.

> Prefira duplicação a uma abstração errada
>
> &mdash; Sandi Metz

#### Não abstrair de mais

Por mais legal que seja aplicar operadores booleanos em problemas comuns... se só você entende o código...

Há coisas que são básicas, um patamar mínimo que todos deveriam ter para poder funcionar como equipe.

Por causa disso, as vezes é necessário deixar aqueles `bitwise operators` de lado e colocar algo que todo mundo entenda.

#### Números Mágicos

Aqui é explicito o que é o `2`.
```js
  function multiplicarPorDois(num){
    return num * 2;
  }
```

Já aqui...
```js
  function f(x){
    return (x === 10) ? true : false;
  }
```
O que é `10`? (porque `f`?)

```js
  function verificaConfiguracaoX(configCheck){
    const configX = 10;
    return (configCheck === configX) ? true : false;
  }
```
Ah... `10` é uma configuração.

#### Refatorar

Maioria dos cursos mostra um mundo onde você "logicamente" vai do passo `A` para o `B` e depois para o `C`.

No mundo real entretanto... você vai do `A` para o `G`, depois `L` e finalmente `C`.

Depois refatoramos para que `A -> B -> C`.

#### "Siglas"

##### DRY - Don't Repeat Yourself

Código duplicado significa que um bug em um lugar precisa ser arrumado em vários lugares. Mas e se esquecemos de alterar?

Código duplicado também significa que foi feito a mesma coisa várias vezes.

Por isso: **Não se Repita!**

##### KISS - Keep It Simple, Stupid

Uma das vantagens to TDD é escrevermos apenas o necessário para resolver o problema (fazer o teste passar).

Isso leva a um código mais "direto ao ponto".

Com ou sem TDD, esse é o objetivo: **manter o código simples**.

##### YAGNI - You Aren't Gonna Need It

**Você não vai precisar disso.**

"Ah... mas e se os usuários quiserem fazer" NÃO!

**Você não vai precisar disso.**

##### SOLID

* S - Single-responsiblity Principle
* O - Open-closed Principle
* L - Liskov Substitution Principle
* I - Interface Segregation Principle
* D - Dependency Inversion Principle

Isso sozinho é um assunto bem amplo, mas se desse pra resumir em algo seria: mantenha o código desacoplado.

Pense em LEGO, cada peça em si não depende de outra, mas elas possuem conexões que deixam você criar coisas. E conectando elas você vai criando coisas maiores e mais complexas.

## Senti falta de alguma coisa ou acho que existem erros

Só deixar um [PR](https://www.youtube.com/watch?v=U-Y_Mtdyo74&ab_channel=WillianJustenCursos) ou abrir uma [issue](https://www.youtube.com/watch?v=WpA2NXdfkNQ&ab_channel=DevSuperior)!
