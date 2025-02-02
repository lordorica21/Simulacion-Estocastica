# Generadores de números pseudoaleatorios congruenciales
## Algoritmo de la división
Sean $m$ un entero positivo y $a$ un entero cualquiera.

Por el algoritmo de la división sabemos que existen enteros únicos $q$ y $r$ tales que:

1. $a = mq+r$
2. $0\leq r<m$

El entero $q$ lo llamamos el cociente y a $r$ el resto (o residuo) de la división de $a$ por $m$.

<u>Ejemplo</u>
$$
2\equiv 5\ \text{mod}\ 3\\
8\equiv 78\ \text{mod}\ 14\\
92\equiv 278\ \text{mod}\ 93\\
127\equiv -26137\ \text{mod}\ 134
$$

Si $x$ y $y$ tienen el mismo residuo módulo $m$ escribimos:
$$x\equiv y\ \text{mod}\ m$$

### Artimética modular
<u>Ejemplo</u>
$$
2\equiv 5\ \text{mod}\ 3\\
-34\equiv 78\ \text{mod}\ 14\\
78\equiv -34\ \text{mod}\ 93\\
670\equiv 938\ \text{mod}\ 134
$$

$$x\equiv y\ \text{mod}\ m\ \iff m\mid x-y$$

Si $x\equiv y\ \text{mod}\ m$, entonces:

- $x+z\equiv y+w\ \text{mod}\ m$
- $x-z\equiv y-w\ \text{mod}\ m$
- $xz\equiv\ \text{mod}\ m$
- $nx\equiv ny\ \text{mod}\ m$ para cualquier $n\in\mathbb{Z}$
- $x^n\equiv y^n\ \text{mod}\ m$ para cualquier $n\in\mathbb{N}$

## Esquema general de un método congruencial
Elegimos un entero no negativo $m$, una función $f:\mathbb{Z}\rightarrow\mathbb{Z}$ y un entero $x_0$, generamos una secuencia de números enteros en $[0,m)$ mediante el siguiente método inductivo:
$$x_{i+1}=f(x_i)\ \text{mod}\ m$$

Después, obtenemos números reales (realmente racionales) en $[0,1)$ tomando:
$$u_i=\frac{x_i}{m}$$