#Responda às seguintes questões:

## 1) O que é uma lista em Dart?

Uma lista em Dart é um tipo de coleção iterável na qual os elementos, sendo bastante similar a uma array. Basicamente armazena elementos de forma sequêncial e indexavel.

## 2) Como criar uma lista vazia em Dart?

Abaixo são mostradas duas opções para se criar uma lista vazia em Dart:

```dart

void main() {
  List<int> empty1  = [];           // usando um simples []
  List<int> empty2 = List.empty();  // usando o construtor List.empty()
  
  print(empty1);
  print(empty2);
}

```

## 3) Como criar uma lista com elementos em Dart?

Abaixo é mostrado como criar uma lista com elementos em Dart:

```dart

void main() {
  List<int> list= [1, 2, 3];           // usando um simples []

  print(list);
}

```

## 4) Qual a diferença entre uma lista e um conjunto em Dart?

Em um conjunto não podem haver dois elementos iguais, já em uma lista isso é possível.

## 5) Como acessar um elemento específico de uma lista em Dart?

Abaixo são mostradas duas formas de se acessar um elemento específico em Dart:

```dart

void main() {
  List<int> lista = [1, 2, 3, 4];

  // Duas formas de se acessar o elemento com index
  print(lista[2]);            // com o índice do elemento entre colchetes
  print(lista.elementAt(2));  // com o índice do elemento como parâmetro do método elementAt()
}

```

## 6) Como adicionar um elemento ao final de uma lista em Dart?

Para isso podemos passar o elemento que desejamos adicionar como parâmetro da chamada ao método `add` da classe `List`.

```dart

void main() {
  List<int> lista = [1, 2, 3];
  
  lista.add(4);
  
  print(lista);
}

```

## 7) Como inserir um elemento em uma posição específica de uma lista em Dart?

Para isso passamos, como parâmetros da chamada ao método `insert`, o índice da posição na qual desejamos fazer a inserção e o elemento ao qual queremos inserir nessa ordem. Abaixo há um exemplo de um programa que faz isso:

```dart

void main() {
  List<int> lista = [1, 3, 4];
  
  lista.insert(1, 2); // inserir, no índice 1, o elemento 2
  
  print(lista);
}

```

## 8) Como remover um elemento de uma lista em Dart?

Para isso usamos o método remove, passando o elemento que queremos remover como parâmetro. No programa abaixo esse método é usado para remover o elemento 8 da lista, fazendo com que restem os elementos 1, 2, 3 e 4. Outros métodos que podem ser usados são `removeAt` e `removeRange`.

```dart

void main() {
  List<int> lista = [1, 2, 8, 3, 4];
  
  lista.remove(8);
  
  print(lista);
}

```

## 9) Como verificar se uma lista contém um determinado elemento em Dart?

Para isso podemos usar o método `contains`, que recebe um elemento e retorna `true` caso ele esteja presente na lista.

```dart

void main() {
  List<String> lista = ["a", "b", "c", "d"];
  
  // a arrow function returnará true caso um elemento "c" da lista seja passado.
  if(lista.contains("c")) {
    print("Contém 'c'");
  }
  else {
    print("Não contém 'c'");
  }
}

```

## 10) Como ordenar uma lista em ordem crescente em Dart?

Para isso podemos usar o método `sort`, que recebe como parâmetro um Comparator, que é uma função que recebe dois elementos, chamados de a e b, e retorna um valor negativo se a é maior que b, zero se a e b são iguais ou um valor positivo se b for maior que a. No programa abaixo o comparator que usamos se trata de uma arrow-function que recebe os dois valores a e b e usa o método `compareTo` da classe num.

```dart

void main() {
  List<int> lista = [4, 3, 2, 1];
  
  lista.sort((a, b) => a.compareTo(b));
  
  print(lista);
}

```

## 11) Como ordenar uma lista em ordem decrescente em Dart?

Usando a função `sort`, podemos alterar a arrow-function usada para que, ao invés de comparar a variável à variável b, faça o oposto. Invertendo a comparação.

```dart

void main() {
  List<int> lista = [1, 2, 3, 4];
  
  lista.sort((a, b) => b.compareTo(a));
  
  print(lista);
}

```

## 12) Como copiar uma lista em Dart?

Pode-se usar o construtor `of` para criar uma lista diferente com os mesmos elementos.

