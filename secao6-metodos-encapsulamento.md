# 8 - Trabalhando com métodos e encapsulamento

## 8.1 retorno

- O único modificador possível num parametro de método é o final, indicando que o parametro não pode ser modificado. Caso tente modificar, resulta em erro de compilação
- Para o caso de parametros de tipo primitivo, qualquer valor compatível mais restrito pode ser passado que a jvm converte no tipo esperado
- Early return é uma instrução de retorno num método void antes dele acabar
- Não se pode ter um código que jamais será executado, depois de uma instrução de return. Ocorre **erro de compilação**
- Em métodos que retornam algum valor, todo fluxo deve ter um return ou exception
- Em métodos void, não é permitido atribuir seu retorno a uma variável. **erro de compilação**

1) a 2) d xxx 3) b 4) a 


## 8.2 - static

- Um método ou atributo de instância dentro de um método estático: **erro de compilação**
- Como se fosse um script, se a variável estática não foi inicializada, ela retorna o valor padrão.
- Uma variável estática pode acessar outra estática
- Não é possível reescrever um método estático com um não estático, mesmo numa subclasse. Caso sobreescreva com outro método estático, a referencia do método é a mesma da classe, ou seja, se A extends B e sobreescreve um método estático, os retornos são diferentes se executar A.method() e B.method().

1) a 2) b 3) d 4) a 5) b


## 8.3 - métodos sobrecarregados

- Métodos sobrecarregados podem ter ou não tipo de retorno e visibilidade diferentes
- Compilador sempre invoca o método com o tipo menos genérico (mais específico). Entre Object e String, escolhe String. (A não ser que seja feito casting)
- É possivel inverter a ordem dos parametros e criar dois metodos totalmente distintos, mas em alguns casos pode ocorrer **compile error** ao passar dois ints para um método que recebe int e double

1) a 2) c 3) a 4) a 5) a xxx 6) b 7) b xxx 8) b


## 8.4 - construtor padrão
