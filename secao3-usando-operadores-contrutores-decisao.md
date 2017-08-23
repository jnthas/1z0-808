# 5 Usando operadores e construções de decisão



## 5.1 Use operadores java

- Para se atribuir um valor a uma variável ambos devem ser do mesmo tipo ou de um tipo menos abrangente.
	- Ordem de compatibilidade:
	- byte -> short -> int -> long -> float -> double
	- char -> int
	- Número sem casa decimal, padrão é int, com casa decimal, padrão é double
	- Exceção com tipos menos abrangentes que int: byte, short, char. É possivel atribuir um int a um desses tipos, desde que não ultrapasse o limite, ex: byte b = 200 //erro
	- Com objetos, a atribuição é sempre por **referência**
	- Para saber o tipo retornado depois de uma operação aritmética, a regra é: o resultado é o tipo mais abrangente entre as variáveis ou **no mínimo int**.
	- int dividido por 0, gera ArithmeticException. float ou double gera + ou - Infinity (independente se tiver no dividendo ou divisor). 
	- Toda comparação envolvendo valores numéricos não considera o tipo da variável, portanto 1 == 1.0 //true
	- Tipo não primitivo (e boolean) só aceita == ou !=
	- char tem valor numerico, portanto, pode ser feito 'a' == 1
	- Usando & ou | a validação é sempre feita em todas as comparações para depois obter o resultado. Já com os operados de curto circuito, && e || basta uma condição ser satisfeita
	- Atribuições em sequencia, sempre da direita pra esquerda, a=b=c // portanto a = c
	- Operadores ternários sempre tem que retornar valores que temos que usar para atribuir, imprimir

1) b 2) b 3) d 4) d 5) a? 6) E/I/E/-I 7) e xxx 8) d 9) e 10) Sim xxx 11) d xxx 12) c 13) a 14) c 15) a 16) f 17) c 18) f 19) a 20) c 21) a
	
## 5.2 Use parênteses 

1) a 2) b

## 5.3 Testde de igualdade entre strings

- Pool de strings, o Java mantem um pool de strings somente as criadas usando **literais**. Ex.: String a = "Hi";
- Se forem criadas duas strings com o mesmo conteudo o java apontam os dois objetos pra mesma referência, por isso se usar == vai retornar true.
- Ao concatenar uma string usando literal, ela tbm vai pro pool. Ex.: String a = "a" + "b";
- Se o método de uma string retornar o mesmo conteúdo, não é criado um objeto novo.
- Questão de prova: contar quantos objetos string foram criados
- Se uma string tiver um "", já é diferente com ==

1) c xxx 2) e xxx 3) e 4) e 5) a

## If/else

- Dentro do if, deve ter um boolean senão dá erro de compilação
- Deve haver pelo menos um comando dentro do bloco do if ou dá erro decompilação
- Grande parte das perguntas na prova são pegadinhas com a identação do if
- Unreachable code = qdo o compilar percebe que um código não será executado em hipótese alguma, ex: um comando após o return.
- Todos os caminhos devem retornar algo ou lançar uma exceção para que o compilador aceite

1) c 2) b xxx 3) a 4) a 5) b 

## Switch

- Deve ser um int, wrapper de int, string ou enum
- O case deve ser do mesmo tipo do switch, ou gera erro compilação
- no case, só é permitido literal e constantes, ou operações envolvendo os dois. Não aceita null. Se a constante não for inicializada na mesma linha da declaração, tbm não aceita.

1) d 2) a 3) b 4) a 5) c xxx 6) a 
