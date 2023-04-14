
# Prova de Fluxo de Controle em Dart

## 01) O que é Fluxo de Controle em Dart?

Fluxo de Controle em Dart é, basicamente, a ordem na qual as instruções são executadas em um programa feito em Dart. Essa ordem pode ser manipulada por meio dos comandos de controle de fluxo.

## 02) Quais são as três estruturas básicas de Fluxo de Controle em Dart?

Estrutura de decisão (como as estruturas if, if-else e switch), estrutura de loop (como as estruturas while e for) e estrutura de pulo (como break e continue).

## 03) O que é uma instrução if em Dart?

Executa um bloco de código caso a expressão entre parênteses resulte em `true`, conforme o mostrado abaixo:

```dart
if (expressão) {
	// bloco a ser executado caso a expressão resulte em true
}
```

Exemplo:

```dart
void main() {
  int x = 4;
  
  // o resto da divisão de 4 por 2 é 0, portanto o resultado da expressão será true
  if(x % 2 == 0) {
    print("par");
  }
}
```

Resulta em:

> par

## 04) O que é uma instrução if-else em Dart?

Executa um bloco de código caso a condição expressa entre parênteses seja verdadeira, do contrário executa o bloco que vem depois da palavra chave `else`. Confome o mostrado a seguir:

```dart
if(expressão) {
  // bloco de código a ser executado caso a expressão resulte em true
}
else {
  // bloco de código a ser executado caso a expressão resulte em false
}
```

Exemplo de programa que usa if-else:  

```dart
void main() {
  int x = 5;
  
  // o resto da divisão de 5 por 2 é 1, portanto o resultado da expressão será false
  if(x % 2 == 0) {
    print("par");
  }
  else {
    print("impar");
  }
}
```

Resulta em:

> impar

## 05) O que é uma instrução switch em Dart?

Tal como o if ou o if-else, é uma instrução de controle de fluxo que pode desviar o fluxo de execução do programa. A grande diferença é que o resultado da expressão é comparado a vários possíveis resultados e para cada um deles poderá haver uma porção de código a ser executada. Opcionalmente poderá ser incluída uma porção de código que será executada caso o resultado da expressão não coincida com nenhuma das possibilidades.

## 06) Como usar a instrução switch em Dart?

Ela é composta de uma expressão que fica entre parênteses seguida de um bloco entre chaves, nesse bloco teremos várias cláusulas `case`, cada uma associa um possível resultado da expressão a um bloco de código a ser executado caso o resultado realmente coincida com o valor expressado na cláusula `case`. Além disso pode conter uma cláusula `default` seguida de uma porção de código a ser executada quando não há um `case` que corresponda ao resultado da expressão. 

Todo case deve ser encerrado com uma instrução `break`.

A sintaxe da instrução é mostrada abaixo:

```dart
switch (expressão) {
  case 1:
    // porção de código a ser executada caso o resultado da expressão seja igual a 1
    break;  // caso o bloco não termine em break, todos os casos abaixo serão executados
  case 2:
    // porção de código a ser executada caso o resultado da expressão seja igual a 2
    break;  // caso o bloco não termine em break, todos os casos abaixo serão executados
  case 3:
    // porção de código a ser executada caso o resultado da expressão seja igual a 3
    break;  // caso o bloco não termine em break, todos os casos abaixo serão executados
	
  ...
	
  default:
  // bloco a ser executado caso `valor` não tenha sido igual a nenhum valor acima
}
```

Exemplo de programa em Dart que usa a instrução switch.

```dart

void main() {
  int diaDaSemana = 2;
  
  switch (diaDaSemana) {
    case 1:
      print("domingo");
      break;
      
    case 2:
      print("segunda");
      break;
      
    case 3:
      print("terça");
      break;
      
    case 4:
      print("quarta");
      break;
      
    case 5:
      print("quinta");
      break;
      
    case 6:
      print("sexta");
      break;
      
    case 7:
      print("sábado");
      break;
     
    default:
      print("Esse valor não corresponde a um dia da semana");
  }
}

```

Saída quando `diaDaSemana` é igual a 2:

> segunda

Saída quando `diaDaSemana` é igual a 8:

> Esse valor não corresponde a um dia da semana

## 07) O que é uma instrução for em Dart?

A instrução for executa um bloco de código até que uma condição resulte em false. Adicionalmente, é possível inicializar uma variável que será usada durante as iterações e uma instrução que é executada depois da finalização de cada bloco. Geralmente essa instrução é utilizada quando é possível determinar quantas vezes o bloco deverá ser executado.

## 08) Como usar a instrução for em Dart?

A sintaxe desse comando é mostrada a seguir:

```dart

for (inicialização ; condição ; iterador) {
	// bloco a ser executado enquanto a condição for true
}

```

- A inicialização é uma instrução executada uma única vez antes do *loop*. Nela podemos inicializar uma variável que poderá ser utilizada durante a execução desse loop.
- Na condição pode-se colocar uma expressão que retorna um valor booleano. Se ele for falso, o loop se encerra. Essa condição é checada antes de cada iteração.
- No iterador põe-se uma instrução que será executada ao fim de cada iteração. Geralmente essa instrução incrementa ou decrementa uma variável.


Exemplo de programa em Dart que utiliza a instrução for:

```dart

void main() {
  print("Começo das iterações");
  for (int x = 0 ; x < 10 ; x++) {
    print("x = $x");
  }
  print("Fim das iterações");
}

```

Saída do programa:

