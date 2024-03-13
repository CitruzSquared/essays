# Part 3. Eclipses

## IX. Solar Eclipses

### Condition for Eclipse
A solar eclipse can only happen if the Moon and the Sun are in the sky in the same position, i.e. only at new Moon. Not all new moons result in a solar eclipse however, due to the inclination of the Moon's orbit to the Ecliptic.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/7bda2d9e-5464-4488-9f92-8359beaccd5c" width="250"/> Consider this diagram. In this diagram, the line $SN$ is the ecliptic and $MN$ is the orbit of the Moon, and therefore $N$ is the lunar orbital (descending) node. Therefore the Moon moves along $MN$ and the Sun moves along $SN$ at a slower pace. 

Say $M$ and $S$ are the positions of the Moon and Sun respectively at the time of ecliptic conjunction, and $M'$ and $S'$ are the positions of the Moon and Sun at their least true separation. 

<br/>

However, an easier way of looking at this is by fixing the Sun in one place and considering the *relative motion* of the Moon to the Sun.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1193b087-f038-455d-a898-a5e8db00faad" width="250"/> In this diagram, the Sun has been fixed in place, and therefore the Moon now travels along an altered orbit $MN'$. $M'$ is still the position of the Moon at its least true separation with the Sun.

Let us put
```math
\begin{align}
\beta &= \text{ The Moon's ecliptic latitude at conjunction }= SM\\
\Sigma &= \text{ The least true separation between the Sun and Moon }= SM'\\
I &= \text{ The inclination of the Moon's orbit to the ecliptic } = SNM\\
I' &= \text{ The inclination of the Moon's orbit to the ecliptic keeping the Sun fixed } = SN'M\\
\end{align}
```

Then, by geometry we have $MSM' = I'$. Therefore:
```math
\Sigma = \beta \cos(I') \tag{9.1}
```
But also,
```math
\tan(I') = \frac{SN}{SN'} \tan(I)
```
If we put
```math
\begin{align}
\sigma &= \text{ The Sun's motion in longitude}\\
\mu &= \text{ The Moon's motion in longitude}\\
t &= \text{ The time it takes for the Moon to reach the node}\\
\end{align}
```
Then,
```math
\begin{align}
SN &= \mu t\\
SN' &= (\mu - \sigma)t\\
\therefore \frac{SN}{SN'} &= \frac{\mu t}{\mu t - \sigma t}
\end{align}
```
Dividing both the numerator and denominator by $\sigma t$ and setting $\sigma /\mu = q$, we get:
```math
\begin{align}
\frac{SN}{SN'} &= \frac{q}{q - 1}\\
\therefore \tan(I') &= \frac{q}{q - 1} \tan(I) \tag{9.2}
\end{align}
```
The apparent least true separation from somewhere on the surface of the Earth may differ from $\Sigma$ however by up to the difference in parallax of the two bodies, so if we put:
```math
\begin{align}
\pi &= \text{ The Moon's equatorial horizontal parallax}\\
\pi' &= \text{ The Sun's equatorial horizontal parallax}\\
\end{align}
```
we get:
```math
\text{least apparent separation } = \Sigma - (\pi - \pi')
```
An eclipse will occur if this least apparent separation is less than the sum of the apparent radii of the Sun and the Moon (i.e. the Sun and the Moon overlap). If we put:
```math
\begin{align}
s &= \text{ The Moon's apparent radius}\\
s' &= \text{ The Sun's apparent radius}\\
\end{align}
```
We have in the case of eclipse:
```math
\Sigma - (\pi - \pi') < s + s'
```
or:
```math
\beta < (s + s' + \pi - \pi')\sec(I') \tag{9.3}
```
This is the condition for solar eclipse.
#### Example 9.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine if the new Moon of $\text{April, } 2024$ will result in a solar eclipse.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We can find via the method of example $4.4$ that the new Moon occured on $\text{April 8, } 2024$ at $18:21$. At this time:
```math
\begin{align}
\lambda_\text{Conjunction} &=19\degree\:4'\:12.19''\\
\beta_\text{Moon} &= 0\degree\:20'\:52.53''\\
\Delta_\text{Moon} &= 359\:807.95 \text{ km}\\
\Delta_\text{Sun} &= 149\:823\:425.56\text{ km}
\end{align}
```
Also:
```math
\begin{align}
\text{Earth's equatorial Radius } &=6378.137 \text{ km}\\
\text{Moon's Radius } &= 1737.4 \text{ km}\\
\text{Sun's Radius } &= 696\:000 \text{ km}\\
I &= 5.14\degree
\end{align}
```
Thus by equations $4.1$ and $8.6$:
```math
\begin{alignat}{2}
s &= \arcsin\left(\frac{1737.4}{359\:807.95}\right) &&= 16'\:35.99''\\
s' &= \arcsin\left(\frac{696\:000}{149\:823\:425.56}\right) &&= 15'\:58.2''\\
\pi &= \arcsin\left(\frac{6378.137}{359\:807.95}\right) &&= 1\degree\:0'\:56.55''\\
\pi' &= \arcsin\left(\frac{6378.137}{149\:823\:425.56}\right) &&= 8.78''
\end{alignat}
```
To determine $q$, we need $\sigma$ and $\mu$, the derivatives of longitude of the Sun and Moon. We take one hour as the time step.\
At $19:21$:
```math
\begin{align}
\lambda_{\text{Moon}} &=19\degree\:41'\:40.88''\\
\therefore \mu &= \frac{19\degree\:41'\:40.88'' - 19\degree\:4'\:12.19''}{1h} = 37.48'/h\\
\lambda_{\text{Sun}} &=19\degree\:6'\:34.7''\\
\therefore \sigma &= \frac{19\degree\:6'\:34.7'' - 19\degree\:4'\:12.19''}{1h} = 2.38'/h\\
\end{align}
```
Therefore:
```math
\begin{align}
q &= \frac{37.48}{2.38} = 15.7479\\
\therefore I' &= \arctan\left(\frac{15.7479}{15.7479 - 1} \tan(5.14\degree)\right) = 5.486\degree
\end{align}
```
Therefore:
```math
\begin{align}
(s + s' + \pi - \pi')\sec(I') &= (16'\:35.99'' + 15'\:58.2'' + 1\degree\:0'\:56.55'' - 8.78'')\sec(5.486\degree) \\
&=1\degree\:33'\:47.73''
\end{align}
```
Which is greater than $\beta_\text{Moon}$ at conjunction. Therefore, a solar eclipse will occur.

