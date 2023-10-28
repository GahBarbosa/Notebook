`useRef` é um [[React]] Hook que permite referenciar um valor que não é necessário para renderização.

```jsx
import { useRef } from 'react';  

function MyComponent() {  
	const intervalRef = useRef(0);  
	const inputRef = useRef(null);  
}
```