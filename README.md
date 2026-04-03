# Plantilla base - Thank You Page Webinar

Esta plantilla está diseñada para reutilizarse con distintos clientes sin tocar la estructura visual.

## Objetivo
Mantener consistencia entre proyectos, evitar que un LLM cambie animaciones, orden visual, bloques o jerarquía HTML.

## Regla de uso
**Solo se edita el bloque `CONFIG`.**

No se debe modificar:
- estructura HTML
- clases Tailwind
- animaciones CSS
- orden de secciones
- nombres de IDs

## Variables editables
Dentro de `CONFIG` puedes cambiar:
- `metaPixelId`
- `page.title`
- `brand.clientName`
- `brand.hostName`
- `brand.hostPhotoUrl`
- `brand.copyrightText`
- `event.name`
- `event.dateText`
- `event.motivationalQuote`
- `event.supportEmailNotice`
- `links.zoomUrl`
- `links.whatsappGroupUrl`
- `webinarMode.isLive`
- textos del modo live o pre-live
- textos del bloque de WhatsApp

## Convención recomendada para futuros LLMs
Usa este prompt interno cuando quieras adaptar la plantilla:

> Edita únicamente el bloque CONFIG del archivo HTML. No modifiques estructura HTML, clases, estilos, animaciones, orden visual, iconos, IDs ni scripts fuera de CONFIG. Solo reemplaza los valores del cliente: nombre del evento, nombre del host, fecha del evento, enlace de Zoom, enlace de grupo de WhatsApp, foto del host y Meta Pixel ID.

## Casos de uso
### 1. Webinar aún no empieza
```js
webinarMode: {
  isLive: false
}
```
Mostrará CTA de reserva o guardado del enlace de Zoom.

### 2. Webinar ya está en vivo
```js
webinarMode: {
  isLive: true
}
```
Mostrará CTA urgente para entrar al Zoom.

## Checklist antes de publicar
- Meta Pixel ID correcto
- Fecha del evento correcta
- Zoom URL correcta
- Grupo de WhatsApp correcto
- Foto del host cargando bien
- Copyright actualizado
- `isLive` en el estado correcto
