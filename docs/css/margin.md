# margin

como aplicar el margen


el margen se puede establecer de forma individual
```css
p{
    margin-top: 2px;
    margin-bottom: 2px;
    margin-rigth: 2px;
    margin-left: 2px
}

/* o bien podemos agregar todo a la vez */

p{
    margin:2px  /* esto afecta a todo los lados por igual*/

}

/* tambien podemos acortar la primera vesion de la siguiente manera
   de izquierda a derecha seria
   1 arriba
   2 derecha
   3 abajo
   4 izquierda
 */

 p{
     margin: 2px 2px 2px 2px
 }

```

para centrar un elemento con respecto a su contenedor podemos hacer lo siguiente

```css

p{
    margin: 0 auto;
}


```