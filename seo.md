# Auditoría SEO · Cap i Cua Pet Store

Auditoría realizada sobre la rama `SEO`.

## Prioridad Alta

### 1. Falta SEO técnico base en `Layout.astro`

Referencia: `src/layouts/Layout.astro`

La web ya tiene `title`, `description`, `og:title` y `og:description`, pero faltan metadatos importantes:

- `canonical`
- `og:url`
- `og:image`
- `twitter:card`
- `twitter:title`
- `twitter:description`
- `twitter:image`

Impacto: Google puede indexar la página, pero la URL canónica no queda declarada y la vista previa al compartir en redes puede ser pobre o inconsistente.

### 2. Falta schema de negocio local

No hay datos estructurados `application/ld+json`.

Para este negocio conviene añadir schema de tipo `LocalBusiness`, idealmente con información de tienda de mascotas y peluquería para mascotas.

Datos recomendados:

- Nombre del negocio
- Teléfono
- Email
- Dirección
- Horarios
- URL
- Redes sociales
- Logo o imagen
- Enlace a Google Maps

Impacto: ayuda a Google a entender mejor el negocio, su ubicación y sus datos principales. Es especialmente útil para SEO local.

### 3. El H1 es poco descriptivo para SEO local

Referencia: `src/components/Hero.astro`

H1 actual:

```text
El cuidado de tu mascota empieza aquí
```

Funciona bien como claim de marca, pero no contiene la intención principal de búsqueda: peluquería canina/felina en Esplugues.

Opciones más SEO friendly:

```text
Peluquería canina y felina en Esplugues
```

```text
Peluquería canina y felina en Esplugues para mimar a tu mascota
```

Recomendación: mantener el tono cercano y visual, pero incluir la keyword local principal en el H1 o muy cerca del H1.

### 4. Falta `robots.txt` y sitemap

No existe:

- `public/robots.txt`
- sitemap generado o estático

Además, `astro.config.mjs` no define `site`.

Impacto: no es crítico para una landing pequeña, pero es básico para producción.

Se puede preparar en local, pero para producción hay que usar la URL real definitiva, por ejemplo:

```js
site: 'https://capicuapetstore.com'
```

## Prioridad Media

### 5. Metadescripción mejorable

Referencia: `src/pages/index.astro`

Actual:

```text
Peluquería canina y felina en Esplugues de Llobregat. Baño, corte profesional, uñas y tratamientos para tu mascota. ¡Reserva tu cita por WhatsApp!
```

Propuesta:

```text
Peluquería canina y felina en Esplugues de Llobregat. Baño, corte, cepillado, uñas, higiene y tienda de mascotas. Reserva tu cita por WhatsApp.
```

### 6. Contenido SEO local mejorable

Referencias:

- `src/components/Hero.astro`
- `src/components/Services.astro`
- `src/components/Store.astro`

La web menciona Esplugues y servicios, pero puede reforzar de forma natural:

- `peluquería canina en Esplugues`
- `peluquería felina en Esplugues`
- `tienda de mascotas en Esplugues`
- `baño y corte para perros y gatos`
- `grooming para perros y gatos`

Recomendación: introducir estas frases sin forzar el texto ni perder el tono cercano.

### 7. Falta una sección breve de confianza/localidad

Podría añadirse una sección corta o bloque dentro de la landing con mensajes como:

- `Tu peluquería de mascotas en Esplugues`
- `Atención personalizada para perros y gatos`
- `En Mestre Joan Corrales, 33`

Impacto: mejora relevancia local y conversión.

### 8. Imágenes de servicios en PNG

Referencia: `src/components/Services.astro`

Varios servicios usan imágenes `.png`.

Recomendación: convertirlas a `.webp` u optimizarlas si se quiere mejorar rendimiento mobile y Lighthouse/Core Web Vitals.

### 9. Imagen principal decorativa

Referencia: `src/components/Hero.astro`

La imagen principal usa `alt=""`, lo cual es correcto si es decorativa.

Si la imagen representa contenido relevante para el negocio, se podría usar un texto alternativo descriptivo. Si es solo decorativa, conviene dejarla como está.

### 10. Google Maps iframe

Referencia: `src/components/ContactForm.astro`

El iframe está correctamente configurado con:

- `title`
- `loading="lazy"`
- `referrerpolicy`

Puede afectar rendimiento en auditorías Lighthouse, pero es aceptable para una página de negocio local.

## Prioridad Baja

### 11. `meta keywords` no aporta valor SEO moderno

Referencia: `src/layouts/Layout.astro`

Google ya no usa `meta keywords` como señal de ranking.

No causa un problema grave, pero tampoco ayuda. Se puede dejar o eliminar.

### 12. Inconsistencia de email en páginas legales

Referencias:

- `src/pages/aviso-legal.astro`
- `src/pages/politica-privacidad.astro`

Email legal actual:

```text
hola@capicuapestore.com
```

Email usado en footer/contacto:

```text
hola@capicuapetstore.com
```

Recomendación: confirmar cuál es el correcto antes de cambiarlo, porque es un dato de negocio.

### 13. Formato de teléfono inconsistente

Footer:

```text
+34 688 95 65 40
```

Contacto:

```text
+34 688 956 540
```

No es grave, pero conviene unificar el formato visual.

## Plan Recomendado

1. Añadir `site` en `astro.config.mjs`, canonical, OG/Twitter tags y `og:image`.
2. Crear `robots.txt` y sitemap.
3. Añadir schema `LocalBusiness`/`PetStore`.
4. Ajustar H1, meta description y algunos textos para SEO local sin perder tono de marca.
5. Confirmar email/teléfono antes de corregir inconsistencias.
6. Optimizar imágenes PNG de servicios si se quiere mejorar rendimiento mobile.
