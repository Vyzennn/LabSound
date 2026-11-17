# LabSound – Validación Científica del Experimento

**Proyecto:** LabSound – MenoresLAB SpA.  
**Responsable asignado:** Vicente Zamorano  
**Área:** Científica y Pedagógica  
**Asignatura:** Proyecto de Innovación Tecnológica  
**Institución:** Universidad Mayor  
**Año:** 2026

---

## 1. Objetivo de la validación científica

Verificar que LabSound permita estudiar correctamente la relación entre la frecuencia de las ondas sonoras y el tono percibido, utilizando mediciones cuantitativas y fundamentos físicos.

La validación busca comprobar que los datos obtenidos sean coherentes con el comportamiento esperado de señales sonoras controladas y que el estudiante pueda interpretarlos científicamente.

## 2. Pregunta experimental

**¿Cómo varía la frecuencia dominante medida (Hz) cuando aumenta el tono percibido de sonidos controlados?**

Esta pregunta establece la relación que se busca estudiar mediante el laboratorio virtual.

## 3. Hipótesis científica

Para sonidos sinusoidales controlados, a medida que aumenta la frecuencia de la onda sonora, el tono percibido será más agudo.

Se espera que:

- Una señal de 220 Hz sea percibida como más grave que una de 440 Hz.
- Una señal de 440 Hz sea percibida como más grave que una de 880 Hz.
- Las mediciones de frecuencia dominante sean cercanas a las frecuencias conocidas de las señales utilizadas.

La hipótesis se limita a sonidos controlados, debido a que los sonidos complejos pueden contener múltiples componentes frecuenciales y armónicos.

## 4. Fundamento científico

El sonido es una onda mecánica que necesita un medio material para propagarse.

La frecuencia representa el número de oscilaciones realizadas por segundo y se expresa en hercios (Hz).

La relación entre frecuencia y período se define mediante:

**f = 1/T**

Donde:

- f es la frecuencia de la onda, medida en Hz.
- T es el período, medido en segundos.

Para una señal sinusoidal ideal:

**x(t) = A · sen(2πft + φ)**

Donde:

- A representa la amplitud.
- f representa la frecuencia.
- t representa el tiempo.
- φ representa la fase inicial.

Estas relaciones permiten describir matemáticamente el comportamiento de los tonos simples utilizados en la experiencia.

## 5. Variables del experimento

| Variable | Tipo | Unidad | Descripción |
|---|---|---|---|
| Frecuencia del tono generado | Independiente | Hz | Frecuencia conocida de la fuente sonora |
| Frecuencia dominante detectada | Dependiente | Hz | Frecuencia estimada por LabSound |
| Amplitud de la señal | Controlada cuando sea posible | Relativa | Magnitud de la señal utilizada |
| Ruido ambiental | Variable de control | — | Interferencias acústicas del entorno |
| Dispositivo de medición | Variable de control | — | Micrófono o dispositivo empleado |
| Frecuencia de muestreo | Parámetro técnico | Hz | Cantidad de muestras de audio por segundo |

El modo demostración actual de LabSound genera una señal fija de 440 Hz. Para evaluar otras frecuencias será necesario utilizar fuentes externas controladas o implementar la generación de tonos variables.

## 6. Instrumentos y recursos

Para ejecutar las pruebas se utilizarán:

- Aplicación web LabSound.
- Computador o teléfono compatible.
- Navegador con soporte para Web Audio API.
- Modo demostración de 440 Hz.
- Micrófono del dispositivo, cuando corresponda.
- Fuente de tonos conocidos para pruebas adicionales.
- Tabla de registro de mediciones.

La aplicación se encuentra disponible en:

https://proyecto-innovacion-lab.netlify.app/

## 7. Procedimiento experimental

### Ensayo 1. Validación del tono de 440 Hz

**Objetivo:** Evaluar la coherencia entre la frecuencia conocida de la señal generada y la frecuencia dominante estimada por LabSound.

**Procedimiento:**

1. Abrir LabSound en el navegador.
2. Seleccionar 440 Hz como frecuencia de referencia.
3. Activar «Modo demo 440 Hz».
4. Observar el gráfico de onda temporal.
5. Observar el espectro de frecuencias.
6. Registrar la frecuencia dominante detectada.
7. Repetir el registro cinco veces.
8. Revisar los indicadores estadísticos.
9. Comparar el promedio obtenido con 440 Hz.

**Resultado esperado:** Una frecuencia dominante cercana a 440 Hz, con error porcentual bajo.

**Resultado obtenido:** Pendiente de medición.

### Ensayo 2. Comparación de diferentes frecuencias

**Objetivo:** Comprobar que las frecuencias detectadas permiten distinguir tonos graves y agudos.

**Procedimiento:**

1. Preparar fuentes sinusoidales conocidas de 220, 440 y 880 Hz.
2. Utilizar el mismo dispositivo de medición cuando sea posible.
3. Mantener condiciones ambientales similares entre ensayos.
4. Capturar cada señal mediante el micrófono de LabSound.
5. Registrar cinco mediciones por frecuencia.
6. Calcular los promedios correspondientes.
7. Comparar los resultados obtenidos.

**Resultado esperado:** Las frecuencias medidas deberán aumentar conforme aumente la frecuencia de las señales utilizadas.

**Resultado obtenido:** Pendiente de medición.

**Observación:** Los botones de referencia de 220, 440 y 880 Hz de la versión actual no modifican el oscilador del modo demostración.

