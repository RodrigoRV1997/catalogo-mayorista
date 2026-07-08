# Catalogo Family Market

Esta carpeta contiene la version actual del catalogo conectado a Google Sheets.

## Archivos para subir a GitHub

- `index.html`
- `README.md`
- `imagenes/logo-family-market.png`
- `imagenes/sin-foto.svg`
- `imagenes/productos/`

La carpeta `imagenes/productos/` contiene las fotos disponibles. Cada foto usa el codigo interno del producto como nombre, por ejemplo:

```text
imagenes/productos/3706.jpg
```

El codigo no se muestra al cliente, solo se usa por dentro para encontrar la foto correcta.

## Datos del catalogo

Los precios se cargan desde la planilla publicada de Google Sheets configurada dentro de `index.html`.

Si un producto no tiene foto en `imagenes/productos/`, el catalogo muestra `imagenes/sin-foto.svg`.

## Importante

Para actualizar precios, basta con modificar la planilla de Google Sheets publicada. Para agregar fotos nuevas, sube un JPG a `imagenes/productos/` usando el codigo del producto como nombre.
