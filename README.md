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

## **Função Expression:**
> As expressões de função têm como principal característica a forma como são atribuídas – primeiramente, é criada dentro de uma expressão (uma variável que recebe a função), depois, são inseridos o comando “function”, parênteses, o(s) parâmetro(s) dentro dos parênteses e as chaves para o corpo. Sintaticamente, é feita de forma quase “oposta” a função declaration. Além disso, por ser atribuída como valor a uma variável, a função expression apenas vai ser lida conforme a execução do código, seguindo a regra de leitura – de cima para baixo, da esquerda para a direita.

**Vantagens:**
>Menor espaço de memória exigida, pois a função é atribuída a uma variável.
>
> Por seguir a regra de leitura de código (de cima para baixo, da esquerda para a direita), a função expression apenas será lida na sua respectiva linha de código e posição, evitando a necessidade de uma informação com uma função global sendo guardada desde o início da execução do algoritmo.
>
> Uma cópia de uma função expression pode ser facilmente criada apenas atribuindo a variável a qual a função foi atribuída, permitindo chamar a função em outras partes do código, mesmo após a sua leitura, além de atribuir novos valores.
>
**Desvantagens:**
> Ao mesmo tempo que pode ser útil, a atribuição de uma função a uma variável requer atenção, pois uma vez que função estiver atribuída, a variável já terá um valor (argumento). Isso pode gerar erros de sintaxe, caso ocorra uma reatribuição de valores a variável ou mais chamadas a ela.
> 
> A função a qual a função será atribuída também deverá ser corretamente declarada (var, let ou const) para evitar erros na saída de dados quando a variável for chamada ou em caso de uma reatribuição aso valores dessas variáveis.

**Exemplos de Função Expression:**

**Exemplo 1:**
>     const media= function(nota1, nota2, nota3) {
>      const soma= nota1 + nota2 + nota3;
>      const resultado= soma / 3;
>      return resultado;
>     }
>     const situacao= media(7, 4.5, 9) ;
>     console.log("A média aritmética é " + situacao);

**Exemplo 2:**
>      let mensagem= function(boasvindas) {
          console.log(boasvindas);
        }
        let escrever= ("Olá, seja bem-vindo(a)!");
        mensagem(escrever);
  
**Exemplo 3:**
>     let area= function(lado) {
>        cal= lado ** 2;
>         return cal
>     }
>     console.log("A área do quadrado é igual a " + area(7))

## **Função Arrow:**
> A função arrow destaca-se pela forma sucinta de como é escrita, sendo possível, em certos códigos, utilizar apenas uma única linha de código para a função. Além disso, não é obrigatório o uso dos comandos “function” e “return” e das chaves, caso a função arrow seja escrita em uma única linha. Todavia, caso haja a necessidade da função possuir mais de uma linha, torna-se essencial a utilização das chaves para definir o “corpo” da função e do comando “return”, para o retorno de algum valor. E para informar o “corpo” da função e o que ocorrerá com os parâmetros passados, utiliza-se “=>”, que é semelhante a uma seta.
>

**Vantagens:**
> Abreviação na escrita da função, pois o comando “function” não é necessário, seja com uma ou mais linhas, assim como o comando “return” e das chaves (em casos de funções arrow com uma linha, o que os torna opcionais). Isso torna a leitura da função breve e entendível.
>
> Necessidade de menor espaço na memória e desempenho na execução, devido a declaração única de uma variável para a atribuição da função, além de não sofrer hoisting.

**Desvantagens:**
> Por ser atribuída a uma variável, deve-se ter cautela quanto as chamadas e possíveis reatribuições de parâmetros a função, pois pode ocasionar erros na saída de dados e na leitura do código.
> 
> Por não sofrer hoisting, uma função arrow não pode ser chamada antes de sua declaração.
> 
> Ao mesmo tempo que a sintaxe mais enxuta possa ser mais compreensível, também pode ser mais complexo de se utilizar, principalmente pela percepção mais “padrão” de como uma função é declarada, a qual a função arrow se difere fortemente.
>

**Exemplos:**

**Exemplo 1:**
> let nomecompleto= (nome) => console.log("Meu nome completo é " + nome);
nomecompleto("Pedro Henrique Santos de Pontes")

**Exemplo 2:**
>const proximo_ano= (ano_atual) => {
>    ano_sucessor= ano_atual + 1;
>    return ano_sucessor;
>}
console.log("Depois de 2025, vem " + proximo_ano(2025));

**Exemplo 3:**
>const definir_sexo= (informacao) => {
>    if (informacao == "h") {
>        console.log("É homem.")
>    } else if (informacao == "m") {
>        console.log("É mulher.")
>    }
>}
>definir_sexo("m")
