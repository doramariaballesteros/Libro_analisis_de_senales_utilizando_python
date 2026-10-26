# 📡 Transformada de Fourier de señales aperiódicas

## 1. Transformada de Fourier y Transformada Inversa de Fourier

A diferencia de las señales periódicas, cuyo espectro está formado por impulsos en frecuencias armónicas, las **señales aperiódicas de energía finita** presentan, en general, un espectro no impulsivo. La Transformada de Fourier (TF) permite representar estas señales en el dominio de la frecuencia.

La TF puede expresarse en función de la frecuencia angular $\omega$ (rad/s) o de la frecuencia $f$ (Hz):

$$
X(j\omega)=\int_{-\infty}^{\infty}x(t)e^{-j\omega t}dt
$$

$$
X(jf)=\int_{-\infty}^{\infty}x(t)e^{-j2\pi ft}dt
$$

La Transformada Inversa de Fourier (ITF) permite recuperar la señal temporal:

$$
x(t)=\frac{1}{2\pi}\int_{-\infty}^{\infty}X(j\omega)e^{j\omega t}d\omega
$$

$$
x(t)=\int_{-\infty}^{\infty}X(jf)e^{j2\pi ft}df
$$

Como $\omega=2\pi f$, se cumple:

$$
\boxed{X(jf)=X(j\omega)\big|_{\omega=2\pi f}}
$$

**Para un espectro representado por una función ordinaria, su amplitud no cambia entre $X(j\omega)$ y $X(jf)$; únicamente cambia la escala del eje horizontal.**

![Transformada de Fourier y Transformada Inversa de Fourier](TF_and_ITF.png)

---

## 2. Espectros continuos e impulsivos

Es importante distinguir entre los espectros descritos mediante funciones ordinarias y aquellos que contienen **impulsos de Dirac**.

- **Señales aperiódicas de energía finita:** su TF no contiene impulsos de Dirac y, en los ejemplos habituales, se representa mediante una curva continua.
- **Señales periódicas:** su TF está formada por impulsos de Dirac ubicados en las frecuencias armónicas.
- **Señal constante o nivel DC:** su TF contiene un único impulso de Dirac en frecuencia cero. Aunque no posee período fundamental, también puede entenderse como una señal periódica con cualquier período positivo.

Para las componentes de tipo impulso, el escalamiento de la delta de Dirac introduce un factor $2\pi$ entre los coeficientes expresados en rad/s y en Hz. Esta diferencia **no** se aplica a la amplitud de las partes espectrales representadas mediante funciones ordinarias.

![Comparación de espectros continuos e impulsivos](Espectros_aperiodica_periodica.png)

---

## 3. Transformada de Fourier de señales exponenciales reales

### Ejemplo 34. Exponencial real unilateral

Consideremos la señal:

$$
x(t)=e^{-at}u(t),\qquad a>0
$$

Su Transformada de Fourier en frecuencia angular es:

$$
X(j\omega)=\int_0^{\infty}e^{-at}e^{-j\omega t}\,dt
=\int_0^{\infty}e^{-(a+j\omega)t}\,dt
$$

$$
X(j\omega)=\left[\frac{e^{-(a+j\omega)t}}{-(a+j\omega)}\right]_0^{\infty}
=\boxed{\frac{1}{a+j\omega}}
$$

La magnitud del espectro es:

$$
\boxed{|X(j\omega)|=\frac{1}{\sqrt{a^2+\omega^2}}}
$$

Dos valores permiten caracterizar su comportamiento:

$$
|X(j0)|=\frac{1}{a},\qquad
|X(ja)|=\frac{1}{a\sqrt{2}}
$$

El espectro de magnitud es par y alcanza su valor máximo en $\omega=0$. La TF, sin embargo, es compleja en general.

### Ejemplo 35. Exponencial real bilateral

Consideremos ahora la señal:

$$
x(t)=e^{-a|t|},\qquad a>0
$$

