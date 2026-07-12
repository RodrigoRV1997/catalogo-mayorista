# Catalogo Family Market

Esta carpeta contiene la version actual del catalogo conectado a Google Sheets.

## Archivos para subir a GitHub

- `index.html`
- `README.md`
- `imagenes/logo-family-market.png`
- `imagenes/sin-foto.svg`
- `imagenes/productos/`

La carpeta `imagenes/productos/` contiene las fotos disponibles. La forma mas simple es usar el codigo interno del producto como nombre:

```text
imagenes/productos/3706.jpg
```

El catalogo tambien puede buscar fotos por el nombre del producto. Para eso conviene usar el nombre normalizado en minusculas, sin tildes y con guiones:

```text
imagenes/productos/azucar-iansa-20-x-1-kg.jpg
imagenes/productos/102-azucar-iansa-20-x-1-kg.jpg
```

Si un codigo se repite en productos distintos, usa mejor el nombre o `codigo-nombre` para evitar que ambos tomen la misma foto.

## Datos del catalogo

Los precios se cargan desde la planilla publicada de Google Sheets configurada dentro de `index.html`.

Si un producto no tiene foto en `imagenes/productos/`, el catalogo muestra `imagenes/sin-foto.svg`.

## Importante

Para actualizar precios y stock, basta con modificar la planilla de Google Sheets publicada. Los productos con stock 0 o precio 0 no se muestran. Para agregar fotos nuevas, sube un JPG a `imagenes/productos/` usando el codigo, el nombre normalizado o `codigo-nombre`.
