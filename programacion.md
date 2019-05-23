
# Table of Contents

1.  [Teoría](#orgeec86f3)
    1.  [Motivación](#org682b46f)
    2.  [Ejemplos](#org4173626)
    3.  [Convexidad](#org98fa387)
    4.  [El método símplex](#orgefb0454)
2.  [Herramientas computacionales](#org237195c)
    1.  [Emacs](#orgca100d5)
    2.  [Git](#org571bf09)
    3.  [Python](#org1105e17)
    4.  [LaTeX](#orga3d3282)



<a id="orgeec86f3"></a>

# Teoría


<a id="org682b46f"></a>

## Motivación

El objetivo de la programación lineal es maximizar funciones lineales
sobre dominios convexos, es decir, definidos sobre regiones dadas por
desigualdades.

![img](linear-programming-example-1b.jpg)


<a id="org4173626"></a>

## Ejemplos

-   El problema de la dieta
-   Optimización de lugares en una excursión
-   Escoger objetos óptimos para un campamento
-   El problema del flujo máximo


<a id="org98fa387"></a>

## Convexidad

Un conjunto \(X\) es **convexo** si para todos \(x,y\in X\) y \(t\in
[0,1]\) se tiene que \(tx+(1-t)y\in X\).


<a id="orgefb0454"></a>

## El método símplex


<a id="org237195c"></a>

# Herramientas computacionales


<a id="orgca100d5"></a>

## Emacs

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="org-left" />

<col  class="org-left" />
</colgroup>
<tbody>
<tr>
<td class="org-left">C-x C-s</td>
<td class="org-left">salvar archivo</td>
</tr>


<tr>
<td class="org-left">C-x C-f</td>
<td class="org-left">abrir archivo</td>
</tr>


<tr>
<td class="org-left">M-q</td>
<td class="org-left">formatear el párrafo</td>
</tr>


<tr>
<td class="org-left">C-x d</td>
<td class="org-left">editar directorios</td>
</tr>


<tr>
<td class="org-left">C-g</td>
<td class="org-left">salir de todo</td>
</tr>


<tr>
<td class="org-left">C-x 2</td>
<td class="org-left">divide horizontalmente</td>
</tr>


<tr>
<td class="org-left">C-x 3</td>
<td class="org-left">divide verticalmente</td>
</tr>


<tr>
<td class="org-left">C-x 1</td>
<td class="org-left">regresa a una sola pantalla</td>
</tr>


<tr>
<td class="org-left">M-w</td>
<td class="org-left">copiar la región</td>
</tr>


<tr>
<td class="org-left">C-w</td>
<td class="org-left">borrar la región</td>
</tr>


<tr>
<td class="org-left">C-y</td>
<td class="org-left">pegar la región</td>
</tr>


<tr>
<td class="org-left">Shift y flechas</td>
<td class="org-left">seleccionar la región</td>
</tr>


<tr>
<td class="org-left">C-x b</td>
<td class="org-left">cambiar buffer</td>
</tr>


<tr>
<td class="org-left">C-x k</td>
<td class="org-left">matar el buffer</td>
</tr>
</tbody>
</table>

1.  Org mode

    <table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">
    
    
    <colgroup>
    <col  class="org-left" />
    
    <col  class="org-left" />
    </colgroup>
    <tbody>
    <tr>
    <td class="org-left">C-c C-c</td>
    <td class="org-left">corre un bloque de código</td>
    </tr>
    
    
    <tr>
    <td class="org-left">&#xa0;</td>
    <td class="org-left">&#xa0;</td>
    </tr>
    </tbody>
    </table>


<a id="org571bf09"></a>

## Git

1.  Git en la terminal

2.  Github


<a id="org1105e17"></a>

## Python

1.  El lenguaje Python

    En el lenguaje Python podemos hacer operaciones:
    
        2+2
    
    También podemos usar la biblioteca pulp. Por ejemplo, encontramos el
    máximo de \(-4x+y\) sujeto a \(x+y\leq\)
    
        from pulp import *
        x = LpVariable("x", 0, 3)
        y = LpVariable("y", 0, 1)
        prob = LpProblem("myProblem", LpMinimize)
        prob += x + y <= 2
        prob += -4*x + y
        status = prob.solve()
        value(x), value(y), value(prob.objective)

2.  Jupyter


<a id="orga3d3282"></a>

## LaTeX

