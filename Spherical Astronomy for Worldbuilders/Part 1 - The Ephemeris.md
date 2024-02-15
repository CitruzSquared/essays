## Introduction
**Astrology**, which is a method of divination based on the location of the stars and planets in the sky, can be a very important part of worldbuilding. The basis of astrology is *Spherical Astronomy*, the science of observing the sky. This post will serve as a guide to spherical astronomy for the worldbuilder, and will start from the basics and build up to calculating the location of stars in the sky and finally a complete ephemeris, from which the worldbuilder can create their own astrological system.

# Part 1. The Ephemeris
An [ephemeris](https://en.wikipedia.org/wiki/Ephemeris) (plural *ephemerides*) is a table listing the locations of celestial objects at specific times. Let us see how to calculate the ephemeris.

## I. Coordinates
Let us begin by talking about how objects are even located in space.

### The Celestial Sphere
The most important thing in spherical astronomy is the location of celestial objects as seen from Earth. From the Earth, the sky appears to be a great dome all around us, and this is called the [Celestial Sphere](https://en.wikipedia.org/wiki/Celestial_sphere). This is a large sphere of arbitrary radius (commonly just put to 1) that surrounds the Earth that all the stars and planets are projected onto. There are two lines (circles in actuality) of great importance on the Celestial Sphere.

- **The [Celestial Equator](https://en.wikipedia.org/wiki/Celestial_equator)**
  * This is the circle on the celestial sphere obtained by projecting the Earth's equator onto the celestial sphere. If one were standing on the equator of the Earth, the celestial equator would appear to be a great circle passing right above the observer, going from East to West.
- **The [Ecliptic](https://en.wikipedia.org/wiki/Ecliptic)**
  * This is the circle the Sun appears to make in the sky over the course of a year. In other words, it is the *plane of the orbit of the Earth*. Due to the axial tilt ($\varepsilon$) of $23.44\degree$ of the Earth, the ecliptic and the celestial equator make an angle of $23.44\degree$ in the sky. Because the Solar System is more or less flat, all the planets, including the Moon, more or less lie on this ecliptic line.
 <br />
 
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3f19e0a6-0121-40a5-bd6d-9ccf522d8804" width="250"/> Because the ecliptic is tilted with respect to the equator, there are two points at which these two great circles meet. The point at which the ecliptic goes from being below the equator to above the equator is known as the [Cusp of Aries](https://en.wikipedia.org/wiki/First_point_of_Aries) (also known as the Vernal Equinox or the First Point of Aries), which, ironically, now lies in Pisces due to the slow (a period of about $26000$ years) precession of the axial tilt of the Earth. (*For the purposes of worldbuilding, this "axial precession" will be ignored.*) This point is of special importance as it is the place at which almost all angular measurements are made with respect to. This point is called the *Equinox point* because, if the Sun is located at it, the sun is passing directly over the equator, and the length of daytime will be exacly $1/2$ of a day ($12$ hours) all across the globe. The *Vernal* comes from the fact that, because the Sun is travelling towards the Northern direction, it is Spring time in the Northern Hemisphere when this event occurs (Vernal means Spring in Latin).

<br/>
<br/>

### Coordinate Axes
Evidently the best way to locate a point on the Celestial *Sphere* is with [*spherical* coordinates](https://en.wikipedia.org/wiki/Spherical_coordinate_system). This is a coordinate system based on three values:
```math
\begin{align}
\varphi &= \text{the vertical angle,}
\\ \theta &= \text{the horizontal angle,}
\\ \rho &= \text{the radius.}
\end{align}
```
$\rho$ is the distance from the origin to the point in question, $\theta$ is the angle East from North, and $\varphi$ is the angle of altitude from the $xy$-plane. (Note in mathematics and physics (and the diagram on Wikipedia), instead of $\varphi$ being the angle above the $xy$-plane, it is the complement of that angle, the angle down from the $z$-axis.) Thus, $\theta$ ranges from $0\degree$ to $360\degree$, and $\varphi$ from $-90\degree$ to $90\degree$.

This coordinate system can be thought of as the longitude-latitude system of Earth, where $\theta$ is the longitude, and $\varphi$ is the latitude.
Using trigonometry, one can find the radius of the latitude circle of a sphere with radius $\rho$ is $\rho \cos(\varphi)$ (View figure), so:
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6d9a1a2f-885a-4f94-98df-4e0814da6e90" width="250"/>

```math
\begin{align}
x &= \rho \cos(\varphi) \cos(\theta)
\\ y &= \rho \cos(\varphi) \sin(\theta) \tag{1}
\\ z &= \rho \sin(\varphi)
\end{align}
```
Where $x$, $y$, and $z$ are the cartesian coordinates of the point described by $\rho$, $\theta$, and $\varphi$.\
The reverse transformation, also derived by simple geometry, is given below:
```math
\begin{align}
\rho &= \sqrt{x^2 + y^2 + z^2}
\\ \theta &= \arctan(y, x) \tag{2}
\\ \varphi &= \arcsin(z / \rho)
\end{align}
```
Where $\arctan(y, x)$ is the [two argument arctangent](https://en.wikipedia.org/wiki/Atan2), used to avoid tangent ambiguity.

There are two coordinate systems in wide use. The [Equatorial Coordinate System](https://en.wikipedia.org/wiki/Equatorial_coordinate_system) and the [Ecliptic Coordinate System](https://en.wikipedia.org/wiki/Ecliptic_coordinate_system). 

- [**The Equatorial Coordinate System**](https://en.wikipedia.org/wiki/Equatorial_coordinate_system)
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Right Ascension* and *Declination* and are denoted $\alpha$ and $\delta$ respectively.
   * The Right Ascension is measured in the plane of the Celestial Equator from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Celestial Equator such that positive is North.
   * The Right Ascension has a peculiar unit, the angle is measured by *hours*, *minutes*, and *seconds*, where $24$ hours is one revolution, $60$ minutes is one hour, and $60$ seconds is one minute.
   * The points of $+90\degree$ and $-90\degree$ Declination are called the *North* and *South* [*Celestial Poles*](https://en.wikipedia.org/wiki/Celestial_pole) respectively. These points can be thought of as the points in the sky right above True North and True South of Earth. From the view of an observer on the Earth, the celestial poles are always in the direction of North and South. Indeed, the reason the North Star always points North is because it is located so close to the North Celestial Pole (Declension $+89\degree 16'$).
- [**The Ecliptic Coordinate System**](https://en.wikipedia.org/wiki/Ecliptic_coordinate_system)
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Ecliptic Longitude* and *Ecliptic Latitude* and are denoted $\lambda$ and $\beta$ respectively.
   * The Ecliptic Longitude is measured in the plane of the Ecliptic from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Ecliptic such that positive is North.
   * By definition of the Ecliptic, the Ecliptic Latitude of the Sun is always $0\degree$.

### Coordinate Transformations
[Coordinate transformations](https://en.wikipedia.org/wiki/Astronomical_coordinate_systems#Converting_coordinates) between the three coordinate systems are given via rotation matrix multiplications.

- **Ecliptic to Equatorial:**
```math
\begin{bmatrix}
x_{\text{equatorial}} \\ y_{\text{equatorial}} \\ z_{\text{equatorial}}
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos{\varepsilon} & -\sin{\varepsilon} \\
0 & \sin{\varepsilon} & \cos{\varepsilon}  \tag{3}
\end{bmatrix}
\begin{bmatrix}
x_{\text{ecliptic}} \\ y_{\text{ecliptic}} \\ z_{\text{ecliptic}}
\end{bmatrix}
```
The $x$ coordinate stays the same as the ecliptic and equatorial coordinate systems have the same $x$-axis: the direction of Vernal Equinox.

- **Equatorial to Ecliptic:**
```math
\begin{bmatrix}
x_{\text{ecliptic}} \\ y_{\text{ecliptic}} \\ z_{\text{ecliptic}}
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos{\varepsilon} & \sin{\varepsilon} \\
0 & -\sin{\varepsilon} & \cos{\varepsilon}  \tag{4}
\end{bmatrix}
\begin{bmatrix}
x_{\text{equatorial}} \\ y_{\text{equatorial}} \\ z_{\text{equatorial}}
\end{bmatrix}
```
Again, the $x$ coordinate stays the same as the ecliptic and equatorial coordinate systems have the same $x$-axis: the direction of Vernal Equinox.

These cartesian coordinates can be transformed to spherical coordinates by equation $2$.

#### Example 1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On $\text{January }2,\:2024$, the Moon's right ascension was $11^{h}\enspace 19^{m}\enspace 30.12^{s}$ and its declination was $+07\degree\enspace 21'\enspace 42.9''.$ <br/>
 Calculate its ecliptic coordinates. (Use $\varepsilon = 23.44\degree$)<br>
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We first convert the sexagesimal notation to degrees:
```math
\begin{alignat}{3}
\alpha &= 11^{h}\enspace 19^{m}\enspace &&30.12^{s} &&= 169.8755\degree \\
\delta &= 07\degree\enspace 21'\enspace &&42.9'' &&= 7.3619\degree
\end{alignat}
```
Keeping in mind that $1^{h}$ is $360\degree/24 = 15\degree$.\
We then convert the equatorial coordinates given to equatorial cartesian coordinates ($\rho = 1$ because the celestial sphere is of arbitrary radius) using equation $1$:
```math
\begin{alignat}{2}
x &= \cos(\delta)\cos(\alpha) &&= -0.976313\\
y &= \cos(\delta)\sin(\alpha) &&= 0.174339\\
z &= \sin(\delta) &&= 0.128136
\end{alignat}
```
Next, we carry out the matrix multiplication (equation $4$):
```math
\begin{alignat}{3}
x_{\text{ecliptic}} &= 1 \cdot x + 0 \cdot y &&+ 0 \cdot z && = -0.976313 \\
y_{\text{ecliptic}} &= 0 \cdot x + \cos{\varepsilon} \cdot y &&+ \sin{\varepsilon} \cdot z &&= 0.210923 \\
z_{\text{ecliptic}} &= 0 \cdot x - \sin{\varepsilon} \cdot y &&+ \cos{\varepsilon} \cdot z &&= 0.0482118
\end{alignat}
```
We then convert to spherical coordinates with $\rho = 1$ using equation $2$.
```math
\begin{alignat}{2}
\lambda &= \arctan(0.210923,-0.976313) &&=  167\degree\enspace48'\enspace32.97''\\
\beta &= \arcsin(0.0482118/1) &&= \enspace\enspace2\degree\enspace45'\enspace48.24''
\end{alignat}
```
$\blacksquare$

The above coordinate systems are *geocentric* in nature, and these are the coordinates an ephemeris lists. However, in order to calculate the ephemeris, we must know the real locations of the planets, and since planets orbit the Sun, we need another set ocoordinates, the *Heliocentric Ecliptic Coordinates*. These are the same as the Ecliptic corodinates, the $x$-axis points towards Aries, and the $xy$-plane is the Earth's orbital plane (the Ecliptic), but it is centered on the Sun. Thus:
```math
\displaylines{
\begin{align}
\lambda_{\text{Geocentric}} \text{ of the Sun } &= \lambda_{\text{Heliocentric}} \text{ of the Earth } + 180\degree\\
\beta_{\text{Geocentric}} \text{ of the Sun } &= -\beta_{\text{Heliocentric}} \text{ of the Earth}
\end{align}
}\tag{5}
```

## II. Celestial Mechanics of the Planets
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
Therefore
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

Let us now calculate the [orbital period](https://en.wikipedia.org/wiki/Orbital_period) $T$ of a planet, given the orbital radius $r$.\
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
We can generalize this formula to elliptical orbits without issue.
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
Given that $G = 6.674\cdot10^{-11}\text{ m}^3\text{ kg}^{-1}\text{ s}^{-2}$, the mass of the sun $M_S = 1.989\cdot 10^{30} \text{ kg}$, the semi-major-axis of the orbit of the Earth $a = 1.496\cdot10^{11}\text{ m}$, and that $1\text{ dy} = 86\:000\text{ s}$, calculate the orbital period of the Earth in days.
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
