
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
ETIQUETA
###### selecciona todos los divs 
```css
div {
 color : "blue";
}

```
ETIQUETA ETIQUETA
###### Todos los span que son descendientes de un div
```css
div span{
	color :red;
}

```
ETIUETA > ETIQUETA
###### Todos los span que son directamente descendientes de un div
```css
div > span {
	color: red;
}
```
ETIQUETA ~ ETIQUETA 
###### Todos los p que son hermanos de p (hermanos que van despúes de la primera p ).
```html
  <p>NEGRO</p>
  <p>ROJO</p>
  <hr>
  <h1>soy un título</h1>
  <p>ROJO</p>
```
```css
p ~ p{
 color: red;
}

```
ETIQUETA + ETIQUETA 
###### Todos los p que van directamente despues de un p.
```html
  <p>NEGRO</p>
  <p>ROJO</p>
  <p>ROJO</p>
  <hr>
  <p>NEGRO</p>
```
```css
p + p {
  color:red;
}
```
------------

### SELECTORES DE ATRIBUTO 
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
div[class="rojo"] {
 color: red;
}
```

##### SELECTOR[ATRIBUTO^="X"]
###### divs donde el valor del atributo class comienza con rojo
```html
  <div class="boxfile">NO SELECCIONADO</div>
  <div class="file-Size">ROJO</div>
  <div class="fileInput">ROJO</div>
```
```css
 div[class^="file"] {
 color: red;
}
```
##### SELECTOR[ATRIBUTO$="X"] 
###### divs donde el valor del atributo class acaba en grande.
```html
<div class="box-grande">ROJO</div>
<div class="boxgrande">ROJO</div>
<div class="box-mediano">NO SELECCIONADO</div>
```

```css
div[class$="grande"] {
 width : 500px; // ancho del elemento a 500px
}
```
##### SELECTOR[ATRIBUTO*="X"]
######  divs donde el valor del atributo class contenga la palabra grande en cualquier sitio
```html
<div class="developer">ROJO</div>
<div class="gamedeveloper">ROJO</div>
<div class="debian">NO SELECCIONADO</div>
```
```css
div[class*="dev"] {
 color: red;
}
```
##### SELECTOR[ATRIBUTO~="X"]
######  divs donde el valor del atributo class contenga la palabra grande
```html
<div class="numero-uno numero-dos">ROJO</div>
<div class="numero-dos numero-tres">NO SELECCIONADO</div>
```

```css
div[class~="numero-uno"] {
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

------------


SELECTOR[ATRIBUTO="X" **i** ]
###### divs con el atributo lang = ES , y todas sus variaciones. (Es,es,sE)
```html
<div lang="EN">Hello</div>
<div lang="es">Hola</div> <!--ESTOY EN ROJO-->
<div lang="zh">你好</div>
<div lang="ES">Hola</div> <!--ESTOY EN ROJO-->

```
```css
div[lang="ES" i] {
 color: red;
}
```

------------
