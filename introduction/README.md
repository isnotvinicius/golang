## Introdução da linguagem

Neste Workspace, será criado um projeto de monitoramento de sites para aprender os conceitos básicos da linguagem.

### Instalando o Go

Para este projeto, estou utilizando o Ubuntu como SO, a instalação do Go foi feita através do comando `sudo apt-get install golang-go`, simples e fácil.

### Iniciando o projeto

Depois de instalar o Go, configurei o projeto. Para configurar, precisei criar as pastas `~/pkg`, `~/src` e `~/bin`

- `pkg`: É a pasta que vai conter os pacotes compartilhados da aplicação.

- `src`: É onde fica o source code da aplicação.

- `bin`: É onde ficarão os binários da aplicação.

### Criando um arquivo, compilando e executando

Os arquivos em Go tem sempre a extensão `.go` e devem ser criados dentro de `/src` que, como explicado acima, é onde fica o source code do app. Abaixo um exemplo simples de como estruturar um arquivo em Go e como compilar e executar ele.

```golang
// hello.go

package main

import "fmt"

func main(){
    fmt.Println("Hello World!")
}
```

Definir o package como `main` diz para o Go que a aplicação deve começar através desse pacote. Dentro do package main deve existir a `func main` que é o ponto de partida da aplicação. Portanto `package main -> func main()`.

Como estou querendo exibir um `Hello World!`, precisei importar o pacote `fmt` que é quem contém a function de fazer um print line. Fiz isso usando o `import "fmt"` no começo do arquivo e depois dentro da função main apenas chamei o `Println` e passei o `Hello World!` como parâmetro.

Para compilar e executar este arquivo, rodei o comando `go build hello.go` no mesmo diretório que contém o arquivo que acabei de criar. Ao fazer isso, foi gerado um arquivo executável chamado `hello`. Para executar este arquivo, apenas utilizei o comando `./hello` e a mensagem apareceu no meu terminal.

Também é possível facilitar este processo de build e exec com o comando `go run <arquivo>`, ele nada mais que compila e executa o código num só comando.
