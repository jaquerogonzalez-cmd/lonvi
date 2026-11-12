# Lonvi — sitio web

## Qué hay en esta carpeta

- `index.html` — el diseño de la tienda. Casi nunca se toca.
- `data/productos.json` — prendas, precios, stock, textos, páginas y ajustes. Lo edita el admin.
- `data/geo.json` — modelos 3D del colgador de Novedades.
- `img/` — fotos de las prendas.
- `admin/` — el panel para editar la tienda.

## Publicar en GitHub Pages

1. Sube **todo el contenido** de esta carpeta a la raíz de tu repositorio (incluido `.nojekyll`).
   El archivo antiguo `lonvi-ficha-producto.html` ya no se usa; puedes borrarlo.
2. En GitHub: **Settings → Pages → Build and deployment**, elige *Deploy from a branch*, rama `main`, carpeta `/ (root)`.
3. La tienda queda en `https://TU-USUARIO.github.io/TU-REPOSITORIO/` y el admin en `.../admin/`.

> Abrir `index.html` con doble clic en tu computador no funciona: la tienda necesita estar servida desde una web (GitHub Pages o Cloudflare).

## Usar el admin

1. Entra a `.../admin/`.
2. La primera vez, crea un token en GitHub:
   - **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
   - *Repository access*: **Only select repositories** → tu repositorio de Lonvi.
   - *Repository permissions* → **Contents: Read and write**.
   - Ponle fecha de vencimiento y créalo.
3. En el admin escribe tu usuario, el nombre del repositorio, la rama (`main`) y pega el token.
4. Edita lo que quieras. **Vista previa** abre la tienda con tus cambios sin publicarlos.
5. **Publicar** sube los cambios a GitHub en un solo paso. La tienda se actualiza en uno o dos minutos.

Si cierras el navegador sin publicar, los cambios quedan guardados y el admin te ofrece recuperarlos.

## Cuidados

- El token es como una llave de tu repositorio: no lo compartas ni lo pegues en otro lado. Si crees que alguien lo vio, bórralo en GitHub y crea otro.
- El stock se actualiza a mano desde el admin. Cuando conectemos el pago, se descontará solo.
- Las prendas nuevas aparecen en el colgador 3D como foto plana hasta que se genere su modelo 3D.
- Las fotos que reemplazas quedan en `img/` (no se borran solas).

## Pasar a Cloudflare

En Cloudflare Pages, conecta este mismo repositorio. Cada vez que publiques desde el admin, Cloudflare publicará la versión nueva sola. El admin sigue funcionando igual.
