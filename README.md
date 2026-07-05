# Cap i Cua Pet Store

Sitio web de Cap i Cua Pet Store, peluqueria canina y felina en Esplugues de Llobregat. La web presenta servicios de grooming, bonos mensuales, tienda de alimentacion y accesorios, canales sociales y contacto por WhatsApp.

## Stack

- Astro 6
- Tailwind CSS 4
- Vite 7
- TypeScript estricto
- npm

## Requisitos

- Node.js
- npm

## Instalacion

```bash
npm install
```

## Desarrollo

```bash
npm run dev
```

Astro mostrara la URL local en la terminal, normalmente `http://localhost:4321`.

## Build

```bash
npm run build
```

El resultado se genera en `dist/`.

## Preview

```bash
npm run preview
```

Ejecuta antes `npm run build` para revisar el build generado.

## Scripts

- `npm run dev`: arranca el servidor de desarrollo.
- `npm run build`: genera el build de produccion.
- `npm run preview`: sirve localmente el build generado.

## Estructura

```text
public/
  images/
    tienda.webp
    cap_i_cua-h-logo.svg
    capicuapetstore-logo.svg
    servicios/
src/
  components/
    Hero.astro
    Services.astro
    Store.astro
    Follow.astro
    ContactForm.astro
    Map.astro
  layouts/
    Layout.astro
  pages/
    index.astro
    aviso-legal.astro
    politica-privacidad.astro
  styles/
    globals.css
```

## Secciones

- `Hero.astro`: primer impacto visual y CTA principal de WhatsApp.
- `Services.astro`: servicios de peluqueria y bonos mensuales.
- `Store.astro`: tienda de alimentacion, snacks, accesorios y productos para perros, gatos, conejos y aves.
- `Follow.astro`: enlaces a WhatsApp, Instagram, TikTok y resenas de Google.
- `ContactForm.astro`: formulario, datos de contacto, horarios y mapa embebido.

## Contenido Editable

- Telefono y WhatsApp: `Hero.astro`, `Follow.astro`, `ContactForm.astro`, `index.astro`.
- Redes sociales: `Follow.astro`, footer en `index.astro`.
- Email del formulario: `ContactForm.astro`.
- Direccion y horarios: `ContactForm.astro`, `Map.astro`.
- Servicios y bonos: arrays `services` y `packs` en `Services.astro`.
- Contenido de tienda: `Store.astro`.
- Metadatos SEO: `Layout.astro` e `index.astro`.

Antes de cambiar telefono, direccion, email, redes sociales, horarios o servicios, confirma que el dato nuevo es definitivo.

## Diseno

La linea visual esta documentada en `DESIGN.md`. Los cambios de UI deben respetar los tokens de `src/styles/globals.css` y la identidad actual:

- Amarillo de marca como base.
- Teal como accion y acento.
- Marron como contraste calido.
- Fondos paper para descanso visual.
- Tipografia display contundente.
- Cards tipo ticket, sombras desplazadas y microinteracciones suaves.

## Calidad

- Mantener componentes en Astro salvo necesidad clara de interactividad avanzada.
- Usar Tailwind y CSS existente antes de introducir dependencias.
- Mantener responsive en movil y escritorio.
- Cuidar accesibilidad: foco visible, `alt` utiles, enlaces externos con `rel="noopener noreferrer"`.
- Verificar cambios importantes con `npm run build`.
