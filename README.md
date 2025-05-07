# **FuncoesJs**
# **1° Trabalho da Disciplina de LS (Linguagem de Script) - Explicando Funções em Js (Javascript)**

## **Função Declaration:**
> A declaração de função (função declaration), por sua sintaxe, segue o “raciocínio lógico” de uma função em uma linguagem de programação – uma palavra de comando obrigatória (“function”, em Javascrpit), seguida pela palavra que nomeará a função e permitirá que seja chamada. É a maneira “convencional” para declarar uma função em Javascript.

**Vantagens:**
> Declaração e sintaxe de fácil interpretação e entendimento, devido, principalmente, pela palavra “function” no começo, o que pode ser associado a como as funções são declaradas de maneira semelhante em outras linguagens de programação (como Python).
>
> Passagem de parâmetros – cada valor pode ser atribuído como um parâmetro para a função, deixando-o(s) ordenadamente visível(eis) e organizado(s). Isso facilita a leitura do código e compreensão dos valores que estão sendo passados como parâmetros.
>
> Chamada de função – apenas é necessário inserir o nome da função, seguido de parênteses e de um ou mais parâmetros (dependendo da função), para utilizá-la em diferentes partes do código.
>
> Hoisting (içamento) – faz com que a função possa ser chamada em qualquer parte do código e quantas vezes quiser.

**Desvantagens:**
> Maior quantidade de linhas, o que pode ocasionar em maior lentidão na execução do código.
> 
> A declaração de uma função ocupa espaço na memória. Então, em um código onde utilizamos esse tipo de função, teria uma quantidade de memória maior reservada, necessitando de maior capacidade de armazenamento e execução por parte da máquina.
> 
**Exemplos de Função Declaration:**

**Exemplo 1:**
>     function idade() {
> 
>       console.log("Qual a sua idade?")
> 
>     }
> 
>     idade()

**Exemplo 2:**
>     function mensagem(msg) {
>       console.log(msg)
>     }
>     mensagem("Olá, Mundo!")

**Exemplo 3:**
>     function cal(valor1, valor2) {
>       r= valor1 + valor2
>      return r
>     }
>     const a= 10
>     const b= 10
>     cal(a, b)
>     console.log("O resultado é " + r)

##**Função Expression:**
> As expressões de função têm como principal característica a forma como são atribuídas – primeiramente, é criada dentro de uma expressão (uma variável que recebe a função), depois, são inseridos o comando “function”, parênteses, o(s) parâmetro(s) dentro dos parênteses e as chaves para o corpo. Sintaticamente, é feita de forma quase “oposta” a função declaration. Além disso, por ser atribuída como valor a uma variável, a função expression apenas vai ser lida conforme a execução do código, seguindo a regra de leitura – de cima para baixo, da esquerda para a direita.

**Vantagens:**
>Menor espaço de memória exigida, pois a função é atribuída a uma variável.
>
> Por seguir a regra de leitura de código (de cima para baixo, da esquerda para a direita), a função expression apenas será lida na sua respectiva linha de código e posição, evitando a necessidade de uma informação com uma função global sendo guardada desde o início da execução do algoritmo.
>
> Uma cópia de uma função expression pode ser facilmente criada apenas atribuindo a variável a qual a função foi atribuída, permitindo chamar a função em outras partes do código, mesmo após a sua leitura, além de atribuir novos valores.
>
** Desvantagens:**
> Ao mesmo tempo que pode ser útil, a atribuição de uma função a uma variável requer atenção, pois uma vez que função estiver atribuída, a variável já terá um valor (argumento). Isso pode gerar erros de sintaxe, caso ocorra uma reatribuição de valores a variável ou mais chamadas a ela.
> 
> A função a qual a função será atribuída também deverá ser corretamente declarada (var, let ou const) para evitar erros na saída de dados quando a variável for chamada ou em caso de uma reatribuição aso valores dessas variáveis.

** Exemplos:**
** Exemplo 1:**
> const media= function(nota1, nota2, nota3) {
>    const soma= nota1 + nota2 + nota3;
>    const resultado= soma / 3;
>    return resultado;
> }
> const situacao= media(7, 4.5, 9) ;
> console.log("A média aritmética é " + situacao);

** //Exemplo 2:**
> let mensagem= function(boasvindas) {
>    console.log(boasvindas);
> }
> let escrever= ("Olá, seja bem-vindo(a)!");
> mensagem(escrever);

** //Exemplo 3:**
> let area= function(lado) {
>    cal= lado ** 2;
>    return cal
> }
> console.log("A área do quadrado é igual a " + area(7))
