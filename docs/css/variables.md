# Variables en CSS

como usar variables en css

para esto podemos definir al principio de nuestra hoja de estilos una etiqueta precedida de `:` y luego indicar los nombres de la variables y asignarles un valor 

por ejemplo:

```css
:root{
    --backgroud:#004643;
    --headline:#fffffe;
    --paragraph:#abd1c6;
    --button:#f9bc60;
    --button-text:#001e1d;

    --stroke:#001e1d;
    --main:#e8e4e6;
    --higlight:#f9bc60;
    --secondary:#abd1c6;
    --tertiary:#e16162;
}
```

ahora para poder usar esta variables necesitamos indicarle CSS que vamos a usarlo

```css
p{
    color: var(--main)
}
```