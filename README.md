# Cap i Cua Pet Store

Sitio web de Cap i Cua Pet Store, peluqueria canina y felina en Esplugues de Llobregat. El proyecto esta construido con Astro y Tailwind CSS, con una pagina principal orientada a presentar servicios, packs, contacto y reserva por WhatsApp.

## Stack

- Astro 6
- Tailwind CSS 4
- Vite 7
- TypeScript en modo estricto mediante `astro/tsconfigs/strict`
- npm como gestor de dependencias

## Requisitos

- Node.js instalado
- npm instalado

## Instalacion

```bash
npm install
```

## Ejecucion local

```bash
npm run dev
```

Astro mostrara la URL local en la terminal, normalmente `http://localhost:4321`.

Si el servidor ya esta arrancado en otra terminal, no es necesario volver a ejecutar este comando.

## Build de produccion

```bash
npm run build
```

El resultado se genera en `dist/`.

## Preview del build

```bash
npm run preview
```

Este comando sirve para revisar localmente el build generado. Ejecuta antes `npm run build`.

## Scripts disponibles

- `npm run dev`: arranca el servidor de desarrollo de Astro.
- `npm run build`: genera el build de produccion.
- `npm run preview`: sirve localmente el build generado.

## Estructura del proyecto

```text
public/
  favicon.svg
  images/
    capicuapetstore-logo.svg
    capicuapetstore-logo-footer.svg
    *.svg
src/
  components/
    Contact.astro
    ContactForm.astro
    Hero.astro
    Map.astro
    Services.astro
  layouts/
    Layout.astro
  pages/
    index.astro
  styles/
    globals.css
package.json
tsconfig.json
```

## Componentes principales

- `src/pages/index.astro`: pagina principal y navegacion superior/footer.
- `src/layouts/Layout.astro`: documento base, metadatos SEO, fuentes y favicon.
- `src/components/Hero.astro`: hero principal, CTA de WhatsApp y entrada visual de marca.
- `src/components/Services.astro`: listado de servicios y packs.
- `src/components/ContactForm.astro`: bloque de contacto, formulario mailto y mapa embebido.
- `src/components/Contact.astro`: alternativa de tarjetas de contacto.
- `src/components/Map.astro`: seccion independiente de ubicacion.
- `src/styles/globals.css`: tokens de color, fuentes, animaciones y utilidades globales.

## Contenido editable

Los datos de negocio aparecen principalmente en estos archivos:

- Telefono y WhatsApp: `Hero.astro`, `ContactForm.astro`, `Contact.astro`, `index.astro`.
- Instagram: `ContactForm.astro`, `Contact.astro`, `index.astro`.
- Email del formulario: `ContactForm.astro`.
- Direccion y horarios: `ContactForm.astro`, `Map.astro`.
- Servicios y packs: arrays `services` y `packs` en `Services.astro`.
- Titulos y descripcion SEO: `Layout.astro` e `index.astro`.

Antes de cambiar telefono, direccion, redes sociales, horarios o servicios, confirma que el dato nuevo es definitivo.

## Linea de diseno

La identidad visual esta documentada en `DESIGN.md`. Cualquier cambio de UI debe respetar ese documento y los tokens definidos en `src/styles/globals.css`.

## Convenciones

- Mantener componentes Astro simples y legibles.
- Priorizar cambios pequenos y coherentes con la estructura actual.
- Usar los tokens `brand-*` en vez de colores arbitrarios.
- Mantener la web responsive en movil y escritorio.
- Cuidar accesibilidad basica: textos alternativos utiles, foco visible, enlaces externos con `rel="noopener noreferrer"`.
- Mantener el idioma principal en espanol.