### Ensayo 3. Repetibilidad de las mediciones

**Objetivo:** Evaluar la variación de los resultados al medir repetidamente una misma señal.

**Procedimiento:**

1. Seleccionar una señal de frecuencia conocida.
2. Mantener la fuente y el dispositivo bajo condiciones similares.
3. Registrar cinco mediciones consecutivas.
4. Calcular el promedio.
5. Calcular la desviación estándar.
6. Interpretar la dispersión observada.

**Resultado esperado:** Los valores deberán presentar una dispersión suficientemente pequeña para permitir identificar de forma consistente la frecuencia estudiada.

**Resultado obtenido:** Pendiente.

## 8. Registro de resultados

### Tabla 1. Ensayo de 440 Hz

| Medición | Frecuencia detectada (Hz) | Error (%) |
|---|---|---|
| 1 | Pendiente | Pendiente |
| 2 | Pendiente | Pendiente |
| 3 | Pendiente | Pendiente |
| 4 | Pendiente | Pendiente |
| 5 | Pendiente | Pendiente |

**Promedio:** Pendiente.

**Desviación estándar:** Pendiente.

**Error porcentual del promedio:** Pendiente.

### Tabla 2. Comparación de tonos

| Tono | Frecuencia de referencia | Promedio medido | Observaciones |
|---|---|---|---|
| Grave | 220 Hz | Pendiente | Pendiente |
| Intermedio | 440 Hz | Pendiente | Pendiente |
| Agudo | 880 Hz | Pendiente | Pendiente |

Esta tabla deberá completarse únicamente después de realizar los ensayos correspondientes.

## 9. Análisis matemático de resultados

### Promedio

El promedio permite obtener una medida representativa de las frecuencias registradas:

**f_prom = (f₁ + f₂ + ... + fₙ) / n**

Donde n corresponde al número de mediciones.

### Desviación estándar

La desviación estándar permite analizar la dispersión de las mediciones respecto del promedio.

La aplicación utiliza una fórmula con divisor n, correspondiente a la desviación estándar poblacional del conjunto registrado.

**σ = √[Σ(fᵢ − f_prom)² / n]**

### Error porcentual

El error porcentual permite comparar un valor experimental con una frecuencia de referencia conocida.

**Error (%) = |f_medida − f_referencia| / f_referencia × 100**

Estas herramientas permiten analizar la repetibilidad y la cercanía de los resultados respecto de los valores de referencia.

## 10. Criterios de evaluación científica

La validación considerará:

**Coherencia física:** Las frecuencias medidas deben ser compatibles con las señales controladas utilizadas.

**Exactitud de medición:** El error porcentual debe ser evaluado respecto de la frecuencia conocida.

**Repetibilidad:** La desviación estándar debe permitir identificar la dispersión entre mediciones.

**Interpretación científica:** Los resultados deben permitir relacionar el aumento de frecuencia con el aumento del tono percibido en señales simples.

**Unidades:** Las frecuencias deben expresarse correctamente en Hz.

No se establece un umbral numérico de aprobación sin contar previamente con un criterio experimental justificado.

## 11. Limitaciones del experimento

Durante la validación deben considerarse las siguientes limitaciones:

1. El ruido ambiental puede afectar la detección de frecuencia mediante micrófono.
2. La calidad y respuesta del micrófono pueden variar según el dispositivo.
3. La frecuencia dominante no necesariamente corresponde a la fundamental en sonidos complejos.
4. La precisión depende de la configuración del análisis espectral y de las características de la señal.
5. El modo demostración de la versión revisada está limitado a 440 Hz.
6. Las mediciones obtenidas mediante una misma señal digital pueden presentar poca variación y no representar todas las condiciones de un ensayo acústico real.

## 12. Evidencias experimentales

Para respaldar la validación se deberán incorporar:

- Captura del modo demostración de 440 Hz.
- Captura del espectro de frecuencias.
- Tabla con cinco mediciones registradas.
- Indicadores estadísticos obtenidos.
- Capturas de las pruebas con otras frecuencias, si se realizan.
- Observaciones de dificultades y decisiones tomadas durante la experimentación.

## 13. Análisis y discusión

Una vez completadas las pruebas, se deberán responder las siguientes preguntas:

1. ¿La frecuencia detectada fue cercana a la frecuencia de referencia?
2. ¿Qué error porcentual se obtuvo?
3. ¿Existió variación entre las cinco mediciones?
4. ¿Qué factores podrían explicar las diferencias observadas?
5. ¿Los resultados permiten distinguir adecuadamente tonos graves y agudos?
6. ¿Qué limitaciones deben considerarse al interpretar el espectro de frecuencias?

Las respuestas deberán fundamentarse en los datos registrados durante la validación.

## 14. Conclusión

El análisis conceptual y la revisión del funcionamiento previsto de LabSound permiten establecer un protocolo de validación basado en frecuencias de referencia, mediciones repetidas y análisis estadístico.

El laboratorio utiliza herramientas de procesamiento espectral para representar cuantitativamente señales sonoras y estudiar su relación con el tono percibido.

La validación experimental deberá determinar la coherencia, exactitud y repetibilidad de las frecuencias detectadas.

Los resultados obtenidos permitirán evaluar la pertinencia científica del MVP y respaldar su aplicación como recurso de aprendizaje de ondas y sonido en estudiantes de primero medio.
