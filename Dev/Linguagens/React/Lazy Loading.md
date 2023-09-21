técnica de dividir seu código em vários pacotes que podem ser carregados sob demanda ou em paralelo.
```jsx
import { useState, Suspense, lazy } from 'react';
const Example = lazy(() => import('./Example.js'));

export default function MarkdownEditor() {
	return (
		<Suspense fallback={<Loading />}>
			<Example />
		</Suspense>
	);
}
function Loading() {
	return <p><i>Loading...</i></p>;
}
```
Somente dados habilitados para Suspense ativarão o componente Suspense. Eles incluem:
- Fetch de dados com frameworks habilitadas para Suspense, como Relay e Next.js
- Código de componente de carregamento lento com lazy

## Revelando o conteúdo conforme ele carrega 
Quando um componente é suspenso, o componente Suspense pai mais próximo mostra o fallback. Isso permite aninhar vários componentes do Suspense para criar uma sequência de carregamento
```jsx
<Suspense fallback={<BigSpinner />}>  
	<Biography />  
	<Suspense fallback={<AlbumsGlimmer />}>  
		<Panel>  
			<Albums />  
		</Panel>  
	</Suspense>  
</Suspense>
```
Com essa mudança, a exibição da Biografia não precisa “esperar” o carregamento dos Álbuns.

A sequência será:

1. Se a Biografia ainda não foi carregada, o BigSpinner é mostrado no lugar.
2. Depois que a Biografia termina de carregar, o BigSpinner é substituído pelo conteúdo.
3. Se os Álbuns ainda não tiverem sido carregados, o AlbumsGlimmer será exibido.
4. Por fim, assim que Albums terminar de carregar, ele substituirá AlbumsGlimmer.