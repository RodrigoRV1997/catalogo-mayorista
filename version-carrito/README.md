# Version experimental con carrito

Esta carpeta es independiente del catalogo vigente ubicado en la raiz del
repositorio.

## Archivos

- `index.html`: catalogo para el cliente, carrito y generacion del QR.
- `caja.html`: lectura del pedido y validacion contra Google Sheets.
- `product-images.json`: listado de fotos existentes para evitar solicitudes
  fallidas y acelerar la carga.
- `vendor/qrcode.js`: generador QR local; no depende de servicios externos.

## Flujo

1. El cliente agrega envases al carrito.
2. El catalogo guarda el carrito en el navegador.
3. El cliente genera y muestra el QR.
4. Caja escanea el QR con un celular o lector QR.
5. `caja.html` contrasta precios y stock con la planilla vigente.

El pedido viaja dentro del fragmento `#pedido=` de la URL. Los fragmentos no se
envian al servidor de GitHub Pages.

## Fotos nuevas

Despues de agregar fotos en `imagenes/productos`, hay que regenerar
`product-images.json`. Desde PowerShell, en la raiz del repositorio:

```powershell
$files = Get-ChildItem -LiteralPath ".\imagenes\productos" -File |
  Sort-Object Name |
  Select-Object -ExpandProperty Name
$files | ConvertTo-Json |
  Set-Content -LiteralPath ".\version-carrito\product-images.json" -Encoding utf8
```

El QR admite hasta 60 productos distintos por pedido. Las cantidades pueden
ser de 1 a 99 envases por producto.
