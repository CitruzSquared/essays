(Continued from Part A...)

### Brightness

[**Apparent magnitude**](https://en.wikipedia.org/wiki/Apparent_magnitude) (denoted by $m$) is a logarithmic scale measuring how bright objects *look* in the sky. It stems from a centuries-old system of categorizing stars, class $1$ for the brightest stars and class $6$ for the dimmest. Thus, our modern system of apparent magnitude also operates with **smaller magnitudes being brighter**: magnitude is defined such that a decrease in apparent magnitude by $x$ is a $100^{1/5 \cdot x}$ times increase in brightness.

For stars, as they produce their own unchanging light, their apparent magnitude is easily calculable:
```math
m = -2.5\log_{10}\left(\frac{F}{F_0}\right)\tag{63}
```
Where $F$ is the intensity of the starlight at the observer in $\text{W}/\text{m}^2$, and $F_0$ is a constant equaling $2.518\cdot10^{-8} \text{ W}/\text{m}^2$.\
$F$ can be calculated with this formula:
```math
F = \frac{P}{4\pi R^2}\tag{64}
```
Where $P$ is the power output of the star in watts$, and $R$ is the distance from the star to the observer in meters$. This makes sense as $4\pi R^2$ is the surface area of a sphere with radius $R$, thus $F$ represents the power output $P$ being spread out over that area.

#### Example 16
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

By equation $64$, the intensity of sunlight on the Earth is:
```math
F = \frac{3.8\cdot10^{26}}{4\cdot\pi \cdot 149\:600\:000\:000^2} = 1351.17 \text{ W}/\text{m}^2
```
Thus, by equation $63$:
```math
m_{\text{Sun}} = -2.5\log_{10}\left(\frac{1351.17}{2.518\cdot10^{-8}}\right) = -26.8
```
Which is very bright (it is a very negative number, and smaller magnitudes are brighter).\
$\blacksquare$

<br/>

The brightness of planets is harder to calculate: it depends on the *absolute* magnitude, which is the apparent magnitude of an object if the observer were exactly $1 \text{ AU}$ away from it.

The actual calculation of the absolute magnitude of planets is very difficult, but if we approximate planets to be ideally reflecting solid matt spheres, it can be calculated by:
```math
H = m_{\text{Sun}} - 5\log_{10}\left(\frac{\sqrt{a}r}{d_0}\right)\tag{65}
```
Where $m_{\text{Sun}}$ is the apparent magnitude of the Sun at $1 \text{ AU}$, $a$ is the [geometric albedo](https://en.wikipedia.org/wiki/Geometric_albedo) of the planet, a value usually between $0$ and $1$ describing how much light it reflects (i.e. how white the planet is), $r$ is the radius of the planet, and $d_0$ is the length of $1 \text{ AU}$, approximately $149,600,000,000\text{ m}$.

Note that this formula is a great approximation, for example the Moon of Earth has a brighter half and a darker half, so the albedo is not the same depending on which side is visible (i.e. depends on the elongation from the Sun). This is not reflected in the formula, which assumes all bodeis to have uniform albedo.

Then, the apparent magnitude can be calculated by:
```math
m = H + 5\log_{10}\left(\frac{d_{PS} d_{PO}}{d_0^2}\right) - 2.5\log_{10}(q(\alpha))\tag{66}
```
Where $d_{PS}$ is the distance from the planet to the Sun in meters, $d_{PO}$ is the distance from the planet to the observer in meters, $d_0$ is the same $d_0$ from before, $1 \text{ AU}$, and $\alpha$ is the phase angle of the planet in degrees.

$q(\alpha)$ is known as the *phase integral*. If we assume planets to be ideally diffusely reflecting spheres, it is given as:
```math
q(\alpha) = \frac{2}{3}\left(\left(1- \frac{\alpha}{180\degree}\right)\cos(\alpha) + \frac{1}{\pi}\sin(\alpha)\right)\tag{67}
```
Note that this formula is quite a great approximation, and does not take into account rings and other factors that may change the brightness of a planet.

#### Example 17
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

We found out in example $12$ that:
```math
\begin{align}
\text{Earth Venus Distance } &= 1.1882 \text{ AU} = 177\:754\:720\:000 \text{ m}\\
\text{Sun Venus Distance } &= 0.7205 \text{ AU} = 107\:786\:800\:000 \text{ m}\\
\text{Venus Phase Angle } &= 55\degree\:43'\:\:57.60''
\end{align}
```
We also found out in example $15$ that the apparent magnitude of the Sun from $1\text{ AU}$ away is $-26.8$.\
Thus, by equation $65$:
```math
\begin{align}
H &= -26.8 - 5\log_{10}\left(\frac{\sqrt{0.69}\cdot 6\:051\:000}{149\:600\:000\:000}\right) \\
&= -4.4316
\end{align}
```
And then by equation $67$:
```math
\begin{align}
q(\alpha) &= \frac{2}{3}\left(\left(1- \frac{55\degree\:43'\:\:57.60''}{180\degree}\right)\cos(55\degree\:43'\:\:57.60'') + \frac{1}{\pi}\sin(55\degree\:43'\:\:57.60'')\right) \\
&= 0.43452
\end{align}
```
And thus finally by equation $66$:
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

This phenomenon is called [*apparent* retrograde motion](https://en.wikipedia.org/wiki/Apparent_retrograde_motion), as it is not a real physical phenomenon, just an illusion caused by the effects of relative motion. This occurs once every synodic period, as inferior conjunctions happen once every synodic period.

The true way to calculate when a planet goes into retrograde and for how long it stays in retrograde would be to calculate $d\lambda/dt$ and see when it is less than $0$. This is not practical for our purposes because $\lambda$ is not a simple function at all due to the ellipticity of orbits. Thus one would have to use bisection or similar methods to numerically approximate (to arbitrary precision) when exactly a planet goes into retrograde.

In this section, we will assume for a moment that the orbits of the planets are perfect circles and try to calculate for how long a planet would stay in retrograde.

Apparent retrograde motion happens when $w_\text{obs}$, the observed angular speed of the outer planet from the view of the Earth, is negative. Because $w_\text{obs}$ is continuous, we only need to find the times when it is $0$ as a continuous function must pass through $0$ to go from positive to negative and back. Consider this diagram:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6a7eac2f-96f0-4e05-bb11-82b229bb7f42" width="400"/> In this diagram, the Sun is at loction $S$, the Earth at location $E$, and the outer planet at location $P$. The distance from the Sun to the Earth is $a$, the distance from the Sun to the outer planet is $b$, and the distance from the Earth to the outer planet is denoted $\rho$. 

The velocity of the Earth is shown with the vector $\vec{EU}$, and the velocity of the outer planet is shown with the vector $\vec{PV}$. The magnitudes of these vectors will be denoted $u$ and $v$ respectively.

The Earth-Sun-Planet angle is $\alpha$, the Sun-Planet-Earth angle is $\theta$, and the angle $UEP$ is $\psi$.

First, from the definition of angular velocity, we know that
```math
w_{\text{obs}} = \frac{v_{\text{rel}}}{\rho} \tag{68}
```
But in $v_{\text{rel}}$, the component of this velocity parallel with $EP$ should not be counted because this part of the velocity is not visible. Thus only the perpendicular components of the velocities $\vec{EU}$ and $\vec{PV}$ should be considered:
```math
v_{\text{rel}} = |\vec{PA} - \vec{EB}| \tag{69}
```
It is evident that:
```math
\displaylines{
\begin{align}
|\vec{EB}| &= u\sin(\psi) \\
|\vec{PA}| &= v \cos(VPA)
\end{align}
}\tag{70}
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
Thus, equation $70$ becomes:
```math
\displaylines{
\begin{align}
|\vec{EB}| &= u\sin(\psi) \\
|\vec{PA}| &= v \cos(90\degree - (\alpha + \psi))\\
&= v\sin(\alpha + \psi)
\end{align}
}\tag{71}
```
Thus by equation $69$ and equation $68$:
```math
\begin{align}
v_{\text{rel}} &= v\sin(\alpha + \psi) -  u\sin(\psi) \\
\therefore w_{\text{obs}} &= \frac{v\sin(\alpha + \psi) -  u\sin(\psi)}{\rho}\\
&= \frac{v\sin(\alpha)\cos(\psi) + v\cos(\alpha)\sin(\psi) -  u\sin(\psi)}{\rho} \tag{72}
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
\sin(\psi) = \frac{b\cos(\alpha) - a}{\rho}\tag{73-i}
```
But also,
```math
\begin{align}
PD &= b\sin(\alpha) = \rho\sin(PED) \\
&= \rho\cos(\psi) \\
\therefore \cos(\psi) &= \frac{b\sin(\alpha)}{\rho}\tag{73-ii}
\end{align}
```
So we can rewrite equation $72$ as:
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
Since this value for $\alpha$ is the angle when $w_{\text{obs}} = 0$, we need to multiply it by $2$ to get the full range of $\alpha$ where there is retrograde motion (the orbit is symmetric about the line $SD$). Then, dividing $2\alpha$ by the relative mean motion $n' = n_P - n_E$ gives the time spent in retrograde:
```math
T_{\text{retro}} = \left|\frac{2\arccos\left(\frac{a^2n_E + b^2n_P}{ab(n_E + n_P)}\right)}{n_P - n_E}\right|
```
Where we use absolute value to keep the answer positive.\
Using $n = 360\degree/T$ gives:
```math
T_{\text{retro}} = \left|\frac{2\arccos\left(\frac{a^2T_P + b^2T_E}{ab(T_E + T_P)}\right)}{\frac{360\degree}{T_P} - \frac{360\degree}{T_E}}\right| \tag{74}
```
If we use $b/a = r$, we can simplify this equation even further using kepler's third law because then, $T_2 = T_1\sqrt{r^3}$:
```math
T_{\text{retro}} = T_1 \left|\frac{2\arccos\left(\frac{r + \sqrt{r}}{r\sqrt{r}+1}\right)}{360\degree\left(r^{-3/2} - 1\right)}\right| \tag{75}
```
As it turns out, even inner planets follow the same principle and the formula works for inner planets as well. For inner planets, they go retrograde near inferior conjunction (i.e. when the Earth is in opposition with the Sun from the inner planet's POV).

#### Example 18
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that Venus orbits at $0.7233 \text{ AU}$ from the Sun, and the Earth takes $365.24\text{ dy}$ to orbit the Sun, <br/>
how long is Venus in retrograde motion for from the view of the Earth?
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

$b/a = 0.7233\text{ AU}/1\text{ AU} = 0.7233$. Therefore, by equation $75$:
```math
\begin{align}
T_{\text{retro}} &= 365.24\text{ dy} \left|\frac{2\arccos\left(\frac{0.7233 + \sqrt{0.7233}}{0.7233\sqrt{0.7233}+1}\right)}{360\degree\left(0.7233^{-3/2} - 1\right)}\right|\\
&= 42.2 \text{ dy}
\end{align}
```

Doing this for all the planets yields:
```math
\begin{array}{ccc}\hline \text{Name} & \text{Equation } 75 & \text{True Value} \\ \hline
\text{Mercury} & 22.9 \text{ dy} & 21\text{ dy} \\
\text{Venus} & 42.2 \text{ dy} & 41\text{ dy}  \\
\text{Mars} & 72.7 \text{ dy} & 72\text{ dy}  \\
\text{Jupiter} & 121 \text{ dy} & 121\text{ dy}  \\
\text{Saturn} & 138  \text{ dy} & 138\text{ dy}  \\
\text{Uranus} & 152 \text{ dy} & 151\text{ dy}  \\
\text{Neptune} & 158 \text{ dy} & 158\text{ dy}  \\ \hline
\end{array}
```
As the planet gets further and further away from the Sun, the time it spends in retrograde motion approaches $T_1/2$, which is $183\text{ dy}$ for the Earth.\
$\blacksquare$
