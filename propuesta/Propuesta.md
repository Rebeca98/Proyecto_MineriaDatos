% Optimizando el desempeño académico
% Equipo JJAR (Julieta, José, Alonso, Rebe)

# Optimizando calificaciones para maximizar la nota final
## O: ¿Por fin voy a pasar eco 2?

# Planteamiento
Queremos optimizar el promedio de un semestre dado que ya pasaron bajas

. . .

😔👌

## Función de calificación

Queremos encontrar la mayor calificación final posible que podríamos obtener
dado que ya conocemos la calificación del 'primer parcial'.

Para no caer en un problema lineal consideramos funciones de
calificación no-lineales.

. . .

Por ejemplo: Peso de parciales depende de si es el más alto o bajo

$$
C(p, y) := \frac{1}{5} p_{\text{lo}} + \frac{2}{5} \left(
\sum_{i} p_{i} \right)
+ \frac{2}{5} y
$$

----

![Calificación final en función de parciales y final](figs/cs_simple.png){.stretch}


# ¿Qué tan probable es tener $x \text{ }$  de calificación Final?

. . .

## Asumiendo que las calificaciones se distribuyen gamma

![Distribución gamma con curvas de nivel en el piso](figs/gamma_3d.png){.stretch}

## Juntando ambas ideas

![](figs/cs_compuesto.png){.stretch}

----

![](figs/probab.png){.stretch}

# ¿Cuál es nuestra función a optimizar?
## Función score

Calcula las posibles calificaciones finales dados los datos,
criterios de calificación y calificaciones dadas, ponderando por la probabilidad de obtener dicha calificación.

Variables de optimización: $x, y$

-----

Concretamente:

Sean $X, Y \sim \text{Ga}(\alpha_i, \beta_i)$ v.a's independientes.

. . .

$X$ representa parcial restante, $Y$ examen final.

$$
\text{Score}(x,y) := C(p, y) * f_{X, Y} (x, y)
$$

. . .

Donde $C(p, y)$ es la función de calificaciones y $f_{X, Y}$ la f.d.p
conjunta de $X, Y$.

## ¿Cómo se ve score?

![Gráfica de score](figs/cono.png){.stretch}

-----

![Curvas de nivel de score](figs/cs-score.png){.stretch}

-----

Obtenemos la máxima posible calificación $×$ probabilidad de sacarla.

# ¿Cómo optimizamos?

Algoritmo de Región de Confianza

- método de Dogleg

----

![Ejemplo de test con Rosen](figs/dogleg-rosen.png){.stretch}

# Resultados

![Region de Confianza](figs/final.png){.stretch}

----

![Region de Confianza](figs/final-zoom.png){.stretch}

## Solución en (6.10, 7.38)

# Problemas de convergencia

## No converge en todos lados

. . .

![Mandelbrot](figs/Mandel.png){.stretch}

-----

![Primer intento](figs/mandel-0.2.png){.stretch}

-----

![Figura estilo mandelbrot](figs/reg-conv.png){.stretch}

# Áreas de oportunidad

::: incremental
- El modelo propuesto no es muy bueno
- Posible problema de escalamiento (pg.26)
- numdifftools
:::
