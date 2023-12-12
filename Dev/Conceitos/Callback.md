Em programação de computadores, um método de callback é uma rotina que é passada como parâmetro para outro método. É esperado então que o método execute o código do argumento em algum momento. A invocação do trecho pode ser imediata, como em um função síncrona, ou em outro momento [[Assíncrono]].

```javascript
const mensagem = function() {  
    console.log("Essa mensagem é exibida depois de 3 segundos");
}
 
setTimeout(mensagem, 3000);
```
Callbacks podem ser funções anônimas 
```javascript
setTimeout(function() {  
    console.log("Essa mensagem é exibida após 3 segundos");
}, 3000);
```
ou Arrow function
```javascript
setTimeout(() => { 
    console.log("Essa mensagem é exibida após 3 segundos");
}, 3000);
```