# 7 - Usando laços

## While

- A condição deve ser um boolean
- Pode-se omitir as chaves se for apenas um comando
- O laço se repete até a condição se torne falsa
- Se tiver algum comando após o laço e ele for infinito, o compilador reconhece e não permite compilar
- Da mesma forma, se o compilador reconhecer um laço que nunca será executado (e que tenha código dentro) ele não permite compilar "unreachable statement"
- O compilador só consegue analisar operaçoes com constantes e literais

1) e 2) c

## For

- Todos os 3 argumentos do for são opcionais, portanto é possivel executar for (;;) {} que após compilado vira, for (;true;) {}
-  Na inicialização do for, é possivel declarar e inicializar diversas variáveis do mesmo tipo, ou inicializar variaveis de tipos diferentes
-  Na inicialização só é permitido definir um tipo de variável, ex: int a=1; int b=2 //não funciona
-  Na atualização, é possível fazer diversas atribuições separadas por vírgula
-  Na atualização podemos executar qualquer trecho de código
-  No enhanced for, não é possível modificar a coleção e nem saber em que índice estamos

1) a 2) a 3) b xxx 4) b 5) a 6) e 

## Do...While

- Se não tiver ';' no fim do while, ocorre erro de compilação. Não deve passar despercebido.
- As chaves podem ser omitidas caso tenha somente um comando

1) b 2) a xxx 3) c 4) c xxx 5) a xxx

## Compare tipos de laço

1) a 2) a 3) b 4) d 5) b

## Break e continue

- Pode ser usado em qualquer estrutura de laço
- break finaliza o laço totalmente; continue somente a iteração atual
- Se um laço contém um laço com true mas tem um break, ele é compilável
- switch só aceita break
- Labeled statements
  - Nome segue as regras de variaveis
  - Label pode ser usado em qualquer comando, mas o break e continue só funciona com for, while e switch
  - Label tem que ser relativo ao for atual e não um que já foi executado
  - Labels podem ser repetidos, desde que não estejam no mesmo escopo
  - Labels e variaveis podem ter o mesmo nome, no mesmo escopo
  - Um mesmo comando pode ter mais de um label

1) a 2) d 3) j  




 
