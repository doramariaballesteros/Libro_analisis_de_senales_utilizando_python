# 📘 Análisis de Señales utilizando Python

> **Repositorio oficial del libro**
>
> **Análisis de Señales Utilizando Python**  
> **Dora María Ballesteros**  
> **Editorial Redipe, 2026**

---

## 📖 Sobre este repositorio

Este repositorio contiene el material práctico del libro **Análisis de Señales utilizando Python** (Editorial Redipe, 2026).

El libro integra los fundamentos teóricos del análisis de señales con ejemplos y casos de estudio completamente reproducibles desarrollados en **Python** mediante **Jupyter Notebooks**, permitiendo al lector comprender, visualizar y experimentar con las principales técnicas de análisis en los dominios del tiempo y de la frecuencia.

Los notebooks acompañan cada uno de los capítulos prácticos del libro e incluyen el desarrollo paso a paso de los algoritmos, la visualización de resultados y el análisis e interpretación de señales reales y sintéticas.

El objetivo del repositorio es facilitar un aprendizaje activo, donde el lector pueda ejecutar, modificar y extender cada uno de los ejemplos presentados en el libro, fortaleciendo sus competencias en procesamiento y análisis de señales utilizando Python.

---

# 📚 Contenido del libro

| Cap. | Tema | Descripción | 📒 Notebook |
|:---:|------|-------------|:----------:|
| **1** | 📈 **Fundamentos de Señales Análogas y Señales Discretas** | Introducción a los conceptos fundamentales de las señales continuas y discretas, operaciones básicas, representación gráfica y propiedades esenciales para el análisis de sistemas. | [Abrir](Capitulo1.ipynb) |
| **2** | ⚙️ **Sistemas LTI (Lineales e Invariantes en el Tiempo)** | Estudio de los sistemas lineales e invariantes en el tiempo, respuesta al impulso, convolución y propiedades fundamentales para el análisis y procesamiento de señales. | [Abrir](Capitulo2.ipynb) |
| **3** | 🎼 **Señal Exponencial Compleja y Series de Fourier** | Representación de señales mediante exponenciales complejas y Series de Fourier para el análisis de señales periódicas en el dominio de la frecuencia. | [Abrir](Capitulo3.ipynb) |
| **4** | 📡 **Transformada de Fourier de Señales Periódicas y Aperiódicas** | Desarrollo de la Transformada de Fourier para el análisis espectral de señales periódicas y aperiódicas, con aplicaciones prácticas implementadas en Python. | [Abrir](Capitulo4.ipynb) |

---

# 📈 Capítulo 1. Fundamentos de Señales Análogas y Señales Discretas

📒 **Notebook:**  
[Capitulo1.ipynb](Capitulo1.ipynb)

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

📒 **Notebook:**  
[Capitulo2.ipynb](Capitulo2.ipynb)

### 🎯 Objetivo

Analizar el comportamiento de los sistemas lineales e invariantes en el tiempo mediante la representación de señales utilizando impulsos y el desarrollo de la operación de convolución.

### 📑 Contenido del notebook

- Señal impulso en tiempo discreto.
- Ejemplo 18. Representación de una señal discreta a partir de impulsos desplazados.
- Ejemplo 19. Convolución de señales discretas mediante la propiedad distributiva.

---

# 🎼 Capítulo 3. Señal Exponencial Compleja y Series de Fourier

📒 **Notebook:**  
[Capitulo3.ipynb](Capitulo3.ipynb)

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

📒 **Notebook:**  
[Capitulo4.ipynb](Capitulo4.ipynb)

### 🎯 Objetivo

Aplicar la Transformada de Fourier para analizar el contenido espectral de señales periódicas y aperiódicas, utilizando herramientas computacionales desarrolladas en Python.

### 📑 Contenido del notebook

- Ejemplo 32. Transformada de Fourier de una suma de señales cosenoidales.
- Ejemplo 43. Análisis espectral de una señal de voz con ruido externo tipo tono.
---

# 🎯 Objetivos de aprendizaje

A través de los notebooks el lector aprenderá a:

- 📈 Representar y visualizar señales en tiempo continuo y tiempo discreto.
- 🔄 Aplicar operaciones básicas sobre señales, como desplazamiento, inversión, compresión y dilatación.
- ⚙️ Analizar sistemas lineales e invariantes en el tiempo (LTI) mediante la convolución y la respuesta al impulso.
- 🎼 Comprender la representación armónica de señales mediante la Serie de Fourier.
- 📡 Analizar el contenido espectral de señales periódicas y aperiódicas mediante la Transformada de Fourier.
- 💻 Implementar algoritmos de análisis de señales utilizando lenguaje Python.
- 🔬 Experimentar con ejemplos completamente reproducibles para fortalecer la comprensión de los conceptos teóricos.

---

# 💻 Requisitos

Los notebooks fueron desarrollados en **Python** utilizando bibliotecas ampliamente empleadas en el análisis y procesamiento digital de señales, entre ellas:

- NumPy
- SciPy
- Matplotlib
- Librosa
- SoundFile
- IPython.display

Los notebooks pueden ejecutarse en:

- Jupyter Notebook
- JupyterLab
- Google Colab (100% compatible)

---

# 📖 Referencia del libro

**Ballesteros, D. M. (2026).**  
*Análisis de Señales utilizando Python.*  
Editorial Redipe.  
ISBN: **978-1-957395-65-4**

---

# 👩‍🏫 Sobre la autora

**Dora María Ballesteros** es profesora e investigadora de la **Universidad Militar Nueva Granada (Colombia)**. Su trabajo se centra en Ciencia de Datos, Inteligencia Artificial, Procesamiento Digital de Señales y Aprendizaje Profundo. Es autora de diversos libros y artículos científicos en Ciencia de Datos, Inteligencia Artificial y Procesamiento Digital de Señales, promoviendo el desarrollo de recursos educativos y herramientas de software de código abierto para la comunidad académica.

---

# 📄 Licencia

Este repositorio se distribuye con fines académicos y educativos. Consulte el archivo **LICENSE** para conocer los términos de uso.


## 📧 Contacto

**Prof. Dora María Ballesteros**  
Universidad Militar Nueva Granada

📧 dora.ballesteros@unimilitar.edu.co

Bogotá, Colombia
