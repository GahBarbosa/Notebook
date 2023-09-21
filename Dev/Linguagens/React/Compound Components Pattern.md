[Repositório com exemplo](https://github.com/GahBarbosa/compound-components-pattern)

O Compound Components pattern é um método de design aonde o componente principal encapsula um grupo de componentes, fornecendo uma arquitetura simples e fácil de entender. Esse método permite que os desenvolvedores criem componentes complexos de maneira flexível, permitindo que criem interfaces do usuário altamente personalizáveis ​​com pouco código extra. 

```jsx
// Declaração de um dos components do Compound 
// NotificationRoot.tsx
import { ReactNode } from "react"

interface NotificationRoot {
    children: ReactNode
}

export function NotificationRoot({children}: NotificationRoot) {
    return(
        <div className="bg-zinc-200 px-8 py-4 flex items-start gap-6">
            {children}
        </div>
    )
}
```

```jsx
// Exportando e juntando os elementos do compound component
// Notification/index.tsx
import { NotificationActions } from "./NotificationActions";
import { NotificationAction } from "./NotificationAction";
import { NotificationContent } from "./NotificationContent";
import { NotificationIcon } from "./NotificationIcon";
import { NotificationRoot } from "./NotificationRoot";

export const Notification = {
    Root: NotificationRoot,
    Icon: NotificationIcon,
    Content: NotificationContent,
    Actions: NotificationActions,
    Action: NotificationAction
}
```

```jsx
// Composição do Compound Component sendo utilizado
// App.tsx
import { Notification } from './Notification';

export function Widget() {
    return (
		<Notification.Root>
			<Notification.Icon icon={PeopleOutlineOutlinedIcon} />
			<Notification.Content text='lorem ipsum' />
		</Notification.Root>
		
		<Notification.Root>
			<Notification.Icon icon={PeopleOutlineOutlinedIcon} />
			<Notification.Content text='lorem ipsum' />
			<Notification.Actions>
				<Notification.Action icon={ClearOutlinedIcon} />
				<Notification.Action icon={CheckOutlinedIcon} className='bg-black'/>
			</Notification.Actions>
		</Notification.Root> 
	)
}
```

## Prós e contras

#### Pros 

Flexibilidade: uma maneira flexível de criar componentes de interface do usuário complexos, mantendo uma API limpa e concisa. Esse padrão permite criar componentes altamente personalizáveis ​​e reutilizáveis ​​sem passar muitos adereços para o componente

Separação de preocupações: cada componente filho é responsável por sua funcionalidade e customização específica

#### Cons 

Herança de props: construir componentes com esse padrão apenas filhos diretos do componente pai terão acesso aos props, o que significa que não podemos agrupar nenhum desses componentes em outro componente.


```jsx
export default function ExampleMenu() {
  return (
    <Example>
      {/* A div quebra a herança das props */}
      <div>
        <Example.Toggle />
        <Example.List>
          <Example.Item>Edit</Example.Item>
          <Example.Item>Delete</Example.Item>
        </Example.List>
      </div>
    </Example>
  );
}
```

Uma solução para esse problema seria usar o padrão de componente composto flexível para compartilhar implicitamente o estado usando a [[Context API]].