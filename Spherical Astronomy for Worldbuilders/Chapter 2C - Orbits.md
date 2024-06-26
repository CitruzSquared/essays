(Continued from Part B...)

### Orientation of Orbits in 3D Space
In examples $2.3$ and $2.4$, we have calculated the position of the Earth in ecliptic coordinates, which was simple because the Earth's perifocal plane was the definition of the Ecliptic plane. Other planets are not so simple. Let:
```math
\displaylines{
\begin{align}
&(p, q, s) \text{ denote the perifocal cartesian coordinates of an object, and}\\
&(x, y, z) \text{ denote the heliocentric ecliptic cartesian coordinates of the object}
\end{align}
}
```

#### Orbital Elements

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/22bef238-757a-4561-8d17-3b41dbf22c5b" width="350"/> This diagram depicts the orbit of a non-Earth planet $Q$ where $O$ is the location of the Sun and $P$ is the periaetas of the orbit. The direction of orbit is given by the arrow pointing from $P$ to $Q$. Thus the true anomaly $\nu$ of $Q$ is the angle $POQ$.

As one can see, the orbit is tilted upwards from the Ecliptic plane by an angle $i$, and therefore forms a line of intersection. The angle $i$ is called the [*inclination*](https://en.wikipedia.org/wiki/Orbital_inclination), and the line where the orbit crosses the ecliptic plane (the line $ND$) is known as the [*line of nodes*](https://en.wikipedia.org/wiki/Orbital_node). The point on the line of nodes where the planet is moving upwards (point $N$) is called the *ascending node* and the other point is known as the *descending node* (point $D$).

The angle $AON$ is known as the [*longitude of the ascending node*](https://en.wikipedia.org/wiki/Longitude_of_the_ascending_node) and is denoted $\Omega$, and the angle $NOP$ is known as the [*argument of periaetas*](https://en.wikipedia.org/wiki/Argument_of_periaetas) and is denoted $\omega$. Then, remembering that the $x$-axis in the ecliptic frame points towards Aries, and that the $p$-axis in the perifocal frame points towards the periaetas, the ecliptic frame can be transformed into the perifocal frame by the procedure below:
```math
\displaylines{
\begin{align}
\text{1. } & \text{Rotate the ecliptic in the direction of the orbit plane by } \Omega.\\
\text{2. } & \text{Then, rotate it upwards by } i.\\
\text{3. } & \text{Then, rotate it in the direction of the orbit by } \omega.\\
\end{align}
}
```
This can be done with rotation matrices:
- Step 1 - we rotate by $\Omega$ about the $z$-axis.
```math
R_1 =
\begin{bmatrix}
\cos{(\Omega)} & \sin{(\Omega)}  & 0\\
-\sin{(\Omega)} & \cos{(\Omega)} & 0\\
0 & 0 & 1
\end{bmatrix}
```
- Step 2 - we rotate by $i$ about the $x$-axis (which now points in the direction of the ascending node).
```math
R_2 =
\begin{bmatrix}
1 & 0 & 0\\
0 & \cos{(i)} & \sin{(i)}\\
0 & -\sin{(i)} & \cos{(i)}
\end{bmatrix}
```
- Step 3 - we rotate by $\omega$ about the $z$-axis (which now points perpendicular to the orbital plane).
```math
R_3 =
\begin{bmatrix}
\cos{(\omega)} & \sin{(\omega)}  & 0\\
-\sin{(\omega)} & \cos{(\omega)} & 0\\
0 & 0 & 1
\end{bmatrix}
```
Now the $x$-axis points towards the periapsis.

The full rotation matrix is given by multiplying all these steps together:
```math
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
=
R_3 R_2 R_1
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
```
Actually carrying out the matrix multiplication, this is:
```math
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
=
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega  &  \sin i \sin\omega \\
  -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega &\sin i \cos\omega \\
   \sin\Omega \sin i  &  -\cos \Omega \sin i  & \cos i
 \end{bmatrix}

\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
\tag{2.24}
```
The reverse transformation, going from the perifocal frame to the ecliptic frame, is given by the transpose of $R_3 R_2 R_1$:
```math
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
=
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & \sin\Omega \sin i \\
  \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega & -\cos \Omega \sin i \\
  \sin i \sin\omega & \sin i \cos\omega &  \cos i
 \end{bmatrix}
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
\tag{2.25}
```
Thus the exact position of $Q$ can be calculated in ecliptic coordinates from the values $a, e, i, \Omega$, and $\omega$ and these are called the [**orbital elements**](https://en.wikipedia.org/wiki/Orbital_elements) of $Q$.

However, if we recognize the fact that $s$ is almost always going to be $0$ in our case (because planets move in the plane of their orbit, there will be almost no cases where we *do* have a $s$ component), we can safely say that, when going from perifocal coordinates to ecliptic coordinates:
```math
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
=
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & 0 \\
  \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega & 0 \\
  \sin i \sin\omega & \sin i \cos\omega & 0
 \end{bmatrix}
\begin{bmatrix}
p \\ q \\ 0
\end{bmatrix}
\tag{2.26}
```

Note that, for the Earth, since $i = 0\degree$, $\Omega$ and $\omega$ are on the same plane, and therefore only their sum matters, and as long as $\Omega$ and $\omega$ sum to the same number, their actual values do not matter and the results of equations $2.24$ to $31$ will not change.

#### Example 2.5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given the orbital elements of Mars and that Mars was last at perihelion on $\text{June 21, } 2022$, <br/> 
calculate its heliocentric ecliptic coordinates on $\text{March 19, }2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Mars' orbital elements are given as:
```math
\begin{align}
a &= 227.939 \text{ Gm}\\
e &= 0.0934\\
i &= 1\degree\:51'\\
\Omega &= 47\degree\:34'\:42.7''\\
\omega &= 286\degree\:30'\\
\end{align}
```
We first need the mean anomaly of Mars, which involves finding the oribital period $T$. By equation $2.10$:
```math
\begin{align}
 T &= \sqrt{\frac{4\pi^2 (227.939 \cdot 10^9)^3}{6.67\cdot10^-11 \cdot 1.989\cdot10^30}}\\
&= 687 \text{ dy}
\end{align}
```
Now we follow example $2.4$.\
Since $\text{March 20, }2024$ is $637$ days after $\text{June 21, } 2022$, by equation $2.20$:
```math
\begin{align}
M &= \frac{2\pi}{687 \text{ dy}}\cdot 637\text{ dy}\\
&= 5.8258938 \text{ rad}
\end{align}
```
Now we iterate equation $2.23$:
```math
\begin{array}{cccc}\hline n & & & E_n \\ \hline
1 & & & 5.8258938 \\
2 & & & 5.7808839 \\
3 & & & 5.7809308 \\
4 & & & 5.7809308 \\ \hline
\end{array}
```
Thus, by equation $2.14$, the perifocal coordinates are:
```math
\begin{align}
p &= 227.939 \cos(5.7809308) - 227.939 \cdot 0.0934\\
&= 178.499 \text{ Gm}\\
q &= 227.939\sqrt{1 - 0.0934^2} \sin(5.7809308)\\
&= -109.251 \text{ Gm}\\
s &= 0 \text{ Gm}
\end{align}
```
Since Mars's orbit is not on the ecliptic plane, we must use equation $2.26$.\
We first fill out the matrix:
```math
\begin{align}
\cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega &= 0.913721676036\\
-\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega &= 0.405596690451\\
\sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega &= −0.405159938675\\
-\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega &= 0.914006157892\\
\sin i \sin\omega &= −0.0309535593079\\
\sin i \cos\omega &= 0.00916886198411
\end{align}
```
Thus, by equation $2.26$:
```math
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
=
 \begin{bmatrix}
0.913721676036 & 0.405596690451 & 0 \\
−0.405159938675 & 0.914006157892 & 0 \\
−0.0309535593079 & 0.00916886198411 & 0
 \end{bmatrix}
\begin{bmatrix}
178.499 \\ -109.251 \\ 0
\end{bmatrix}
=
\begin{bmatrix}
118.787 \\ −172.177 \\ −6.527
\end{bmatrix}
\:[\text{Gm}]
```
$\blacksquare$

In order to get geocentric coordinates, which we will denote by $(\xi, \eta, \zeta)$, we simply subtract the Earth's cartesian coordinates from the target's.
```math
 \begin{bmatrix}
\xi_{\text{Planet}} \\ \eta_{\text{Planet}} \\ \zeta_{\text{Planet}}
 \end{bmatrix}
=
 \begin{bmatrix}
x_{\text{Planet}}\\ y_{\text{Planet}}\\ z_{\text{Planet}}
 \end{bmatrix}
-
 \begin{bmatrix}
x_{\text{Earth}}\\ y_{\text{Earth}}\\ z_{\text{Earth}}
 \end{bmatrix}
\tag{2.27}
```
Considering that $(x_{\text{Sun}}, y_{\text{Sun}}, z_{\text{Sun}}) = (0, 0, 0)$, equation $2.26$ proves equation $1.5$.

For the Moon, because it orbits the Earth and not the Sun, the perifocal frame is around the Earth, and equation $2.26$ would give the geocentric coordinates already, therefore equation $2.27$ is not needed.

### Calculating the Ephemeris for a Planet
We've come a long way. Let's put it all together.

**Algorithm to calculate the ephemeris of a planet:**
1. Assign orbital elements to the Earth and the target planet.
2. Choose a time $t$.
3. Calculate where the planet would be along its orbit at this time using equations $2.20$, $2.21$, and $2.14$.
4. Transform this to heliocentric ecliptic cartesian coordinates by equation $2.26$.
5. Repeat step $3$ and $4$ for the Earth.
6. Calculate the geocentric ecliptic cartesian coordinates of the planet by equation $2.27$.
7. Use equations $1.2$ and $1.3$ to convert to spherical coordinates, either ecliptic or equatorial.
8. Increment $t$ by some amount $\Delta t$ and repeat steps $3$ to $7$.

#### Example 2.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Calculate Mars' geocentric <i>equatorial</i> coordinates on $\text{March 19, }2024$. <br/>
 Use $\varepsilon = 23.44\degree$ for the Earth.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Recall example $2.4$ where we calculated Earth's perifocal coordinates on this date. Using equation $2.26$ with
```math
\begin{align}
\Omega &= 0\degree\\
\omega &= 102\degree\:56'\:49.9''\\
i &= 0\degree
\end{align}
```
(Remember, only the sum $\Omega + \omega$ matters for the Earth) we get for $(x_{\text{Earth}}, y_{\text{Earth}}, z_{\text{Earth}})$:
```math
\begin{bmatrix}
x_{\text{Earth}} \\ y_{\text{Earth}} \\ z_{\text{Earth}}
\end{bmatrix}
=
 \begin{bmatrix}
-0.224052873866 & -0.974576990141 & 0 \\
0.974576990141 & −0.224052873866 & 0 \\
0 & 0 & 0
 \end{bmatrix}
\begin{bmatrix}
33.384 \\ 145.213 \\ 0
\end{bmatrix}
=
\begin{bmatrix}
-149.001 \\ 0 \\ 0
\end{bmatrix}
\:[\text{Gm}]
```
Therefore, using this new result and the result of example $2.5$, by equation $2.27$:
```math
 \begin{bmatrix}
\xi_{\text{Mars}} \\ \eta_{\text{Mars}} \\ \zeta_{\text{Mars}}
 \end{bmatrix}
=
\begin{bmatrix}
118.787 \\ −172.177 \\ −6.527
\end{bmatrix}
-
\begin{bmatrix}
-149.001 \\ 0 \\ 0
\end{bmatrix}
=
\begin{bmatrix}
267.788 \\ -172.177 \\ -6.527
\end{bmatrix}
\:[\text{Gm}]
```
We need equatorial coordinates, so by equation $1.3$:
```math
\begin{bmatrix}
\xi_{\text{Mars; equatorial}} \\ \eta_{\text{Mars; equatorial}} \\ \zeta_{\text{Mars; equatorial}}
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos{(23.44\degree)} & -\sin{(23.44\degree)} \\
0 & \sin{(23.44\degree)} & \cos{(23.44\degree)}
\end{bmatrix}
\begin{bmatrix}
267.788 \\ -172.177 \\ -6.527
\end{bmatrix}
=
\begin{bmatrix}
267.788 \\ -155.372 \\-74.478
\end{bmatrix}
\:[\text{Gm}]
```
Then, by equation $1.2$:
```math
\begin{align}
\rho &= \sqrt{267.788^2 + (-155.372)^2 + (-74.478)^2}\\
&= 318.430 \text{ Gm} \\
&= 2.128 \text{ AU}\\
\alpha &= \arctan(-155.372, 267.788) \\
&= 21^h\:59^m\:30.59^s\\
\delta &= \arcsin \left(\frac{-74.478}{\rho}\right) \\
&= -13\degree\:31'\:34.55''\\
\end{align}
```
Comparing this to the true value of
```math
\begin{align}
\rho &= 2.136\text{ AU}\\
\alpha &= 21^h\:59^m\:47^s\\
\delta &= -13\degree\:29'\:50''\\
\end{align}
```
We can see we were very close considering we ignored all perturbation.\
Using this method, we can compute an ephemeris for any planet we want in our Solar System.\
Keep in mind that for the Moon, because it orbits the Earth, equation $2.26$ gives the geocentric coordinates directly.
$\blacksquare$
