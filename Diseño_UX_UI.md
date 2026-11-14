# LabSound – Documentación de Diseño UX/UI

**Proyecto:** LabSound – MenoresLAB SpA.  
**Responsable asignado:** Lucas Espinoza  
**Área:** Diseño de Interfaz y Experiencia de Usuario (UX/UI)  
**Asignatura:** Proyecto de Innovación Tecnológica  
**Institución:** Universidad Mayor  
**Año:** 2026

---

## 1. Objetivo del diseño

El diseño de la interfaz de LabSound busca proporcionar una experiencia educativa sencilla, intuitiva y accesible para estudiantes de primero medio.

La aplicación está orientada a facilitar la comprensión de la relación entre el tono percibido y la frecuencia de las ondas sonoras mediante herramientas visuales e interactivas.

La propuesta considera tres principios:

- **Claridad:** presentar la información de manera ordenada y comprensible.
- **Interactividad:** permitir al estudiante experimentar con señales sonoras y observar sus resultados.
- **Autonomía:** facilitar la utilización del laboratorio sin intervención constante de los desarrolladores.

## 2. Público objetivo

LabSound está dirigido principalmente a estudiantes de primero medio que estudian contenidos relacionados con ondas y sonido.

El diseño considera usuarios con conocimientos iniciales de física, por lo que prioriza controles identificables, instrucciones breves e indicadores cuantitativos visibles.

## 3. Diseño visual de la aplicación

La interfaz utiliza una estética digital de laboratorio científico, caracterizada por un fondo oscuro y colores de contraste.

La inspección del código CSS confirma los siguientes colores principales:

| Elemento | Código de color | Función |
|---|---|---|
| Fondo principal | `#07101d` | Base visual oscura |
| Paneles | `#0d192a` | Organización del contenido |
| Texto principal | `#f3f7fb` | Lectura de información |
| Verde turquesa | `#41d6c3` | Botones principales y señal temporal |
| Azul | `#7aa7ff` | Elementos gráficos y acentos |
| Amarillo | `#f7c66b` | Acciones destacadas |

Se utiliza una familia tipográfica de sistema con preferencia por Inter cuando está disponible.

Los paneles presentan bordes redondeados, separación entre componentes y agrupaciones visuales para organizar la información.

## 4. Distribución de la interfaz

LabSound utiliza una distribución principal de dos columnas en pantallas amplias.

**Zona principal:**

- Identificación del laboratorio.
- Estado del micrófono.
- Controles del experimento.
- Instrucciones de conexión.
- Gráfico de onda en el tiempo.
- Gráfico de espectro de frecuencias.
- Indicadores de frecuencia dominante, nivel relativo y muestreo.

**Zona secundaria:**

- Pregunta experimental.
- Frecuencia de referencia.
- Controles de referencia de 220, 440 y 880 Hz.
- Tabla de mediciones.
- Indicadores estadísticos.
- Botón para limpiar registros.

Esta distribución permite visualizar los controles y los resultados dentro de una misma interfaz.

## 5. Flujo de navegación del usuario

El recorrido previsto del estudiante se organiza de la siguiente manera:

1. **Ingreso:** el estudiante abre LabSound y visualiza el objetivo del laboratorio.
2. **Configuración:** selecciona una frecuencia de referencia.
3. **Inicio:** activa el micrófono o el modo demostración.
4. **Observación:** analiza la señal temporal y el espectro de frecuencias.
5. **Medición:** observa la frecuencia dominante detectada.
6. **Registro:** utiliza el botón «Registrar medición».
7. **Repetición:** realiza nuevas mediciones para comparar resultados.
8. **Análisis:** consulta el promedio, la desviación estándar y el error porcentual.
9. **Finalización:** detiene el experimento y revisa los resultados.

La navegación está implementada como un tablero único, por lo que el usuario no necesita cambiar entre múltiples páginas.

## 6. Diseño de controles interactivos

La aplicación incorpora botones con funciones específicas:

| Control | Función |
|---|---|
| Activar micrófono | Solicitar acceso a la entrada de audio |
| Modo demo 440 Hz | Iniciar una señal digital de demostración |
| Detener | Finalizar la adquisición o simulación |
| Registrar medición | Incorporar una frecuencia detectada a la tabla |
| 220, 440 y 880 Hz | Cambiar la frecuencia de referencia |
| Limpiar tabla | Eliminar los registros de medición actuales |

