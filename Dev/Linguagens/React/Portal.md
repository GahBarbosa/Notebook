Os [[React]] Portals são um conceito que permite aos desenvolvedores renderizar seus elementos fora da árvore hierárquica do React sem comprometer o relacionamento pai-filho entre os componentes
```jsx
export default function App() {
	const [showModal, setShowModal] = useState(false);
	return (
		<>
			<button onClick={() => setShowModal(true)}>
				Show modal using a portal
			</button>
			{showModal && createPortal(<Modal />,document.body)}
		</>
	);
}
```
Os portais são ótimos para locais onde você deseja renderizar elementos uns sobre os outros. Alguns exemplos comuns abaixo:
- Telas de carregamento: quando uma tarefa está acontecendo em segundo plano  é sensato mostrar uma tela de carregamento.
- Cartões de perfil: Fornece informações rápidas sobre o perfil do usuário sem clicar em sua página:![[react-portal-use.gif]]
- Alertas de cookies: fornece ao usuário opções para permitir que ele escolha quais cookies deseja permitir em seu navegador da web:![[Pasted image 20230804174622.png]]