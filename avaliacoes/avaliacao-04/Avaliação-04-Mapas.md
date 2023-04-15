## 01) O que é um mapa em Dart?

Um mapa é uma coleção de valores que são associados a chaves únicas para cada um deles.

## 02) Como criar um mapa vazio em Dart?

```dart

Map<K, V> map = {};

```

03) Como criar um mapa com elementos em Dart?

Colocando os elementos entre chaves. Os elementos devem estar separados entre si por vírgulas e a chave e o valor de cada um separados por ":".

Exemplo:

```

Map<num, String> mapa = {
  1: "Pessoa 01",
  2: "Pessoa 02",
  3: "Pessoa 03"
};

```

04) Qual a diferença entre uma lista e um mapa em Dart?

Uma lista é iterável e seus elementos são alcançaveis por meio de índices que resultam da ordem na qual os elementos são inseridos. Já um mapa não é iterável e seus elementos são acessíveis por meio de suas chaves. 

05) Como adicionar um elemento a um mapa em Dart?

Colocando a chave entre colchetes ao chamar o objeto e atribuindo ao novo elemento conforme visto a seguir.

```

Map<num, String> mapa = {
  1: "Pessoa 01",
  2: "Pessoa 02",
  3: "Pessoa 03"
};

mapa[4] = "Pessoa 04";

```

06) Como remover um elemento de um mapa em Dart?

Chamando o método `remove` do mapa e passando como parâmetro a chave do elemento a ser removido.

07) Como verificar se um mapa contém uma determinada chave em Dart?

Com o método `containsKey` passando a chave como parâmetro. Se o mapa já contem essa chave, o método retorna true, caso contrário retorna false.

08) Como verificar se um mapa é vazio em Dart?

Com a propriedade `isEmpty`, que será true quando o mapa for vazio e false caso contrário.

09) Como acessar o valor de uma chave em um mapa em Dart?

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

10) Como alterar o valor de uma chave em um mapa em Dart?

Simplesmente reatribuindo o valor da chave ou com o método `update`.

11) Como obter todas as chaves de um mapa em Dart?



12) Como obter todos os valores de um mapa em Dart?

13) Como verificar se duas chaves em um mapa são iguais em Dart?

14) Como criar um mapa a partir de duas listas em Dart?

15) Como criar uma lista de chaves a partir de um mapa em Dart?

16) Como criar uma lista de valores a partir de um mapa em Dart?

17) Como transformar um mapa em uma lista de pares chave-valor em Dart?

18) Como remover todos os elementos de um mapa em Dart?

19) Como calcular o tamanho de um mapa em Dart?

20) Como verificar se dois mapas são iguais em Dart?