```dart

void main() {
  List<int> original = [1, 2, 3, 4];     // Lista original
  List<int> copia = List.of(original);   // Criação de uma cópia da lista
  
  if (original == copia) {
    print("original e copia são a mesma lista");
  }
  else {
    print("original e copia são duas listas distintas");
  }
}

```

## 13) Como verificar se duas listas são iguais em Dart?

Para isso pode-se usar o objeto `ListEquality` e usar o método equals para comparar as duas listas, mas antes o pacote collection deve ser importado.

```dart

import 'package:collection/collection.dart';

void main() {
  List<int> lista1 = [1, 2, 3, 4, 5];
  List<int> lista2 = [1, 2, 3, 4, 5];
  List<int> lista3 = [1, 2, 3, 4, 6];
  
  if (ListEquality().equals(lista1, lista2)) {
    print("A lista 1 é igual a lista 2");
  }
  else {
    print("A lista 1 é diferente da lista 2");
  }
  
  if (ListEquality().equals(lista1, lista3)) {
    print("A lista 1 é igual a lista 3");
  }
  else {
    print("A lista 1 é diferente da lista 3");
  }
}

```

## 14) Como criar uma lista a partir de outra lista em Dart?

Podemos usar o método `map` para gerar outra lista a partir da anteriror, mas é preciso lembrar que esse método retorna um Iterable, portanto deve-se usar o método `toList` para converter esse iterable para uma lista.

```dart

void main() {
  List<int> lista = [1, 2, 3, 4, 5];
  
  List<int> novaLista = lista.map((elemento) => 2 * elemento).toList(); // a nova lista terá cada elemento da primeira multiplicado por 2
  
  print(novaLista);
}

```

## 15) Como transformar uma lista em uma lista de strings em Dart?

Podemos usar o método `map` para gerar uma nova lista onde todos os elementos da anterior estão convertidos para string através do método `toString`.
```dart

void main() {
  List lista = ['a', 1, 2.2];
 
  List<String> novaLista = lista.map((element) => element.toString()).toList();
  
  print(novaLista);
}

```
## 16) Como calcular a soma dos elementos de uma lista em Dart?

Para isso podemos utilizar o método `reduce`, que combina o primeiro elemento da lista aos demais iterativamente, conforme pode ser visto a seguir:

```dart

void main() {
  List<int> lista = [1, 2, 3, 4, 5];
  
  int soma = lista.reduce((valor, elemento) => valor + elemento);
  
  print(soma);
}

```

## 17) Como calcular a média dos elementos de uma lista em Dart?

Tendo o programa que soma os valores de todos os elementos, pode-se simplesmente dividir a soma pela quantidade de elementos da lista, como é possível ver no código a seguir:

```dart

void main() {
  List<int> lista = [1, 2, 3, 4, 5];
  
  int soma = lista.reduce((acc, element) => acc + element);
  double media = soma / lista.length;
  
  print(media);
}

```

## 18) Como calcular o valor máximo e mínimo de uma lista em Dart?

Para achar cada um, é possível usar o método reduce.

Pode-se colocar os elementos em ordem crescente, fazendo com que o mínimo seja o primeiro da lista e o máximo seja o último, conforme mostrado a seguir

```dart

void main() {
  List<int> lista = [1, 4, 5, 2, 3];
  
  lista.sort((a, b) => a.compareTo(b));
  
  print("O valor mínimo é ${lista.first}");
  print("O valor máximo é ${lista.last}");
}

```

## 19) Como contar quantas vezes um elemento aparece em uma lista em Dart?

Para isso pode-se usar o método `where` para filtrar os elementos que são iguais ao que queremos contar e obter o tamanho dessa lista, conforme mostrado na aplicação abaixo:

```dart

void main() {
  List<int> lista = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5];
  
  int repeticoes = lista.where((elemento) => elemento == 4).length;
  
  print("O número 4 se repete $repeticoes vezes");
}

```

## 20) Como remover todos os elementos duplicados de uma lista em Dart?

Uma abordagem é converter a List para um Set, pois quando os elementos forem passados para o Set os repetidos serão naturalmente eliminados já que esse tipo de coleção não os permite. Um exemplo disso pode ser visto abaixo:

```dart

void main() {
  
  List<int> lista = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, 5, 5, 5, 5];
  
  List<int> novaLista = lista.toSet().toList();

  print(novaLista);
}

```

## 21) Espero que essa prova ajude a avaliar o conhecimento dos alunos sobre Listas em Dart!

Com certeza ajudou!
