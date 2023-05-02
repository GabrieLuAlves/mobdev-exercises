## 01) O que é um mapa em Dart?

Um mapa é uma coleção de valores que são associados a chaves únicas para cada um deles.

## 02) Como criar um mapa vazio em Dart?

```dart

Map<K, V> map = {};

```

## 03) Como criar um mapa com elementos em Dart?

Colocando os elementos entre chaves. Os elementos devem estar separados entre si por vírgulas e a chave e o valor de cada um separados por ":".

Exemplo:

```

Map<num, String> mapa = {
  1: "Pessoa 01",
  2: "Pessoa 02",
  3: "Pessoa 03"
};

```

## 04) Qual a diferença entre uma lista e um mapa em Dart?

Uma lista é iterável e seus elementos são alcançaveis por meio de índices que resultam da ordem na qual os elementos são inseridos. Já um mapa não é iterável e seus elementos são acessíveis por meio de suas chaves. 

## 05) Como adicionar um elemento a um mapa em Dart?

Colocando a chave entre colchetes ao chamar o objeto e atribuindo ao novo elemento conforme visto a seguir.

```

Map<num, String> mapa = {
  1: "Pessoa 01",
  2: "Pessoa 02",
  3: "Pessoa 03"
};

mapa[4] = "Pessoa 04";

```

## 06) Como remover um elemento de um mapa em Dart?

Chamando o método `remove` do mapa e passando como parâmetro a chave do elemento a ser removido.

## 07) Como verificar se um mapa contém uma determinada chave em Dart?

Com o método `containsKey` passando a chave como parâmetro. Se o mapa já contem essa chave, o método retorna true, caso contrário retorna false.

## 08) Como verificar se um mapa é vazio em Dart?

Com a propriedade `isEmpty`, que será true quando o mapa for vazio e false caso contrário.

## 09) Como acessar o valor de uma chave em um mapa em Dart?

Passando a chave entre colchetes ao chamar o objeto, conforme visto no programa a seguir:

```dart

void main() {
  Map<num, String> mapa = {
    1: "Pessoa 01",
    2: "Pessoa 02",
    3: "Pessoa 03"
  };
  
  mapa[4] = "Pessoa 04";

  print(mapa[4]); // valor acessado
}

```

## 10) Como alterar o valor de uma chave em um mapa em Dart?

Simplesmente reatribuindo o valor da chave ou com o método `update`.

## 11) Como obter todas as chaves de um mapa em Dart?

A propriedade `keys` de um mapa se trata de um iterable do tipo das chaves, como pode ser visto no exemplo a seguir:

```dart
void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  Iterable<String> keys = map.keys;
  
  print(keys);
}
```

Saída:
>
> \[nome, idade, email\]
>

## 12) Como obter todos os valores de um mapa em Dart?

A propriedade values retorna um iterable do tipo dos valores com todos os valores, como visto no exemplo a seguir:

```dart
void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  Iterable<dynamic> values = map.values;
  
  print(values);
}
```

Output:

> 
> (Gabriel Luan, 22, gabrielluan.valentim@gmail.com)
> 

## 13) Como verificar se duas chaves em um mapa são iguais em Dart?

Em Dart, uma chave de um mapa não pode referenciar dois objetos distintos, de modo que o valor pode, no máximo, ser redefinido ao se referenciar a mesma chave.

Exemplo:

```dart

void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com",
    "nome": "Gabriel"
  };
  
  map["idade"] = 21;
  
  print(map);
}

```

Saída:

> 
> {nome: Gabriel, idade: 21, email: gabrielluan.valentim@gmail.com}
> 

Para verificar se os valores de duas chaves são iguais pode-se usar o operador `==` e para checar se uma chave já está atribuída a um valor de um mapa, pode-se usar o método `containsKey`.

## 14) Como criar um mapa a partir de duas listas em Dart?

Atravez do construtor `fromIterables` é possível criar um mapa passando como parâmetros dois iteráveis. O primeiro iterável será o das chaves e o segundo o dos valores e toda chave no índice de um índice é associado a uma chave no mesmo índice do outro iterável.

```dart
void main() {
  Map<String, dynamic> map = Map.fromIterables(["nome", "idade", "email"], ["Gabriel Luan", 22, "gabrielluan.valentim@gmail.com"]);
  
  print(map);
}
```

