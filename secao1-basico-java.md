# O básico do Java

## Escopo

- Variável de instância (ou objeto) = this
- Shadowing: declarar variável local com mesmo nome de uma variável de instância (this.x = x)

## Estrutura classe Java

- Default package: quando classe não tem pacote 
- Construtor da classe pode ter "return" vazio
- Se existir alguma classe/interface pública o arquivo deve ter o mesmo nome
- Imports e packages só existem 1 por arquivo

## Classes executáveis

- main(String[] args) ou main(String... args) ou main(String args[])
- Definir em que versão do java código foi escrito "javac teste.java -source 1.3"
- Passar parâmetros para o java "java -Dkey=value -Dkey=value teste arg1"
- 2 formas de configurar o classpath:
  - variável de ambiente CLASSPATH do SO (é global)
  - usando -cp ou -classpath no javac e java
- Criar JAR: jar -cf lib.jar certification
- META-INF/Manifest.mf
  - Especifica a classe do main -> Main-Class: Certification
  - Gerando o jar -> jar cfm lib.jar manifest Certification 
  - O arquivo DEVE possuir a última linha vazia senão não entra no JAR

## Imports

- Se houver import específico e outro genérico, java usa o específico. Ex: import java.util.* / java.sql.Date;
- Por padrão java importa java.lang.* então é opcional importar classes desse pacote

## Pacotes

- Usar classe com mesmo nome, mas de pacotes diferentes:
  - Usar import genérico -> erro ao acessar a classe
  - Tentar importar classe de mesmo nome de pacotes diferentes usando import específico -> erro no import


