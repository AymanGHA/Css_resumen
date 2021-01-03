
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

2.  Css externo: 
###### Etiqueta <link>
```html
 <head> 
… <! -- Algunos metadatos --> 
<link rel = “stylesheet” href=”ruta-del-archivo.css”/> 
 </head> 
```

3. CSS en línea: 
###### Atributo style 
```html
  <span style = “border:2px solid blue;”> Sasuke </span> 
```
------------
#### SINTAXIS BÁSICA 
```css
Selector {
 propiedad : valor;
 propiedad: valor;
 ...
}
```
**- Selector** : Selecciona los elementos (ETIQUETAS) a modificar su estilo ;
**- propiedad** : Lo que le vamos a cambiar al elemento seleccionado ;
**- valor** : Valor de la propiedad ;

EJEMPLO : 
```css
p{
	color : red; // cambiamos el color del texto
}
```

-------------
#### LISTA DE SELECTORES Y EJEMPLOS 
SELECTOR
###### selecciona todos los divs 
```css
div {
 color : "blue";
}

```
SELECTOR[ATRIBUTO]
###### divs con el atributo class
```css
div[class] {
 color: red;
}
```
SELECTOR[ATRIBUTO="X"]
###### div donde el valor del atributo sea rojogrande
```css
div[class="rojogrande"] {
 color: red;
}
```

##### SELECTOR[ATRIBUTO^="X"]
###### divs donde el valor del atributo class comienza con rojo
```css
 div[class^="rojo"] {
 color: red;
}
```
##### SELECTOR[ATRIBUTO$="X"] 
###### divs donde el valor del atributo class acaba en grande.
```css
div[class$="grande"] {
 width : 500px; // ancho del elemento a 500px
}
```
#### SELECTOR[ATRIBUTO*="X"]
######  divs donde el valor del atributo class contenga la palabra grande en cualquier sitio
```css
div[class*="ojo"] {
 color: red;
}
```
#### SELECTOR[ATRIBUTO~="X"]
######  divs donde el valor del atributo class contenga la palabra grande
```css
div[class~="rojo grande"] {
 color: red;
}
```
SELECTOR[ATRIBUTO|="X"]
###### divs donde el valor del attributo class es exactamente rojo ,o comienza con rojo inmediatamente 
```css
div[class|="rojo"] {
 color: red;
}
```
