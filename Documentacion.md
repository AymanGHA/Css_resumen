## CSS (Hojas de estilo en cascada) 


El CSS sirve para aplicar, el HTML es esqueleto por tanto lo recomendable es no usar algunas etiquetas HTML que sirven para modificar el estilo. 

#### NO HACER: 
```html
<p> Lorem ipsum dolor sit amet, <strong>consectetur adipiscing </strong> Nuncvulputate semper 	sapien eget vulputate. Vivamus sed tortor et nulla.<p>
```

#### HACER: 
```html
<p> Lorem ipsum dolor sit amet, <span class=”negrita”>consectetur adipiscing </span> Nuncvulputate semper sapien eget vulputate. Vivamus sed tortor et nulla. <p> 
```

El termino hojas de estilo en cascado nos dice que los estilos se aplicaran de arriba abajo por consecuencia si se modifica dos veces un elemento, se le aplicará la última modificación.

------------

Hay **3** formas de aplicar CSS:

1. Css interno: 
Etiqueta style
```html
 <head> 
… <! -- Algunos metadatos --> 
<style>//css code</style> 
 </head> 
```

1.  Css externo: 
###### Etiqueta <link>
```html
 <head> 
… <! -- Algunos metadatos --> 
<link rel = “stylesheet” href=”ruta-del-archivo.css”/> 
 </head> 
```

1. CSS en línea: 
###### Atributo style 
```html
  <span style = “border:2px solid blue;”> Sasuke </span> 
```
