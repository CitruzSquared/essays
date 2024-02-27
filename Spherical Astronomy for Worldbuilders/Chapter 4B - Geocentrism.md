(Continued from Part A...)

### Brightness

[**Apparent magnitude**](https://en.wikipedia.org/wiki/Apparent_magnitude) (denoted by $m$) is a logarithmic scale measuring how bright objects *look* in the sky. It stems from a centuries-old system of categorizing stars, class $1$ for the brightest stars and class $6$ for the dimmest. Thus, our modern system of apparent magnitude also operates with **smaller magnitudes being brighter**: magnitude is defined such that a decrease in apparent magnitude by $x$ is a $100^{x/5}$ times increase in brightness.

For stars, as they produce their own unchanging light, their apparent magnitude is easily calculable:
```math
m = -2.5\log_{10}\left(\frac{F}{F_0}\right)\tag{4.10}
```
Where $F$ is the intensity of the starlight at the observer in $\text{W}/\text{m}^2$, and $F_0$ is a constant equaling $2.518\cdot10^{-8} \text{ W}/\text{m}^2$.\
$F$ can be calculated with this formula:
```math
F = \frac{P}{4\pi R^2}\tag{4.11}
```
Where $P$ is the power output of the star in watts$, and $R$ is the distance from the star to the observer in meters$. This makes sense as $4\pi R^2$ is the surface area of a sphere with radius $R$, thus $F$ represents the power output $P$ being spread out over that area.

#### Example 4.5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that the Sun has a power output of $3.8\cdot10^{26} \text{ W}$ and the average distance from the Earth to the Sun is $149\:600\:000\:000\text{ m}$, <br/>
Calculate the average apparent magnitude of the Sun from the Earth.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $4.11$, the intensity of sunlight on the Earth is:
```math
F = \frac{3.8\cdot10^{26}}{4\cdot\pi \cdot 149\:600\:000\:000^2} = 1351.17 \text{ W}/\text{m}^2
```
Thus, by equation $4.10$:
```math
m_{\text{Sun}} = -2.5\log_{10}\left(\frac{1351.17}{2.518\cdot10^{-8}}\right) = -26.8
```
Which is very bright (it is a very negative number, and smaller magnitudes are brighter).\
$\blacksquare$

<br/>

The brightness of planets is harder to calculate: it depends on the *absolute* magnitude, which is the apparent magnitude of an object if the observer were exactly $1 \text{ AU}$ away from it.

The actual calculation of the absolute magnitude of planets is very difficult, but if we approximate planets to be ideally reflecting solid matt spheres, it can be calculated by:
```math
H = m_{\text{Sun}} - 5\log_{10}\left(\frac{\sqrt{a}r}{d_0}\right)\tag{4.12}
```
Where $m_{\text{Sun}}$ is the apparent magnitude of the Sun at $1 \text{ AU}$, $a$ is the [geometric albedo](https://en.wikipedia.org/wiki/Geometric_albedo) of the planet, a value usually between $0$ and $1$ describing how much light it reflects (i.e. how white the planet is), $r$ is the radius of the planet, and $d_0$ is the length of $1 \text{ AU}$, approximately $149,600,000,000\text{ m}$.

Note that this formula is a great approximation, for example the Moon of Earth has a brighter half and a darker half, so the albedo is not the same depending on which side is visible (i.e. depends on the elongation from the Sun). This is not reflected in the formula, which assumes all bodeis to have uniform albedo.

Then, the apparent magnitude can be calculated by:
```math
m = H + 5\log_{10}\left(\frac{d_{PS} d_{PO}}{d_0^2}\right) - 2.5\log_{10}(q(\alpha))\tag{4.13}
```
Where $d_{PS}$ is the distance from the planet to the Sun in meters, $d_{PO}$ is the distance from the planet to the observer in meters, $d_0$ is the same $d_0$ from before, $1 \text{ AU}$, and $\alpha$ is the phase angle of the planet in degrees.

$q(\alpha)$ is known as the *phase integral*. If we assume planets to be ideally diffusely reflecting spheres, it is given as (the derivation is too difficult to go into detail):
```math
q(\alpha) = \frac{2}{3}\left(\left(1- \frac{\alpha}{180\degree}\right)\cos(\alpha) + \frac{1}{\pi}\sin(\alpha)\right)\tag{4.14}
```
Note that this formula is a very loose approximation, and does not take into account rings and other factors that may change the brightness of a planet.

#### Example 4.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that the albedo of Venus is $0.69$ and that its radius is $6\:051\:000 \text{ m}$, <br/>
Calculate the apparent magnitude of Venus on $\text{January 1, } 2024$. <br/>
Use $1 \text{ AU} = 149\:600\:000\:000 \text{ m}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We found out in example $4.1$ that:
```math
\begin{align}
\text{Earth Venus Distance } &= 1.1882 \text{ AU} = 177\:754\:720\:000 \text{ m}\\
\text{Sun Venus Distance } &= 0.7205 \text{ AU} = 107\:786\:800\:000 \text{ m}\\
\text{Venus Phase Angle } &= 55\degree\:43'\:\:57.60''
\end{align}
```
We also found out in example $4.4$ that the apparent magnitude of the Sun from $1\text{ AU}$ away is $-26.8$.\
Thus, by equation $4.12$:
```math
\begin{align}
H &= -26.8 - 5\log_{10}\left(\frac{\sqrt{0.69}\cdot 6\:051\:000}{149\:600\:000\:000}\right) \\
&= -4.4316
\end{align}
```
And then by equation $4.14$:
```math
\begin{align}
q(\alpha) &= \frac{2}{3}\left(\left(1- \frac{55\degree\:43'\:\:57.60''}{180\degree}\right)\cos(55\degree\:43'\:\:57.60'') + \frac{1}{\pi}\sin(55\degree\:43'\:\:57.60'')\right) \\
&= 0.43452
\end{align}
```
And thus finally by equation $4.13$:
```math
\begin{align}
m &= -4.4316 + 5\log_{10}\left(\frac{107\:786\:800\:000 \cdot 177\:754\:720\:000}{149\:600\:000\:000^2}\right) - 2.5\log_{10}(0.43452)\\
&= -3.86
\end{align}
```
Comparing this to the true value of $-4.1$, we can see how crude the approximation really is. (We have estimated Venus to be about $15$% darker than it really was.) However, this is the best we can realistically do.\
$\blacksquare$

### Apparent Retrograde Motion

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/0ece4e9d-73c6-4e48-a633-0fc2134669e5" width="350"/> This diagram depicts the Earth (which we have put as stationary at $C$) and an outer planet, with orbital directions (counterclockwise) marked with arrows. 

From the view of the Earth, the outer planet would look to orbit from West to East (i.e. increasing in longitude) most of the time (when it is on the far side of the Sun), but when the planet is near opposition ($O$), it would appear to move East to West (i.e. decreasing in longitude). This makes it seem like the planet moves backwards for a period of time before going forward again.

This phenomenon is called [*apparent* retrograde motion](https://en.wikipedia.org/wiki/Apparent_retrograde_motion), as it is not a real physical phenomenon, just an illusion caused by the effects of relative motion. This occurs only once every synodic period, as oppositions only happen once every synodic period.

The true way to calculate when a planet goes into retrograde and for how long it stays in retrograde would be to calculate $d\lambda/dt$ and see when it is less than $0$. This is not practical for our purposes because $\lambda$ is not a simple function at all due to the ellipticity of orbits. Thus one would have to use bisection or similar methods to numerically approximate (to arbitrary precision) when exactly a planet goes into retrograde.

In this section, we will assume for a moment that the orbits of the planets are perfect circles and try to calculate for how long a planet would stay in retrograde (i.e. calculate the average time a planet stays in regrograde).

Apparent retrograde motion happens when $w_\text{obs}$, the observed angular speed of the outer planet from the view of the Earth, is negative. Because $w_\text{obs}$ is continuous, we only need to find the times when it is $0$ as a continuous function must pass through $0$ to go from positive to negative and back. Consider this diagram:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6a7eac2f-96f0-4e05-bb11-82b229bb7f42" width="300"/> In this diagram, the Sun is at loction $S$, the Earth at location $E$, and the outer planet at location $P$. The distance from the Sun to the Earth is $a$, the distance from the Sun to the outer planet is $b$, and the distance from the Earth to the outer planet is denoted $\rho$. 

The velocity of the Earth is shown with the vector $\vec{EU}$, and the velocity of the outer planet is shown with the vector $\vec{PV}$. The magnitudes of these vectors will be denoted $u$ and $v$ respectively.

The Earth-Sun-Planet angle is $\alpha$ (not to be confused with right ascension), the Sun-Planet-Earth angle is $\theta$, and the angle $UEP$ is $\psi$.

First, from the definition of angular velocity, we know that
```math
w_{\text{obs}} = \frac{v_{\text{rel}}}{\rho} \tag{4.15}
```
But in $v_{\text{rel}}$, the component of this velocity parallel with $EP$ should not be counted because this part of the velocity is not visible. Thus only the perpendicular components of the velocities $\vec{EU}$ and $\vec{PV}$ should be considered:
```math
v_{\text{rel}} = |\vec{PA} - \vec{EB}| \tag{4.16}
```
It is evident that:
```math
\displaylines{
\begin{align}
|\vec{EB}| &= u\sin(\psi) \\
|\vec{PA}| &= v \cos(VPA)
\end{align}
}\tag{4.17}
```
Let us determine $VPA$. Because velocity is always perpendicular to the radius in circular motion (because velocity is always tangential, and tangents to a circle are always perpendicular to radii), angle $SPV = 90\degree = SEU$, and so
```math
\begin{align}
SPA &= 90\degree - VPA = 90\degree - \theta\\
\therefore VPA &= \theta
\end{align}
```
But $\theta = 180\degree - \alpha - SEP$, where $SEP = 90\degree + \psi$.
Thus:
```math
\begin{align}
VPA &= \theta = 180\degree - \alpha - (90\degree + \psi)\\
&= 90\degree - (\alpha + \psi)
\end{align}
```
Thus, equation $4.17$ becomes:
```math
\displaylines{
\begin{align}
|\vec{EB}| &= u\sin(\psi) \\
|\vec{PA}| &= v \cos(90\degree - (\alpha + \psi))\\
&= v\sin(\alpha + \psi)
\end{align}
}\tag{4.18}
```
Thus by equation $4.16$ and equation $4.15$:
```math
\begin{align}
v_{\text{rel}} &= v\sin(\alpha + \psi) -  u\sin(\psi) \\
\therefore w_{\text{obs}} &= \frac{v\sin(\alpha + \psi) -  u\sin(\psi)}{\rho}\\
&= \frac{v\sin(\alpha)\cos(\psi) + v\cos(\alpha)\sin(\psi) -  u\sin(\psi)}{\rho} \tag{4.19}
\end{align}
```
Now let's analyze the distances and $\psi$.
```math
\begin{align}
a &= SD - ED \\
&= b\cos(\alpha) - \rho\cos(PED)
\end{align}
```
But $PED = 90\degree - \psi$, so:
```math
a = b\cos(\alpha) - \rho\sin(\psi)
```
Therefore
```math
\sin(\psi) = \frac{b\cos(\alpha) - a}{\rho}\tag{4.20-i}
```
But also,
```math
\begin{align}
PD &= b\sin(\alpha) = \rho\sin(PED) \\
&= \rho\cos(\psi) \\
\therefore \cos(\psi) &= \frac{b\sin(\alpha)}{\rho}\tag{4.20-ii}
\end{align}
```
Using equations $4.20$ we can rewrite equation $4.19$ as:
```math
\begin{align}
w_{\text{obs}} &= \frac{v\sin(\alpha) \frac{b\sin(\alpha)}{\rho} + v\cos(\alpha)\frac{b\cos(\alpha) - a}{\rho} -  u\frac{b\cos(\alpha) - a}{\rho}}{\rho}\\
&= \frac{vb\sin^2(\alpha) - va\cos(\alpha) + vb\cos^2(\alpha) + ua - ub\cos(\alpha)}{\rho^2}\\
&= \frac{vb + ua - (va + ub)\cos(\alpha)}{\rho^2}
\end{align}
```
We need to find when $w_{\text{obs}} = 0$, so:
```math
\begin{align}
0 &= \frac{vb + ua - (va + ub)\cos(\alpha)}{\rho^2} \\
&= vb + ua - (va + ub)\cos(\alpha) \\
\therefore \cos(\alpha) &= \frac{vb + ua}{va + ub}
\end{align}
```
We can write $v = b\cdot n_P$ and $u = a\cdot n_E$, where $n$ is the mean motion, so:
```math
\cos(\alpha) = \frac{a^2n_E + b^2n_P}{ab(n_E + n_P)}
```
Since this value for $\alpha$ is the angle when $w_{\text{obs}} = 0$, we need to multiply it by $2$ to get the full range of $\alpha$ where there is retrograde motion (the orbit is symmetric about the line of conjunction). Then, dividing $2\alpha$ by the relative mean motion $n' = n_P - n_E$ gives the time spent in retrograde:
```math
T_{\text{retro}} = \left|\frac{2\arccos\left(\frac{a^2n_E + b^2n_P}{ab(n_E + n_P)}\right)}{n_P - n_E}\right|
```
Where we use absolute value to keep the answer positive.\
Using $n = 360\degree/T$ gives:
```math
T_{\text{retro}} = \left|\frac{2\arccos\left(\frac{a^2T_P + b^2T_E}{ab(T_E + T_P)}\right)}{\frac{360\degree}{T_P} - \frac{360\degree}{T_E}}\right| \tag{4.21}
```
If we use $b/a = r$, we can simplify this equation even further using kepler's third law because then, $T_P = T_E\sqrt{r^3}$:
```math
T_{\text{retro}} = T_E \left|\frac{2\arccos\left(\frac{r + \sqrt{r}}{r\sqrt{r}+1}\right)}{360\degree\left(r^{-3/2} - 1\right)}\right| \tag{4.22}
```
Again, this formula is just an approximation assuming the orbits are perfectly circular.

As it turns out, even inner planets follow the same principle and the formula works for inner planets as well. For inner planets, they go retrograde near inferior conjunction (i.e. when the Earth is in opposition with the Sun from the inner planet's POV).

#### Example 4.7
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that Venus orbits at $0.7233 \text{ AU}$ from the Sun, and the Earth takes $365.24\text{ dy}$ to orbit the Sun, <br/>
for how long is Venus in retrograde motion from the view of the Earth on average?
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

$r = b/a = 0.7233\text{ AU}/1\text{ AU} = 0.7233$. Therefore, by equation $4.22$:
```math
\begin{align}
T_{\text{retro}} &= 365.24\text{ dy} \left|\frac{2\arccos\left(\frac{0.7233 + \sqrt{0.7233}}{0.7233\sqrt{0.7233}+1}\right)}{360\degree\left(0.7233^{-3/2} - 1\right)}\right|\\
&= 42.2 \text{ dy}
\end{align}
```
Thus Venus is in retrograde for $42.2 \text{ dy}$ every $583.96 \text{ dy}$ (See example $4.3$), or roughly $7.2$% of the time. (Apparently the stars are pretty benevolent and only want to break up romantic relationships only about $7$% of the time.)

Doing this for all the planets yields:
```math
\begin{array}{cccc}\hline \text{Name} & \text{Equation } 4.22 & \text{True Value} & \text{\% Retro. Time} \\ \hline
\text{Mercury} & 22.9 \text{ dy} & 21\text{ dy} & 18\% \\
\text{Venus} & 42.2 \text{ dy} & 41\text{ dy} & 7\% \\
\text{Mars} & 72.7 \text{ dy} & 72\text{ dy} & 9\% \\
\text{Jupiter} & 121 \text{ dy} & 121\text{ dy} & 30\% \\
\text{Saturn} & 138  \text{ dy} & 138\text{ dy} & 37\% \\
\text{Uranus} & 152 \text{ dy} & 151\text{ dy} & 41\% \\
\text{Neptune} & 158 \text{ dy} & 158\text{ dy} & 43\% \\ \hline
\end{array}
```
As we can see, as the planet gets further and further away from the Sun, the time it spends in apparent retrograde motion approaches $T_E/2$ (percentage of time spent in retrograde approaches $50$% as the synodic period approaches $T_E$), which is $182.6\text{ dy}$ for our Earth.\
Examples of very far out bodies:
```math
\begin{array}{cccc}\hline \text{Name} & \text{Equation } 4.22 & \text{True Value} & \text{\% Retro. Time} \\ \hline
\text{Quaoar} & 163 \text{ dy} & \approx163\text{ dy} & 45\% \\
\text{500 AU Planet} & 177 \text{ dy} & ?\text{ dy} & 48\% \\ \hline
\end{array}
```
This formula works so well because all these bodies have orbital eccentricities very close to $0$.\
$\blacksquare$

<br/>

Now we know how long a planet is in retrograde for, but how *far* does the planet go back by? This is called the angle "recovered" during retrograde.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/4604b40a-1d6d-4fa7-bad0-4698e825ff1e" width="250"/> In this diagram, the Sun is at point $S$, and $E$ and $P$ are the positions of the Earth and the planet at the moment $P$ starts going into retrograde. $E'$ and $P'$ are the positions of the Earth and the planet at the moment $P$ comes out of retrograde. Thus the angles $PSE$ and $P'SE'$ are both the $\alpha$ that we have calculated before. $P''$ is located where the planet would be if its geocentric location did not change (i.e. the planet never went into retrograde), that is: $EP$ and $E'P''$ are parallel. (Note that the angle $SE'P''$ is not $180\degree$.) The distances $SE$ and $SP$ (or $SE'$ and $SP'$ since we are assuming circular orbits), and the Earth-planet distance $EP$ are denoted by $a$, $b$, and $\rho$ respectively just like before. We are interested in how far the planet has gone backwards in its apparent retrograde motion, that is, we are interested in the angle $P''EP'$. 

Because $EP$ and $E'P''$ are parallel, $P''EP' = PQP'$. Because $SEQE'$ forms a quadrilateral, all the angles inside it must sum to $360\degree$. Also note that because triangles $\triangle SEP$ and $\triangle SE'P$ are congruent (by SAS congruency), the angles $SEP$ and $SE'P$ are congruent too. Thus:
```math
PQP' = 360\degree - ESE' - 2SEP \tag{4.23}
```
$ESE$ is just the angular motion the Earth has moved in the time of the planet's retrograde motion:
```math
ESE' = \frac{360\degree}{T_E}\cdot T_{\text{retro}}\tag{4.24}
```
We now only need $SEP$, which we use the law of sines for:
```math
SEP = \arcsin\left(\frac{\sin(\alpha)}{\rho}\cdot b\right)\tag{4.25}
```
$\rho$ can be calculated with the law of cosines:
```math
\rho = \sqrt{a^2 + b^2 - 2ab\cos(\alpha)}\tag{4.26}
```
And now we finally have all the necessary parts to calculate $PQP'$.

If the planet in question is an inner planet (that is, the planet in question is $E$ and the Earth is $P$), the geometry is the same and all the formulas work out but $E$ and $P$ must be switched:
```math
\begin{align}
EQE' &= 360\degree - PSP' - 2SPE \tag{4.27}\\
PSP' &= \frac{360\degree}{T_P}\cdot T_{\text{retro}} = \frac{360\degree}{T_E\sqrt{r^3}}\cdot T_{\text{retro}}\tag{4.28}\\
SPE &= \arcsin\left(\frac{\sin(\alpha)}{\rho}\cdot a\right)\tag{4.29}\\
\end{align}
```
Where $r = b/a$.\
Note that the formula for $\rho$ stays the same.

Note that as with equation $4.22$, these formulae are not exact as they assume circular orbits; the angle recovered is different every retrograde cycle.

#### Example 4.8
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Calculate the average angle recovered during retrograde for every planet in the Solar System, using $T_E = 365.24\text{ dy}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Let's do Uranus as an example of an outer planet:\
For Uranus, $b =19.19 \text{ AU}$, $\alpha = 73\degree$ $54'$ $48''$ (the arccosine value of equation $4.22$), and $T_{\text{retro}} = 151.8\text{ dy}$ (by equation $4.22$).\
Thus, by equation $4.26$:
```math
\begin{align}
\rho &= \sqrt{1^2 + 19.19^2 - 2\cdot1\cdot19.19\cdot\cos(73\degree\:54'\:48'')}\\
&= 18.94\text{ AU}
\end{align}
```
Then, by equation $4.25$:
```math
\begin{align}
SEP &= \arcsin\left(\frac{\sin(73\degree\:54'\:48'')}{19.19}\cdot 1\right)\\
&= 103\degree\:10'
\end{align}
```
Also, by equation $4.24$:
```math
\begin{align}
ESE' &= \frac{360\degree}{365.24}\cdot 151.8\\
&= 149\degree\:36'
\end{align}
```
Thus, by equation $4.23$:
```math
\begin{align}
PQP' &= 360\degree - 149\degree\:36' - 2\cdot103\degree\:10'\\
&= 4\degree\:4'
\end{align}
```

Let's now do Venus as an example of an inner planet:\
For Venus, $b =0.7233 \text{ AU}$, $\alpha = 12\degree$ $59'$ $48''$ (the arccosine value of equation $4.22$), and $T_{\text{retro}} = 42.2\text{ dy}$ (by equation $4.22$).\
Thus, by equation $4.26$:
```math
\begin{align}
\rho &= \sqrt{1^2 + 0.7233^2 - 2\cdot1\cdot0.7233\cdot\cos(12\degree\:59'\:48'')}\\
&= 0.33708\text{ AU}
\end{align}
```
Then, by equation $4.29$:
```math
\begin{align}
SPE &= \arcsin\left(\frac{\sin(12\degree\:59'\:48'')}{0.33708}\cdot 1\right)\\
&= 138\degree\:9'
\end{align}
```
Also, by equation $4.28$:
```math
\begin{align}
PSP' &= \frac{360\degree}{365.24\sqrt{(0.7233/1)^3}}\cdot 42.2\\
&= 67\degree\:32'
\end{align}
```
Thus, by equation $4.27$:
```math
\begin{align}
EQE' &= 360\degree - 67\degree\:32' - 2\cdot138\degree\:8'\\
&= 16\degree\:12'
\end{align}
```
Doing this for all the planets yields:
```math
\begin{array}{ccc}\hline \text{Name} & \text{Equations} & \text{True Value} \\ \hline
\text{Mercury} & 13\degree\:49' & \approx9\degree\text{ to }16\degree\\
\text{Venus} & 16\degree\:12' & \approx15\degree\text{ to }18\degree\\
\text{Mars} & 15\degree\:55' & \approx10\degree\text{ to }20\degree\\
\text{Jupiter} & 9\degree\:57' & \approx10\degree\\
\text{Saturn} & 6\degree\:46' & \approx7\degree\\
\text{Uranus} & 4\degree\:04' & \approx4\degree\\
\text{Neptune} & 2\degree\:48' & \approx3\degree\\ \hline
\end{array}
```
As we can see, as the planet gets further and further away from the Sun, the average recovered angle during retrogradation approaches $0\degree$.\
Examples of very far out bodies:
```math
\begin{array}{ccc}\hline \text{Name} & \text{Equations} & \text{True Value} \\ \hline
\text{Quaoar} & 2\degree\:02' & ?\degree\\
\text{500 AU Planet} & 0\degree\:13' & ?\degree\\ \hline
\end{array}
```
$\blacksquare$

- Other things regarding apparent retrograde motion:

On Mercury, near perihelion, the orbital speed exceeds the rotational speed, leading to an apparent retrograde motion of the Sun: the Sun appears to go backwards for a period of time, and thus some places on Mercury experience a double sunrise or double sunset.

Sometimes, a conjunction happens between two planets just before one (or both) of them goes into retrograde. This makes it seem like one of the planets goes backwards to conjunct with the other planet again, and when it goes out of retrograde, it goes forward to conjunct again. This phenomenon is called a [triple conjunction](https://en.wikipedia.org/wiki/Triple_conjunction). \
An example is the Jupiter - Saturn triple conjunction of $1980$ ~ $1981$:
```math
\begin{align}
\text{1st Conjunction : } & \text{December 31, } 1980\\
\text{Saturn Retrograde Begins : } & \text{January 18, } 1981 \\
\text{Jupiter Retrograde Begins : } & \text{January 24, } 1981 \\
\text{2nd Conjunction : } & \text{March 4, } 1981	\\
\text{Jupiter Retrograde Ends : } & \text{May 27, } 1981 \\
\text{Saturn Retrograde Ends : } & \text{June 5, } 1981 \\
\text{3rd Conjunction : } & \text{July 24, } 1981 \\ 
\end{align}
```
