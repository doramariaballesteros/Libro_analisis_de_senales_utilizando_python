# 🎧 Proyecto de Análisis de Señales
## 🔐 Ocultamiento y recuperación de mensajes mediante permutación espectral

### 🎯 Objetivo

Desarrollar un procedimiento de **codificación espectral (*Imitation*)** que permita ocultar cinco mensajes de audio mediante la reorganización de sus coeficientes de Fourier. Posteriormente, recuperar los mensajes con el procedimiento **Reverse**, proporcionado por la profesora, y evaluar cuantitativamente la calidad de las señales reconstruidas.

El procedimiento debe trabajar con **coeficientes espectrales complejos completos** (parte real e imaginaria), no únicamente con sus magnitudes. El audio codificado puede percibirse como ruido, aunque debe conservar la información necesaria para recuperar el mensaje secreto.

## 🧩 Parte I. Imitation — Desarrollo del estudiante

### 🎙️ 1. Carga y exploración temporal

Cargar el audio de referencia (**Target**) y uno de los audios secretos (**Secret**). Verificar que ambos tengan la misma frecuencia de muestreo y cantidad de muestras. Representar las dos señales en el dominio temporal y escucharlas.

![Señales originales en el dominio temporal](Grafica_tiempo.png)

**🔎 Analiza:** ¿cómo difieren las señales en amplitud, pausas y distribución temporal de la actividad?

### 📊 2. Análisis espectral

Calcular los coeficientes espectrales de ambas señales mediante **`rfft`** y representar sus espectros de magnitud en función de la frecuencia (Hz).

![Espectros de magnitud de Target y Secret](Grafica_espectro.png)

**🔎 Analiza:** identifica las regiones de mayor magnitud y compara la ubicación de los picos principales. Recuerda que cada coeficiente de `rfft` contiene información de magnitud y fase.

### 🔀 3. Reorganización de coeficientes complejos

Diseñar una permutación que reubique los coeficientes complejos del **Secret** según el orden de magnitudes de los coeficientes del **Target**. Para ello:

1. Identifica las posiciones de los coeficientes de ambas señales ordenados por magnitud.
2. Establece una correspondencia entre posiciones de igual rango.
3. Reorganiza **los coeficientes completos** del secreto, conservando juntas sus partes real e imaginaria.
4. Mantén sin permutar el coeficiente de **DC** y, si el número de muestras es par, el coeficiente de **Nyquist**.
5. Construye una **clave de permutación** que permita invertir el procedimiento.

![Comparación del espectro original y el espectro reorganizado](Grafica_espectro_ordenado.png)


### 🔀 Permutación espectral y creación de la clave

```python
# 1. Ordenar las posiciones según la magnitud
I1 = argsort(abs(S))
I2 = argsort(abs(T))

# 2. Crear la clave de permutación
K[I2] = I1

# 3. Reorganizar los coeficientes complejos
E = S[K]
```

**Donde:**

- **`S`**: coeficientes espectrales complejos del secreto.
- **`T`**: coeficientes espectrales complejos del target.
- **`I1`**: posiciones de los coeficientes del secreto, ordenadas de menor a mayor magnitud.
- **`I2`**: posiciones de los coeficientes del target, ordenadas de menor a mayor magnitud.
- **`K`**: clave que relaciona las posiciones originales del secreto con las posiciones del espectro codificado.
- **`E`**: espectro codificado, obtenido al reorganizar los coeficientes complejos del secreto.

> 📌 **Importante:** el ordenamiento y la permutación se aplican únicamente a los coeficientes que pueden intercambiarse. Los coeficientes DC y Nyquist (cuando existe) deben permanecer fijos. La permutación conserva tanto la parte real como la imaginaria de cada coeficiente.


**🔎 Analiza:** explica por qué el espectro reorganizado presenta sus picos en posiciones semejantes a las del Target, aunque conserva las magnitudes de los coeficientes originales del Secret.

### 🔊 4. Generación del audio codificado

