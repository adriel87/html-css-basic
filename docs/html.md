# estructura

primero todo html tien estas 2 etiquetas

```html
<html>
    ....
</html>
```

Luego dentro de estas etiquetas nosotros debemos organizar nuestro docuemntos con diversas etiquetas

main, aside, aritcle... son solo alguna de las eitquetas que usamos para la confeccion de nuestro HTML

estas nos ayudan a dar un sentido semantico a nuestro pagina y que se indexe de forma correcta


## Headers

# h1
## h2
### h3
#### h4
##### h5
###### h6

las cabeceras o headers sirven para dar importancia al texto que escribamos en su interior
empezando por el 1 y terminando por el 6

# parrafos

cuando el texto que vayamos a escribir en nuestra pagina no tenga una importancia relevante podemos introducirlo dentro de un parrafo

### `<p></p>`

## estrucutar una pagina

normalmente para darle un sentido a la pagina se suelen agrupar los diferentes contenidos en diferentes etiquetas con diferente sentido semantico

- `<header>`
- `<footer>`
- `<nav>`
- `<main>`
- `<section>`
- `<article>`
- `<aside>`
- `<div>`

### estructura standar

```html
<header></header>
<nav></nav>
<main></main>
<section></section>
<aside></aside>
<footer></footer>
```

y cuando no puedas darle un sentido semantico a un una parte de tu documento utiliza un div

#### como y cuando estrucutura

como normal general lee el contenido o el sentido de lo que quieras mostrar en una pagina si el contenido que quieres mostrar esta relacionado o crees que tiene que estar a grupado, agrupalo empieza por `section` y luego sigue implementando el resto de etiquetas

## navegacion

para  crear menus de navegacion debemos usar la etiqueta nav y dentro usar la etiqueta a

```html
<nav>
    <a href="tuenlace.com">tuenlace.com</a>
</nav>
```

como vemos la etiqueta `a` tiene un atributo dentro de la etiqueta

## atributos de las etiquetas

los atributos cambian cierta funcionalidad de las etiquetas como vimos anteriormente en la etiqueta `a` usamos el atributo `href` para indicarle el punto a donde apunta el enlace

para ver mas informacion sobre los atributos podemos ver la sioguiente pagina 👀

# [💁](https://developer.mozilla.org/es/docs/Web/HTML/Attributes) ⬅️ pinchalo

## formularios

se susan para obtener un feedback del usuario

`fieldset` se utiliza para determinar un espacio de trabajo dentro de un formulario
`legend` con esto podemos Colocar informacion sobre el fieldset
`label` etiqueta para indicar el nombre de un campo
`input` espacio reservado para la respuesta del usuario

atributos de la etiqueta input

- text: introduce texto
- num: para numeros
- tel: numeros de telefono
- email: introduce el correo electronico





