Uma instrução `defer` adiciona a chamada da função em uma pilha. Todas as chamadas naquela pilha são chamadas quando as funções do mesmo nível  de execução são retornadas. Como as chamadas são colocadas em uma pilha, elas são chamadas na ordem último a entrar, primeiro a sair, [[LIFO]].

Os argumentos da chamada adiada são avaliados imediatamente, mas a chamada de função não é executada até que as funções do mesmo nível retorne.

```go
package main

import "fmt"

func main() {
	defer fmt.Println("eee")	
	defer fmt.Println("ddd")	
	defer fmt.Println("ccc")
	fmt.Println("aaa")
	fmt.Println("bbb")
}
```

```go
// Resultado
aaa
bbb
ccc
ddd
eee

```
