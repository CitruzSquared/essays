# Introduction
**Astrology**, which is a method of divination based on the location of the stars and planets in the sky, can be a very important part of worldbuilding as pretty much every culture has some reference to astrology. The basis of astrology is *Spherical Astronomy*, the science of observing the sky. This post will serve as a guide to spherical astronomy for the worldbuilder, and will start from the basics and build up to calculating the location of objects in the sky, and also calculate various astronomical phenomena such that the worldbuilder can use these calculations in their astrological systems.

**NOTE!** Please use dark mode for the diagrams to show properly.

**NOTE!** Some of the derivations of formulae in this guide assumes the reader is familiar with algebra, trigonometry, basic differentiation and integration, basic vector operations, and basic matrix operations. (See § Useful Mathematics)

## Table of Contents
### 1. The Ephemeris
1. **Coordinates** (Eq. $1.1$ to $1.5$, Ex. $1.1$)
   - The Celestial Sphere
   - Coordinate Axes
   - Coordinate Transformations
2. **Orbits**
   - Part A (Eq. $2.1$ to $2.11$, Ex. $2.1$ to $2.2$)
     * Newton and Kepler
     * Kepler's First Law
     * Kepler's Third Law
   - Part B (Eq. $2.12$ to $2.23$, Ex. $2.3$ to $2.4$)
     * Perifocal Coordinates
     * Kepler's Second Law
   - Part C (Eq. $2.24$ to $2.27$, Ex. $2.5$ to $2.6$)
     * Orientation of Orbits in 3D Space
     * Calculating the Ephemeris for a Planet
3. **Moons**
   - Part A (Eq. $3.1$ to $3.13$, Ex. $3.1$ to $3.2$)
     * Change in Ω and ω
     * The Two Types of Moons
     * Orbit-Aligned Moons
   - Part B (Eq. $3.14$ to $3.21$, Ex. $3.3$ to $3.4$)
     * Equator-Aligned Moons
     * The Anomalistic Period
     * Multi Moon Systems
### 2. Terrestrial Observation
4. **Geocentrism**
   - Part A (Eq. $4.1$ to $4.9$, Ex. $4.1$ to $4.4$)
     * Apparent Size
     * Phase
     * Elongation
     * The Synodic Period
     * Solving for Time of Conjunction
   - Part B (Eq. $4.10$ to $4.29$, Ex. $4.5$ to $4.8$)
     * Brightness
     * Apparent Retrograde Motion
   - Part C (Eq. $4.30$ to $4.36$, Ex. $4.9$)
     * Lunar Libration
5. **Time** (Eq. $5.1$ to $5.4$, Ex. $5.1$ to $5.3$)
   - Sidereal and Solar time
   - Converting between Times
6. **Horizontal Coordinates**
   - Part A (Eq. $6.1$ to $6.6$, Ex. $6.1$ to $6.6$)
     * The Hour Angle
     * Horizontal Coordinates
     * Time of Sunrise
     * The Terminator
   - Part B (Eq. $6.7$ to $6.17$, Ex. $6.7$ to $6.12$)
     * The Ascending Sign
     * Heliacal Rising
     * The Medium Coeli
     * The Subsolar Point
     * Lighting Direction
   - Part C
     * Saturn in the Sky
7. **The Shape of the Earth** (Eq. $7.1$ to $7.9$, Ex. $7.1$)
   - The Ellipsoid
   - Latitude
8. **Parallax** (Eq. $8.1$ to $8.11$, Ex. $8.1$ to $8.5$)
   - Apparent Equatorial Coordinates
   - Apparent Horizontal Coordinates
   - Parallax Corrected Sunrise Equation
   - Horizontal Parallax
   - Parallax Corrected Subsolar Point
