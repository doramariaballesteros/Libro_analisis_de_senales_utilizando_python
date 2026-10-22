# 📘 Análisis de Señales utilizando Python

> **Repositorio oficial del libro**  
> **Dora María Ballesteros**  
> Primera edición, 2026  
> ISBN: 978-1-957395-65-4
>
> 🔗 **[Consultar el libro en Editorial REDIPE](https://editorial.redipe.org/index.php/1/catalog/book/250)**

### 🎬 Presentación de la autora

Conoce a **Dora María Ballesteros**, autora del libro *Análisis de Señales utilizando Python*, y su trayectoria académica e investigativa.

[![Presentación de Dora María Ballesteros](https://img.youtube.com/vi/hHAS6AaVm5Q/hqdefault.jpg)](https://youtu.be/hHAS6AaVm5Q)

▶️ **[Ver presentación en YouTube](https://youtu.be/hHAS6AaVm5Q)**

---

## 📖 Sobre este repositorio

Este repositorio contiene los **recursos educativos complementarios** del libro **Análisis de Señales utilizando Python** (Editorial REDIPE, 2026).

El libro integra los fundamentos teóricos del análisis de señales con ejemplos y casos de estudio desarrollados en **Python**, utilizando **Jupyter Notebooks** para facilitar la comprensión, visualización y experimentación con señales en los dominios del tiempo y de la frecuencia.

Además de los notebooks, el repositorio incluye **documentos explicativos, material gráfico y ejemplos desarrollados paso a paso**, que permiten profundizar en los conceptos y procedimientos matemáticos estudiados en el libro.

Los recursos están organizados por capítulos y tienen como propósito facilitar un aprendizaje activo, en el que el lector pueda consultar las explicaciones, ejecutar los códigos, modificar los parámetros y analizar los resultados obtenidos.

---


## 📚 Organización del repositorio

| Cap. | Tema | Recursos disponibles |
|:---:|---|---|
| **1** | 📈 **Fundamentos de Señales Análogas y Señales Discretas** | [📒 Notebook](Capitulo1/Python_Capitulo1.ipynb) |
| **2** | ⚙️ **Sistemas LTI (Lineales e Invariantes en el Tiempo)** | [📒 Notebook](Capitulo2/Python_Capitulo2.ipynb) · [📄 Convolución continua](Capitulo2/Convolucion_continua.pdf) · [Propiedades de los Sistemas LTI](Capitulo2/Propiedades_Sistemas_LTI.pdf) |
| **3** | 🎼 **Señal Exponencial Compleja y Series de Fourier** | [📒 Notebook](Capitulo3/Python_Capitulo3.ipynb) |
| **4** | 📡 **Transformada de Fourier de Señales Periódicas y Aperiódicas** | [📒 Notebook principal](Capitulo4/Python_Capitulo4.ipynb) · [📒 Suma de cosenoidales](Capitulo4/Python_TF_suma_cosenoidales.ipynb) · [📄 Transformada de Fourier de señales periódicas](Capitulo4/Texto_TF_periodicas.md) |

---

# 📈 Capítulo 1. Fundamentos de Señales Análogas y Señales Discretas

📒 **Notebook:** [Python_Capitulo1.ipynb](Capitulo1/Python_Capitulo1.ipynb)

### 🎯 Objetivo

Comprender los conceptos fundamentales de las señales en tiempo continuo y tiempo discreto, así como las principales transformaciones temporales utilizadas en el análisis de señales mediante ejemplos desarrollados en Python.

### 📑 Contenido del notebook

- Ejemplo 1. Señal senoidal.
- Ejemplo 2. Señales discretas con índice entero.
- Ejemplo 3. Desplazamiento en tiempo continuo.
- Ejemplo 4. Desplazamiento en tiempo discreto.
- Ejemplo 5. Inversión temporal de señales de soporte finito en tiempo continuo.
- Ejemplo 6. Inversión temporal de señales de soporte finito en tiempo continuo y discreto.
- Ejemplo 7. Compresión de una señal en tiempo continuo.
- Ejemplo 8. Dilatación de una señal en tiempo continuo.
- Ejemplo 9. Compresión de una señal discreta.
- Ejemplo 10. Dilatación de una señal discreta (α = 1/q).
- Ejemplo 11. Dilatación de una señal discreta (α = p/q).
- Ejemplo 12. Combinación de transformaciones en una señal discreta.
- Ejemplo 17. Sistema invariante.

---

# 🔄 Capítulo 2. Sistemas LTI (Lineales e Invariantes en el Tiempo)

📒 **Notebook:** [Python_Capitulo2.ipynb](Capitulo2/Python_Capitulo2.ipynb)

### 🎯 Objetivo

Analizar el comportamiento de los sistemas lineales e invariantes en el tiempo mediante la representación de señales utilizando impulsos y el desarrollo de la operación de convolución.

### 📑 Contenido del notebook

- Señal impulso en tiempo discreto.
- Ejemplo 18. Representación de una señal discreta a partir de impulsos desplazados.
- Ejemplo 19. Convolución de señales discretas mediante la propiedad distributiva.

### 📂 Material complementario

- 📄 **[Convolución continua](Capitulo2/Convolucion_continua.pdf):** Documento de apoyo para el estudio de la operación de convolución de señales en tiempo continuo.
- 📄 **[Propiedades de los Sistemas LTI](Capitulo2/Propiedades_Sistemas_LTI.pdf):** Material complementario para el estudio de las propiedades de los sistemas lineales e invariantes en el tiempo.

Documento de apoyo para el estudio de la operación de convolución de señales en tiempo continuo.


---

# 🎼 Capítulo 3. Señal Exponencial Compleja y Series de Fourier

📒 **Notebook:** [Python_Capitulo3.ipynb](Capitulo3/Python_Capitulo3.ipynb)

### 🎯 Objetivo

Estudiar la representación de señales periódicas mediante exponenciales complejas y Series de Fourier, interpretando su contenido espectral a través de ejemplos desarrollados en Python.

### 📑 Contenido del notebook

- Ejemplo 21. Manipulación de exponenciales complejas.
- Ejemplo 24. Serie de Fourier de una señal cuadrada periódica.
- Ejemplo 25. Serie de Fourier de un tren de impulsos.
- Ejemplo 26. Fenómeno de Gibbs en una señal cuadrada.
- Ejemplo 29. Cálculo de los coeficientes de la Serie de Fourier de una señal periódica formada por componentes senoidales armónicamente relacionados.
- Ejemplo 30. Cálculo de los coeficientes de la Serie de Fourier de una señal periódica expresada como producto de cosenos.

---


# 📡 Capítulo 4. Transformada de Fourier de Señales Periódicas y Aperiódicas

### 🎯 Objetivo

Aplicar la Transformada de Fourier para analizar el contenido espectral de señales periódicas y aperiódicas, utilizando herramientas computacionales desarrolladas en Python.

### 📑 Contenido de los notebooks

📒 **[Python_Capitulo4.ipynb](Capitulo4/Python_Capitulo4.ipynb)**

- Ejemplo 32. Transformada de Fourier de una suma de señales cosenoidales.
- Ejemplo 43. Análisis espectral de una señal de voz con ruido externo tipo tono.

📒 **[Python_TF_suma_cosenoidales.ipynb](Capitulo4/Python_TF_suma_cosenoidales.ipynb)**

Representación de una señal periódica compuesta por tres señales cosenoidales:

1. Señal en el dominio del tiempo.
2. Coeficientes de la Serie de Fourier.
3. Espectro $X(jf)$ en frecuencia (Hz).
4. Espectro $X(j\omega)$ en frecuencia angular (rad/s).

### 📂 Material complementario

**📄 [Transformada de Fourier de señales periódicas](Capitulo4/Texto_TF_periodicas.md)**

Explicación gráfica y matemática del procedimiento para obtener la Transformada de Fourier de una señal periódica a partir de los coeficientes de su Serie de Fourier.

El material desarrolla:

1. La relación entre la Serie de Fourier y la Transformada de Fourier de señales periódicas.
2. El cálculo de la frecuencia fundamental y la identificación de los armónicos.
3. La obtención de los coeficientes mediante las propiedades de multiplicación y linealidad de la Serie de Fourier.
4. La construcción de los espectros en frecuencia (Hz) y frecuencia angular (rad/s).

**🖼️ Recursos gráficos**

- [Transformada de Fourier de señales periódicas](Capitulo4/Imagen_TF_señales_periodicas.png)
- [Coeficientes de la Serie de Fourier mediante propiedades](Capitulo4/Imagen_Ejemplo_SF.png)
- [Espectro de una señal periódica a partir de sus coeficientes](Capitulo4/Imagen_Ejemplo_TF_periodica.png)

---

# 🎯 Objetivos de aprendizaje

A través de los recursos de este repositorio, el lector podrá:

- 📈 Representar y visualizar señales en tiempo continuo y tiempo discreto.
- 🔄 Aplicar operaciones sobre señales, como desplazamiento, inversión, compresión y dilatación.
- ⚙️ Analizar sistemas lineales e invariantes en el tiempo mediante la convolución y la respuesta al impulso.
- 🎼 Comprender la representación armónica de señales mediante la Serie de Fourier.
- 📡 Relacionar los coeficientes de la Serie de Fourier con el espectro de una señal periódica.
- 💻 Implementar algoritmos de análisis de señales utilizando Python.
- 🔬 Experimentar con ejemplos reproducibles y fortalecer la interpretación de los resultados.

---

# 💻 Requisitos

Los notebooks fueron desarrollados en **Python**, utilizando bibliotecas empleadas en análisis y procesamiento de señales, entre ellas:

- NumPy
- SciPy
- Matplotlib
- Librosa
- SoundFile
- IPython.display

Los notebooks pueden ejecutarse en:

- Jupyter Notebook
- JupyterLab
- Google Colab

Los documentos Markdown, PDF y las imágenes pueden consultarse directamente desde GitHub, sin necesidad de ejecutar código.

---

# 📖 Referencia del libro

**Ballesteros, D. M. (2026).**  
*Análisis de Señales utilizando Python.*  
Editorial REDIPE.  
ISBN: **978-1-957395-65-4**

🔗 [Consultar publicación](https://editorial.redipe.org/index.php/1/catalog/book/250)

---

# 👩‍🏫 Sobre la autora

**Dora María Ballesteros** es profesora e investigadora de la **Universidad Militar Nueva Granada (Colombia)**. Su trabajo se centra en Ciencia de Datos, Inteligencia Artificial, Procesamiento Digital de Señales y Aprendizaje Profundo.

Es autora de diversos libros y artículos científicos en estas áreas y promueve el desarrollo de recursos educativos y herramientas de software de código abierto para la comunidad académica.

---

# 📄 Licencia

Este repositorio se distribuye con fines académicos y educativos. Consulte el archivo **LICENSE**, si está disponible, para conocer los términos de uso.

---

# 📧 Contacto

**Dora María Ballesteros**  
Profesora e Investigadora  
Universidad Militar Nueva Granada

📧 **dora.ballesteros@unimilitar.edu.co**
📍 Bogotá, Colombia
