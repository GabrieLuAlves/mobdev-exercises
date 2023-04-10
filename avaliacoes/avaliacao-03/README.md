# Respostas da avaliação 03


## 1) Qual o resultado da expressão `5 + 3 * 2`?

A primeira operação a ser executada será a multiplicação, que resultará em 6. Em seguida o resultado dessa operação será somado a 5, portanto **a resposta será 11**.  

## 2) Qual o resultado da expressão `10 / 2 - 3`?

Como a multiplicação, a divisão será a primeira a ser execultada, em seguida o resultado da divisão é subtraído por 3, logo **o resultado será 2**.

## 3) Qual o resultado da expressão `7 % 3`?

O operador % retorna o resto da divisão entre 7 e 3, que **é igual a 1**.

## 4) Qual o valor de x após a execução da expressão `x += 5`?

Essa expressão equivale a `x = x + 5`.
Portanto o novo valor de x **será o valor anterior de x somado a 5**

## 5) Qual o valor de y após a execução da expressão `y *= 3`?

Essa expressão equivale a `y = y * 3`.
Portanto o novo valor de y **será o valor anterior de y multiplicado por 3**

## 6) Qual o resultado da expressão `!(2 < 5) || (3 > 1)`?

As primeiras operações a serem executadas serão as que estão entre parenteses.  
Logo, teremos que:  

`(2 < 5)` resultará no valor booleano `true`, pois 2 é de fato menor que 5  
`(3 > 1)` resultará no valor booleano `true`, pois 3 é de fato maior que 1

Em seguida, será a vez da negação ser executada, fazendo com que o `true` que resulta de `(2 < 5)` se torne `false`.  
Por fim, o que resta será a expressão `false || true`, que **resulta em `true`**.

## 7) Qual o valor de z após a execução da expressão `z ?? 10`?

O operador ?? fará com que o valor de z seja checado.  

**Caso z não seja null, a expressão resulta no valor de z, do contrário resultará em 10.**

## 8) Qual o resultado da expressão `2 + 2 == 4 && 3 + 3 == 6`?

Nessa expressão, as somas `2 + 2` e `3 + 3` serão as primeiras a serem executadas e resultarão respectivamente em 4 e 6.  

Em seguida, as comparações `4 == 4` e `6 == 6` serão executadas. Ambas retornam `true`.

A última operação, `true && true`, **resultará em true**.

## 9) Qual o resultado da expressão `5 < 3 || 4 > 2 && 6 != 6`?

Nesse caso a última operação a ser executada será a and (representada com &&), e do lado esquerdo temos a operação 6 != 6, que resultará em `false`. Como a operação and só resulta em true caso os dois valores booleanos forem `true`, pode-se afirmar com certeza que **o resultado será false**.

## 10 ) Qual o valor de a após a execução da expressão `a ??= 10`?

O operador ?? fará com que o valor de `a` seja checado.  

**Caso o valor de `a` seja `null`, o valor 10 será atribuído a a, do contrário o valor de `a` continuará o mesmo.** 

