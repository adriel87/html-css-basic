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

para 

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