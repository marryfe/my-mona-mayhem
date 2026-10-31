<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización desde el diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Es desarrollo desde el diseño: empieza con una visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo de planificación.
<!-- track:cli:end -->

Introduce este prompt:

> Quiero transformar esta página en una experiencia completa de arcade retro. Planifica una renovación visual que incluya: efectos de líneas de barrido CRT en el fondo, un resplandor de neón en el título que pulse como un letrero luminoso, una insignia VS animada con cambios de color en el degradado, una capa de brillo sobre las tarjetas de resultados de usuario, animaciones de entrada flotante para los campos de entrada, texto de carga que alterne entre verde y morado, y efectos de resplandor al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) y usa verde (`#5fed83`) y morado (`#8a2be2`) como colores de acento. Usa un tema oscuro con la tipografía de videojuegos retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación que abarque todos los efectos visuales. **No lo aceptes de inmediato**: revisa el plan e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo, *«Haz que el pulso de neón sea más lento, de unos 3 segundos»*).
- Pregunta por efectos concretos (por ejemplo, *«¿Cómo funcionará la capa de brillo de las tarjetas?»*).
- Solicita cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés satisfecho con el plan, pide a Copilot que lo implemente.

> Implementa el plan de tema de arcade retro que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones en la hoja de estilos. Puede incluir:

- `@keyframes` para las líneas de barrido, el pulso de neón, el brillo y los efectos de entrada flotante
- Pseudoelementos (`::before`, `::after`) para los efectos de superposición
- Propiedades personalizadas de CSS para los colores del tema
- Transiciones y estados hover para los elementos interactivos

<!-- track:cli:start -->
Cuando se apliquen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta el estilo

> **⚠️ ¿No ves los cambios?** Si el tema o las animaciones no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y actualiza el navegador con **Ctrl+Shift+R**.

Mantén abierta la vista previa del navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un ligero parpadeo eléctrico al texto del título.

> La insignia VS debería pulsar con más intensidad.

Esto es **desarrollo desde el diseño**: iteras sobre el resultado visual en tiempo real. Cada prompt refina la experiencia hasta que tenga el aspecto adecuado. No te conformes con algo «suficientemente bueno»: ajusta el estilo hasta que la página parezca una máquina arcade.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deben reflejar las decisiones de diseño importantes para que los prompts posteriores mantengan la coherencia.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Añade a `copilot-instructions.md` una sección de guía de diseño que describa nuestro tema de arcade retro: colores, tipografías y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Actualiza las instrucciones del repositorio con una breve guía de diseño para el tema de arcade retro: colores, tipografías, estilo de animación y la regla de que la nueva interfaz mantenga la estética de neón.
<!-- track:cli:end -->

Cuando la página tenga el aspecto adecuado, haz commit de las instrucciones y los cambios de diseño.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para diseñar un **sistema visual antes de implementarlo**
- **Iterar sobre el resultado visual** con prompts de seguimiento
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener la identidad visual
