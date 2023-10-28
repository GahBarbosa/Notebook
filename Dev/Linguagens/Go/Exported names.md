No [[Go]], um nome é exportado se começar com letra maiúscula. Por exemplo, Pizza é um nome exportado, assim como Pi, que é exportado do pacote math.

pizza e pi não começam com letra maiúscula, portanto não são exportados.

Ao importar um pacote, você pode utilizar apenas os nomes exportados. Quaisquer nomes "não exportados" não são acessíveis fora do pacote.

```go
import "math"

math.pi // não exportado pelo pacote, undefined
math.Pi // 3.141592653589793
```