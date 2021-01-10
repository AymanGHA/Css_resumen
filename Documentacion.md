
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
### MODELO DE LA CAJA
###### Cada etiqueta en Html es una especie de caja la cual posee las siguientes propiedades :
##### ANCHO , ALTO , MARGIN , BORDE , MARGEN INTERNO = PADDING
![](https://miro.medium.com/max/725/1*FqGQIGmGdW5EetfS3HFkvA.png)
#### EJEMPLO :
**Borde** : línea rosa que delimita la etiqueta .

**Margen interno (padding)**: distancia entre el borde y el contenido .

**Margen externo**: distancia entre la etiqueta y otros elementos o la misma ventana .

**Ancho** : Ancho del elemento .
**Alto**: Alto del elemento .

![](https://lh3.googleusercontent.com/proxy/7mi5tk-2PBf8hOkc9rT2zZdxlBeZ9OgqTKIg1QTnOw6aq3nIosDGdUwyYFlzndTiknWtDZprx0w0N9WUSduUOgiYowge5K1m7nfj7DzEev0FfnHHdqrtIoQwDxvSxpjnWy2jFu7Sm59dQnBG43Gs5f0)

------------


### Comentarios 
##### los comentarios son una forma de documentar a otros programadores o a tí mismo de lo que se esta programando y lo que hace cierto bloque de código. 
NO AFECTAN AL FUNCIONAMIENTO DE PROGRAMA . 

como se hacen en css :


` //esto es un comentario de una sola línea . `

```css
/*esto es un comentario 
multilínea , para explicaciones largas , etc...*/
```

### Modificar el ancho

```css
 Selector {
  width : 500 px;  // El elemento tendrá un ancho de 500 pixeles . 
 // width : auto ; El elemento tendrá un ancho según el contenido del elemento
 // width : 50% ;  El ancho del elemento será del 50% del ancho disponible  de la ventana . 
 }
```

### Modificar el alto
```css
 Selector {
 // height : cantidad (500) , unidades(px)
  height : 500 px;  // El elemento tendrá un alto de 500 pixeles . 
 }
```
-- Según el contenido --
**height : auto ;** El elemento tendrá un alto según el contenido del elemento
###### ------------------------ Hay más unidades a parte de pixeles ------------------------------
 -- PORCENTAJES --
 
**height : 50% ;** El alto del elemento será del 50% del ancho disponible  de la ventana .


> EL TEMA DE LAS UNIDADES SE EXLICARÁN APARTE 

------------


Al modificar el tamaño de la ventana, las dimensiones de un elemento establecido en porcentajes también cambia, con las siguientes propiedades obligamos al elemento a no superar cierto tamaño o a no reducirse más de lo establecido. 

- **max-width** : El ancho máximo del elemento será de cierto tamaño .
- **min-width** : El ancho mínimo del elemento será de cierto tamaño .
- **max-height** : El alto máximo del elemento será de cierto tamaño .
- **min-height** : El alto mínimo del elemento será de cierto tamaño .


------------


### Modificar el borde 
```css
 Selector {
 /* margin : grosor del borde , tipo de borde , color del borde; */
 // solid -> borde liso(____) , dashed -> borde punteado (.....)
	border : 2px solid blue ; 
	border : 2px dashed blue ;
 }
```
### Modificar el margen Interno 
```css
 Selector {
 /* margin : cantidad(2) unidades(pixeles) ; 
 
  -- Primer caso :
  el margen se aplicará hacia sentido del reloj , 5px arriba , 10px derecha , 5   abajo y 10 izquierda .
  
  -- Segundo caso : 5 px vertialmente y 10px horizontalmente. 
  
  -- Tercer caso : 5px hacia todos los sentidos (arriba , abajo , derecha e izquierda )
  
 */
	margin : 5px 10px 5px 10px ; /
	margin : 5px 10px;
	margin : 5px ;
 }
```
### Modificar el margen externo
