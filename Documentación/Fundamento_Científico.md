# LabSound – Fundamento Científico y Pedagógico

**Proyecto:** LabSound – MenoresLAB SpA.  
**Responsable asignado:** Vicente Zamorano  
**Área:** Científica y Pedagógica  
**Asignatura:** Proyecto de Innovación Tecnológica  
**Institución:** Universidad Mayor  
**Año:** 2026

---

## 1. Introducción

LabSound es un laboratorio virtual educativo destinado a estudiantes de primero medio, orientado al aprendizaje de las ondas sonoras y la relación entre frecuencia y tono.

El proyecto surge de la necesidad de complementar la enseñanza teórica de las ondas mediante una experiencia experimental que permita visualizar, medir y comparar señales acústicas.

La aplicación permite utilizar el micrófono de un dispositivo o generar un sonido de demostración para observar las características de una señal sonora mediante representaciones gráficas.

## 2. Problema de aprendizaje identificado

En el estudio de ondas y sonido, los estudiantes pueden distinguir auditivamente un sonido grave de uno agudo sin comprender necesariamente cómo esa diferencia se relaciona con la frecuencia física de la señal.

Esta dificultad limita la interpretación de gráficos y el análisis cuantitativo del fenómeno.

LabSound busca abordar esta necesidad permitiendo observar la señal temporal, visualizar su espectro y registrar valores de frecuencia expresados en hercios.

## 3. Pregunta experimental

**¿Cómo varía la frecuencia dominante medida (Hz) cuando aumenta el tono percibido de sonidos controlados?**

Esta pregunta orienta el desarrollo del experimento y permite relacionar una percepción auditiva con una variable física cuantificable.

## 4. Hipótesis

Para sonidos sinusoidales controlados, a medida que aumenta la frecuencia de la señal sonora, el tono percibido será más agudo.

Por lo tanto, se espera que un sonido de 880 Hz sea percibido como más agudo que uno de 440 Hz, mientras que uno de 220 Hz sea percibido como más grave.

Esta hipótesis se aplica a tonos controlados y no debe generalizarse automáticamente a sonidos complejos con múltiples componentes frecuenciales.

## 5. Fundamento físico de las ondas sonoras

El sonido es una onda mecánica que necesita un medio material para propagarse.

En el aire, las ondas sonoras se producen mediante variaciones de presión que se propagan a través del medio.

Entre las características principales de una onda sonora se encuentran:

- **Frecuencia:** número de oscilaciones realizadas por segundo.
- **Período:** tiempo necesario para completar una oscilación.
- **Amplitud:** magnitud de la variación de la señal.
- **Longitud de onda:** distancia espacial correspondiente a un ciclo de la onda.
- **Velocidad de propagación:** rapidez con que la perturbación se desplaza por el medio.

La frecuencia se mide en hercios (Hz), unidad equivalente a ciclos por segundo.

## 6. Relación entre frecuencia y tono

El tono es una característica perceptiva del sonido que permite clasificarlo como grave o agudo.

Para tonos sinusoidales simples:

- Las frecuencias menores se perciben generalmente como sonidos más graves.
- Las frecuencias mayores se perciben generalmente como sonidos más agudos.

Por ejemplo:

| Frecuencia | Clasificación relativa |
|---|---|
| 220 Hz | Grave |
| 440 Hz | Intermedio |
| 880 Hz | Agudo |

Estas clasificaciones son relativas a los tonos comparados y no constituyen límites universales entre sonidos graves y agudos.

## 7. Modelo matemático

### Relación entre frecuencia y período

La frecuencia de una onda periódica se expresa mediante:

**f = 1/T**

Donde:

- f: frecuencia, en Hz.
- T: período, en segundos.

Despejando:

**T = 1/f**

Por ejemplo, para una señal de 440 Hz:

T = 1/440 ≈ 0,00227 s.

Esto corresponde aproximadamente a 2,27 milisegundos por oscilación.

### Modelo de onda sinusoidal

Una señal sinusoidal ideal puede representarse mediante:

**x(t) = A · sen(2πft + φ)**

Donde:

- x(t): valor de la señal en el instante t.
- A: amplitud.
- f: frecuencia de oscilación.
- t: tiempo.
- φ: fase inicial.

Este modelo permite representar matemáticamente el tipo de señal generado por el modo demostración de LabSound.

### Relación entre velocidad, frecuencia y longitud de onda

Para una onda periódica:

**v = λ · f**

Donde:

- v: velocidad de propagación.
- λ: longitud de onda.
- f: frecuencia.

Esta relación proporciona contexto físico sobre la propagación del sonido, aunque LabSound no mide directamente la longitud de onda ni la velocidad de propagación.

