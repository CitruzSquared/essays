## Introduction
**Astrology**, which is a method of divination based on the location of the stars and planets in the sky, can be a very important part of worldbuilding. The basis of astrology is *Spherical Astronomy*, the science of observing the sky. This post will serve as a guide to spherical astronomy for the worldbuilder, and will start from the basics and build up to calculating the location of stars in the sky and finally a complete ephemeris, from which the worldbuilder can create their own astrological system.

**NOTE!** Please use dark mode for the diagrams to show properly.

**NOTE!** Some of the derivations of formulae in this guide assumes the reader is familiar with algebra, trigonometry, vectors, basic differentiation and integration, and basic operations with matrices. (See § Useful Mathematics)

## Table of Contents
1. Coordinates
   - Equations $1$ to $5$
   - Example $1$
2. Orbits
   - Part A
     * Equations $6$ to $21$
     * Examples $2$ to $3$
   - Part B
     * Equations $22$ to $28$
     * Examples $4$ to $5$
   - Part C
     * Equations $29$ to $32$
     * Examples $6$ to $7$
3. Moons
4. Appearance
5. Horizontal Coordinates
6. Time
7. Earthly Parallax

## Useful Mathematics

### Algebra
```math
\begin{align}
(a + b)(c + d) &= ac + ad + bc + bd\\
x^{a/b} &= \sqrt[b]{x^a} \\
x^{-a} &= \frac{1}{x^a} \\
x^a\cdot x^b &= x^{a + b} \\
\left(x^a\right)^b & =x^{ab} \\
ax^2 + bx + c &\implies x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\\
\end{align}
```

### Geometry
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/669a9787-9f70-4c9e-89d5-e7f390f5bdbc" width="250"/>

```math
\begin{align}
\frac{\sin(a)}{A} &= \frac{\sin(b)}{B} = \frac{\sin(c)}{C}\\
c^2 &= a^2 + b^2 - 2ac\cos(C)\\
S &= \frac{1}{2}ab\sin(C)\\
A + B + C &= 180\degree \\
\pi\text{ rad} &= 180\degree\\
1\degree &= 60' = 3600''
\end{align}
```

<br/>

