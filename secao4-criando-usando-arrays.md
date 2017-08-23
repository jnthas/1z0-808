# 6 Criando e usando arrays

## 6.1 Array unidimensional

- É possível colocar o [] após o nome da variável. Ex: double size[]
- Variável local não tem valor padrão null, por isso dá erro de compilação
- Criar e inicializar array com tamanho 0, compila e roda
- Já criar um array e inicializar com numero negativo, compila, mas ao rodar gera um NegativeArraySizeException
- Num array incializado com valores, é possivel ter valores null, desde que o array seja de referência 
- int[] numbers = {1,2,3,4,5}; //funciona mas a criação e inicialização devem estar **na mesma linha**, senão dá compile error
- Tentar acessar um posição inválida no array, gera ArrayIndexOutOfBounds
- Num array de objetos, todas as posições se tornam null após a inicialização do array

1) e 2) b 3) b 4) c 5) c xxx 6) f 7) c xxx 8) a,b,f,j


## 6.2 Array multidimensional

