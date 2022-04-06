# tips para estilar navs

intenta usar un display flex en el padre junto con justify content

```html
<nav class="navigation">
    <a href="#">enlace</a>
    <a href="#">enlace</a>
    <a href="#">enlace</a>
    <a href="#">enlace</a>
    <a href="#">enlace</a>

</nav>
```

```css
.navigation{
    display: flex;
    jsutify-content: space-between
}
```

esto colocara los enlaces en linea y con una separacion uniforme entre ellos