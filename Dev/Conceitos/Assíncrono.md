O conceito de "assíncrono" se refere a operações ou processos que não ocorrem simultaneamente ou que não dependem do término de uma operação anterior para começar. O código síncrono é lido e executado da primeira até a última linha, em ordem. O código  assíncrono, por sua vez, não necessariamente respeitará a ordem das linhas do código, podendo ter funções sendo lidas e executadas simultaneamente ou aleatoriamente.

```jsx
// Função assíncrona 
async function fetchData() { 
	try { 
		// Espera pela resposta da API 
		let response = await fetch('https://api.example.com/data'); 
		// Converte a resposta em JSON 
		let data = await response.json(); 
		console.log(data); 
	} catch (error) { 
	console.error('Erro ao buscar dados:', error); 
	} 
} 
fetchData(); // Chama a função assíncrona
```