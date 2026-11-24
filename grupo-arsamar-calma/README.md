# Grupo Arsamar — Web corporativa B2B con área Arsamar Member (versión calma)

## Qué cambia en la versión calma

La web actual de Arsamar satura: entras y no sabes ni qué venden. Esta versión se inspira en la calma de Lululemon:

- **Una idea por pantalla.** La portada tiene 7 bloques cortos: frase principal, qué hacemos, qué vendemos (3 familias), marcas, cómo trabajamos, Member y contacto.
- **Se entiende en 2 segundos qué vende:** «Equipaje que viaja tranquilo» y tres fotos grandes (maletas rígidas, juegos y semirrígidas, bolsas y mochilas).
- **Colores cálidos y suaves:** hueso, piedra y carbón cálido. Member, en carbón y arena dorada.
- **Tipografía ligera** (Inter 300), mucho espacio en blanco, sin bordes ni cajas innecesarias.
- **Movimiento lento:** las maletas de la portada flotan y su sombra «respira», y las secciones aparecen suavemente al bajar (sin JavaScript, con `animation-timeline: view()`). Si alguien tiene activada la opción «reducir movimiento», todo queda quieto.
- **Ilustraciones en perspectiva 3/4** con luz de estudio, sombras suaves y textura. Aun así, las **fotos reales** serán lo que la haga definitiva (ver `FOTOS.md`).


Web de muestra del **Grupo Arsamar** (Atzeneta d'Albaida): maletas, bolsas de viaje y mochilas de las marcas **Jaslen, Itaca y Skpat**.
Está pensada para tiendas, distribuidores y agentes comerciales, e incluye el programa privado **Arsamar Member · Colaboradores VIP** para las mejores tiendas físicas.

Está hecha sobre la base técnica del proyecto Rocalm v10: HTML5 semántico y CSS3, *mobile first*, sin JavaScript, con fuentes locales y lista para GitHub Pages.

## Cómo abrirla

1. Descomprime el zip (no la abras desde dentro del zip).
2. Abre `index.html` con el navegador. No hace falta servidor ni conexión a internet.

## Cómo publicarla en GitHub Pages (igual que Rocalm)

1. Crea un repositorio nuevo, por ejemplo `Arsamar`.
2. Sube **el contenido** de esta carpeta (que `index.html` quede en la raíz).
3. Ve a *Settings → Pages → Branch: main / root* y guarda.
4. En un par de minutos estará en `https://josepvidal1.github.io/Arsamar/`. Ese enlace es el que puedes enviar al cliente.

## Páginas

| Página | Contenido |
|---|---|
| `index.html` | Portada a pantalla completa, datos de confianza, el grupo, marcas, bloque Arsamar Member, ventajas, destacados, cómo empezar |
| `grupo.html` | Historia, estructura del grupo (Arsamar Enterprise, marcas, Jaslen Shops), valores y dónde estamos |
| `catalogo.html` | Catálogo por marca con **filtro sin JavaScript** (incluye «Exclusivos Member» bloqueados) |
| `producto.html` | Ficha técnica B2B con **galería de 4 vistas**, selector de color, tabla y precio profesional bajo solicitud |
| `distribuidores.html` | Qué ofrecemos, con quién trabajamos, paso a Member, preguntas frecuentes y formulario de alta |
| `member.html` | **Arsamar Member**: 6 privilegios, avance de exclusivos, niveles Member y Member Signature, cómo se accede, preguntas frecuentes |
| `member-acceso.html` | Inicio de sesión Member y solicitud de invitación |
| `member-area.html` | **Área privada de demostración**: avances con reserva, ediciones exclusivas, pedido de merchandising, documentos y gestor personal |
| `contacto.html` | Datos de contacto y formulario |
| `legal.html` | Aviso legal, privacidad y cookies (plantilla) |

## La idea de marca (para explicársela al cliente)

- **Grupo, no tienda:** se presenta como un grupo familiar con estructura (diseño, almacén, marcas y venta al público). Eso transmite solidez.
- **Hechos, no adjetivos:** 3 marcas propias, almacén propio, vendedor oficial en Decathlon y empresa familiar.
- **Sin precios públicos:** el precio profesional se pide. Así funcionan las marcas serias del sector.
- **Arsamar Member es lo que lo diferencia de la competencia.** Las marcas del sector suelen ofrecer a las tiendas un catálogo y una tarifa. Arsamar les ofrece pertenecer a un círculo: ven antes la colección, venden ediciones que nadie más tiene y llevan la firma Arsamar a su escaparate. «No se compra. Se gana.»
- **Dos ambientes visuales:** azul marino, crema y cuero para la parte corporativa (confianza y oficio), y negro y oro para Member (exclusividad).
- **Lujo cercano, no inalcanzable:** el discurso habla de trabajo bien hecho y precio justo, no de ostentación.

## Interactividad sin JavaScript

- **Filtro del catálogo:** radios ocultos y selector `:has()` (sección 23h del CSS).
- **Galería de la ficha:** cada miniatura es un `label` que marca un radio (sección 23i).
- **Selector de color:** radios con estilo de muestra.
- **Acceso Member de demostración:** el formulario lleva a `member-area.html`. La contraseña no tiene atributo `name`, así que no se envía.
- **Desplegables:** `details` y `summary`.

## ⚠️ Pendiente de confirmar con el cliente antes de publicar

Busca `CONFIRMAR` en los ficheros HTML.

1. **Fotos reales** (ver `FOTOS.md`). Las imágenes de `img/` son ilustraciones provisionales.
2. **Logotipos** del grupo y de las tres marcas (ahora son texto y un monograma provisional).
3. **Contacto:** el teléfono `+34 960 00 00 00` es inventado. Hay que confirmar también los correos, la dirección y el horario.
4. **Estructura del grupo:** qué hace exactamente Jaslen Shops y cómo se relaciona con Arsamar Enterprise.
5. **Productos:** nombres, medidas y capacidades sacados de las fichas de Arsamar en decathlon.es. En la Venecia, la referencia, las ruedas, el cierre y los colores son de ejemplo.
6. **Programa Member:** los nombres de las ediciones (Venecia Cuero, Turín Noir), los avances (Oslo, Tajo, Tokio), los niveles, los requisitos y el merchandising son una **propuesta** que hay que decidir con la dirección.
7. **Condiciones comerciales:** pedido mínimo, plazos, exclusividad y defectos.
8. **Textos legales:** completar CIF, domicilio y datos registrales, y revisarlos con su gestoría.
9. **Formularios y acceso Member:** ahora son de demostración. Para que funcionen de verdad hace falta un sistema de usuarios y formularios. Por ejemplo, WordPress con un plugin B2B o Shopify B2B. Eso es una **fase 2 con presupuesto aparte**.

## Estructura de carpetas

```
grupo-arsamar/
├── *.html               10 páginas
├── css/estilos.css      Hoja única, comentada y numerada por secciones
├── fonts/               Inter en .woff2 (licencia SIL OFL)
├── img/                 Ilustraciones SVG provisionales y monograma
├── datos/catalogo.xml   Catálogo en XML bien formado (incluye exclusivos y avances Member)
├── capturas/            Capturas en escritorio, tableta y móvil
├── backlog.md           Product Backlog
└── FOTOS.md             Lista de fotos reales que hay que pedir al cliente
```
