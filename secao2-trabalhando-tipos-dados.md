# Trabalhando com tipos de dados em java

## Declarar e inicializar variáveis

Se uma variável for apenas declarada, ao tentar usa-la, ocorre erro de **compilação**.

- Explicit initialization: quando se declara uma variável e se atribui um valor a ela. 
- Implicit initialization: são variáveis membros de classe, em o que o próprio java as inicializa com valores default. 
    + Primitivos numericos: 0 ou 0.0
    + boolean: false
    + char: vazio (mesmo que 0)
    + referências (não primitivos): null

- São oito tipos primitivos em java: byte (1 byte, de -128 a 127), short (2 bytes), char (1 byte só positivo), int (4 bytes), long (8 bytes), float (4 bytes), double (8 bytes) e boolean.
- Todos os números de ponto flutuante podem assumir os valores
    + +/- infinity
    + +/- 0
    + NaN
- Ao tentar atribuir um valor maior que o limite da variável, **não compila**.

### Bases diferentes

- Java suporta além da decimal, a base octal, hexadecimal e binária.
    + Octal: começar com "0" e só pode ter números entre 0 e 7. Ex: int i = 0467;
    + Hexa: começar com "0x" e números e letras, de 0 a 9, de A a F. 
    + Binário: começa com "0b" e somente os números 0 e 1.
- Se colocar algum número que a base não suporta, **não compila**.

### Notação científica

- Só funcionam com double ou float
    + double d = 3.1E2; resulta em 310.0
    + float e = 2e3f; resulta em 2000.0
    + float f = 1E4F; resulta em 10000.0

### Underlines em literais

- Usado para facilitar a leitura do código
- Só podem ser colocados com valores númericos em ambos os lados, caso contrário resultam em erro de compilação.
    + int v1 = 0_100_267_760; ok
    + int v2 = _123_341; erro
    + double d = 345.45_e3; erro
    + double d = 345._45e3; erro

### Iniciando chars

- Use aspas simples. char c = 'A'
- ou o número que representa o caracter na tabela unicode. char c = 65; //A
- É possivel usar a representação de um caracter unicode de outras línguas iniciando o char com \u. char c = '\u3A9';

### Identificadores

- São 50 palavras chave como class, void, this, static, strictfp, native, etc. E mais 3 reservadas, null, true e false que a especificação não considera como palavra chave e sim como literal.
- Um identificador é válido deve seguir as regras
    + Deve ser diferente de uma palavra chave
    + Pode usar letras (unicode), números, $ e _
    + O primeiro caracter não pode ser número

Exercicios
1) d 2) a 3) d 4) f 5) b 6) f xxx 7) a 8) c 9) e 10) d 



## 4.2 Variáveis de referência

1) e 2) f

1) c xxx -> variavel membro é a variável da classe

## 4.4 Ciclo vida objeto

- O objeto está **acessível** quando ele foi criado e atribuido a uma variável. Ex: Person p = new Person()
- Se num trecho de código foram criados 2 objetos (Person p = new Person() e new Person()) e atribuido uma string a uma propriedade de um deles (p.nome = "Fulano"), então foram criados 3 objetos.
- Pode haver questões perguntando quantos objetos são elegíveis ao garbage collector

1) c 2) b 3) b


## 4.5 Chame métodos em objetos

- Ao tentar atribuir uma variável a um método void, ocorre erro de compilação
- enchanced for = for each
- ao chamar um método varargs com o mesmo nome de um comum (param sem ser vararg), java dá prioridade para comum
- 
1) b 2) c 3) e 4) e 


## 4.6 StringBuilder

- new StringBuilder(50) não aloca 50 espaços em branco, portanto o length ainda será 0

