`useEffect` é um [[Hook]] que permite sincronizar um componente com um sistema externo. 

Alguns componentes precisam ser sincronizados com sistemas externos. Por exemplo, você pode querer controlar um componente não [[React]] com base no estado React, configurar uma conexão de servidor ou enviar um log analítico quando um componente aparecer na tela. Os efeitos permitem executar algum código após a renderização para que você possa sincronizar seu componente com algum sistema fora do React.

```jsx
import { useEffect } from 'react';  
import { createConnection } from './chat.js';  

function ChatRoom({ roomId }) {  
	const [serverUrl, setServerUrl] = useState('');  
	useEffect(() => {  
		const connection = createConnection(serverUrl, roomId);  
		connection.connect();  
		return () => { connection.disconnect() };
	}, [serverUrl, roomId]);  
}
```