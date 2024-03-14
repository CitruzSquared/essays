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
\lambda_{\text{Sun}} &=19\degree\:6'\:34.7''
\end{align}
```
Therefore:
```math
\begin{align}
\mu &= \frac{19\degree\:41'\:40.88'' - 19\degree\:4'\:12.19''}{1h} = 37.48'/h\\
\sigma &= \frac{19\degree\:6'\:34.7'' - 19\degree\:4'\:12.19''}{1h} = 2.38'/h
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

### Partial Total, and Annular Eclipses

<p align="center">
  <img width="600" src="https://github.com/CitruzSquared/essays/assets/23460281/1d634c03-a53b-4d23-90ab-56df30abf0fc"> <br/>
</p>

Any object illuminated by a non-point source casts two shadows: *penumbral* and *umbral*. In the diagram above, the penumbral shadow cast by the Moon ($M$) is shown by regions $A$ and $B$. An observer in these regions sees the Moon slightly offset from the Sun ($S$) and so only sees a part of the Sun covered by the Moon. This is known as a *partial solar eclipse* (see leftmost figure below).

The umbral region is marked by regions $C$ and $D$. An observer in region $C$ cannot see the Sun at all since it is completely blocked by the Moon. This is known as a *total solar eclipse* (usually, the corona (the outer atmosphere) of the Sun is still visible; see middle figure below). In region $D$, the Moon still coveres the center of the Sun but does not appear large enough to cover all of it. Therefore the Sun looks like a glowing ring around the Moon, and therefore this is known as an *annular solar eclipse* (see rightmost figure below).

On our Earth, our Moon is just at the perfect distance where the orbital eccentricity allows the Moon to be both close enough and far enough to create all three partial, total, and annular solar eclipses (and sometimes a total eclipse becomes annular halfway through or vice versa, this is known as a *hybrid solar eclipse*). This is not true for the vast majority of planets: Mars with its two small moons only experiences annular and partial solar eclipses.

<p align="center">
  <img width="600" src="https://github.com/CitruzSquared/essays/assets/23460281/8d22bfd0-acef-48a7-9fea-894b6a7043b5"> <br/>
  Left: Partial Solar Eclipse. Center: Total Solar Eclipse. Right: Annular Solar Eclipse.