Saída:

> 
> {nome: Gabriel Luan, idade: 22, email: gabrielluan.valentim@gmail.com}
> 

## 15) Como criar uma lista de chaves a partir de um mapa em Dart?

A propriedade `keys` de um mapa se trata de um iterable do tipo das chaves, que pode ser convertido para uma lista, como pode ser visto no exemplo a seguir:

```dart
void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  List<String> keys = map.keys.toList();
  
  print(keys);
}
```

Saída:
>
> \[nome, idade, email\]
>

## 16) Como criar uma lista de valores a partir de um mapa em Dart?

A propriedade values retorna um iterable do tipo dos valores, que contém todos eles e que pode ser convertidado em uma lista, como visto no exemplo a seguir:

```dart
void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  List<dynamic> values = map.values.toList();
  
  print(values);
}
```

Output:

> 
> \[Gabriel Luan, 22, gabrielluan.valentim@gmail.com\]
> 

## 17) Como transformar um mapa em uma lista de pares chave-valor em Dart?

Para isso usaremos a propriedade `entries` do tipo `Map`. Essa propriedade retorna um iterável com os objetos do tipo `MapEntry` que compõe o objeto do tiṕo `Map`. Um `MapEntry` basicamente associa uma chave a um valor. Assim, podemos transformar o iterável em uma lista, que conterá todos os pares chave-valor do mapa em questão. O exemplo abaixo demonstra isso:

```dart

void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  print(map.entries.toList());
}

```

Saída:

> 
> \[MapEntry(nome: Gabriel Luan), MapEntry(idade: 22), MapEntry(email: gabrielluan.valentim@gmail.com)\]
> 

Para acessar a chave de um dos objetos é só usar a propriedade `key`, e para acessar o valor de um deles é só usar a propriedade `value`.

## 18) Como remover todos os elementos de um mapa em Dart?

Utilizando o método `clear`, conforme mostrado a seguir:

```dart

void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  map.clear();
  
  print(map);
}

```

Saída:

> 
> {}
> 

## 19) Como calcular o tamanho de um mapa em Dart?

Para conseguir o tamanho de um mapa em Dart é necessário usar a propriedade `entries` do tipo `Map`. Essa propriedade retorna um iterable do tipo `MapEntry`, que é um tipo que contem um par chave-valor e que compõe o tipo `Map`. Esse iterable contem todos as `MapEntries` do mapa, e podemos ver seu tamanho com a propriedade length, como visto a seguir:

```dart

void main() {
  Map<String, dynamic> map = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  print(map.entries.length);
}

```

## 20) Como verificar se dois mapas são iguais em Dart?

Inicialmente, pode-se pensar em usar o operador `==`, porém, conforme é mostrado nos dois programas a seguir, ele só checa se as duas variáveis passadas referenciam o mesmo mapa.

```dart

void main() {
  Map<String, dynamic> map1 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  Map<String, dynamic> map2 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };

  print(map1 == map2);
}

```

Saída do programa acima:

>
> false
>

```dart

void main() {
  Map<String, dynamic> map1 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  Map<String, dynamic> map2 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  }; // não é usado

  print(map1 == map1);
}

```

Saída do programa acima:

> 
> true
> 

Essa geralmente não é a definição de igualdade buscada, que seria a no qual os mapas possuem a mesma quantidade de elementos e as chaves dois dois apontam para objetos iguais (a definição de igualdade dos objetos pode ser ampla).

Nesse caso teremos que fazer nossa própria implementação:

```dart

void main() {
  
  Map<String, dynamic> map1 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  Map<String, dynamic> map2 = {
    "nome": "Gabriel Luan",
    "idade": 22,
    "email": "gabrielluan.valentim@gmail.com"
  };
  
  List<String> keys = map1.keys.toList();
  
  bool elementosIguais = keys.every((key) => map1[key] == map2[key]);
  bool mesmaQuantidadeDeEntradas = map1.entries.length == map2.entries.length;
  
  if (elementosIguais && mesmaQuantidadeDeEntradas) {
    print("Listas iguais");
  }
  else {
    print("Listas diferentes");
  }
  
}

```
Saída:

> 
> Listas iguais
> 