Equivalentemente:

$$
x(t)=\begin{cases}
e^{at},&t<0\\
e^{-at},&t\geq0
\end{cases}
$$

Su TF se obtiene separando las integrales para tiempos negativos y positivos:

$$
X(j\omega)=\int_{-\infty}^{0}e^{at}e^{-j\omega t}\,dt
+\int_0^{\infty}e^{-at}e^{-j\omega t}\,dt
$$

$$
X(j\omega)=\frac{1}{a-j\omega}+\frac{1}{a+j\omega}
=\boxed{\frac{2a}{a^2+\omega^2}}
$$

En este caso, el espectro es **real, par y no negativo**, por lo que:

$$
\boxed{|X(j\omega)|=\frac{2a}{a^2+\omega^2}}
$$

Sus valores característicos son:

$$
|X(j0)|=\frac{2}{a},\qquad
|X(ja)|=\frac{1}{a}
$$

La siguiente figura compara las señales temporales y los espectros de magnitud de ambas exponenciales.

![Transformada de Fourier de señales exponenciales unilaterales y bilaterales](TF_exponencial_unilateral_bilateral.png)

---

## 4. Transformada de Fourier del impulso unitario y de una señal constante

### Ejemplo 36. Impulso unitario en tiempo continuo

Sea:

$$
x(t)=\delta(t)
$$

Aplicando la propiedad de muestreo del impulso de Dirac:

$$
X(j\omega)=\int_{-\infty}^{\infty}\delta(t)e^{-j\omega t}\,dt=\boxed{1}
$$

De igual manera, en Hz:

$$
\boxed{X(jf)=1}
$$

El impulso en el tiempo tiene un **espectro constante e igual a 1** en ambas representaciones de frecuencia.

### Ejemplo 37. Señal constante en el tiempo (nivel DC)

Sea:

$$
x(t)=1
$$

Su Transformada de Fourier en frecuencia angular es:

$$
\boxed{X(j\omega)=2\pi\delta(\omega)}
$$

En frecuencia ordinaria:

$$
\boxed{X(jf)=\delta(f)}
$$

El espectro está formado por **un único impulso en frecuencia cero**. Los coeficientes que acompañan al impulso son $2\pi$ en rad/s y $1$ en Hz, debido a la propiedad de escalamiento de la delta de Dirac. Estos coeficientes representan el peso del impulso, no una altura finita de la función delta.

La figura muestra las dos señales temporales y sus espectros expresados tanto en Hz como en rad/s.

![Transformada de Fourier del impulso unitario y de la señal DC](TF_impulso_DC.png)

---

## 5. Transformada de Fourier de una señal cuadrada aperiódica

Consideremos una señal cuadrada aperiódica, de amplitud unitaria y duración finita. A diferencia de la señal cuadrada periódica, cuyo espectro está formado por infinitos impulsos de Dirac, la señal cuadrada aperiódica tiene un **espectro continuo de forma sinc**.

### Ejemplo 38. TF de la señal cuadrada aperiódica

Sea la señal:

$$
x(t)=
\begin{cases}
1, & |t|<T_1\\
0, & \text{en otro caso}
\end{cases}
$$

Donde $2T_1$ corresponde a la duración total de la señal (tiempo en alto), centrada en $t=0$.

### Cálculo de la Transformada de Fourier

Partimos de la definición:

$$
X(j\omega)=\int_{-\infty}^{\infty}x(t)e^{-j\omega t}\,dt
$$

Como la señal solamente es diferente de cero en el intervalo $-T_1<t<T_1$, tenemos:

$$
X(j\omega)=\int_{-T_1}^{T_1}e^{-j\omega t}\,dt
$$

Resolviendo la integral:

$$
X(j\omega)=\left[\frac{e^{-j\omega t}}{-j\omega}\right]_{-T_1}^{T_1}
$$

$$
X(j\omega)=\frac{e^{-j\omega T_1}-e^{j\omega T_1}}{-j\omega}
$$