### Trigonometry
```math
\begin{align}
\tan(\alpha) &= \frac{\sin(\alpha)}{\cos(\alpha)} \\
\sin(\alpha) &= -\sin(-\alpha) = -\sin(\alpha + 180\degree) = \sin(180\degree - \alpha) \\
\cos(\alpha) &= \cos(-\alpha) = -\cos(\alpha + 180\degree) = -\cos(180\degree - \alpha)\\
\tan(\alpha) &= -\tan(-\alpha) = \tan(\alpha + 180\degree) = -\tan(180\degree - \alpha)\\
\sin(\alpha) &= \cos(\alpha - 90\degree) \\
\csc(\alpha) &= \frac{1}{\sin(\alpha)}\\
\sec(\alpha) &= \frac{1}{\cos(\alpha)}\\
\cot(\alpha) &= \frac{1}{\tan(\alpha)}\\
\sin(\alpha\pm\beta) &= \sin(\alpha)\cos(\beta)\pm\cos(\alpha)\sin(\beta) \\
\cos(\alpha\pm\beta) &= \cos(\alpha)\cos(\beta)\mp\sin(\alpha)\sin(\beta) \\
\sin^2(\alpha) + \cos^2(\alpha) &= 1 \\
\end{align}
```
```math
\begin{alignat}{2}
\arctan(y, x) &= \arctan(y/x)&&\text{ if } x > 0 \\
&= \arctan(y/x) + 180\degree&&\text{ if } x < 0 \text{ and } y \geq 0\\
&= \arctan(y/x) - 180\degree&&\text{ if } x < 0 \text{ and } y < 0\\
&= \pi/2\text{ if } x = 0 &&\text{ and } y > 0 \\
&= 3\pi/2\text{ if } x = 0 &&\text{ and } y < 0 \\
\end{alignat}
```
### Calculus
```math
\begin{align}
\frac{d}{dx} c &= 0 \\
\frac{d}{dx} ax^b &= abx^{b-1} \\
\frac{d}{dx} \sin(x) &= \cos(x) \\
\frac{d}{dx} \cos(x) &= -\sin(x) \\
\frac{d}{dx} \tan(x) &= \sec^2(x) \\
\frac{d}{dx} \arcsin(x) &= \frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arccos(x) &= -\frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arctan(x) &= \frac{1}{1 + x^2} \\
\frac{dy}{dt} &= \frac{dy}{dx_1}\frac{dx_1}{dx_2}\frac{dx_2}{dx_3}\cdots\frac{dx_{n-1}}{dx_n}\frac{dx_n}{dt} \\
\frac{d}{dx} [f(x)g(x)] &= \frac{df(x)}{dx}g(x) + f(x)\frac{dg(x)}{dx}
\end{align}
```
### Matrices
```math
\begin{align}
c \begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
+
d \begin{bmatrix}
b_1 & b_2 & b_3 \\
b_4 & b_5 & b_6 \\
b_7 & b_8 & b_9
\end{bmatrix}
&=
\begin{bmatrix}
ca_1 + db_1 & ca_2 + db_2 & ca_3 + db_3 \\
ca_4 + db_4 & ca_5 + db_5 & ca_6 + db_6 \\
ca_7 + db_7 & ca_8 + db_8 & ca_9 + db_9
\end{bmatrix}\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
\begin{bmatrix}
b_1 \\ b_2 \\ b_3
\end{bmatrix}
&=
\begin{bmatrix}
a_1b_1 + a_2b_2 + a_3b_3 \\
a_4b_1 + a_5b_2 + a_6b_3 \\
a_7b_1 + a_8b_2 + a_9b_3
\end{bmatrix}\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
\begin{bmatrix}
b_1 & b_2 & b_3 \\
b_4 & b_5 & b_6 \\
b_7 & b_8 & b_9
\end{bmatrix}
&=
\begin{bmatrix}
a_1b_1 + a_2b_4 + a_3b_7 & a_1b_2 + a_2b_5 + a_3b_8 & a_1b_3 + a_2b_6 + a_3b_9 \\
a_4b_1 + a_5b_4 + a_6b_7 & a_4b_2 + a_5b_5 + a_6b_8 & a_4b_3 + a_5b_6 + a_6b_9 \\
a_7b_1 + a_8b_4 + a_9b_7 & a_7b_2 + a_8b_5 + a_9b_8 & a_7b_3 + a_8b_6 + a_9b_9
\end{bmatrix}
\end{align}
```
### Vectors
```math
\begin{align}
\textbf{v} &= v_1\textbf{i} + v_2\textbf{j} + v_3\textbf{k} = \begin{bmatrix}
v_1 \\ v_2 \\ v_3
\end{bmatrix}\\
|\textbf{v}| &= \sqrt{v_1^2 + v_2^2 + v_3^3} \\
\textbf{v}\cdot\textbf{u} &= v_1u_1 + v_2u_2 + v_3u_3 \\
&= \textbf{u}\cdot\textbf{v}\\
&= |\textbf{v}||\textbf{u}|\cos(\theta)\\
\textbf{v}\cdot\textbf{v} &= |\textbf{v}|^2\\
\textbf{v}\times\textbf{u} &= (v_2u_3-v_3u_2)\textbf{i} + (v_3u_1-v_1u_3)\textbf{j} + (v_1u_2-v_2u_1)\textbf{k}\\
&= -\textbf{u}\times\textbf{v}\\
|\textbf{v}\times\textbf{u}| &= |\textbf{v}||\textbf{u}|\sin(\theta)\\
\textbf{v}\times\textbf{v} &= \textbf{0}\\
(\textbf{v}\times\textbf{u})\times\textbf{w} &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{v}\cdot\textbf{u})\textbf{w}\\
\textbf{v}\times(\textbf{u}\times\textbf{w}) &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{u}\cdot\textbf{w})\textbf{v}
\end{align}
```
