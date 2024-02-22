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

Then, the apparent magnitude can be calculated by:
```math
m = H + 5\log_{10}\left(\frac{d_{PS} \cdot d_{PO}}{d_0^2}\right) - 2.5\log_{10}(q(\alpha))\tag{66}
```
Where $d_{PS}$ is the distance from the planet to the Sun in meters, $d_{PO}$ is the distance from the planet to the observer in meters, $d_0$ is the same $d_0$ from before, $1 \text{ AU}$, and $\alpha$ is the phase angle of the planet in degrees.

$q(\alpha)$ is known as the *phase integral*. If we assume planets to be ideally diffusely reflecting spheres, it is given as:
```math
q(\alpha) = \frac{2}{3}\left(\left(1- \frac{\alpha}{180\degree}\right)\cos(\alpha) + \frac{1}{\pi}\sin(\alpha)\right)\tag{67}
```

#### Example 17
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Calculate the apparent magnitude of Venus on $\text{January 1, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>
