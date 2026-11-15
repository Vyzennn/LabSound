# LabSound – Documentación Técnica de Software y Datos

*Proyecto:* LabSound – MenoresLAB SpA.  
*Área responsable:* Software y Datos  
*Responsable asignado:* Ignacio Miranda  
*Asignatura:* Proyecto de Innovación Tecnológica  
*Institución:* Universidad Mayor  
*Año:* 2026

---

## 1. Descripción del sistema

LabSound es una aplicación web educativa desarrollada para facilitar el aprendizaje de las ondas sonoras en estudiantes de primero medio.

El sistema permite capturar señales acústicas mediante el micrófono del dispositivo o generar una señal simulada, procesar las muestras digitales y representar sus características mediante gráficos e indicadores cuantitativos.

Su objetivo es relacionar el tono percibido con la frecuencia dominante de sonidos controlados.

## 2. Arquitectura tecnológica

La aplicación utiliza una arquitectura web ejecutada directamente en el navegador.

*Tecnologías implementadas:*

- HTML5: estructura de la interfaz.
- CSS3: diseño visual, distribución y adaptación a diferentes pantallas.
- JavaScript: programación de controles, procesamiento y registro de mediciones.
- Web Audio API: adquisición y análisis de señales de audio.
- Canvas API: representación gráfica de las señales.
- Netlify: alojamiento y publicación de la aplicación.
- GitHub: repositorio del código y gestión de versiones.

La implementación está contenida en un archivo principal index.html, que integra HTML, CSS y JavaScript sin requerir librerías externas.

## 3. Adquisición de datos

LabSound incorpora dos modalidades de adquisición:

*Modo micrófono*

Utiliza navigator.mediaDevices.getUserMedia() para solicitar acceso al micrófono.

La señal obtenida se conecta a un nodo de análisis de Web Audio API para extraer información temporal y frecuencial.

El sistema solicita desactivar la cancelación de eco, la supresión de ruido y el control automático de ganancia, aunque su aplicación efectiva depende del dispositivo y navegador.

*Modo demostración*

Utiliza OscillatorNode para generar una señal sinusoidal de 440 Hz.

Esta señal se procesa mediante el mismo analizador que utiliza el modo micrófono.

El modo demostración permite observar el comportamiento del procesamiento digital sin necesitar una fuente sonora externa.

## 4. Procesamiento de señales

El motor de procesamiento utiliza un objeto AnalyserNode configurado con los siguientes parámetros:

- Tamaño FFT: 8192 muestras.
- Factor de suavizado temporal: 0,62.
- Intervalo de búsqueda de frecuencia dominante: aproximadamente 70 a 2000 Hz.
- Frecuencia de muestreo: obtenida automáticamente desde AudioContext.sampleRate.

La frecuencia dominante se determina identificando el máximo espectral dentro del intervalo definido.

El algoritmo incorpora interpolación parabólica entre el máximo y sus dos valores vecinos para refinar la estimación de frecuencia.

La resolución espectral nominal depende de la frecuencia de muestreo y se expresa como:

*Δf = fs / N*

Donde:

- Δf: separación entre bins espectrales, en Hz.
- fs: frecuencia de muestreo, en Hz.
- N: tamaño de la FFT, equivalente a 8192.

## 5. Variables y unidades

| Variable | Unidad | Descripción |
|---|---|---|
| Frecuencia dominante | Hz | Frecuencia correspondiente al máximo espectral detectado |
| Tiempo | s | Variable temporal de la señal |
| Amplitud | Relativa | Magnitud digital de la señal |
| Nivel digital | dBFS | Nivel relativo calculado a partir del valor RMS |
| Frecuencia de muestreo | Hz | Muestras de audio por segundo |
| Frecuencia de referencia | Hz | Valor utilizado para calcular el error |

El indicador de nivel digital no constituye una medición calibrada de presión sonora en dB SPL.

## 6. Visualización científica

La aplicación utiliza dos elementos Canvas:

*Onda temporal*

Representa las muestras de amplitud digital de la señal y permite observar sus oscilaciones a lo largo del tiempo.

*Espectro de frecuencias*

Representa la información espectral obtenida mediante FFT dentro de un intervalo de hasta 2000 Hz.

El sistema también destaca gráficamente la frecuencia dominante estimada.

Estos gráficos permiten observar diferencias entre señales y apoyar el estudio experimental de la relación entre tono y frecuencia.

## 7. Registro y análisis estadístico

LabSound incorpora una tabla que almacena las frecuencias dominantes registradas por el estudiante durante la sesión.

El programa calcula automáticamente:

*Promedio:*

Promedio = suma de las frecuencias / número de mediciones.

*Desviación estándar:*

Se calcula la raíz cuadrada de la media de las diferencias cuadráticas respecto del promedio, utilizando el divisor N.

*Error porcentual:*

Error (%) = |frecuencia medida − frecuencia de referencia| / frecuencia de referencia × 100.

El sistema muestra el error individual de cada medición y el error porcentual del promedio.

Las mediciones se almacenan temporalmente en memoria durante la ejecución de la aplicación.

## 8. Interfaz y controles

Los controles implementados incluyen:

- Activar micrófono.
- Iniciar modo demostración de 440 Hz.
- Detener adquisición o simulación.
- Registrar medición.
- Seleccionar una frecuencia de referencia de 220, 440 u 880 Hz.
- Introducir manualmente una frecuencia de referencia.
- Limpiar la tabla de mediciones.

Los controles de referencia permiten modificar el valor utilizado en los cálculos de error, pero actualmente no modifican el tono generado en el modo demostración.

## 9. Consideraciones y limitaciones técnicas

Se identifican las siguientes condiciones:

1. El acceso al micrófono requiere un contexto seguro compatible, como HTTPS.
2. La frecuencia de muestreo depende de la configuración del navegador y dispositivo.
3. La frecuencia dominante no siempre coincide con la frecuencia fundamental en sonidos complejos.
4. Los valores dBFS son relativos y no equivalen a intensidad acústica calibrada.
5. El modo demostración genera un tono fijo de 440 Hz.
6. Los registros no se conservan después de recargar o cerrar la página.
7. Los gráficos presentan referencias de escala, pero pueden mejorarse incorporando ejes numéricos más detallados.

## 10. Validación técnica pendiente

Para comprobar el funcionamiento del sistema se deben ejecutar las siguientes pruebas:

- Activación del micrófono en computador y teléfono.
- Generación y detección del tono demostrativo de 440 Hz.
- Visualización de la onda temporal.
- Actualización del espectro FFT.
- Registro consecutivo de cinco mediciones.
- Cálculo de promedio, desviación estándar y error.
- Cambio de frecuencia de referencia.
- Detención y reinicio del experimento.

Los resultados deben registrarse con capturas de pantalla y valores obtenidos en pruebas reales.

## 11. Conclusión

El análisis del código fuente confirma que LabSound implementa un sistema de adquisición, procesamiento y visualización de señales sonoras utilizando tecnologías web.

La integración de Web Audio API, FFT, Canvas y los cálculos estadísticos proporciona una base funcional para desarrollar experiencias educativas de análisis de frecuencias.

Para completar su validación como MVP integrado, es necesario comprobar experimentalmente la estabilidad del sistema, la exactitud de las mediciones y la autonomía de uso por parte del estudiante.
