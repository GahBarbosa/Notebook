`useState` é um [[React]] Hook que permite adicionar uma variável de estado ao seu componente.

```jsx
import { useState } from 'react';  

function MyComponent() {  
	const [age, setAge] = useState(28);  
	const [name, setName] = useState('Taylor');  
	const [todos, setTodos] = useState(() => createTodos());  
 return ()
}
```