Aplicando la identidad de Euler:

$$
e^{j\theta}-e^{-j\theta}=2j\operatorname{sen}(\theta)
$$

Obtenemos:

$$
X(j\omega)=\frac{2\operatorname{sen}(\omega T_1)}{\omega}
$$

Por tanto:

$$
\boxed{X(j\omega)=2T_1\frac{\operatorname{sen}(\omega T_1)}{\omega T_1}}
$$

Esta expresión corresponde a una función de tipo sinc.

### Representación temporal y espectral

La siguiente figura presenta la señal cuadrada aperiódica en el dominio temporal y la magnitud de su Transformada de Fourier.

![Señal cuadrada aperiódica y su Transformada de Fourier](TF_cuadrada_aperiodica.png)

### Análisis del espectro

A partir de la expresión matemática y de la representación gráfica, podemos identificar las siguientes características:

1. **Espectro continuo:** a diferencia de la señal cuadrada periódica, su espectro no está formado por impulsos de Dirac, sino por una función continua de tipo sinc.

2. **Máximo en frecuencia cero:** el valor máximo de la magnitud del espectro se obtiene en $\omega=0$. Aplicando el límite:

   $$
   X(j0)=\lim_{\omega\to0}\frac{2\operatorname{sen}(\omega T_1)}{\omega}=2T_1
   $$

3. **Ceros del espectro:** ocurren cuando el argumento de la función seno corresponde a múltiplos enteros de $\pi$, diferentes de cero:

   $$
   \omega=\pm\frac{\pi}{T_1},\ \pm\frac{2\pi}{T_1},\ \pm\frac{3\pi}{T_1},\ldots
   $$

4. **Relación entre duración y ancho espectral:** a mayor duración de la señal en el tiempo, el espectro se hace más angosto. Por el contrario, a menor duración, el espectro se ensancha.

5. **Concentración de energía:** la mayor concentración de energía se encuentra alrededor de $\omega=0$, en el lóbulo principal de la función sinc.

### Transformada de Fourier en Hz

Si expresamos el espectro en función de la frecuencia $f$, utilizando $\omega=2\pi f$, obtenemos:

$$
X(jf)=\frac{2\operatorname{sen}(2\pi fT_1)}{2\pi f}
$$

Simplificando:

$$
\boxed{X(jf)=2T_1\frac{\operatorname{sen}(2\pi fT_1)}{2\pi fT_1}}
$$

**La amplitud del espectro no cambia entre $X(j\omega)$ y $X(jf)$; únicamente cambia la escala del eje horizontal.**

En ambas representaciones, el máximo del espectro es $2T_1$.
---


## 🎯 Conclusiones

- La TF y la ITF pueden formularse utilizando frecuencia angular $\omega$ (rad/s) o frecuencia ordinaria $f$ (Hz).
- En los **espectros ordinarios**, la relación $\omega=2\pi f$ modifica la escala horizontal, **no la amplitud**.
- La exponencial unilateral $e^{-at}u(t)$ tiene $X(j\omega)=1/(a+j\omega)$ y magnitud $1/\sqrt{a^2+\omega^2}$.
- La exponencial bilateral $e^{-a|t|}$ tiene $X(j\omega)=2a/(a^2+\omega^2)$, un espectro real y par.
- El impulso unitario $\delta(t)$ tiene espectro constante: $X(j\omega)=X(jf)=1$.
- La señal constante $x(t)=1$ tiene espectro impulsivo: $X(j\omega)=2\pi\delta(\omega)$ y $X(jf)=\delta(f)$.
- **En los espectros impulsivos cambian los coeficientes de los impulsos por un factor $2\pi$** al pasar de Hz a rad/s.

**La diferencia esencial no es únicamente si la señal es periódica o aperiódica, sino si su espectro se representa mediante una función ordinaria o contiene impulsos de Dirac.**
