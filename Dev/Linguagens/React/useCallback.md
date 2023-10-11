O Hook React useCallback retorna uma função de retorno de chamada memorizada.
Pense na memoização como armazenar um valor em [[Caching]] para que ele não precise ser recalculado.
Isso nos permite isolar funções que consomem muitos recursos para que não sejam executadas automaticamente em todas as renderizações.
Os ganchos Callback e [[useMemo]] são semelhantes. A principal diferença é que useMemo retorna um valor memorizado e useCallback retorna uma função memorizada. 
Um motivo para usar useCallback é evitar que um componente seja renderizado novamente, a menos que seus acessórios tenham sido alterados.

```jsx
import { useState, useCallback } from "react";
import ReactDOM from "react-dom/client";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = useCallback(() => {
    setTodos((t) => [...t, "New Todo"]);
  }, [todos]);

  return (
    <>
      <Todos todos={todos} addTodo={addTodo} />
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
      </div>
    </>
  );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```