## II. Orbits
Let us calculate the motion and position of the planets.
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
- 3. The square of the orbital period ($T$) of the planet is proportional to the cube of the *semi-major axis* of the orbit of the planet.

Since all orbits are ellipses, let us quickly investigate the ellipse.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/bb81dcca-4a3c-4ad7-9f70-6f4eea3af818" width="350"/> In the diagram is an ellipse with center $O$. The distance $OP$ is known as the semi-major axis and is denoted $a$. The distance $OB$ is known as the semi-minor axis and is denoted $b$. The ellipse can be represented algebraically using these two measures: the ellipse is the locus of all points satisfying the equation
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
Finding the semi-major axis length given the periapsis and apoapsis distances is trivial:
```math
a = \frac{1}{2} (FA + FP) \tag{11}
```

#### Example 2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that the semi-major axis of the orbit of the Earth is $149\:598\:023 \text{ km}$, and its eccentricity is $0.0167$, <br/>
Find the semi-minor axis, the perihelion distance, and the apohelion distance.
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

Furthermore, the ellipse can also be written in polar form (with the origin at the focus):
```math
r = \frac{ep}{1 + e\cos(\theta)}\tag{12}
```
where $p$ is the distance to the [*directrix*](https://en.wikipedia.org/wiki/Conic_section#Eccentricity,_focus_and_directrix) of the ellipse.\
This form of the equation for an ellipse will not be used much.

<br/>

#### Proof of Kepler's First Law
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
Then,
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
Where $a$ is the sum of the two semi-major axes.
#### Example 3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that $G = 6.674\cdot10^{-11}\text{ m}^3\text{ kg}^{-1}\text{ s}^{-2}$, the mass of the Sun $M_S = 1.989\cdot 10^{30} \text{ kg}$, and the semi-major axis of the orbit of the Earth $a = 1.496\cdot10^{11}\text{ m}$, calculate the orbital period of the Earth.
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

### Perifocal Coordinates
Before we move on to calculating the location of the planets, we need to come up with a system of describing the position of a planet. A natural way of describing that would be to put the Sun at the origin, and describe its coordinates with the $xy$-plane as the orbital plane. These coordinates, defined with the positive $x$ axis towards the periapsis, are called the [**perifocal coordinates**](https://en.wikipedia.org/wiki/Perifocal_coordinate_system).

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/84b9f828-3fc9-4dd8-a3a8-dda6d9f7c572" width="350"/> In the diagram, the orbit of a planet $A$ is shown, where $O$, the origin, is the focus, and therefore the location of the Sun, and $P$ is the perihelion. The angle $PSA$ is known as the [*true anomaly*](https://en.wikipedia.org/wiki/True_anomaly), and is denoted $\nu$. 

Using the true anomaly, the position $(x, y)$ of the planet can be fully described as:
```math
\displaylines{
\begin{align}
x &= r\cos(\nu)\\
y &= r\sin(\nu)
\end{align}
\tag{17}
}
```
Now let's calculate $r$ to calculate $x$ and $y$.

By equation $7$:
```math
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
```

But remember we have put the (right) focus as the origin and therefore $x$ becomes $x + ae$:
```math
\frac{(x + ae)^2}{a^2} + \frac{y^2}{b^2} = 1
```
Substituting $b^2 = a^2(1 - e^2)$:
```math
\begin{align}
\frac{(x + ae)^2}{a^2} + \frac{y^2}{a^2(1 - e^2)} &= 1\\
(x + ae)^2 + \frac{y^2}{1 - e^2} &= a^2\\
x^2 + 2aex + a^2e^2  + \frac{y^2}{1 - e^2} &= a^2
\end{align}
```
Now we substitute equation $17$:
```math
(r\cos(\nu))^2 + 2ae(r\cos(\nu)) + a^2e^2  + \frac{(r\sin(\nu))^2}{1 - e^2} = a^2
```
Which gives the following quadratic equation in $r$:
```math
\frac{1 - e^2 \cos^2(\nu)}{1 - e^2} r^2 + 2ae\cos(\nu) r - a^2(1 - e^2) = 0.
```
Finally, solving for $r$ gives us
```math
r = \frac{a(1 - e^2)}{1 + e\cos(\nu)}.\tag{18}
```
Which we can now use to give exact coordinates for $x$ and $y$.\
(Equation $18$ also works as an alternative for equation $12$.)

However, putting the right origin at the focus is cumbersome. What if we approximated the orbit as a circle?

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/8f9a0758-fcdf-4de7-a4fc-80249d57a4fc" width="350"/> In this diagram, we have drawn a circle with radius $a$ over the ellipse. We then projected the position of the planet $A$ onto this circle and called it $A'$. Thus a new angle is defined: $PCA'$ defines the [*eccentric anomaly*](https://en.wikipedia.org/wiki/Eccentric_anomaly), and is denoted $E$.

Defined as such, the coordinates of $A$ are much easier to determine. Putting $C$ as the origin,
```math
\sin (E) = \frac{x}{a}
```
and because $x^2/a^2 + y^2/b^2 = 1$,
```math
\begin{align}
\left(\frac{y}{b}\right)^2 &= 1 - \left(\frac{x}{a}\right)^2\\
&= 1 - \sin^2 (E)\\
\therefore \frac{y}{b} &= \cos (E)
\end{align}
```
<br/>
<br/>

Therefore,
```math
\displaylines{
\begin{align}
x &= a\sin (E)\\
y &= b\cos (E)\\
\end{align}
} 
```
Now, translating the origin to the focus $O$,
```math
\displaylines{
\begin{align}
x &= a\sin (E) - ae\\
y &= b\cos (E)\\
&= a\sqrt{1 - e^2}\sin (E)
\end{align}
\tag{19}
} 
```
Additionally, by the Pythagorean theorem then,
```math
\begin{align}
r^2 &= (a\cos (E) - ae)^2 + (a\sqrt{1 - e^2}\sin (E))^2\\
&= a^2 \cos^2 (E) - 2a^2e\cos (E) + a^2e^2 + a^2(1 - e^2) \sin^2 (E)\\
&= a^2 \cos^2 (E) - 2a^2e\cos (E) + a^2e^2 + (a^2 - a^2e^2)(1 - \cos^2 (E)) \\
&= a^2 \cos^2 (E) - 2a^2e\cos (E) + a^2e^2 + a^2 - a^2\cos^2 (E) - a^2e^2 + a^2e^2\cos^2 (E) \\
&= a^2 - 2a^2e\cos (E) + a^2e^2\cos^2 (E)\\
&= (a - ae\cos (E))^2\\
\therefore r &= a(1 - e\cos (E)) \tag{20}
\end{align}
```
Let's now relate $\nu$ with $E$. Putting $C$ as the origin again,
```math
\begin{align}
\cos (E) &= \frac{x}{a} = \frac{ae + r \cos (\nu)}{a} = e(1 - e\cos (E))\cos(\nu)\\
\therefore \cos (E) &= \frac{e + \cos(\nu)}{1 + e\cos(\nu)}\tag{21}\\
\end{align}
```

### Kepler's second law
Let us now determine how to find the eccentric or true anomaly at any point in time, thus finally allowing us to determine the position of the planets. Kepler's second law will come in handy here.

Kepler's second law states that an object moves faster when it is closer to the primary, in a way that the area sweeped out by the object per unit time is constant. That is, the true anomaly increases faster when the object is near the periapsis. We can intuitively see why an object would move faster when it is near the periapsis: an object moving closer to the primary under the influence of gravity means that it is, in a sense, falling towards the primary, and therefore would obviously gain speed. Indeed, iin the proof of Kepler's first law we showed that:
```math
\textbf{r}\times\textbf{v} = \textbf{h}
```

where $\textbf{h}$ is a constant vector, $\textbf{r}$ is the object's position with the primary at the origin, and $\textbf{v}$ is its velocity. This means that if the magnitude of $\textbf{r}$ decreases, i.e. the distance between the primary and the object decreases, then the magnitude of $\textbf{v}$, i.e. the object's speed, must increase (because $\textbf{h}$ must be constant). The property $\textbf{r}\times\textbf{v} = \textbf{h}$ is known as the [conservation of angular momentum](https://en.wikipedia.org/wiki/Angular_momentum#Conservation_of_angular_momentum).

But dealing with differential vector equations is hardly appealing. So let us approach this problem from another perspective. Let's first flaunt all of Kepler's laws and assume that the planet moves along a circular orbit at a uniform speed. Then, the true anomaly equals the eccentric anomaly and also equals:
```math
\frac{360\degree}{T}\cdot t \tag{22}
```
Where $t$ is the time elapsed since periapsis. We call this quantity the [*mean anomaly*](https://en.wikipedia.org/wiki/Mean_anomaly) and is denoted $M$. Now let's account for Kepler's second law. Fortunately, there is a very easy relation between the mean and eccentric anomalies: they can be related to each other by [Kepler's equation](https://en.wikipedia.org/wiki/Kepler%27s_equation):
```math
M = E - e\sin (E) \tag{23}
```
#### Example 4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The orbital period of the Earth $T = 365\text{ dy}\enspace5h\enspace48m\enspace46s$, and the eccentricity of its orbit is $0.0167$. <br/>
Additionally, when it is at periapsis, its heliocentric ecliptic longitude is $102\degree\enspace56'\enspace49.9''$. <br/>
Given that the time of perihelion in $2024$ was $\text{January 3, }2024\enspace 00:38$, <br/>
calculate the time of Spring Equinox in the Northern Hemisphere in $2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Because ecliptic coordinates are based on the Earth's orbital plane, it effectively is equal to the Earth's perifocal coordinate frame, except that the $x$-axis is rotated from the location of perihelion to Aries. Therefore, we can use our equations.

Spring Equinox in the Northern Hemisphere is defined as $\lambda_{\text{Geocentric}}\text{ of the Sun } = 0\degree$, therefore (by equation $5$) it occurs when $\lambda_{\text{Heliocentric}}\text{ of the Earth } = 180\degree$. Thus, the true anomaly of the Earth at the time of Northern Spring Equinox is:
```math
\begin{align}
\nu &= 180\degree - 102\degree\enspace56'\enspace49.9''\\
&= 77\degree\enspace3'\enspace50.1''
\end{align}
```
Now, by equation $21$:
```math
\begin{align}
\cos (E) &= \frac{e + \cos(\nu)}{1 + e\cos(\nu)}\\
&= \frac{0.0167 + \cos(77\degree\enspace3'\enspace50.1'')}{1 + 0.0167\cos(77\degree\enspace3'\enspace50.1'')}\\
&= 0.239855411\\
\therefore E &= 76\degree\enspace7'\enspace19.18''
\end{align}
```
Now, by Kepler's equation (equation $23$):
```math
\begin{align}
M &= E - e\sin (E)\\
&= 76\degree\enspace7'\enspace19.18'' - 0.0167 \sin (76\degree\enspace7'\enspace19.18'')\\
&= 76\degree\enspace6'\enspace20.81''
\end{align}
```
Therefore, by the definition of $M$ (equation $22$):
```math
\begin{align}
M &= \frac{360\degree}{T}\cdot t\\
\therefore t &= \frac{TM}{t}\\
&=\frac{365\text{ dy}\enspace5h\enspace48m\enspace46s \cdot 6\degree\enspace6'\enspace20.81''}{360\degree}\\
&= 77\text{ dy}\enspace5h\enspace8m.
\end{align}
```
$77\text{ dy}\enspace5h\enspace8m$ after $\text{January 3, }2024\enspace00:38$ is $\text{March 20, }2024\enspace05:46$.\
Comparing to the true time ($\text{March 20, }2024\enspace03:07$), we can see that we are very close. The discrepancy comes from rounding error and the fact that the motion of the Earth is not a true two body problem.\
$\blacksquare$

However what we really want is the reverse operation of example $4$: going from a specific time to a location. (Continued..)