Los botones de inicio y registro poseen estados habilitados y deshabilitados según la condición del sistema.

Esto permite orientar al estudiante y evitar determinadas acciones cuando el laboratorio no se encuentra activo.

## 7. Diseño responsivo

El código CSS incluye reglas de adaptación mediante media queries.

**Pantallas de hasta 900 píxeles:**

La distribución de dos columnas pasa a una sola columna, facilitando la visualización en dispositivos de menor tamaño.

**Pantallas de hasta 560 píxeles:**

Se ajustan los márgenes, el tamaño de los gráficos y la distribución de indicadores.

Esto permite adaptar el diseño a computadores, tabletas y teléfonos móviles.

La adaptación está implementada en el código y debe complementarse con pruebas visuales en dispositivos reales.

## 8. Elementos de usabilidad

LabSound incorpora características que favorecen su utilización:

- Textos descriptivos en botones y secciones.
- Estado visible del micrófono.
- Mensajes sobre permisos y errores de acceso al audio.
- Controles agrupados según su función.
- Gráficos ubicados cerca de los indicadores numéricos.
- Unidades de frecuencia identificadas como Hz.
- Mensaje cuando todavía no existen mediciones.
- Instrucciones para realizar al menos cinco registros por tono.

Estos elementos buscan reducir la necesidad de asistencia durante el experimento.

## 9. Visualización científica

La interfaz incorpora dos gráficos principales.

**Onda en el tiempo**

Presenta una representación de la amplitud relativa de la señal sonora, permitiendo observar su comportamiento temporal.

**Espectro de frecuencias**

Presenta las componentes frecuenciales de la señal analizada mediante FFT dentro de un rango de hasta 2000 Hz.

Los gráficos se representan mediante Canvas y se actualizan mientras el sistema está activo.

El diseño también incorpora tarjetas de indicadores que muestran la frecuencia dominante, el nivel relativo en dBFS y la frecuencia de muestreo.

## 10. Mejoras propuestas

Para fortalecer la experiencia de usuario y aspirar al Nivel 4 de la rúbrica, se identifican las siguientes mejoras:

1. Incorporar instrucciones numeradas del procedimiento experimental.
2. Agregar escalas numéricas y unidades visibles en los ejes de los gráficos.
3. Incorporar una comparación visual entre los tonos registrados.
4. Agregar un resumen final que permita formular conclusiones.
5. Verificar la legibilidad de gráficos, tablas y botones en teléfonos móviles.
6. Realizar pruebas con estudiantes externos al equipo para evaluar la autonomía de uso.

Estas mejoras se encuentran propuestas y no deben considerarse implementadas hasta comprobar su incorporación.

## 11. Plan de validación UX/UI

Para evaluar la usabilidad se propone solicitar a un usuario externo que complete el experimento sin recibir instrucciones adicionales de los desarrolladores.

Las actividades de evaluación serán:

- Ingresar a LabSound.
- Identificar cómo comenzar el experimento.
- Activar el micrófono o la demostración.
- Interpretar la frecuencia dominante.
- Registrar cinco mediciones.
- Consultar los resultados estadísticos.
- Detener el experimento.

Durante la prueba se registrarán las dificultades observadas, las ayudas solicitadas y las acciones completadas de manera autónoma.

**Estado de la validación:** Pendiente de ejecución y registro.

## 12. Evidencias de diseño

Para documentar la implementación y revisión de la interfaz se recomienda incluir:

- Captura general del tablero LabSound.
- Captura de los controles principales.
- Captura de los gráficos con datos activos.
- Captura de la tabla de resultados.
- Captura de la visualización en un teléfono móvil.
- Registro de observaciones obtenidas en pruebas de usabilidad.

## 13. Conclusión

La inspección del código fuente confirma que LabSound cuenta con una interfaz responsiva, organizada en paneles y diseñada para representar información científica mediante gráficos, indicadores y controles interactivos.

La distribución visual y los estados de los botones proporcionan una base para que el estudiante realice el experimento de manera autónoma.

Para completar la validación UX/UI es necesario realizar pruebas prácticas con usuarios y comprobar que la experiencia pueda desarrollarse sin asistencia técnica.

---

**Responsable de revisión UX/UI:** Lucas Espinoza.  
**Estado:** Características de diseño verificadas mediante revisión del código. Pruebas de usabilidad pendientes.