### 3. Syzygy
9. **Solar Eclipses**
    - Part A (Eq. $9.1$ to $9.15$, Ex. $9.1$ to $9.2$)
      * Partial Total, and Annular Solar Eclipses
      * Condition for Eclipse
      * Direction of the Shadow
      * Position of the Shadow and the Observer
      * The Size of the Shadow
   - Part B (Eq. $9.16$ to $9.34$, Ex. $9.3$)
      * The Outline of the Shadow on the Surface of the Earth
   - Part C (Eq. $9.35$ to $9.50$, Ex. $9.4$)
     * Beginning / Ending Condition
   - Part D (Eq. $9.51$ to $9.63$, Ex. $9.5$ to $9.6$)
     * Contacts
     * Rising / Setting Limits
   - Part E (Eq. $9.64$ to $9.76$, Ex. $9.7$ to $9.9$)
     * Curve of Maximum Eclipse on the Horizon
     * Greatest Eclipse
     * Curve of Centrality
   - Part F (Eq. $9.77$ to $9.78$, Ex $9.10$ to $9.11$)
     * Limits of Partiality
     * Limits of Centrality
     * Eclipse Maps
     * A Note on Time Steps
     * Local Predictions
     * Transits and Occultations
   - Part Z
     * Besselian Element Table
10. **Lunar Eclipses** (Eq. $10.1$ to $10.9$, Ex $10.1$ to $10.5$)
    - Penumbral, Partial, and Total Lunar Eclipses
    - Conditions for Eclipse
    - Besselian Elements
    - Contacts
    - Greatest Eclipse, Gamma, and Magnitude
    - A Note on Time Steps
11. **Eclipse Patterns** (Eq. $11.1$ to $11.2$, Ex $11.1$ to $11.6$)
    - Eclipse Seasons
    - Eclipse Years and Draconic Months
    - Periodicity of Eclipses and the Saros

## Useful Mathematics

### Algebra
```math
\begin{align}
(a + b)(c + d) &= ac + ad + bc + bd \\
\frac{a}{b} = \frac{c}{d} &\implies ad = bc\\
x^0 &= 1 \\
x^{a/b} &= \sqrt[b]{x^a} \\
x^{-a} &= \frac{1}{x^a} \\
x^a\cdot x^b &= x^{a + b} \\
\left(x^a\right)^b & =x^{ab} \\
ax^2 + bx + c = 0 &\implies x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\\
\end{align}
```

### Trigonometry
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/d0fd51e1-67d1-44fd-8777-89537e5ecbf6" width="250"/>

```math
\begin{align}
\\
\\
\sin(\alpha) &= \frac{o}{h}\\
\cos(\alpha) &= \frac{a}{h}\\
\tan(\alpha) &= \frac{o}{a}
\end{align}
```

<br/>
<br/>

