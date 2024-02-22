(Continued from Part A...)

### Equator-Aligned Moons

The precession rates of equator aligned moons depend on the gravitational potential field of the primary planet, which can be expressed as an infinite series with coefficients involving "[zonal spherical harmonics](https://en.wikipedia.org/wiki/Zonal_spherical_harmonics)" $J_1, J_2, J_3, \cdots$ . Fortunately, $J_2$ is about a thousand times larger than all the other terms, so we can focus on the $J_2$ term and ignore the others. Unfortunately, $J_2$ is not easily calculable. It depends on the specific distribution of mass in the three-dimensional structure of the primary, and the only way to truly know the value of $J_2$ is through observation of the precession rates. So what now? 

Well, we can make a *very* crude approximation that the planet is a perfect spheroid of uniform density throughout. Then, $J_2$ is given by:
```math
J_2 \approx \left|\frac{2f}{3} - \frac{R_E^3 w^2}{3GM}\right|\tag{46}
```
where $f$ is the [flattening](https://en.wikipedia.org/wiki/Flattening), calculated from the equatorial radius $R_E$ and the polar radius $R_P$ of the planet as such:
```math
f = \frac{R_E - R_P}{R_E}\tag{47}
```
$w$ is the rotational speed of the planet in $\text{rad}$,\
$G$ is the gravitational constant, and\
$M$ is the mass of the planet.

The table of $J_2$ values by planet in the Solar System is given here:
```math
\begin{array}{cccc}\hline \text{Name} & J_2 & \text{Flattening} & \text{Equation }46 \\ \hline
\text{Mercury} & 60\cdot10^{-6} & 0.000900 & 600\cdot 10^{-6}\\
\text{Venus} & 4.458\cdot10^{-6} & 0.000000 & 0.02\cdot 10^{-6}\\
\text{Earth} & 1.08263\cdot10^{-3} & 0.003353 & 1.08136\cdot10^{-3} \\
\text{Mars} & 1.96045\cdot10^{-3} & 0.005890 & 2.39485\cdot10^{-3}\\
\text{Jupiter} & 14.7360\cdot10^{-3} & 0.064870 & 13.5152\cdot 10^{-3}\\
\text{Saturn} & 16.2980\cdot10^{-3} & 0.097960 & 12.5902\cdot10^{-3}\\
\text{Uranus} & 3.34343\cdot10^{-3} & 0.022930 & 5.44115\cdot10^{-3}\\
\text{Neptune} & 3.411\cdot10^{-3} & 0.017080 & 2.69509\cdot10^{-3}\\ \hline
\end{array}
```
Evidently, the approximation is very crude; however it's the best we've got. Now that we have $J_2$, we can calculate the precession rates.\
The precession depends on this value which we will call $K$ for simplicity:
```math
K = \frac{3J_2nR_{\text{avg}}^2}{2a^2(1-e^2)^2}\tag{48}
```
Where $R_{\text{avg}}$ is the average radius of the planet, given by:
```math
R_{\text{avg}} = \sqrt[3]{R_E^2 \cdot R_P} \tag{49}
```
and $a$, $n$, and $e$ are the semi-major axis, mean motion, and eccentricity of the orbit of the satellite respectively.

Then, the nodal precession rate is given as:
```math
\dot\Omega = -K\cos(i)\tag{50}
```
where $i$ is the inclination (with respect to the equator) of the orbit of the satellite.\
Note that nodal precession is always in the direction opposite to the orbit.

The apsidal precession rate is given as:
```math
\dot\omega = K\left(2 - \frac{5}{2}\sin^2(i)\right)\tag{51}
```
Note that the formula gives $\dot\omega$ directly and not $\dot\varpi$, and so $\dot\omega$ is constant. Thus for equator aligned moons, equation $40$ gives:
```math
\omega = \omega_0 + (t - t_0)\dot\omega\tag{52}
```
Also note that if $0\degree \leq i \leq 63.4\degree$ or $116.6\degree \leq i \leq 180\degree$, then the precession of the apses are in the direction of the orbit.
#### Example 10
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Mars' largest moon Phobos is an equator aligned moon. <br/>
Given that for Mars: 
$J_2 = 1.96045\cdot10^{-3}$, $R_\text{avg} = 3389.5 \text{ km}$, and $M = 6.4171\cdot10^{23}\text{ kg}$, <br/>
And for Phobos: 
$a = 9376\text{ km}$, $e = 0.0151$, and $i = 1.09\degree$, <br/>
Find the precession rates of the orbit of Phobos in units of $\degree/\text{dy}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

To find the precession rates, we need $K$, and so we need $T$ because we need to find $n = 360\degree/T$ (equation $25$) for $K$.\
By equation $15$:
```math
\begin{align}
T &= \sqrt{\frac{4\pi^2 a^3}{GM}}\\
&= \sqrt{\frac{4\pi^2 (9376000)^3}{(6.674\cdot10^{-11})(6.4171\cdot10^{23})}}\\
&= 27564s\\
&= 0.319\text{ dy}
\end{align}
```
Now find $K$ by equation $48$.
```math
\begin{align}
K &= \frac{3J_2nR_{\text{avg}}^2}{2a^2(1-e^2)^2}\\
&= \frac{3\cdot(1.96045\cdot10^{-3})\cdot(360\degree/0.319)\cdot(3389.5)^2}{2\cdot(9376)^2\cdot(1-0.0151^2)^2}\\
&= 0.4339 \degree/\text{dy}
\end{align}
```
Then, $\dot\Omega$ is given by equation $50$:
```math
\begin{align}
\dot\Omega &= -K \cos(i) \\
&= -0.4339 \cdot \cos(1.09\degree) \\
&= -0.4338 \degree/\text{dy}
\end{align}
```
And $\dot\omega$ by equation $51$:
```math
\begin{align}
\dot\omega &= K \left(2 - \frac{5}{2}\sin^2(i)\right) \\
&= 0.4339 \cdot \left(2 - \frac{5}{2}\sin^2(1.09\degree)\right) \\
&= 0.8674 \degree/\text{dy}
\end{align}
```
Let's check our answers. A data sheet gives values of
```math
\begin{align}
\dot\Omega &= -0.4358 \degree/\text{dy}\\
\dot\varpi &= 0.4352 \degree/\text{dy}
\end{align}
```
Since we have $\dot\omega$ but the data sheet has $\dot\varpi$, we use equation $41$ with the data sheet values ($i = 1.09\degree$ is very small):
```math
\dot\omega \approx 0.4352 - (-0.4358) = 0.8710\degree/\text{dy}
```
We can see we came pretty close. The discrepancy comes from other perturbation factors, such as the small but not-nonexistent perturbation from the Sun.\
$\blacksquare$

### The Anomalistic Period

Remember in Chapter $2$ when we calculated the mean anomaly to calculate the eccentric anomaly then to calculate the position of the orbiting object. The mean anomaly was calculated by:
```math
M = \frac{2\pi}{T}\cdot t
```
Where $t$ was measured from the time of periapsis. However, when dealing with moons, the periapsis would have moved by the time the moon makes an orbit. Thus, the $T$ used in the formula for $M$ cannot be just the simple $T$ calculated from $15$, which is just the (average) time it takes for the moon to reach the same location (longitude or right ascension) again. (This period is called the *sidereal period*.) To account for the fact that the periapsis has moved, we need a new period, and this is called the *anomalistic period* (as it is the period of repetition of the anomalies). It can be calculated as such:
```math
T_A = \frac{T_S T_{\dot\varpi}}{T_{\dot\varpi} - T_S}\tag{53}
```
Where $T_S$ is the sidereal period and $T_{\dot\varpi}$ is the period of the precession of periapsis, positive if the precession is in the direction of the orbit, and negative if not.

#### Example 11
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The moon has a sidereal period of $27.321 \text{ dy}$, and the longitude of the perigee precesses by $1 \text{ rev}$ every $3233\text{ dy}$. <br/>
What is the length of the anomalistic period of the Moon?
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $53$:
```math
\begin{align}
T_A &= \frac{27.321 \cdot 3233}{3233 - 27.321}\\
&= 27.554\text{ dy}
\end{align}
```
Which we can now use to calculate the mean anomaly.\
$\blacksquare$

### Multi Moon Systems
For multi moon systems, because the moons perturb each other, the math gets increasingly difficult, and the only plausible way to calculate the location of the moons is with a numerical integrator of the equations of motion. For example, in example $9$, solving for the precession of Deimos would result in less accurate results because of the perturbation of Deimos by Phobos. The only reason example $9$ worked is because Deimos is much smaller than Phobos and so the effect Deimos has on Phobos is almost negligible.

Recommended solutions are ignoring the perturbation of moons by other moons and just focusing on the perturbations by the equatorial bulge or by the Sun, or just making up precession values for multi moon systems.
