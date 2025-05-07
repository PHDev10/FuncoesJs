# FuncoesJs
# 1° Trabalho da Disciplina de LS (Linguagem de Script) - Explicando Funções em Js (Javascript)

## Função Declaration:
A declaração de função (função declaration), por sua sintaxe, segue o “raciocínio lógico” de uma função em uma linguagem de programação – uma palavra de comando obrigatória (“function”, em Javascrpit), seguida pela palavra que nomeará a função e permitirá que seja chamada. É a maneira “convencional” para declarar uma função em Javascript.
## Vantagens:
Declaração e sintaxe de fácil interpretação e entendimento, devido, principalmente, pela palavra “function” no começo, o que pode ser associado a como as funções são declaradas de maneira semelhante em outras linguagens de programação (como Python).
Passagem de parâmetros – cada valor pode ser atribuído como um parâmetro para a função, deixando-o(s) ordenadamente visível(eis) e organizado(s). Isso facilita a leitura do código e compreensão dos valores que estão sendo passados como parâmetros.
Chamada de função – apenas é necessário inserir o nome da função, seguido de parênteses e de um ou mais parâmetros (dependendo da função), para utilizá-la em diferentes partes do código.
Hoisting (içamento) – faz com que a função possa ser chamada em qualquer parte do código e quantas vezes quiser.
## Desvantagens:
Maior quantidade de linhas, o que pode ocasionar em maior lentidão na execução do código.
A declaração de uma função ocupa espaço na memória. Então, em um código onde utilizamos esse tipo de função, teria uma quantidade de memória maior reservada, necessitando de maior capacidade de armazenamento e execução por parte da máquina.
## Exemplos de Função Declaration:
//Exemplo 1:
function idade() {
    console.log("Qual a sua idade?")
}
idade()

//Exemplo 2:
function mensagem(msg) {
    console.log(msg)
}
mensagem("Olá, Mundo!")

//Exemplo 3:
function cal(valor1, valor2) {
    r= valor1 + valor2
    return r
}
const a= 10
const b= 10
cal(a, b)
console.log("O resultado é " + r)
