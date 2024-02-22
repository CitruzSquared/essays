(Continued from Part A...)

### Brightness

[**Apparent magnitude**](https://en.wikipedia.org/wiki/Apparent_magnitude) (denoted $m$) is a logarithmic scale measuring how bright objects *look* in the sky. It stems from a centuries-old system of categorizing stars, class $1$ for the brightest stars and class $6$ for the dimmest. Thus, our modern system of apparent magnitude also operates with **smaller magnitudes being brighter**: magnitude is defined such that a decrease in apparent magnitude by $1$ is a $100^{1/5} = 2.512$ times increase in brightness.

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
Where $m_{\text{Sun}}$ is the apparent magnitude of the Sun at $1 \text{ AU}$, $a$ is the [albedo](https://en.wikipedia.org/wiki/Albedo) of the planet, a value between $0$ and $1$ describing how much light it reflects (i.e. how white the planet is), $r$ is the radius of the planet, and $d_0$ is the length of $1 \text{ AU}$, approximately $149,600,000,000\text{ m}$.

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
Given that the albedo of Venus is $0.76$ and that its radius is $6\:051\:000 \text{ m}$, <br/>
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
\text{Venus Phase Angle } &= 55\degree\enspace43'\enspace\enspace57.60''
\end{align}
```
We also found out in example $15$ that the apparent magnitude of the Sun from $1\text{ AU}$ away is $-26.8$.\
Thus, by equation $65$:
```math
\begin{align}
H &= -26.8 - 5\log_{10}\left(\frac{\sqrt{0.76}\cdot 6\:051\:000}{149\:600\:000\:000}\right) \\
&= -4.5365
\end{align}
```
And then by equation $67$:
```math
\begin{align}
q(\alpha) &= \frac{2}{3}\left(\left(1- \frac{55\degree\enspace43'\enspace\enspace57.60''}{180\degree}\right)\cos(55\degree\enspace43'\enspace\enspace57.60'') + \frac{1}{\pi}\sin(55\degree\enspace43'\enspace\enspace57.60'')\right) \\
&= 0.43452
\end{align}
```
And thus finally by equation $66$:
```math
\begin{align}
m &= -4.5365 + 5\log_{10}\left(\frac{107\:786\:800\:000 \cdot 177\:754\:720\:000}{149\:600\:000\:000^2}\right) - 2.5\log_{10}(0.43452)\\
&= -3.97
\end{align}
```
Comparing this to the true value of $-4.1$, we can see how crude the approximation really is. However, this is the best we can realistically do.\
$\blacksquare$

### Apparent Retrograde Motion
