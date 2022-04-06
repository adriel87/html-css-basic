# display

los display basicamente son las formas de en las que los elementos se organizan dentro de otros elementos

```html
<div class="display">
    <div>
        cositas
    </div>
    <div>
        cositas
    </div>
    <div>
        cositas
    </div>

</div>

```

```css
.display div{
    display:block
}
```

## block

los elementos se colocan unos encima de otros

ejemplo iconil

⚾
🏀
:crystal_ball:


## inline

los elementos se colocan seguidos uno de otros a la derecha

⚾🏀:crystal_ball:

por defecto los navegadores utilizan o `block` o `inline` 

## flexbox / flex

Con este tipo de display hacemos que los elementos por defecto cogan por defecto todo el espacio que tiene el contenedor.

sin embargo este display afecta a los hijos del padre donde se aplique

ejemplo

```html
 <nav class="navigation-principal container">
    <a href="#">Home</a>
    <a href="./nosotros.html">Sobre</a>
    <a href="#">tienda</a>
    <a href="#">contanct</a>
</nav>
```
```css
.navigation-principal{
    display: flex;
    justify-content: space-between;
}
```

como vemos en el nav el padre/madre 👨/👩 es el que organiza a los ninios 🧒

`justify-conten` ➡️ es lo que indica como ordenar, arriba space-between deja un espacio equivalente entre los diferentes hijos

### info
con flexbox solo podemos trabajar los elementos o en filas o columnas

```css
p{
    display:flex;
    flex: row-reverse /* empezamos por el ultimo elemento hasta el primero */
}
```

row y  row-reverse trabajan en fila

column y column-reverse trabajan en columnas



