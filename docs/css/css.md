# CSS

hojas de estilo en casacada

basicamente se encarga de dar formato y con sus ultimas versiones se le puede dar "vida" a la pagina.

- colores
- tamanios
- espacios
- margenes
- animaciones


***!important*** ten en cuenta que el nombre css no esta puesto al azar, los estilos se aplican igual en cascada, es decir de arriba a abajo. esto quiere  decir que si 2 reglas afectan al mismo selector,class, id. Los cambios reflejados seran los ultimos leidos

## anatomia

### selectores

los selectores apuntan a las etiquetas, clases o id

- etiqueta : html ➡️`<p></p>` css ➡️ *p*
- clase : html div `class=hola` css ➡️ *.hola*
- id : html div `id=hola` css ➡️ *#hola*

los selectores tienen atributos

por en el siguiente ejemplo de css veremos el atributo color

```css
p{
    color : red;
}
```

como vemos el atributo apunta a la propiedad color y la modifica


### como escribir en css

primero selecionamos la etiqueta

#### tamanios

- *px* aplica el valor en pixeles
- *em* aplica el tamanio dependiendo del tamanio que viene por su padre
   - si le aplicamos `1em` a cualquier elemento hijo tomara el mismo tamanio del padre, y el doble con `2em` y la mitad con `0.5em`
- *rem* rem es relativo al documento
- 

#### seleccionar elementos

ya vimos en los [selectores](#selectores) como podemos  seleccionar un solo elemento

sin embargo podemos ser mas especificos por ejemplo apuntar a una imagen con el atributo src y el nombre de su imagen

```css
img [src="img.jpg"]{
    /* aqui el css */
}
```

##### descendentes

- aqui determinamos los elementos que tiene que ser formateados por el orden de poner sus etiquetas por ejemplo

```css
h1 span:{
    /* tu codigo */
}
```
esto logra solo actuar sobre los span que esten detro de los h1, es decir afecta al ultimo hijo dentro de la secuencia

h1 span
`herencia->hijo`

div .tuclase span
`herencia->herencia->hijo`

- ahora imaginemos que queremos todos los parrafos dentro de un elemento article vamos a usar ***`>`***

```html
<article>
    <p>askdjlaskjd</p>
    <aside>
        <p>
            aksjdlkaj
        </p>
        <p>
            lkasjlka
        </p>
    </aside>
    <ul>
        <li>
            <p>alsjlasjdlaksj</p>
        </li>
    </ul>
</article>
```

para seleccionar todos esos parrafos solo los que estan dentro del article en css seria de la siguiente forma

```css
article > p{
    /* tu codigo aqui */
}
```
###### operadores

- and ➡️ `,` 

para agregar el mismo estilo a varios componentes utilizamos una coma separando los componentes que van a tener el mismo estilo


```css

p, h2, h3, section h1{
    color: blue;
}

```


##### especificidad

en resumen es como nosotros apuntamos exactamente al objeto que queremos modificar y su orden en el css


### tips

#### trabajando con rem

```css
html{
    /* tip para trabajar con rem */
    font-size: 62.5%;   
}

body{
    /* tip para trabajar con rem */
    font-size: 16px;
}
```


#### fuentas


para cambiar la fuente de nuestra pagina web podemos usar la propiedad de `font-family`

pero para poder usarla debemos 
1. importarla haciendo referencia a la nueva fuente desde nuestro head
```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- importar fuentes, en este caso googlefonts -->
     <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Overpass+Mono:wght@300;400;500;600;700&display=swap" rel="stylesheet"> 
    <!--  -->
    <link rel="preload" href="./styles/style.css" as="style">
    <link rel="stylesheet" href="./styles/style.css">
    <title>probando</title>
</head>
```

y luego tendremos que indicar en nuestro css que vamos a usarla

[google fonts](https://fonts.google.com/?query=mono)


#### normalizando nuestras webs

Es posible que nuestra webs se vean diferentes segun el navegador con el cual veamos la pagina, esto es por que los navegadores utilizan una serie de normas por defecto que las aniade a nuestro html

para evitar que esto pase y asegurarnos que nuestra pagina se vea igual en todos los navegadores, podemos ayudarnos del CSS. Para esto ya existen soluciones como [normalize](http://necolas.github.io/normalize.css/)

#### Agregando clases

Normalmente a la hora de estilar como uso comun le damos 1 o mas clases a nuestras etiquetas

para ello simplemente separa las clases con un espacio dentro del atributo `class`

ejemplo
```html
<p class="primario border25">laksjdlkasjdlkas</p>
```
como vemos tenemos 2 clases en el mismo parrafo

### estilos para escribir css

#### - BEM
primero definimos los estilos del padre y luego vamos profundizando

```css
.ejemplo{
    /* definimos primero */
}
.ejemplo__titulo{
    ...
}
.ejemplo__imagen{
    ...
}
.ejemplo__imagen--opacada{
    ...
}
```
#### - utility first
crearemos clases con una sola propiedad y luego en funcion de su necesidad la vamos usando

```css
.text-center{
    ....
}
.color-red-100{
    ...
}
```
```html

<div class="text-center color-red-100">
    ...
</div>

```

#### - modulos

con los modulos elegimos clase y luego vamos definiendo los estilos de las etiquetas o clase de su interior

```css
.home {}
.home h1{}
.home img{}
```

