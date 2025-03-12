# Variables en CSS

Se pueden crear variables de CSS para reutilizar valores en diferentes partes del codigo

- Mejora la legibilidad del codigo
- Facilita la actualizacion de valores

Se suelen crear de manera global en la raiz del documento, en web el root es la etiqueta <html>, en svg es la etiqueta <svg>, ademas tiene mayor especificidad ":root" que "html".

```css
:root{
    --blue: #1e90ff;
    --indigo: #6610f2;
    --mi-color-principal: #fff;
    --mi-bg-principal: #000;
}

.contanier{
    background-color: var(--mi-bg-principal);
    color: var(--mi-color-principal);
}