```math
\begin{align}
\text{trig}(\alpha + n\cdot 360\degree) &= \text{trig}(\alpha)\enspace\{n \in \mathbb{Z}\}\\
\tan(\alpha) &= \frac{\sin(\alpha)}{\cos(\alpha)} \\
\csc(\alpha) &= \frac{1}{\sin(\alpha)}\\
\sec(\alpha) &= \frac{1}{\cos(\alpha)}\\
\cot(\alpha) &= \frac{1}{\tan(\alpha)}\\
\sin(\alpha) &= -\sin(-\alpha) = -\sin(\alpha + 180\degree) = \sin(180\degree - \alpha) \\
\cos(\alpha) &= \cos(-\alpha) = -\cos(\alpha + 180\degree) = -\cos(180\degree - \alpha)\\
\tan(\alpha) &= -\tan(-\alpha) = \tan(\alpha + 180\degree) = -\tan(180\degree - \alpha)\\
\sin(\alpha) &= \cos(90\degree - \alpha) = -\cos(90\degree + \alpha) = \cos(\alpha - 90\degree)\\
\cos(\alpha) &= \sin(90\degree - \alpha) = \sin(90\degree + \alpha) = -\sin(\alpha - 90\degree)\\
\tan(\alpha) &= \cot(90\degree - \alpha) = -\cot(90\degree  + \alpha) = -\cot(\alpha - 90\degree)\\
\sin^2(\alpha) + \cos^2(\alpha) &= 1 \\
\tan^2(\alpha) + 1 &= \sec^2(\alpha) \\
\cot^2(\alpha) + 1 &= \csc^2(\alpha) \\
\sin(\alpha\pm\beta) &= \sin(\alpha)\cos(\beta)\pm\cos(\alpha)\sin(\beta) \\
\cos(\alpha\pm\beta) &= \cos(\alpha)\cos(\beta)\mp\sin(\alpha)\sin(\beta) \\
\sin(2\alpha) &= 2\sin(\alpha)\cos(\alpha) \\
\cos(2\alpha) &= \cos^2(\alpha) - \sin^2(\alpha) = 2\cos^2(\alpha) - 1 = 1 - 2\sin^2(\alpha) \\
\sin^2(\alpha) &= \frac{1}{2}(1 - \cos(2\alpha)) \\
\cos^2(\alpha) &= \frac{1}{2}(1 + \cos(2\alpha))
\end{align}
```
**Two Argument Arctangent:**
```math
\arctan(y, x) = \begin{cases}
\arctan(y/x) &\text{ if } x > 0 \\
\arctan(y/x) + 180\degree&\text{ if } x < 0 \text{ and } y \geq 0\\
\arctan(y/x) - 180\degree&\text{ if } x < 0 \text{ and } y < 0\\
90\degree&\text{ if } x = 0 \text{ and } y > 0 \\
-90\degree&\text{ if } x = 0 \text{ and } y < 0 \\
\text{undefined} &\text{ if } x = 0 \text{ and } y = 0
\end{cases}
```

### Geometry
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/669a9787-9f70-4c9e-89d5-e7f390f5bdbc" width="250"/>

```math
\begin{align}
\\
A + B + C &= 180\degree \\
a^2 &= b^2 + c^2 - 2bc\cos(A)\\
\frac{a}{\sin(A)} &= \frac{b}{\sin(B)} = \frac{c}{\sin(C)}\\
S &= \frac{1}{2}ab\sin(C)\\
\end{align}
```
<br/>

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/e5e14475-0c35-41fb-affc-e0c08afefc50" width="250"/>

```math
\begin{align}
(\theta \text{ in} &\text{ radians})\\
C &= r\theta\\
S &= \frac{1}{2}r^2 \theta \\
\\
1\text{ rev} &= 2\pi\text{ rad} = 360\degree = 24^h\\
1\degree &= 60' = 3600''\\
1^h &= 60^m = 3600^s
\end{align}
```

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/2d384219-b162-4b88-a5e3-4def24e6bc2f" width="250"/>

$A$, $B$, $C$ are points on a sphere with center $O$. Let the angles $BAC$, $ABC$, and $BCA$ be denoted $A$, $B$, and $C$ respectively, and the angles $BOC$, $AOC$, and $AOB$ be denoted $a$, $b$, and $c$ respectively.
```math
\begin{align}
A + B + C &\geq 180\degree\\
\cos(a) &= \cos(b)\cos(c) + \sin(b)\sin(c)\cos(A) \\
\cos(A) &= -\cos(B)\cos(C) + \sin(B)\sin(C)\cos(a) \\
\sin(a)\cos(B) &= \cos(b)\sin(c) - \sin(b)\cos(c)\cos(A) \\
\sin(A)\cos(b) &= \cos(B)\sin(C) - \sin(B)\cos(C)\cos(a) \\
\frac{\sin(a)}{\sin(A)} &= \frac{\sin(b)}{\sin(B)} = \frac{\sin(c)}{\sin(C)}\\
\cos(a)\cos(C) &= \sin(a)\cot(b) - \sin(C)\cot(B) \\
\cos(A)\cos(c) &= \sin(A)\cot(B) - \sin(c)\cot(b)
\end{align}
```