> Começo das iterações  
> x = 0  
> x = 1  
> x = 2  
> x = 3  
> x = 4  
> x = 5  
> x = 6  
> x = 7  
> x = 8  
> x = 9  
> Fim das iterações  

Também pode ser usada para iterar entre os elementos de um iterável, como listas ou mapas, conforme pode ser visto a seguir:

```dart

void main() {
  int sum = 0;
  
  List<int> numeros = [1, 2, 3, 4];
  
  for (int x in numeros) {
    sum += x;
  }
  print("Total: $sum");
}

```

Saída do programa:

> Total: 10

## 09) O que é uma instrução while em Dart?

Tal como a instrução for, o while executa um bloco de código enquanto uma condição, que é expressada entre parênteses. Geralmente é utilizado quando a quantidade de vezes que o bloco deverá ser executado é indeterminada.

## 10) Como usar a instrução while em Dart?

A sintaxe da instrução é mostrada abaixo:

```dart
while (condição) {
  // bloco a ser executado enquanto a condição for true.
}
```

Exemplo de programa em Dart que usa a instrução while:

```dart

void main() {
  int x = 0;
  
  while (x < 5) {
    print("x = $x");
    x += 1;
  }
  
  print("Fim");
}

```

Saída do programa:

> x = 0  
> x = 1  
> x = 2  
> x = 3  
> x = 4  
> Fim  

Note que se `x` fosse igual a 6 o bloco de código do while não seria executado.

## 11) O que é uma instrução do-while em Dart?

Funciona de maneira quase idêntica ao while, entretanto a comparação ocorre depois da execução do bloco de código, fazendo com que ele seja executado ao menos uma vez.

## 12) Como usar a instrução do-while em Dart?

A sintaxe desse comando é mostrada a seguir:

```dart

do {
	// bloco a ser executado enquanto a condição for true.
	// diferente do while, nesse loop o bloco é executado e depois é feita a checagem da condição, fazendo com que ele seja executado ao menos uma vez
} while (condição);

```

Exemplo de programa em Dart que usa a instrução do while:

```dart

void main() {
  int x = 0;
  
  do {
    print("x = $x");
  } while(x > 0);
}

```

Saída do programa:

> x = 0

## 13) O que é uma instrução break em Dart?

A instrução `break` faz com que um loop, seja simplesmente encerrado.

## 14) Como usar a instrução break em Dart?

No programa a seguiros valores de x deveriam ir de 1 a 5 ao longo da execução do *loop* feito com a instrução `for`, mas quando x é igual a 3 a condição no `if` se torna true, fazendo com que a instrução break seja executada, interrompendo o *loop*.

```dart

void main() {
  for (int x = 1 ; x <= 5 ; x++) {
    if (x == 3) break;
    
    print("x = $x");
  }
}

```

Saída do programa:

> x = 1  
> x = 2  

## 15) O que é uma instrução continue em Dart?

A instrução continue faz com que a execução do bloco de código de um *loop* seja interrompida, mas, ao contrário da instrução `break`, a execução do programa continua na próxima iteração. 

## 16) Como usar a instrução continue em Dart?

No programa a seguir o valor de x é imprimido em quase todas as iterações, exceto a em que x é igual a 3, pois quando isso ocorre a condição expressa no if resulta em true, fazendo com que a instrução continue seja executada. Assim, todo o resto do bloco é ignorado e a iteração seguinte, em que x é igual a 4, se inicia.

```dart

void main() {
  for (int x = 1 ; x <= 5 ; x++) {
    if (x == 3) continue;
    
    print("x = $x");
  }
}

```

Saída do programa:

> x = 1  
> x = 2  
> x = 4  
> x = 5  

## 17) O que é uma instrução try-catch em Dart?

Em um try-catch, o bloco de código que vem após a palavra-chave `try` é executado normalmente, contanto que não seja lançada nenhuma uma excessão, que consiste em um objeto que contém informações a respeito de uma falha que tenha ocorrido durante a execução do programa. Exceções podem ter vários tipos e com a cláusula `on` podemos especificar um bloco de código a ser executado caso um certo tipo de exceção seja lançada. Para capturar o objeto da exceção lançada utilizamos a palavra-chave catch para capturá-la.

## 18) Como usar a instrução try-catch em Dart?

No código a seguir ocorre uma divisão por zero dentro do bloco `try`, causando o lançamento de uma exceção do tipo UnsupportedError. Por causa do `on UnsupportedError`, o bloco que vem a seguir faz com que seja exibida a mensagem "Não pode haver uma divisão por zero" e o objeto que representa a exceção lançada é capturado e chamado de `e`.

```dart

void main() {
  
  int x = 4;
  int y = 0;
  int resultado = 0;
  
  try {
    resultado = x ~/ y;
  
    print("O resultado da divisão é $resultado");
  }
  on UnsupportedError catch(e) {
    print("Não pode haver uma divisão por zero");
    print("Detalhes: $e");
  }
  
}

```

## 19) O que é uma instrução finally em Dart?

A instrução finally faz com que um bloco de código seja executado depois do bloco try-catch tendo uma exceção sido levantada ou não. Nesse bloco se põe instruções que encerram a ação que começou no bloco `try` como, por exemplo, fechar uma conexão que foi aberta dentro do `try`. É importante notar que esse bloco será executado mesmo que haja um `return` no bloco do `try`.

## 20) Como usar a instrução finally em Dart?

Para que haja um `finally` deve haver um try antes. Conforme a sintaxe mostrada a seguir:

```dart

try {
  // código
}
finally {
  // código a ser executado depois do try ou catch
}

```