There is a shorter way of doing this: we can precalculate the minimum possible value of $(s + s' + \pi - \pi')\sec(I')$, and if $\beta_\text{Moon}$ at conjunction is less than this minimum value, a solar eclipse must surely occur. We can also precalculate the maximum possible value of $(s + s' + \pi - \pi')\sec(I')$, and if $\beta_\text{Moon}$ at conjunction is greater than this maximum value, a solar eclipse will surely not occur. If it is in between these two values, the full calculation is required.\
$\blacksquare$

### Direction of the Shadow
The shadow of the Moon points in the direction of the Moon from the Sun. Thus, if we say that:
```math
\begin{align}
v, u, w &= \text{The geocentric equatorial cartesian coordinates of the Moon}\\
v', u', w' &= \text{The geocentric equatorial cartesian coordinates of the Sun}
\end{align}
```
We have for the coordinates of the Sun from the Moon:
```math
(v' - v, u' - u, w' - w)
```
And thus if we convert these to spherical coordinates:
```math
\begin{align}
G \cos(d) \cos(a) &= v' - v\\
G \cos(d) \sin(a) &= u' - u\\
G \sin(d) &= w' - w
\end{align}
```
We have the direction of the shadow of the Moon in equatorial spherical coordinates as right ascension $a$ and declination $d$, and $G$ is the distance from the Moon to the Sun.

### Position of the Observer relative to the Shadow

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/cd42ee6a-6c20-4031-bf9a-021b7d883cec" width="350"/> Consider this diagram. Here, $O$ is the center of the Earth, $P$ is the celestial North pole, and $M$ and $S$ are the true positions of the center of the Moon and Sun. $M'$ and $S'$ are their positions projected on to the celestial sphere. Thus, $SM$ is the shadow.

We define a coordinate system as such: Let the origin be the center of the Earth, $z$-axis point in the direction of the shadow $SM$, the $y$-axis perpendicular to the $z$-axis such that it points towards North, and the $x$ axis perpendicular to both such that it points to the point on the celestial equator with right ascension $a + 90\degree$.

In this coordinate system, the $xy$-plane is known as the *fundamental plane*, and the point at which the shadow meets the fundamental plane is $F$.