Aplicar **`irfft`** al espectro complejo reorganizado para obtener la señal **Encoded**. Representarla en el dominio temporal y escucharla. El resultado puede sonar como ruido o como un mensaje ininteligible.

Guardar el archivo `encoded.wav` y la clave correspondiente `FFT_key.csv`. La convención de la clave debe ser compatible con el código **Reverse** suministrado.

### 🎵 5. Repetición con cinco secretos

Repetir el procedimiento utilizando **los cinco audios secretos suministrados** y el mismo Target. Generar **cinco audios codificados y cinco claves**, evitando sobrescribir los resultados de cada caso. Identificar claramente los archivos mediante nombres diferenciados.

## 🔓 Parte II. Reverse — Código suministrado

Utilizar el procedimiento **Reverse** proporcionado por la profesora para recuperar cada mensaje a partir de su audio codificado y de la clave correspondiente.

Verificar mediante escucha que los **cinco mensajes secretos recuperados** sean inteligibles. Conservar el código utilizado y los cinco archivos de audio recuperados.

## 📏 Parte III. Evaluación de la calidad

Comparar cada audio secreto original, \(x[n]\), con su reconstrucción, \(\hat{x}[n]\), mediante **dos métricas**:

**Relación señal a ruido de reconstrucción (SNR):**

\[
\mathrm{SNR}=10\log_{10}\left(\frac{\sum_n x[n]^2}{\sum_n (x[n]-\hat{x}[n])^2}\right)
\]

**Coeficiente de correlación de Pearson:**

\[
\rho=\frac{\operatorname{cov}(x,\hat{x})}{\sigma_x\sigma_{\hat{x}}}
\]

Calcular ambas métricas para los cinco mensajes y presentar los resultados en una tabla:

| Mensaje secreto | SNR (dB) | Correlación de Pearson |
|---|---:|---:|
| Secret 1 | | |
| Secret 2 | | |
| Secret 3 | | |
| Secret 4 | | |
| Secret 5 | | |

**🔎 Análisis requerido:** identifica qué mensaje obtuvo la mejor calidad de recuperación, determina si los cinco resultados son similares o si alguno presenta una diferencia considerable y propón explicaciones. Interpreta **ambas métricas**, no solo sus valores máximos. Explica por qué una permutación matemáticamente reversible puede presentar pequeños errores después de guardar y volver a cargar un audio digital.

## 🐙 Entrega en GitHub

Cada grupo deberá publicar el trabajo en un repositorio de la **cuenta personal de GitHub** de uno de sus integrantes. El repositorio deberá contener:

- Código desarrollado de **Imitation**, cinco audios `encoded` y sus cinco claves.
- Código **Reverse** proporcionado y cinco audios secretos recuperados.
- Código utilizado para calcular **SNR** y **correlación de Pearson**.
- Tabla de resultados y análisis comparativo en el `README.md`.

La entrega se formaliza mediante el enlace al repositorio con todos los archivos solicitados.

## 📋 Evaluación y condiciones

**🏅 Calidad:** la calificación dependerá del funcionamiento de los procedimientos, la calidad de los cinco mensajes recuperados y el análisis de resultados.

**⏱️ Oportunidad:** la **primera entrega válida** establecerá la fecha de referencia. A partir de ella, se descontarán **0,2 puntos de la nota por cada día transcurrido** hasta la entrega de cada grupo.

**🛡️ Originalidad:** se reconocerán similitudes inevitables por tratarse de un mismo problema. No obstante, coincidencias significativas en nombres de variables no indicados en la guía, organización del código, comentarios y decisiones particulares de implementación podrán ser indicios de copia. Si se confirma copia entre entregas, se descartará el código presentado posteriormente.

**🗣️ Sustentación:** cada grupo deberá sustentar presencialmente, **en la oficina de la profesora**, el código desarrollado y sus resultados.

**📅 Fecha máxima de entrega: 19 de noviembre de 2026.**
