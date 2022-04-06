# Performance

como mejorar la velocidad de nuestras paginas web

## dentro de head

precargando nuestros estilos css de la siguiente forma

```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- como vemos link con preload preacarga el css de nuestra pagina web lo mas rapido posible -->
    <link rel="preload" href="./styles/style.css" as="style">
    <link rel="stylesheet" href="./styles/style.css">
    <title>probando</title>
</head>
```