## 8. Variables experimentales

| Variable | Tipo | Unidad | Descripción |
|---|---|---|---|
| Frecuencia del tono generado | Independiente propuesta | Hz | Frecuencia seleccionada para comparar sonidos controlados |
| Frecuencia dominante detectada | Dependiente | Hz | Frecuencia estimada por el algoritmo de análisis |
| Amplitud de señal | Controlada cuando sea posible | Relativa | Magnitud de la señal utilizada |
| Dispositivo de medición | Controlada | — | Micrófono o sistema de adquisición empleado |
| Condiciones de ruido ambiental | Controlada cuando sea posible | — | Condiciones acústicas durante el ensayo |
| Frecuencia de muestreo | Parámetro técnico | Hz | Cantidad de muestras digitales obtenidas por segundo |

En la versión actual del modo demostración, el oscilador genera 440 Hz. Los controles de 220, 440 y 880 Hz modifican la referencia utilizada en los cálculos, pero no cambian por sí mismos la frecuencia generada.

Por esta razón, la comparación experimental entre distintos tonos requiere implementar una selección de frecuencia para el oscilador o utilizar fuentes externas conocidas.

## 9. Procesamiento de señales y FFT

LabSound utiliza la Transformada Rápida de Fourier (FFT) mediante Web Audio API para analizar las componentes frecuenciales de la señal sonora.

El sistema emplea un analizador configurado con un tamaño FFT de 8192 muestras.

El algoritmo busca la componente de mayor magnitud dentro del rango aproximado de 70 a 2000 Hz y presenta una estimación de su frecuencia.

**Frecuencia dominante:** componente frecuencial con mayor magnitud detectada dentro del intervalo analizado.

**Frecuencia fundamental:** frecuencia asociada a la periodicidad básica de una señal periódica.

En una señal sinusoidal ideal ambas coinciden. En sonidos complejos, la frecuencia dominante puede corresponder a un armónico diferente de la frecuencia fundamental.

Esta distinción es importante para evitar interpretaciones científicas incorrectas.

## 10. Interpretación de resultados

El estudiante puede observar dos representaciones principales:

**Onda en el tiempo:** permite visualizar las oscilaciones de la señal en el dominio temporal.

**Espectro de frecuencias:** permite observar las componentes frecuenciales obtenidas mediante el procesamiento FFT.

El análisis cuantitativo permite comparar el valor medido con una frecuencia de referencia conocida.

La aplicación también incorpora indicadores estadísticos para analizar múltiples mediciones.

Estos resultados pueden utilizarse para estudiar la repetibilidad y la cercanía de las mediciones respecto de un valor de referencia.

## 11. Pertinencia pedagógica

LabSound está dirigido a estudiantes de primero medio y se relaciona con el aprendizaje de ondas y sonido.

La propuesta busca contribuir a las siguientes capacidades:

- Reconocer características de las ondas sonoras.
- Relacionar la frecuencia con la percepción del tono.
- Interpretar información presentada mediante gráficos.
- Registrar datos experimentales.
- Comparar mediciones con valores de referencia.
- Formular conclusiones fundamentadas en evidencia cuantitativa.

## 12. Procedimiento pedagógico propuesto

1. Ingresar a LabSound.
2. Leer la pregunta experimental.
3. Seleccionar una frecuencia de referencia.
4. Activar el modo demostración de 440 Hz.
5. Observar la onda en el tiempo.
6. Identificar el espectro de frecuencias.
7. Registrar cinco mediciones.
8. Consultar el promedio y la desviación estándar.
9. Comparar las mediciones con la referencia de 440 Hz.
10. Interpretar los resultados y formular una conclusión.

Para estudiar experimentalmente tonos de diferentes frecuencias será necesario emplear fuentes de tonos conocidos o actualizar el modo demostración.

## 13. Criterios de validación científica

La validación científica debe comprobar:

- Coherencia entre la frecuencia conocida y la frecuencia detectada.
- Correcta identificación de las unidades de medida.
- Repetibilidad de las mediciones.
- Pertinencia del análisis FFT para tonos controlados.
- Diferenciación entre frecuencia dominante y fundamental.
- Correcta interpretación de las estadísticas.
- Relación entre el resultado experimental y la pregunta científica.

## 14. Conclusión

LabSound ofrece una herramienta digital para complementar la enseñanza de ondas y sonido mediante visualización y análisis cuantitativo.

Su fundamento científico se basa en la relación entre frecuencia, período y tono percibido, utilizando señales sonoras controladas y procesamiento digital para representar el fenómeno.

La aplicación permite acercar conceptos abstractos a una experiencia observable, favoreciendo la interpretación de datos y el razonamiento científico.
