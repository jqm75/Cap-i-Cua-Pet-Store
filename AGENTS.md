# AGENTS.md

Instrucciones para agentes de IA y colaboradores automatizados que trabajen en este repositorio.

## Contexto del proyecto

Este repositorio contiene el sitio web de Cap i Cua Pet Store, una peluqueria canina y felina en Esplugues de Llobregat. Es una web de una sola pagina construida con Astro y Tailwind CSS.

El objetivo principal de la web es transmitir cercania, profesionalidad y energia de tienda de barrio, y facilitar la reserva/contacto por WhatsApp.

## Reglas operativas

- No ejecutes `npm run dev` salvo que el usuario lo pida explicitamente. El servidor puede estar ya arrancado en otra terminal.
- Si necesitas verificar compilacion, usa `npm run build`.
- No cambies datos de negocio como telefono, direccion, email, Instagram, horarios o servicios sin confirmacion del usuario.
- No introduzcas dependencias nuevas si el cambio puede resolverse con Astro, Tailwind y CSS existente.
- No reestructures el proyecto de forma amplia si el objetivo se puede resolver con un cambio localizado.
- No elimines componentes no usados sin preguntar; algunos pueden servir como alternativas o trabajo en curso.

## Comandos utiles

```bash
npm install
npm run build
npm run preview
```

`npm run dev` existe, pero solo debe ejecutarse con permiso explicito.

## Criterios de implementacion

- Prefiere cambios pequenos, directos y faciles de revisar.
- Mantener componentes en `.astro` salvo que haya una necesidad clara de interactividad avanzada.
- Mantener la configuracion TypeScript estricta.
- Usar Tailwind CSS siguiendo los patrones actuales del proyecto.
- Reutilizar tokens de `src/styles/globals.css`.
- Mantener textos en espanol y con tono cercano.
- Evitar soluciones genericas o visualmente neutras que rompan la identidad existente.

## UI y diseno

Antes de modificar interfaz, lee `DESIGN.md`.

La direccion visual actual se basa en:

- Amarillo de marca como fondo dominante.
- Teal como color de accion y acento.
- Marron como bloque de contraste calido.
- Tipografia display contundente con `Alfa Slab One`.
- Texto con `Noto Sans` en pesos altos.
- Tarjetas tipo ticket mediante `.ticket-cut`.
- Sombras desplazadas, hover antigravity y animaciones suaves.

No sustituyas esta direccion por una estetica corporativa gris/blanca, minimalista generica o excesivamente clinica.

## Accesibilidad y calidad

- Mantener foco visible y navegacion por teclado razonable.
- Los enlaces externos deben usar `target="_blank"` con `rel="noopener noreferrer"`.
- Los iconos decorativos deben tener `alt=""` o `aria-hidden="true"` cuando corresponda.
- Los iframes deben incluir `title`.
- Comprobar responsive al tocar layouts principales.
- Mantener metadatos SEO relevantes en `Layout.astro` y `index.astro`.

## Archivos relevantes

- `src/styles/globals.css`: tokens, fuentes, animaciones y utilidades.
- `src/layouts/Layout.astro`: HTML base, SEO, fuentes y favicon.
- `src/pages/index.astro`: composicion de pagina, nav y footer.
- `src/components/Hero.astro`: primer impacto visual y CTA principal.
- `src/components/Services.astro`: servicios y packs.
- `src/components/ContactForm.astro`: contacto, formulario y mapa.
- `DESIGN.md`: linea de diseno obligatoria.
