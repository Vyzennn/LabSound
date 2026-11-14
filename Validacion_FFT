# LabSound – Validación del Procesamiento FFT

*Proyecto:* LabSound – MenoresLAB SpA.  
*Responsable:* Ignacio Miranda  
*Área:* Software y Datos  
*Asignatura:* Proyecto de Innovación Tecnológica  
*Universidad:* Universidad Mayor  
*Año:* 2026

---

## 1. Objetivo de la validación

Verificar que el sistema de procesamiento digital de señales de LabSound permita identificar frecuencias sonoras de manera consistente mediante la Transformada Rápida de Fourier (FFT).

La validación busca comprobar la correspondencia entre las frecuencias de referencia y las frecuencias dominantes detectadas por la aplicación.

## 2. Descripción del sistema

LabSound es una aplicación web educativa que permite analizar señales sonoras mediante el micrófono del dispositivo o mediante una señal generada digitalmente.

El sistema utiliza JavaScript y Web Audio API para procesar audio directamente en el navegador.

El procesamiento FFT permite transformar la información de una señal sonora desde el dominio temporal al dominio de la frecuencia.

Los resultados se muestran mediante un espectro de frecuencias y un indicador numérico expresado en hercios (Hz).

## 3. Configuración técnica del algoritmo

La revisión del código fuente index.html permite identificar los siguientes parámetros:

| Parámetro | Configuración |
|---|---|
| Motor de audio | Web Audio API |
| Analizador | AnalyserNode |
| Tamaño FFT | 8192 |
| Suavizado temporal | 0,62 |
| Intervalo de búsqueda | Aproximadamente 70–2000 Hz |
| Muestreo | Determinado por AudioContext |
| Procesamiento | Análisis espectral y detección del máximo |
| Visualización | Canvas API |

El algoritmo identifica el máximo espectral dentro del intervalo establecido y aplica una interpolación parabólica para refinar la estimación de frecuencia.

## 4. Fundamento matemático

La frecuencia de una señal periódica se relaciona con su período mediante:

*f = 1/T*

Donde:

- f representa la frecuencia en hercios (Hz).
- T representa el período en segundos (s).

Para el análisis FFT, la separación nominal entre componentes espectrales consecutivas es:

*Δf = fs/N*

Donde:

- Δf: separación entre bins, en Hz.
- fs: frecuencia de muestreo del sistema, en Hz.
- N: tamaño FFT, equivalente a 8192.

Por ejemplo, para una frecuencia de muestreo hipotética de 48.000 Hz:

Δf = 48.000 / 8192 ≈ 5,86 Hz.

Este ejemplo es un cálculo teórico. La frecuencia de muestreo real debe obtenerse de la aplicación durante las pruebas.

## 5. Metodología de validación

Se propone utilizar tonos sinusoidales de frecuencia conocida para comparar el valor esperado con la frecuencia detectada por LabSound.

El procedimiento será:

1. Abrir LabSound desde su dirección HTTPS.
2. Seleccionar el modo demostración de 440 Hz.
3. Comprobar que se visualice la onda temporal.
4. Observar el espectro FFT.
5. Registrar la frecuencia dominante indicada.
6. Repetir la medición al menos cinco veces.
7. Calcular el promedio, la desviación estándar y el error porcentual.
8. Comparar los resultados con la frecuencia de referencia.

Para evaluar frecuencias adicionales como 220 y 880 Hz será necesario generar externamente tonos conocidos o implementar primero la selección de frecuencia en el oscilador de demostración.

## 6. Registro de resultados experimentales

*Frecuencia de referencia:* 440 Hz.

| Medición | Frecuencia detectada (Hz) | Error porcentual |
|---|---|---|
| 1 | Pendiente | Pendiente |
| 2 | Pendiente | Pendiente |
| 3 | Pendiente | Pendiente |
| 4 | Pendiente | Pendiente |
| 5 | Pendiente | Pendiente |

*Resultados estadísticos:*

- Promedio de frecuencia: pendiente.
- Desviación estándar: pendiente.
- Error porcentual del promedio: pendiente.

Los datos deberán completarse utilizando mediciones reales obtenidas durante la ejecución de LabSound.

## 7. Evaluación de precisión

La precisión del sistema se evaluará mediante el error porcentual respecto de una frecuencia de referencia conocida.

*Error (%) = |f medida − f referencia| / f referencia × 100*

El análisis permitirá determinar qué tan cercana es la frecuencia detectada al valor esperado.

También se evaluará la repetibilidad mediante la desviación estándar de las cinco mediciones.

Una desviación estándar pequeña indicaría baja dispersión de los resultados bajo las condiciones específicas del ensayo.

## 8. Pruebas complementarias

Se recomienda verificar:

- Estabilidad del análisis FFT durante varios segundos.
- Respuesta del sistema ante señales de diferentes frecuencias.
- Funcionamiento del micrófono en distintos navegadores.
- Ausencia de resultados válidos cuando no existe una señal detectable.
- Correcta actualización del espectro y los indicadores.
- Comportamiento al detener y reiniciar el experimento.

Los resultados de estas pruebas deben documentarse con observaciones y evidencias.

## 9. Evidencias requeridas

Para respaldar el procedimiento se deberán incorporar:

- Captura de LabSound ejecutando el modo demostración de 440 Hz.
- Captura del espectro FFT con la frecuencia dominante visible.
- Captura de la tabla con cinco mediciones.
- Resultados estadísticos calculados por la aplicación.
- Registro de errores encontrados y correcciones realizadas, cuando corresponda.

## 10. Conclusión

La inspección del código fuente confirma que LabSound incorpora un analizador FFT mediante Web Audio API y un algoritmo de detección de frecuencia dominante.

Esta implementación permite desarrollar un procedimiento de validación utilizando frecuencias controladas como referencia.

La precisión y estabilidad del sistema todavía deben determinarse mediante las pruebas experimentales descritas.

Una vez registrados los valores obtenidos, será posible evaluar cuantitativamente el desempeño del algoritmo y establecer conclusiones respaldadas por evidencia.

---

*Responsable de la validación:* Ignacio Miranda.  
*Estado:* Revisión de implementación completada; validación experimental pendiente.
