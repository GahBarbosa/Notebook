#Incompleto 
#### Tailwind Variants
biblioteca que permite configurações de variantes de modo mais limpo e fácil 
```javascript
{/* Declaração */}
import { tv, VariantProps } from 'tailwind-variants'
const button = tv({
    base: 'flex items-center justify-center rounded',
    variants: {
        size: {
            default: 'h-10 px-4',
            sm: 'h-8 px-3',
            xs: 'h-6 px-2 text-xs',
        },
        success: {
            true: 'bg-emerald-500 hover:bg-emerald-600',
        },
    },
    defaultVariants: {
        size: 'default',
        success: false,
    },
})
export type ButtonProps = ComponentProps<'button'> & VariantProps<typeof button>
export function Button({ success, size, className, ... props }: ButtonProps) {
    return (
    <button
        data-success={success}
        className= {button ({ size, success, className })}
        { ... props}
    >
        {success ? <CheckCircle className="h-4 w-4" /> : props .children}
    </button>
    )
}
```

```javascript
{/* Uso */}
export function App(){
	return(
		<Button success className="w-20">Sign in</Button>
		<Button size="sm">Sign in</Button>
		<Button size="xs">Sign in‹/Button>
		<Button>Sign in‹/Button>
	)
}
```
#### Tailwind merge
biblioteca que substitui classes conflitantes e mantém todo o resto intocado
```javascript
import { twMerge } from 'tailwind-merge'

export function Button({ className, ...props }: ButtonProps) {
    return (
        <button
            cLassName={twMerge('flex h-10',className)}
            { ... props)
        ></button>
    )
}
```