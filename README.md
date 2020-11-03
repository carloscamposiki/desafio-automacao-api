# Desafio Automação API

Autor: Carlos Henrique da Silveira Campos

Projeto para automação de api do [desafio-sicredi](https://github.com/desafios-qa-automacao/desafio-sicredi).

## Ferramentas Utilizadas

- Java 8
- Rest Assured
- Cucumber
- Jackson
- Hancrest (para asserções em conjunto com o Rest Assured)
- Cluecumber (para geração de relatório HTML)
- Maven

## Requisitos para Execução da Automação API

- Java 8 SDK instalado (para verificar se está instalado execute o comando `javac -version` no console).
- Maven instalado (para verificar se está instalado execute o comando `mvn -v` no console).
- [desafio-sicredi](https://github.com/desafios-qa-automacao/desafio-sicredi) executando.

## Executando

Para executar a automação execute, na raiz do projeto onde está o arquivo .pom, o seguinte comando:

`mvn clean -Dtest=Suite test`

Caso a AÇK esteja executando em um endereço ou porta diferente da padrão (http://localhost:8080) execute a automação utilizando o seguinte comando:

`mvn clean -Dtest=Suite -Dhost=http://localhost:8888 test`

## Gerando Relatório HTML

Pelo Cluecumber é possível gerar um report HTML dos resultados. Para isso, após fazer a execução da automação conforme explicado acima execute o seguinte comando:

`mvn cluecumber-report:reporting`

Lembrando que:
- O relatório vai ser gerado na pasta report/cluecumber-report.
- O relatório vai sobreescrever qualquer relatório anterior que se encontrar nessa pasta.
- O relatório possui um [bug](https://github.com/trivago/cluecumber-report-plugin/issues/253) de codificação ao exibir exception stacktrace.
- Um relatório de exemplo se encontra na pasta documentos.
- O relatório não é compatível com o Internet Explorer.

## Documentos

Na pasta documentos se encontra:
- Cenários de testes elaborados conforme a documentação disponibilizada.
- Relatório de defeitos encontrados na aplicação.
- Exemplo de relatório HTML gerado pelo Cluecumber.


