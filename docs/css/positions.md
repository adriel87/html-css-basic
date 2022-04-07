# absolute

cuando queremos colocar algun elemento en una posicion concreta, lo que buscamos usar `absolute`

hay que tener un especial cuidado para utilizar este tipo de posicionador

lo mejor seria que el padre del elemento tenga una posicion relativa, normalmente al documento. Y el hijo tenga una posicion absoluta

## ⬇️⬇️⬇️⬇️⬇️

```html
<div class="padre">
    <div class="hijo">
        some things
    </div>
</div>
```

```css

.padre{
    position:relative;
}

.hijo {
    position:absolute;
}

```

esto colocara al hijo en la partes superior izquierda del contenido del padre

ahora bien vamos a definir donde queremos colocarlo

por ejemplo abajo a la derecha

```css
.hijo {
    position:absolute;
    bottom:0;
    rigth:0;
}
```

podemos hacer que el hijo tome todo el espacio que ocupa el padre de forma absoluta de asi

⬇️⬇️⬇️⬇️⬇️

```css
.hijo {
    position:absolute;
    top:0;
    bottom:0;
    rigth:0;
    left:0
}

/* o bien */

.hijo {
    position:absolute;
    width:100%;
    heigth:100%:    
}
```
