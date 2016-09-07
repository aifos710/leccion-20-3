# leccion-20-3

Modificar el siguiente script para que muestre el resultado correcto.

```javascript
feature = 'closures'; 
(function () {     
	if ( typeof feature === 'undefined' ){         
		var feature = 'callbacks';         
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();
```


El código muestra el mensaje JS coders love its callbacks, porque es una funcion anonima autoejecutable, por lo tanto busca la variable declarada dentro de ella.



```javascript
feature = 'closures'; 
(function () {     
	if ( typeof feature === 'undefined' ){         
		 feature = 'callbacks';        
		console.log('JS coders love its ' + feature );     
	} else {         
		console.log('JS developers love its ' + feature );     
	} 
})();
```

Nota: Solo modificar una línea para que se obtenga el resultado deseado.
 
 ```javascript
 feature = 'callbacks'; 
 ```
 al quitar el 
 ```javascript
 var
 ```
 la funcion autoejecutable no tiene una variable declarada y por lo tanto el Hoisting hace que use la variable global.
