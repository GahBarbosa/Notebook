Framework de testes, compatível com [[Jest]], e desenvolvido em Vite .

ESM nativo e Out-of-the-box [[TypeScript]] não necessitando de uma biblioteca de asserção separada. Requer configuração mínima e execução mais rápida em comparação com projetos baseados em [[Jest]] e Babel.

```javascript
// sum.js
export function sum(a, b) {
  return a + b
}
```

```javascript
// sum.test.js
import { expect, test } from 'vitest'
import { sum } from './sum'

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3)
})
```