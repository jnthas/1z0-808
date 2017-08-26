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

- Pode-se criar arrays de quantas dimensões quiser
- Pode-se inicializar somente a primeira dimensão, deixando as outras pra depois. Se for com valores conhecidos, deve-se inicializar todas as dimensões.
- Ao tentar atribuir um double a um array de int, não compila (possible loss of precision)

1) a 2) f 3) g 4) a 


## 6.3 ArrayList

- Jamais se esqueça de importar a ArrayList!!! (java.util.ArrayList)
- O método remove() remove somente a primeira ocorrência na lista
- Ao reescrever o equals, o parametro correto é Object e não o proprio elemento!!!
- ArrayList aponta para referencias, se um objeto for modificado, ele será também no ArrayList
- Num enhanced-for, é possivel setar um valor na variavel do laço, mas o arryalist não é modificado

1) a 2) d 3) f 4) h 5) a 6) b 7) a 8) b 9) a xxx