### Calculus
```math
\begin{align}
\frac{d}{dx} f(x) &= f'(x) = \dot f\\
&= \lim_{h\to 0}\frac{f(x+h)-f(x)}{h}\\
\frac{d}{dx} a &= 0 \\
\frac{d}{dx} x^a &= ax^{a-1} \\
\\
(x \text{ in} &\text{ radians})\\
\frac{d}{dx} \sin(x) &= \cos(x) \\
\frac{d}{dx} \cos(x) &= -\sin(x) \\
\frac{d}{dx} \tan(x) &= \sec^2(x) \\
\frac{d}{dx} \arcsin(x) &= \frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arccos(x) &= -\frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arctan(x) &= \frac{1}{1 + x^2} \\
\\
\frac{d}{dx} [af(x) + bg(x)] &= af'(x) + bg'(x)\\
\frac{d}{dx} [f(x)g(x)] &= f'(x)g(x) + f(x)g'(x)\\
\frac{dy}{dx} &= \frac{dy}{du_1}\frac{du_1}{du_2}\frac{du_2}{du_3}\cdots\frac{du_{n-1}}{du_n}\frac{du_n}{dx} \\
\therefore \frac{d}{dx}[f(g(x))] &= f'(g(x))g'(x)\\
\\
\int_{a}^{b} f'(x) dx &= \lim_{n\to\infty} \sum_{i=1}^n f'(x_i)\Delta x\\
&= f(b) - f(a)
\end{align}
```

### 3D Coordinates
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/94cceab5-f476-40ff-a7fa-393ea8eb08f1" width="250"/>

$O$ is the origin. Lines $OX$, $OY$, and $OZ$ are the $x$, $y$, and $z$ axes respectively and are all perpendicular to each other. \
Planes $OXY$, $OXZ$, and $OYZ$ are the $xy$, $xz$, and $yz$ planes respectively and are all perpendicular to each other. \
$F$ is the orthogonal projection of $P$ onto the $xy$-plane. \
$I$ and $J$ are the orthogonal projections of $F$ onto the $x$ and $y$ axes respectively.

The coordinates of $P$ can be expressed in *cartesian* (or *rectangular*) coordinates as:
```math
x = JF \enspace\enspace y = IF \enspace\enspace z = FP
```
or in *spherical* coordinates as:
```math
\rho = OP \enspace\enspace \theta = XOF \enspace\enspace \phi = FOP
```
The position vector $\textbf{r}$ is given as:
```math
\textbf{r} = \begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
```

### Vectors
$\textbf{e}_x$, $\textbf{e}_y$, and $\textbf{e}_z$ are the unit cartesian basis vectors of $\mathbb{R}^3$.\
$\theta$ is the angle between $\textbf{v}$ and $\textbf{u}$.\
$\textbf{0}$ is the zero vector.
```math
\begin{align}
\textbf{v} &= \begin{bmatrix}
v_1 \\ v_2 \\ v_3
\end{bmatrix} = v_1\textbf{e}_x + v_2\textbf{e}_y + v_3\textbf{e}_z \\
|\textbf{v}| &= \sqrt{v_1^2 + v_2^2 + v_3^3} \\
\hat{\textbf{v}} &= \frac{\textbf{v}}{|\textbf{v}|}\\
a\textbf{v} + b\textbf{u} &= \begin{bmatrix}
av_1 + bu_1 \\ av_1 + bu_2 \\ av_3 + bu_3
\end{bmatrix}\\
\textbf{v}\cdot\textbf{u} &= v_1u_1 + v_2u_2 + v_3u_3 \\
&= \textbf{u}\cdot\textbf{v}\\
&= |\textbf{v}||\textbf{u}|\cos(\theta)\\
\textbf{v}\cdot\textbf{v} &= |\textbf{v}|^2\\
\textbf{v}\times\textbf{u} &= \begin{bmatrix}
v_2u_3-v_3u_2 \\ v_3u_1-v_1u_3 \\ v_1u_2-v_2u_1
\end{bmatrix}\\
&= -\textbf{u}\times\textbf{v}\\
|\textbf{v}\times\textbf{u}| &= |\textbf{v}||\textbf{u}|\sin(\theta)\\
\textbf{v}\times\textbf{v} &= \textbf{0}\\
\textbf{v}\cdot(\textbf{v}\times\textbf{u}) &= 0 = \textbf{u}\cdot(\textbf{v}\times\textbf{u}) \\
\textbf{v}\cdot(\textbf{u}\times\textbf{w}) &= \textbf{u}\cdot(\textbf{w}\times\textbf{v}) = \textbf{w}\cdot(\textbf{v}\times\textbf{u})\\
\textbf{v}\times(\textbf{u}\times\textbf{w}) &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{v}\cdot\textbf{u})\textbf{w}\\
(\textbf{v}\times\textbf{u})\times\textbf{w} &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{u}\cdot\textbf{w})\textbf{v}
\end{align}
```
**Orthogonal Projections of Vectors onto other Vectors:**

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/454bfcf5-b628-406b-b2b9-0a0fc3a83502" width="250"/>

