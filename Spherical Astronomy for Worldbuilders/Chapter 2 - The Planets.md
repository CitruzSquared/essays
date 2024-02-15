## II. The Planets
Let us calculate the motion of the planets.
### Kepler's laws
All planets in space obey [Newton's law of gravitation](https://en.wikipedia.org/wiki/Newton%27s_law_of_universal_gravitation). \
It tells us:
```math
\textbf{F} = -\frac{G M m}{r^3} \cdot \textbf{r}\tag{6}
```
where $\textbf{F}$ is the gravitational force on the planet, $G$ is the [*gravitational constant*](https://en.wikipedia.org/wiki/Gravitational_constant), which is $6.674\cdot10^{-11}\text{ m}^3\text{ kg}^{-1}\text{ s}^{-2}$ in SI units, $M$ and $m$ are the masses of the Sun and the planet respectively, and $\textbf{r}$ and $r$ are the position vector of the planet and its magnitude (the distance between the Sun and the planet) respectively.

Turns out this equation has already been solved for the most part, and the problem of the planets in motion around the Sun, or the Moon in orbit around the Earth, can be modeled as an ideal Newtonian [two body problem](https://en.wikipedia.org/wiki/Two-body_problem). Thus they obey [Kepler's laws of planetary motion](https://en.wikipedia.org/wiki/Kepler's_laws_of_planetary_motion):
- 1. Planets orbit in an [ellipse](https://en.wikipedia.org/wiki/Ellipse) with the Sun at a [*focus*](https://en.wikipedia.org/wiki/Focus_(geometry)).
  * Thus there is a point in the orbit where it is closest to the Sun and a point where it is furthest away. These two points are diametrically opposite each other.
- 2. Planets in orbit "sweep out" the same area per unit time.
  * This tells us that the object travels faster when it is in the part of its orbit that is closer to the primary, and slower when it is further away.
- 3. The square of the orbital period ($T$) of the planet is proportional to the cube of the *semi-major-axis* of the orbit of the planet.

Since all orbits are ellipses, let us quickly investigate the ellipse.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/bb81dcca-4a3c-4ad7-9f70-6f4eea3af818" width="350"/> In the diagram is an ellipse with center $O$. The distance $OP$ is known as the semi-major-axis and is denoted $a$. The distance $OB$ is known as the semi-minor-axis and is denoted $b$. The ellipse can be represented algebraically using these two measures: the ellipse is the locus of all points satisfying the equation
```math
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1.\tag{7}
```

Point $F$ is located at the point where the length $BF = a$. This point $F$ is known as the [focus](https://en.wikipedia.org/wiki/Focus_(geometry)) of an ellipse and this is where the Sun lies in a planetary orbit. 

<br/>

The points $P$ and $A$ then are the points closest to and furthest away from the focus, and are known as the *periapsis* and *apoapsis* respectively, and [*apses*](https://en.wikipedia.org/wiki/Apsis) (singular *apsis*) collectively. When the primary object (the object at the focus) is the Sun, these points can be called the *perihelion* and *apohelion*, and when the primary object is the Earth, they can be called the *perigee* and *apogee*.

The amount of "squishing" of an ellipse is given by the quantity $c/a$ where $c$ is the distance $OF$. This quantity is known as the [*eccentricity*](https://en.wikipedia.org/wiki/Eccentricity_(mathematics)) and is denoted $e$. When the eccentricity is $0$, the ellipse becomes a perfect circle, and when the eccentricity is greater than or equal to $1$, the ellipse breaks and becomes a [parabola](https://en.wikipedia.org/wiki/Parabola) or [hyperbola](https://en.wikipedia.org/wiki/Hyperbola). 

Because $BF = a$, $c^2 = a^2 - b^2$, and $e$ can also be written:
```math
e^2 = \frac{a^2-b^2}{a^2} = 1 - \frac{b^2}{a^2}.\tag{8}
```

The periapsis distance is then
```math
\begin{align}
FP &= a - c = a - ae\\
&= a(1 - e)\tag{9}
\end{align}
```
and the apoapsis distance is
```math
\begin{align}
FA &= a + c = a + ae\\
&= a(1 + e)\tag{10}
\end{align}
```
Finding the semi-major-axis length given the periapsis and apoapsis distances is trivial:
```math
a = \frac{1}{2} (FA + FP) \tag{11}
```

#### Example 2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that the semi-major-axis of the orbit of the Earth is $149\:598\:023 \text{ km}$, and its eccentricity is $0.0167$, <br/>
Find the semi-minor-axis, the perihelion distance, and the apohelion distance.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By rearranging equation $8$:
```math
\begin{align}
b &= \sqrt{a^2(1 - e^2)}\\
&= \sqrt{149\:598\:023^2\text{ km}^2 (1 - 0.0167^2)}\\
&= 149\:577\:161 \text{ km}
\end{align}
```
The periapsis distance is given by equation $9$:
```math
149\:598\:023\text{ km }(1 - 0.0167) = 147\:099\:736\text{ km}
```
And the apoapsis distance is given by equation $10$:
```math
149\:598\:023\text{ km }(1 + 0.0167) = 152\:096\:309\text{ km}
```
$\blacksquare$

Furthermore, the ellipse can also be written in polar form:
```math
r = \frac{ep}{1 + e\cos(\theta)}\tag{12}
```
where $p$ is the distance to the [*directrix*](https://en.wikipedia.org/wiki/Conic_section#Eccentricity,_focus_and_directrix) of the ellipse.\
This form of the equation for an ellipse will not be used much.

<br/>

#### Example 3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Prove that all planets orbit the Sun in an ellipse. <br/>
Disclaimer: the proof is mathematically dense and there is no need to know it. <br/>
It is advised for the average reader to skip this investigation.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

[Newton's law of gravitation](https://en.wikipedia.org/wiki/Newton%27s_law_of_universal_gravitation) (equation $6$) tells us:
```math
\textbf{F} = -\frac{G M m}{r^3} \cdot \textbf{r}
```
This can be rewritten:
```math
\textbf{F} = -\frac{G M m}{r^2} \cdot \textbf{u}
```
where $\textbf{u}$ is the [unit vector](https://en.wikipedia.org/wiki/Unit_vector) in the direction of $\textbf{r}$.\
Furthermore, [Newton's second law of motion](https://en.wikipedia.org/wiki/Newton%27s_laws_of_motion#Second_law) tells us:
```math
\textbf{F} = m \textbf{a}
```
where $\textbf{F}$ is the force on an object, $m$ is the mass of the object, and $\textbf{a}$ is its acceleration, defined by $\textbf{a} = d\textbf{v}/dt = d^2\textbf{r}/dt^2$, where $\textbf{v}$ is the velocity of the object.

By equating the two laws we obtain:
```math
\textbf{a} = -\frac{G M}{r^3} \cdot \textbf{r}
```
which shows that $\textbf{a}$ and $\textbf{r}$ are a scalar multiple of each other (they are parallel), which means that $\textbf{a} \times \textbf{r} = \textbf{0}$.\
In addition,
```math
\begin{align}
\frac{d}{dt}(\textbf{r}\times\textbf{v}) &= \textbf{r}'\times\textbf{v}+\textbf{r}\times\textbf{v}'\\
&=\textbf{v}\times\textbf{v}+\textbf{r}\times\textbf{a}\\
&=\textbf{0}\times\textbf{0}\\
&=\textbf{0}.
\end{align}
```
By integrating both sides of this equation we obtain:
```math
\textbf{r}\times\textbf{v} = \textbf{h}
```
where $\textbf{h}$ is a constant vector. We can reasonably assume $\textbf{r}$ and $\textbf{v}$ are not parallel (that is, the planet does not move in a straight line), and thus $\textbf{h} \neq \textbf{0}$. Thus all possible $\textbf{r}$ is perpendicular to $\textbf{h}$, and since $\textbf{h}$ is constant, all $\textbf{r}$ must lie flat on a plane with $\textbf{h}$ as its normal vector.

Let us now rewrite $\textbf{h}$.
```math
\begin{align}
\textbf{h} &= \textbf{r}\times\textbf{v} = \textbf{r}\times\textbf{r}' =r\textbf{u}\times(r\textbf{u})'\\
&=r\textbf{u}\times(r'\textbf{u}+r\textbf{u}') =r^2(\textbf{u}\times\textbf{u}')+rr'(\textbf{u}\times\textbf{u})\\
&=r^2(\textbf{u}\times\textbf{u}').
\end{align}
```
Then
```math
\begin{align}
\textbf{a}\times\textbf{h} &= -\frac{GM}{r^2}\textbf{u}\times r^2(\textbf{u}\times\textbf{u}')\\
&= -GM\textbf{u}\times(\textbf{u}\times\textbf{u}')\\
&= -GM[(\textbf{u}\cdot\textbf{u}')\textbf{u}-(\textbf{u}\cdot\textbf{u})\textbf{u}')]
\end{align}
```
But since $\textbf{u}$ is a unit vector ($|\textbf{u}| = 1$), $\textbf{u}\cdot\textbf{u} = 1$ (a constant) and so:
```math
\begin{align}
\frac{d}{dt}(\textbf{u}\cdot\textbf{u}) &= \textbf{u}'\cdot\textbf{u}+\textbf{u}\cdot\textbf{u}'\\
&=2\textbf{u}\cdot\textbf{u}'= 0.\\
\therefore \textbf{u}\cdot\textbf{u}'&=0\\
\therefore \textbf{a}\times\textbf{h}&=GM\textbf{u}'
\end{align}
```
Therefore we can write
```math
\begin{align}
\frac{d}{dt}(\textbf{v}\times\textbf{h})&=\textbf{v}'\times\textbf{h}+\textbf{v}\times\textbf{h}'=\textbf{v}'\times\textbf{h}\\
&=\textbf{a}\times\textbf{h} = GM\textbf{u}'
\end{align}
```
Integrating both sides of this equation gives us
```math
\textbf{v}\times\textbf{h}=GM\textbf{u}+\textbf{C}\tag{13}
```
where $\textbf{C}$ is a constant vector.

Let us now choose coordinate axes such that positive $z$-axis lies in the direction of $\textbf{h}$. Thus the planet moves in the $xy$-plane.\
Now, because $\textbf{v}\times\textbf{h}$ and $\textbf{u}$ are perpendicular to $\textbf{h}$ (i.e. in the $xy$-plane), $\textbf{C}$ must be in the $xy$-plane as well. Since $\textbf{C}$ is a constant vector, we choose the positive $x$-axis to be in the direction of it, and now $r$ and the angle between $\textbf{C}$ and $\textbf{r}$ (which we call $\theta$) define $\textbf{r}$ in polar coordinates.

From equation $13$ we now have:
```math
\begin{align}
\textbf{r}\cdot(\textbf{v}\times\textbf{h})&=\textbf{r}\cdot(GM\textbf{u}+\textbf{C})\\
&=GM\textbf{r}\cdot\textbf{u}+\textbf{r}\cdot\textbf{C}\\
&=GMr\textbf{u}\cdot\textbf{u}+|\textbf{r}||\textbf{C}|\cos(\theta)\\
&=GMr + rc\cos(\theta)
\end{align}
```
where $c = |\textbf{C}|$. Now, solving for $r$,
```math
r=\frac{\textbf{r}\cdot(\textbf{b}\times\textbf{h})}{GM+c\cos(\theta)}
```
If we put $c/(GM)$ = $e$ (and thus $GM = c/e$),
```math
r=\frac{1}{GM}\cdot\frac{\textbf{r}\cdot(\textbf{v}\times\textbf{h})}{1+e\cos(\theta)}=\frac{e}{c}\cdot\frac{\textbf{r}\cdot(\textbf{v}\times\textbf{h})}{1+e\cos(\theta)}
```
But,
```math
\textbf{r}\cdot(\textbf{v}\times\textbf{h})=(\textbf{r}\times\textbf{v})\cdot\textbf{h}=\textbf{h}\cdot\textbf{h}=h^2
```
where $h = |\textbf{h}|$.\
Thus:
```math
r= \frac{h^2e/c}{1+e\cos(\theta)}
```
If we now set $p=h^2/c$, we obtain for $r$:
```math
r=\frac{ep}{1+e\cos(\theta)}
```
which is precisely equation $12$.\
$\blacksquare$

<br/>
<br/>

Let us now calculate the [orbital period](https://en.wikipedia.org/wiki/Orbital_period) $T$ of a planet in a circular orbit, given the orbital radius $r$.\
Newton's law of gravitation (equation $6$) tells us:
```math
\textbf{F} = -\frac{G M m}{r^3} \cdot \textbf{r}
```
For objects to rotate, there must be a force pointing inwards (called the [centripetal force](https://en.wikipedia.org/wiki/Centripetal_force)), and this force is given as:
```math
\textbf{F} = -\frac{mv^2}{r^2} \cdot \textbf{r}
```
Where $m$ is the mass of the rotating body, and $v$ is its speed.\
Equating the two equations,
```math
\begin{align}
-\frac{mv^2}{r^2} \cdot \textbf{r} &= -\frac{G M m}{r^3} \cdot \textbf{r}\\
v^2 &= \frac{GM}{r}\\
v &= \sqrt{\frac{GM}{r}}
\end{align}
```
Using the fact that time $=$ distance $/$ speed and that the circumference of the orbit is $2\pi r$,
```math
\begin{align}
T &= \frac{2\pi r}{v} = \frac{2\pi r}{\sqrt{GM/r}}\\
&=\sqrt{\frac{4 \pi^2 r^3}{GM}}\tag{14}
\end{align}
```
We can see that equation $14$ obeys Kepler's third law, $T^2 \propto r^3$.\
Turns out, we can generalize this formula to elliptical orbits without issue!
```math
T = \sqrt{\frac{4 \pi^2 a^3}{GM}}\tag{15}
```
If we have two objects comparable in mass, they will orbit each other about their center of mass, and the period will be:
```math
 T = \sqrt{\frac{4 \pi^2 a^3}{G(M_1 + M_2)}}. \tag{16}
```
#### Example 4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that $G = 6.674\cdot10^{-11}\text{ m}^3\text{ kg}^{-1}\text{ s}^{-2}$, the mass of the Sun $M_S = 1.989\cdot 10^{30} \text{ kg}$, the semi-major-axis of the orbit of the Earth $a = 1.496\cdot10^{11}\text{ m}$, and that $1\text{ dy} = 86\:000\text{ s}$, calculate the orbital period of the Earth in days.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation 15:
```math
\begin{align}
T &= \sqrt{\frac{4 \pi^2 a^3}{GM}}\\
&=\sqrt{\frac{4 \pi^2 (1.496\cdot10^{11}\text{ m})^3}{(6.674\cdot10^{-11}\text{ m}^3\text{ kg}^{-1}\text{ s}^{-2})(1.989\cdot 10^{30} \text{ kg})}}\\
&= 3.1554897 \cdot 10^7 \text{ s}
\end{align}
```
Converting to days:
```math
T = 365.219 \text{ dy}
```
Which is close enough to the true value of the year, $365.2422 \text{ dy}$. The difference comes from the fact that there are gravitational perturbations from other Solar System objects on the Earth, and therefore the motion of the Earth is not *exactly* a true two-body problem. The precise math is too difficult for worldbuilding purposes and therefore the perturbation effects of planets on planets will be ignored.\
$\blacksquare$
