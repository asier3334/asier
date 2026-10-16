# Mala Cara · Página de venta (tema Horizon)

## Qué hay en este repositorio

| Archivo | Para qué sirve |
|---|---|
| `sections/mala-cara-venta.liquid` | La página de venta completa, editable desde el personalizador. |
| `snippets/mc-icon.liquid` | Iconos (envío, devolución, candado, talla). |
| `assets/mc-bagel-fat-one.woff2`, `assets/mc-archivo.woff2` | Tipografías alojadas en tu tienda. Sin Google Fonts: carga más rápida y sin enviar la IP de tus clientes a Google (RGPD). |

Es una sección nueva. No sustituye a `mala-cara-producto.liquid`, porque si reescribiera ese archivo, Shopify podría rechazar el guardado: tus plantillas guardan bloques del diseño anterior. Cuando compruebes que la nueva te convence, ocultas la antigua y la borras.

---

## 1. Diagnóstico (ordenado por impacto en ventas)

> No he podido abrir la tienda: la red de mi entorno bloquea `g7agat-ft.myshopify.com`. El diagnóstico se basa en el resumen del proyecto. Cuando el dominio esté permitido, lo reviso en vivo.

1. **La tienda no puede cobrar.** Los pagos y el plan siguen sin activar. Mientras sea así, cada clic de anuncio se pierde. Es lo primero, antes de gastar 1 € en Meta o TikTok.
2. **Las fotos son capturas de baja calidad.** En un producto que se compra por impulso, la foto es el argumento. Con capturas, la marca parece dropshipping barato y el CTR del anuncio no se convierte en compra.
3. **No hay prueba real.** Faltan vídeo, UGC y fotos de detalle. «Tejido, no impreso» solo se cree si se ve de cerca.
4. **La primera pantalla en móvil probablemente no lo dice todo.** Con barra en movimiento, foto flotante y sello, lo normal es que el botón y el precio queden por debajo del pliegue.
5. **No hay botón fijo en móvil.** Al bajar a leer, el comprador pierde el botón.
6. **No hay aviso legal ni dominio propio.** Faltan nombre, NIF y dirección (obligatorio en la LSSI) y la tienda sigue en `myshopify.com`. Todo esto resta confianza y además es un requisito legal.
7. **El checkout usa colores y logo por defecto.** Ese salto visual en el último paso hace dudar.
8. **Quedan textos del tema en inglés o de ejemplo.** En el carrito, el pie y las páginas sin tocar.

## 2. Estructura de la página (gancho → producto → prueba → oferta → dudas → compra)

| # | Sección | Por qué |
|---|---|---|
| 1 | **Barra superior** con envío, 14 días y pago seguro | Quita las 3 dudas básicas antes de leer nada. Solo datos reales. |
| 2 | **Primera pantalla**: foto, nombre, gancho, los 2 packs con precio, ahorro real y botón con precio | Quien viene de un anuncio decide en 3 segundos. Todo cabe en la pantalla de un iPhone sin hacer scroll (comprobado a 390×664 con cabecera). |
| 3 | **Franja de garantías** (envío, devolución, pago, talla) | Refuerza justo debajo del botón, para el que duda. |
| 4 | **«Tejido, no impreso»** con 2 fotos de detalle y composición | Es la prueba de calidad y el diferencial frente a los estampados baratos. |
| 5 | **Por qué mola** (3 ventajas) | Beneficios cortos y escaneables. |
| 6 | **Franja inclinada** con el lema | Respiro visual y personalidad de marca. |
| 7 | **Vídeos / UGC** | La prueba social más fuerte en TikTok y Meta. Los huecos vacíos solo se ven en el personalizador, nunca en la tienda. |
| 8 | **Así se lleva** (galería) | Ayuda a imaginarse con él puesto. También se oculta si está vacía. |
| 9 | **Oferta**: 1 ud. o pack de 2 (destacado) | Segunda oportunidad de compra, con el ahorro calculado y sin trucos. |
| 10 | **Preguntas** sobre talla, gafas, transpirabilidad, lavado, plazos y devoluciones | Resuelve objeciones justo antes de la decisión. |
| 11 | **Cierre** con el lema y un botón | Último empujón. |
| — | **Botón fijo en móvil** | Aparece al pasar la primera pantalla y se esconde cuando se ve el botón del cierre. |

Detalles de conversión y legales:
- **Ahorro real.** Se calcula con los precios de tus variantes: 2 × 24,99 − 39,99 = 9,99 €. No hay precio tachado ni precio «antes».
- **Pack preseleccionado.** Se puede desactivar. El botón siempre dice qué compras y cuánto cuesta («Quiero el pack · 39,99 €»).
- **«Ir directo al pago».** Al pulsar comprar se salta el carrito, que es un paso menos para tráfico de anuncios. Se cambia a «Ir al carrito» en los ajustes.
- **Sin cuentas atrás, sin «quedan X» y sin reseñas inventadas.** La sección no tiene nada de eso.
- **Rendimiento.** Imágenes en tamaños adaptados, solo la primera con prioridad y el resto en diferido. Los vídeos no se descargan hasta que se ven. JavaScript propio de unas 100 líneas, sin librerías.
- **Accesibilidad.** Contrastes AA (negro sobre amarillo 12:1, blanco sobre rojo 5,2:1), botones de 52–64 px, foco visible, textos alternativos y respeto a «reducir movimiento».

