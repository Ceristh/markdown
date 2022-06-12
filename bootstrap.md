# Bootstrap

**Terminal**  
[My_Github](https://github.com/Ceristh/markdown)
\*repositorio en github

## Buttons

```
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
```

## Popovers

- Los popovers se basan en la biblioteca de terceros Popper para el posicionamiento. Debe incluir popper.min.js antes bootstrap.js o usar uno bootstrap.bundle.min.js que contenga Popper.

:::HTML

```
<button type="button" class="btn btn-lg btn-danger" data-bs-toggle="popover" title="Popover title" data-bs-content="And here's some amazing content. It's very engaging. Right?">Click to toggle popover</button>
```

:::js

```
var popoverTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="popover"]'));
var popoverList = popoverTriggerList.map(function (popoverTriggerEl) {
    return new bootstrap.Popover(popoverTriggerEl)
});
```

## Modal

- Los modales se construyen con HTML, CSS y JavaScript. Se colocan sobre todo lo demás en el documento y eliminan el desplazamiento `<body>` para que el contenido modal se desplace en su lugar.

:::HTML

```
<section class="container" id="modal">
    <h2>Modal</h2>
    <!-- Button trigger modal -->
    <button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#modaldia3">Abrir Modal</button>

    <!-- Modal -->
    <div class="modal fade" id="modaldia3" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="exampleModalLabel">Javascript Día 3</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    Clase de Jquery
                </div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Cerrar</button>
                    <button type="button" class="btn btn-primary">Salvar</button>
                </div>
            </div>
        </div>
    </div>
</section>
```

:::js

```
var myModalEl = document.getElementById('modaldia3')
myModalEl.addEventListener('hidden.bs.modal', function (event) {
    alert("Ha cerrado el modaldia3")
});
```

## Tooltips

- Documentación y ejemplos para agregar información sobre herramientas de Bootstrap personalizada con CSS y JavaScript usando CSS3 para animaciones y data-bs-attributes para el almacenamiento local de títulos.

:::HTML

```
<section class="container" id="tooltip">
    <h2>Tooltip</h2>

    <button type="button" class="btn btn-secondary" data-bs-toggle="tooltip" data-bs-placement="left" title="Tooltip on left">Tooltip on left</button>
    <button type="button" class="btn btn-secondary" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Tooltip on bottom">Tooltip on bottom</button>
    <button type="button" class="btn btn-secondary" data-bs-toggle="tooltip" data-bs-placement="top" title="Tooltip on top">Tooltip on top</button>
    <button type="button" class="btn btn-secondary" data-bs-toggle="tooltip" data-bs-placement="right" title="Tooltip on right">Tooltip on right</button>
</section>
```

:::js

```
var tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'))
var tooltipList = tooltipTriggerList.map(function (tooltipTriggerEl) {
    return new bootstrap.Tooltip(tooltipTriggerEl)
});
```