```math
\begin{align}
\\
\\
\text{proj}_\textbf{v} \textbf{u} &= (\textbf{v}\cdot\textbf{u})\hat{\textbf{v}} = \frac{\textbf{v}\cdot\textbf{u}}{\textbf{v}\cdot\textbf{v}}\textbf{v} = \frac{\textbf{v}\textbf{v}^T}{\textbf{v}\cdot\textbf{v}}\textbf{u}\\
\text{oproj}_\textbf{v} \textbf{u} &= \textbf{u} - \text{proj}_\textbf{v} \textbf{u}\\
\textbf{v} \cdot \text{proj}_\textbf{v} \textbf{u} &= \textbf{v}\cdot\textbf{u}\\
\textbf{v} \cdot \text{oproj}_\textbf{v} \textbf{u} &= 0\\
\\
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
\end{bmatrix}\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}^T
&=
\begin{bmatrix}
a_1 & a_4 & a_7 \\
a_2 & a_5 & a_8 \\
a_3 & a_6 & a_9
\end{bmatrix}\\
\begin{bmatrix}
a_1 \\ a_2 \\ a_3 
\end{bmatrix}^T
&=
\begin{bmatrix}
a_1 & a_2 & a_3 
\end{bmatrix}\\
AB &\neq BA\\
\left(A^T\right)^T &= A\\
(AB)^T &= B^TA^T
\end{align}
```
Let $\textbf{a}$ and $\textbf{b}$ be two vectors in $\mathbb{R}^3$.
```math
\begin{align}
\textbf{a}^T \textbf{b} &= \textbf{a} \cdot \textbf{b}\\
\textbf{a} \textbf{b}^T &= \begin{bmatrix}
a_1b_1 & a_1b_2 & a_1b_3 \\
a_2b_1 & a_2b_2 & a_2b_3 \\
a_3b_1 & a_3b_2 & a_3b_3
\end{bmatrix}
\end{align}
```
**Coordinate Transformation Rotation Matrices:**\
$R_x$ denotes a rotation about the $x$-axis by $\theta$, similar for $R_y$ and $R_z$.
```math
\textbf{v}_{\text{New Coordinate Frame}} = R_n R_{n-1}\cdots R_2 R_1\textbf{v}_{\text{Old Coordinate Frame}}
```
```math
R_x = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(\theta) & \sin(\theta) \\
0 & -\sin(\theta) & \cos(\theta)
\end{bmatrix},
\enspace\enspace
R_y = 
\begin{bmatrix}
\cos(\theta) & 0 & -\sin(\theta)\\
0 & 1 & 0\\
\sin(\theta) & 0 & \cos(\theta)
\end{bmatrix},
\enspace\enspace
R_z = 
\begin{bmatrix}
\cos(\theta) & \sin(\theta) & 0 \\
-\sin(\theta) & \cos(\theta) & 0 \\
0 & 0 & 1
\end{bmatrix}
```
The inverse transformation is given by the transpose of $R_n R_{n-1}\cdots R_2 R_1$ because rotation matrices are [orthogonal](https://en.wikipedia.org/wiki/Orthogonal_matrix).
