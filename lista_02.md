# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```

- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

~~B)~~ O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.


______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

~~B)~~ A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

~~D)~~ O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.


~~D)~~

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

~~B)~~ Preload -> Create -> Update

C) Load -> Initialize -> Render

D) Begin -> Play -> End
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

~~B)~~ Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)


Resposta:
```
Iniciar


variavel     idade

idade = prompt("Inserir sua idade")

se (idade < 16) {
	imprimir("Não pode votar!")
}

se não (idade >= 16 e idade < 18 ){
	imprimir("Voto facultativo!")
}

outro {
 	imprimir("Voto obrigatótio")
}



Finalalgoritmo
```

______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

```

Resposta:

```
Inicio


Classe FormaGeometrica:
    Método Construtor(cor, tipo, area):
	parametros:
        - cor
	- tipo
	- area

}



Classe Circulo extende FormaGeometrica {
   Método Construtor(cor, tipo, raio) {
      parametros:
       	herdar cor, tipo
   	- raio
   }	

   Método CalcularArea1() {
      imprimir(A área do (tipo) (cor) é (2 * 3.14 * raio)cm)
   }
}

variavel circulo1 novo Circulo('azul', 'circulo' 10)
     circulo1.CalcularArea1()



Classe Retangulo extende FormaGeometrica {
    Método Construtor(cor, tipo, altura, base) {
       parametros:
         herdar cor, tipo
         - altura
         - base
   }

Método CalcularArea2() {
      imprimir(A área do (tipo) (cor) é (base * altura)cm)
   }
}

variavel retangulo1 novo Retangulo ('verde', 'retangulo', 25, 20)
     circulo1.CalcularArea2()





finalalgoritmo
```
______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

Resposta:
```
    Função simular_corrida(distancia, velocidade_inicial, aceleracao, velocidade_maxima, tempo_maximo):
    tempo = 0
    velocidade = velocidade_inicial

    	Enquanto tempo < tempo_maximo:
        Se velocidade < velocidade_maxima:
            velocidade = velocidade + aceleracao * tempo
            Se velocidade > velocidade_maxima{
                velocidade = velocidade_maxima
		}        

        	distancia_percorrida = velocidade * tempo
        	Se distancia_percorrida >= distancia{
         	   Retornar tempo
		}        

        tempo = tempo + 1
	} 
   
    Retornar "Não foi possível completar a corrida dentro do tempo máximo."
}

tempoParaCompletar = simularCorrida(2000, 0, 10, 190, 300)
      imprimir(Tempo para completar a corrida:  + (tempoParaCompletar) +  minutos.)
	      //comentario 5min = 300seg
              //comentario 2km  = 2000m
```

______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.


Resposta:
```
Inicio


Função MultiplicaçãoDeMatrizes(MatrizA, MatrizB){
 Se colunas(matrizA) ≠ linhas(matrizB) então{
	Retornar "As matrizes não poder ser multiplicadas. Elas têm dimensões diferentes."
  }
 

Senão:
linhasA = tamanho(matrizA) {
    colunasA = tamanho(matrizA[0])
    linhasB = tamanho(matrizB)
    colunasB = tamanho(matrizB[0])


	Para i = 0 ate linhaA:
	   Para j de 0 ate colunaB:
               resultado[i][j] = 0
               Para k de 0 ate colunaA:
                  resultado[i][j] += matrizA[i][j] * matrizB[i][j]
  }
}


matrizA = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB = [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizMultiplicacao = MultiplicaçãoDeMatrizes(matrizA, matrizB)
 Escrever("Multiplicação das matrizes:")
   ImprimirMatriz(matrizMultiplicacao)


Finalalgoritmo
```