O React useMemo Hook retorna um valor memorizado permitindo fazer [[Caching]] de valores entre renderizações.
O useMemo só é executado quando uma de suas dependências é atualizada.
Os ganchos Memo e [[Callback]] são semelhantes. A principal diferença é que useMemo retorna um valor memorizado e useCallback retorna uma função memorizada. 
### Desempenho
O useMemo pode ser usado para evitar que funções pesadas de uso intensivo de recursos sejam executadas desnecessariamente.
Neste exemplo, temos uma função cara que é executada em todas as renderizações.
```jsx
const App = () => {
  const [count, setCount] = useState(0);

  const calculation = expensiveCalculation(count);

  return (
  <div>
	Count: {count}
	<button onClick={increment}>+</button>
	<h2>Expensive Calculation</h2>
	{calculation}
  </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};
```

Para corrigir esse problema de desempenho, podemos usar o useMemo Hook para memorizar a função "expensiveCalculation". Isso fará com que a função seja executada apenas quando necessário.
O useMemoHook aceita um segundo parâmetro para declarar dependências. A função cara só será executada quando suas dependências forem alteradas.
```jsx
  const calculation = useMemo(() => expensiveCalculation(count), [count]);
```