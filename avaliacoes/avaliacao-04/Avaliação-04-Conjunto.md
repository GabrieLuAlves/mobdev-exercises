## 01) O que é um conjunto em Dart?

Um set é uma coleção iterável na qual não são admitidos elementos iguais.

## 02) Como criar um conjunto vazio em Dart?

Da seguinte forma:

```dart

Set conjuntoVazio = {};

```

Mas caso seja necessário definir um conjunto vazio, as chaves não bastarão pois por padrão serã considerado um mapa vazio. Nesse caso, deve-se especificar o tipo usando `<>` com o tipo de dado que o conjunto armazena.

Exemplo:

```dart

void main() {
  print({} is Set);           // Isso não é um conjunto.
  print(<dynamic> {} is Set); // Isso é.
}

```

## 03) Como criar um conjunto com elementos em Dart?

A seguir é criado um conjunto com os números 1, 2, 3, 4 e 5

```dart

Set conjuntoComElementos = {1, 2, 3, 4, 5};

```

## 04) Qual a diferença entre um conjunto e uma lista em Dart?

Um conjunto não admite elementos repetidos, uma lista admite.

## 05) Como adicionar um elemento a um conjunto em Dart?

Usando o método add e passando o elemento a ser adicionado como parâmetro. Essa função retorna true caso o valor não exista na coleção, indicando que foi adicionado com sucesso, ou false caso ele já existir, indicando que esse elemento foi ignorado.

## 06) Como remover um elemento de um conjunto em Dart?

Usando o método remove e passando o elemento que deve ser removido como parâmetro.

## 07) Como verificar se um conjunto contém um determinado elemento em Dart?

Usando o método `contain` e passando o elemento como parâmetro, caso ele exista o método retorna true, do contrário retorna false.

## 08) Como verificar se um conjunto é vazio em Dart?

Usando o método `isEmpty`, que retorna true se o conjunto estiver vazio, do contrário retorna false.

## 09) Como unir dois conjuntos em Dart?

Chamando o método `union` de um e passando o outro como parâmetro. O valor retornado será o conjunto resultante da união.

## 10) Como obter a interseção de dois conjuntos em Dart?

Chamando o método `intersection` de um e passando o outro como parâmetro. O valor retornado será o resultado da diferença entre os dois.

## 11) Como obter a diferença entre dois conjuntos em Dart?

Chamando o método `difference` de um e passando o outro como parâmetro. O valor retornado será o resultado da diferença entre os dois.

## 12) Como verificar se um conjunto é subconjunto de outro conjunto em Dart?

Chamando o método `containsAll` do conjunto que teoricamente contém o subconjunto e passando-o como parâmetro. Se o subconjunto realmente estiver contido dentro do conjunto o método retorna true, caso contrário retorna false.

## 13) Como verificar se dois conjuntos são iguais em Dart?

Dois conjuntos serão iguais se os dois tiverem os mesmos elementos. Portanto se ao usar o método `containsAll` de um passando o outro como argumento o resultado for true e os dois conjuntos tiverem a mesma quantidade de elementos (isso pode ser checado com a propriedade `lenght`) eles serão iguais.

## 14) Como criar um conjunto a partir de uma lista em Dart?

Usando o construtor `Set.from` ou `Set.of` e passando a lista como parâmetro.

## 15) Como criar uma lista a partir de um conjunto em Dart?

Usando o construtor `List.from` ou `List.of` e passando o conjunto como parâmetro.

## 16) Como transformar um conjunto em uma lista de strings em Dart?

Chamando o método `map` e passando uma arrow-function como parâmetro que recebe um elemento do conjunto e retorna esse elemento convertido para string através da chamada do método `toString`. O método `map` retorna um iterável, portanto pode ser necessário chamar o método `toSet` para que seja retornado um conjunto.

## 17) Como calcular a união de vários conjuntos em Dart?

Chamando o método `union` de um, passando outro como parâmetro e continuar chamado union em cascata até que todos sejam chamados.

Exemplo:

```dart

void main() {
  Set<int> set1 = {1, 2};
  Set<int> set2 = {2, 3};
  Set<int> set3 = {3, 4};
  Set<int> set4 = {4, 5};
  
  Set<int> union = set1
    .union(set2)
    .union(set3)
    .union(set4);
  
  print(union);
}

```

## 18) Como calcular a interseção de vários conjuntos em Dart?

Chamando o método `intersection` de um, passando outro como parâmetro e continuar chamado union em cascata até que todos sejam chamados.

Exemplo:

```dart

void main() {
  Set<int> set1 = {1, 5};
  Set<int> set2 = {2, 5};
  Set<int> set3 = {3, 5};
  Set<int> set4 = {4, 5};
  
  Set<int> intersection = set1
    .intersection(set2)
    .intersection(set3)
    .intersection(set4);
  
  print(intersection);
}

```

## 19) Como verificar se dois conjuntos são disjuntos em Dart?

Verificando se a interseção deles é vazia usando o método `intersection` e chamando o `isEmpty` do resultado.

## 20) Como remover todos os elementos duplicados de uma lista usando um conjunto em Dart?

Convertendo a lista para um conjunto e depois para uma lista novamente.