## 3. Cómo instalarlo

### Opción A · Conectar GitHub (recomendada)
1. Shopify → **Tienda online → Temas → Añadir tema → Conectar desde GitHub**.
2. Elige el repositorio `asier3334/asier` y la rama `claude/hola-ame6i6`.

⚠️ El repositorio solo contiene la sección, no el tema entero. Para esta opción primero hay que subir tu tema completo al repositorio. Pásame el ZIP del tema (Temas → ⋯ → Descargar archivo del tema) y lo preparo.

### Opción B · Copiar y pegar (5 minutos)
1. **Haz una copia de seguridad.** Temas → ⋯ junto a Horizon → **Duplicar**. Trabaja sobre la copia.
2. En la copia: ⋯ → **Editar código**.
3. `sections` → **Añadir nueva sección** → nombre `mala-cara-venta` → borra el contenido y pega el de `sections/mala-cara-venta.liquid`.
4. `snippets` → **Añadir nuevo snippet** → `mc-icon` → pega el de `snippets/mc-icon.liquid`.
5. `assets` → **Subir activo** → sube los dos archivos `.woff2`.
6. **Personalizar** → plantilla de producto → **Añadir sección → Mala Cara · Venta**. Oculta la sección antigua.
7. En la portada, haz lo mismo y elige el producto en los ajustes de la sección.
8. Revisa en móvil (icono del móvil arriba en el personalizador) y publica la copia.

## 4. Carrito, checkout y textos en inglés (lo haces tú en el panel)

**Idioma**
- Configuración → **Idiomas**: el español debe ser el idioma predeterminado.
- Temas → ⋯ → **Editar contenido predeterminado del tema** → busca «Add to cart», «Your cart», «Checkout», «Sold out», «Continue shopping» y similares. Revisa que estén en español. Si alguno sale en inglés, escribe la traducción.

**Checkout** (Configuración → **Checkout** → **Personalizar**)
- Logo: el de Mala Cara en PNG o SVG, sobre fondo transparente.
- Fondo principal: `#F4EFE3`. Barra lateral (resumen del pedido): `#FFCD00`.
- Color de acento y botones: `#141210`. Errores: `#D22630`.
- Tipografía: Archivo, si aparece en la lista. Bagel Fat One no está disponible en el checkout.
- Bordes de los botones: redondeados.

**Carrito** (Personalizar → Configuración del tema → Carrito)
- Si mantienes «Ir al carrito», usa el tipo **cajón**.
- El texto del botón del carrito («Pagar» o «Finalizar compra») se cambia en el contenido predeterminado del tema.

**Textos de ejemplo**
- Pie de página: borra los menús o bloques de ejemplo y deja Envíos, Devoluciones, Privacidad, Aviso legal y Contacto.
- Cabecera: barra de anuncios vacía o con un dato real. Logo propio.
- Páginas → borra las páginas de ejemplo si las hay.

## 5. Lo que tienes que aportar para dejarla al 100 %

**Fotos** (cuadradas o 4:5, mínimo 1500 px, luz natural, fondo liso crema o amarillo)
- [ ] 4–6 fotos de producto: frente, perfil, espalda (etiqueta de la nuca) y el pack de 2 juntos.
- [ ] Primer plano del tejido de la cara (para «Tejido, no impreso», foto 1).
- [ ] Primer plano de la etiqueta MALA CARA en la nuca (foto 2).
- [ ] 4–8 fotos «así se lleva»: en la calle, en la nieve, en moto, con gafas…
- [ ] Logo en PNG o SVG transparente (para el checkout).
- [ ] Texto alternativo en cada imagen (Contenido → Archivos → imagen → texto alternativo).

**Vídeos** (verticales 9:16, de 10 a 30 segundos, MP4)
- [ ] 3 o más vídeos: ponérselo, el detalle del tejido y una reacción o uso real. Sirven a la vez para los anuncios.
- [ ] Permiso por escrito de cualquier persona que salga en ellos.

**Datos y textos que debes confirmar con la muestra final**
- [ ] Pregunta «¿Puedo llevarlo con gafas?»: pruébalo y reescribe la respuesta.
- [ ] Pregunta «¿Se puede respirar bien?»: lo mismo.
- [ ] Pregunta «¿Cómo se lava?» y el dato «Cuidado»: copia las instrucciones de la etiqueta.
- [ ] Peso (dato 4): rellénalo o déjalo vacío.
- [ ] Coste de la devolución: quién la paga, tanto en la política como en la respuesta de la FAQ.
- [ ] Si el envío es gratis o cuesta algo: añádelo a la barra superior y a las garantías.

**Legal y cuenta** (son tuyos: pagos, contraseñas y datos bancarios)
- [ ] Activar pagos y plan.
- [ ] Aviso legal con nombre, NIF y dirección.
- [ ] Dominio `malacara.es`.
- [ ] Permitir el dominio de la tienda en la red de esta sesión, si quieres que haga la revisión en vivo.