To convert from the equatorial coordinate frame to the fundamental frame, we first rotate the equatorial frame by $a + 90\degree$ about the $z$-axis to align the $x$-axis:
```math
R_1 = \begin{bmatrix}
\cos(a + 90\degree) & \sin(a + 90\degree) & 0 \\
-\sin(a + 90\degree) & \cos(a + 90\degree) & 0 \\
0 & 0 & 1
\end{bmatrix}
```
Then we rotate by $d + 90\degree$ about the $x$-axis to align the $z$-axis with the shadow while keeping the $y$-axis pointed towards North.
```math
R_2 = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(d + 90\degree) & \sin(d + 90\degree) \\
0 & -\sin(d + 90\degree) & \cos(d + 90\degree)
\end{bmatrix}
```
The total rotation is the product of the two matrices:
```math
R = R_2R_1 = \begin{bmatrix}
-\sin(a) & \cos(a) & 0\\
\cos(a) \sin(d) & \sin(a) \sin(d) & \cos(d) \tag{9.4} \\
\cos(a) \cos(d) & \sin(a) \cos(d) & -\sin(d)
\end{bmatrix}
```
We can now express the coordinates of both the Moon and observer in this new system. Let:
```math
\begin{align}
x, y, z &= \text{The geocentric fundamental cartesian coordinates of the Moon}\\
\xi, \eta, \zeta &= \text{The geocentric fundamental cartesian coordinates of the observer}
\end{align}
```
Then:
```math
\begin{align}
\begin{bmatrix}
x\\y\\z
\end{bmatrix} &= R \begin{bmatrix}
v\\ u\\ w
\end{bmatrix}\\
\tag{9.5}\\
\begin{bmatrix}
\xi\\\eta\\\zeta
\end{bmatrix} &= R \begin{bmatrix}
\rho \cos(\phi')\cos(\Theta_L)\\
\rho \cos(\phi')\sin(\Theta_L) \\ 
\rho \sin(\phi')
\end{bmatrix}
\end{align}
```
Where $\rho$ is the radius of the Earth at geocentric latitude $\phi'$.\
These equations, letting $r, \alpha, \delta$ be the geocentric spherical equatorial coordinates of the Moon, expand to (using angle addition formulae to simplify):
```math
\begin{align}
x &= r \cos(\delta) \sin(\alpha - a) \\
y &= r [\sin(\delta)\cos(d) - \cos(\delta)\sin(d)\cos(\alpha - a)] \tag{9.6}\\
z &= r [\sin(\delta)\sin(d) + \cos(\delta)\cos(d)\cos(\alpha - a)] \\
\end{align}
```
and
```math
\begin{align}
\xi &= \rho \cos(\phi') \sin(\Theta_L - a) \\
\eta &= \rho [\sin(\phi')\cos(d) - \cos(\phi')\sin(d)\cos(\Theta_L - a)] \\
\zeta &= \rho [\sin(\phi')\sin(d) + \cos(\phi')\cos(d)\cos(\Theta_L - a)] \\
\end{align}
```
But $\Theta_L - a$ is the local hour angle of the point $Z$ (the point pointing in the direction of the shadow), which we will denote by $h$, therefore:
```math
\begin{align}
\xi &= \rho \cos(\phi') \sin(h) \\
\eta &= \rho [\sin(\phi')\cos(d) - \cos(\phi')\sin(d)\cos(h)] \tag{9.7}\\
\zeta &= \rho [\sin(\phi')\sin(d) + \cos(\phi')\cos(d)\cos(h)] \\
\end{align}
```
The inverse transformation is given by the transpose of $R$:
```math
R^{-1} = R^T = \begin{bmatrix}
-\sin(a) & \cos(a) \sin(d) & \cos(a) \cos(d)\\
\cos(a) & \sin(a) \sin(d) & \sin(a) \cos(d) \tag{9.7} \\
0 & \cos(d) & -\sin(d)
\end{bmatrix}
```

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/23f53b50-7d4e-4737-a573-1c400ea75c00" width="350"/> On the fundamental plane, the situation looks like this diagram: where the shadow of the Moon is centered on $M_1$, the projection of $(x, y, z)$ onto the fundamental plane, and the observer is at $C_1$, the projection of $(\xi, \eta, \zeta)$ on the fundamental plane.

The distance between the shadow and the observer $\Delta$ is given by:
```math
\Delta^2 = (x - \xi)^2 + (y - \eta)^2 \tag{9.8}
```
Which can also be expressed as:
```math
\displaylines{
\begin{align}
\Delta \cos(Q) &= x - \xi\\
\Delta \sin(Q) &= y - \eta
\end{align}
}\tag{9.9}
```
Where $Q$ is the angle $NC_1M_1$. By geometry, this is also $PZM'$ from the previous diagram.

### The Size of the Shadow
