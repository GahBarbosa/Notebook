[[React]]
Quando precisamos que um componente filho tenha os dados do pai, precisamos informar esses dados e funções através das props, com a Context API esse cenário é diferente podendo ser lido e alterado de qualquer lugar da aplicação, já que ela é um gerenciador de estado global.
![[Pasted image 20230802222700.png]]

```jsx
// Criação do contexto 
// Context.js 
import React, { createContext } from 'react';
const Context = createContext(0);
export default Context;
```

```jsx
// Utilização do Contexto 
// App.js 
import React, { useState } from 'react';
import Context from './Context';
import Counter from './Counter';
export default function App() {
	const [total, setTotal] = useState(0);
	return (
		<Context.Provider value={[total, setTotal]}>
			<div>
				<p>{ total }</p>
				<Counter />
			</div>
		</Context.Provider>
	);
}
```

```jsx
// Manipulação do Contexto
// Counter.js
import React, { useContext } from "react";
import Context from "./Context";

export default function Counter() {
	const [total, setTotal] = useContext(Context);
	return (
		<div>
			<h3>{total}</h3>
			<button type="button" onClick={() => setTotal(total + 1)}>
				Contador
			</button>
		</div>
	);
}
```
