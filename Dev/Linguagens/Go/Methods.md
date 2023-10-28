Um método é uma função com um argumento receptor especial.
O receptor aparece em sua própria lista de argumentos entre a palavra-chave `func` e o nome do método.
Métodos podem ser definidos para qualquer tipo de receptor ponteiro ou valor. Go trata automaticamente conversões entre valores e ponteiros para métodos de chamada. Você pode querer usar um ponteiro do tipo receptor para evitar a cópia de um método de chamada ou para permitir que o método faça mutação da estrutura recebida.
```go
func (r *rect) area() int {
    return r.width * r.height
}

func (r rect) perim() int {
    return 2*r.width + 2*r.height
}
```