</p>

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
G \cos(d) \sin(a) &= u' - u \tag{9.4}\\
G \sin(d) &= w' - w
\end{align}
```
We have the direction of the shadow of the Moon in equatorial spherical coordinates as right ascension $a$ and declination $d$, and $G$ is the distance from the Moon to the Sun.

### Position of the Shadow and the Observer
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/23c9a897-b36b-4c97-b15b-14ba270cfee5" width="350"/> Consider this diagram. Here, $O$ is the center of the Earth, $P$ is the celestial North pole, and $M$ and $S$ are the true positions of the center of the Moon and Sun. $M'$ and $S'$ are their positions projected on to the celestial sphere. Thus, $SM$ is the shadow.

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
Then we rotate by $90\degree - d$ about the $x$-axis to align the $z$-axis with the shadow while keeping the $y$-axis pointed towards North.
```math
R_2 = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(90\degree - d) & \sin(90\degree - d) \\
0 & -\sin(90\degree - d) & \cos(90\degree - d)
\end{bmatrix}
```
The total rotation is the product of the two matrices:
```math
R = R_2R_1 = \begin{bmatrix}
-\sin(a) & \cos(a) & 0\\
-\cos(a) \sin(d) & -\sin(a) \sin(d) & \cos(d) \tag{9.5}\\
\cos(a) \cos(d) & \sin(a) \cos(d) & \sin(d)
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
\begin{bmatrix}
x\\y\\z
\end{bmatrix} = R \begin{bmatrix}
v\\ u\\ w
\end{bmatrix} \enspace\enspace \text{ and } \enspace\enspace
\begin{bmatrix}
\xi\\\eta\\\zeta
\end{bmatrix} = R \begin{bmatrix}
\rho \cos(\phi')\cos(\Theta_L)\\
\rho \cos(\phi')\sin(\Theta_L) \\ \tag{9.6}
\rho \sin(\phi')
\end{bmatrix}
```
Where $\rho$ is the radius of the Earth at geocentric latitude $\phi'$.\
Let's expand the second of these equations (using angle addition formulae to simplify):
```math
\begin{align}
\xi &= \rho \cos(\phi') \sin(\Theta_L - a) \\
\eta &= \rho [\sin(\phi')\cos(d) - \cos(\phi')\sin(d)\cos(\Theta_L - a)] \\
\zeta &= \rho [\sin(\phi')\sin(d) + \cos(\phi')\cos(d)\cos(\Theta_L - a)] 
\end{align}
```
But $\Theta_L - a$ is the local hour angle of the point $Z$ (the point pointing in the direction of the shadow), which we will denote by $\theta$ (note that some other sources denote it by $\mu$), therefore:
```math
\begin{align}
\xi &= \rho \cos(\phi') \sin(\theta) \\
\eta &= \rho [\sin(\phi')\cos(d) - \cos(\phi')\sin(d)\cos(\theta)] \tag{9.7}\\
\zeta &= \rho [\sin(\phi')\sin(d) + \cos(\phi')\cos(d)\cos(\theta)] 
\end{align}
```
The inverse transformation is given by the transpose of $R$:
```math
R^{-1} = R^T = \begin{bmatrix}
-\sin(a) & \cos(a) \sin(d) & \cos(a) \cos(d)\\
\cos(a) & \sin(a) \sin(d) & \sin(a) \cos(d) \tag{9.8} \\
0 & \cos(d) & -\sin(d)
\end{bmatrix}
```

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/23f53b50-7d4e-4737-a573-1c400ea75c00" width="350"/> On the fundamental plane, the situation looks like this diagram: where the shadow of the Moon is centered on $M_1$, the projection of $(x, y, z)$ onto the fundamental plane, and the observer is at $C_1$, the projection of $(\xi, \eta, \zeta)$ on the fundamental plane.

The distance between the shadow and the observer $\Delta = M_1C_1$ is given by:
```math
\Delta^2 = (x - \xi)^2 + (y - \eta)^2 \tag{9.9}
```
Which can also be expressed as:
```math
\displaylines{
\begin{align}
\Delta \cos(Q) &= x - \xi\\
\Delta \sin(Q) &= y - \eta
\end{align}
}\tag{9.10}
```
Where $Q$ is the angle $NC_1M_1$. By geometry, this is also $PZM'$ from the previous diagram.

<br/>

### The Size of the Shadow

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/4599e516-fdbc-42eb-8f61-db7e7f41246e" width="450"/> In these diagrams, $S$ is the center of the Sun, $M$ is the center of the Moon, the line $EF$ is the fundamental plane, and the line $CD$ is a parallel plane a distance $DF = \zeta$ above the fundamental plane. Let:
```math
\begin{align}
K &= \text{ The Sun's radius } = SA\\
k &= \text{ The Moon's radius } = MB\\
G &= \text{ The distance between }\\
&\text{the Sun and the Moon } = SM\\
f &= \text{ The angle of the shadow cone } = EVF\\
c &= \text{ The distance between the vertex }\\
& \text{ of the cone and the fundamental plane} = VF\\
l &= \text{ The radius of the shadow }\\
& \text{ on the fundamental plane } = EF\\
L &= \text{ The radius of the shadow}\\
&\text{ on the parallel plane } = CD\\
\zeta &= \text{ The distance from the parallel plane}\\
&\text{ to the fundamental plane } = DF\\
z &= \text{ The distance from the Moon}\\
&\text{ to the fundamental plane } = MF\\
\end{align}
```

We can see from the left diagram (the penumbral cone) that $SV + MV = G$. We can also see that $SA/SV = MB/MV = \sin(f)$. Thus:
```math
\sin(f) = \frac{K + k}{G} \tag{9.11}
```
For the right diagram (the umbral cone), the vertex of the cone is below the parallel plane (total eclipse). Regardless, we can see that $SV - MV = G$ and thus:
```math
\sin(f) = \frac{K - k}{G} \tag{9.12}
```
Equation $9.12$ is true for annular eclipses as well (in which case the vertex of the cone is between the Moon and the parallel plane).

Then, because $MV = k/\sin(f)$, $c$ is given by:
```math
c = z\pm \frac{k}{\sin(f)} \tag{9.13}
```
the upper sign being used for the penumbra and the lower for the umbra.\
We then have:
```math
\displaylines{
\begin{align}
l &= c\tan(f) = z\tan(f) \pm k\sec(f)\\
L &= (c-\zeta)\tan(f) = l - \zeta\tan(f)
\end{align}
}\tag{9.14}
```
For the umbral cone, $c - \zeta$ is negative when the vertex of the cone falls beneath the parallel plane, in which case we have total eclipse. Therefore we have $L$ as a negative number when there is a total eclipse, and positive for partial and annular eclipses. $l$, being a distance, a positive quantity should be "correct", but keeping it as a negative number will be convenient later.

For brevity we will put:
```math
\begin{align}
i &= \tan(f)\\
l &= ic \tag{5.15}\\
L &= l - i\zeta
\end{align}
```

The quantities $a$, $d$, $\theta$, $x$, $y$, $i_1$, $i_2$, $l_1$ ($l$ for the penumbra), and $l_2$ ($l$ for the umbra) are known as the [Besselian elements](https://en.wikipedia.org/wiki/Besselian_elements) of a solar eclipse.

#### Example 9.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the Besselian elements for the solar eclipse of $\text{April 8, } 2024$ for the time $18:00$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Let $r, \alpha, \delta$ be the equatorial spherical coordinates of the Moon and $r', \alpha', \delta'$ be the equatorial spherical coordinates of the Sun. From an ephemeris, we find that on $\text{April 8, } 2024$ at $18:00$:
```math
\begin{align}
r &= 359\:780.727\text{ km}\\
\alpha &= 1^h\:9^m\:4.27^s\\
\delta &= 7\degree\:41'\:16.5''\\
r' &= 149\:822\:802.516 \text{ km}\\
\alpha' &= 1^h\:10^m\:19.99^s \\
\delta' &= 7\degree\:27'\:36.9''
\end{align}
```
Thus the cartesian coordinates of the Moon and Sun are:
```math
\begin{align}
v &= 340\:068.149\text{ km}\\
u &= 107\:766.833\text{ km}\\
w &= 46\:713.3280\text{ km}\\
v' &= 141\:783\:968 \text{ km}\\
u' &= 44\:073\:369.0 \text{ km} \\
w' &= 20\:042\:873.5 \text{ km}
\end{align}
```
(If vectors are already known, the above step may be skipped.)\
Therefore, by equation $9.4$:
```math
\begin{alignat}{2}
G \cos(d) \cos(a) &= 141\:783\:968 - 340\:068.149 &&= 141\:273\:455\text{ km}\\
G \cos(d) \sin(a) &= 44\:073\:369.0 - 107\:766.833 &&= 44\:771\:300.3\text{ km}\\
G \sin(d) &= 20\:042\:873.5 - 46\:713.3280 &&= 19\:404\:611.7\text{ km}
\end{alignat}
```
Therefore:
```math
\begin{alignat}{2}
G &= \sqrt{141\:273\:455^2 + 44\:771\:300.3^2 + 19\:404\:611.7^2} &&= 149\:463\:030\text{ km}\\
a &= \arctan(44\:771\:300.3, 141\:273\:455) &&= 17\degree\:35'\:2.58''\\
d &= \arcsin(19\:404\:611.7 / G) &&= 7\degree\:27'\:34.93''\\
\end{alignat}
```
Thus, by equation $9.5$, the rotation matrix is:
```math
R = \begin{bmatrix}
-0.302104542 & 0.9532748008 & 0\\
-0.12376256 & -0.039221882 & 0.991536420\\
0.945206683 & 0.299547656 & 0.12982884
\end{bmatrix}
```
Thus, by equation $9.6$:
```math
\begin{align}
x &= -1968.0435\text{ km}\\
y &= 1433.7449\text{ km}\\
z &= 359\:772.487\text{ km}
\end{align}
```
Additionally, the sidereal time for $18:00, \text{ April 8, } 2024$ is:
```math
\Theta = 107\degree\:29'\:7.05''
```
So, by equation $6.1$, the hour angle of the shadow axis (at the Greenwich (standard) meridian) is:
```math
\theta = 107\degree\:29'\:7.05'' - 17\degree\:35'\:2.58'' = 89\degree\:54'\:4.47''
```
By equation $9.11$, $9.12$, $9.13$, and $9.15$ (and the radius data from example $9.1$):
```math
\begin{alignat}{2}
f_1 &= \arcsin\left(\frac{696\:000 + 1737.4}{149\:463\:030}\right) &&= 16.80592''\\
f_2 &= \arcsin\left(\frac{696\:000 - 1737.4}{149\:463\:030}\right) &&= 16.72222''\\
i_1 &= \tan(16.80592'') &&= 0.0046683\\
i_2 &= \tan(16.72222'') &&= 0.0046451\\
c_1 &= 359\:772.487 + \frac{1737.4}{\sin(16.80592'')} &&= 731\:942.688 \text{ km}\\
c_2 &= 359\:772.487 - \frac{1737.4}{\sin(16.80592'')} &&= -12\:397.713 \text{ km}\\
l_1 &= 0.0046683 \cdot 719\:445.246 &&= 3416.961\text{ km}\\
l_2 &= 0.0046451 \cdot -12\:397.713 &&= -57.589\text{ km}
\end{alignat}
```
Expressing distances in terms of Earth equatorial radii ($6378.137\text{ km}$) as is customary, the Besselian elements of this eclipse at $18:00$ are:
```math
\begin{align}
a &= 17\degree\:35'\:2.58''\\
d &= 7\degree\:27'\:34.93''\\
\theta &= 89\degree\:54'\:4.47''\\
x &= -0.30856088 \:R_E\\
y &= 0.22479055 \:R_E\\
i_1 &= 0.0046683\\
i_2 &= 0.0046451\\
l_1 &= 0.53573027 \:R_E\\
l_2 &= -0.00902906 \:R_E
\end{align}
```
Also of importance are the derivatives of the quantities $x$, $y$, and $\theta$ (in radians). By taking a time step of $\pm 15$ minutes, we find:\
At $17:45$:
```math
\begin{align}
x &= -0.4364434 \:R_E\\
y &= 0.15693548 \:R_E\\
\theta &= 86\degree\:9'\:0.73''\\
\end{align}
```
At $18:15$:
```math
\begin{align}
x &= -0.18070657 \:R_E\\
y &= 0.29258104 \:R_E\\
\theta &= 93\degree\:39'\:8.07''\\
\end{align}
```
Therefore:
```math
\begin{alignat}{2}
x' &= \frac{-0.18070657 - (-0.4364434)}{0.5h} &&= 0.51147366 \: R_E/h\\
y' &= \frac{0.29258104 - 0.15693548}{0.5h} &&= 0.27129112 \:R_E/h\\
\theta' &= \frac{93\degree\:39'\:8.07'' - 86\degree\:9'\:0.73''}{0.5h} \cdot{1\text{ rad}}{180\degree} &&= 0.26187054 \text{ rad}/h\\
\end{alignat}
```
$\blacksquare$
