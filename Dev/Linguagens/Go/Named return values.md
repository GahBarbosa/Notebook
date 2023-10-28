Os valores de retorno de [[Go]] podem ser nomeados. Nesse caso, elas são tratadas como variáveis ​​definidas no topo da função.
Esses nomes devem ser usados ​​para documentar o significado dos valores de retorno.
```go
func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}
```

Uma instrução `return` sem argumentos retorna os valores de retorno nomeados. Isso é conhecido como retorno "nu".

As instruções de retorno nomeados devem ser usadas apenas em funções curtas, como no exemplo mostrado aqui. Eles podem prejudicar a legibilidade em funções mais longas.