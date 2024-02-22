(Continued from Part A...)

### Brightness

[**Apparent magnitude**](https://en.wikipedia.org/wiki/Apparent_magnitude) (denoted $m$) is a logarithmic scale measuring how bright objects *look* in the sky. It stems from a centuries-old system of categorizing stars, class $1$ for the brightest stars and class $6$ for the dimmest. Thus, our modern system of apparent magnitude also operates with **smaller magnitudes being brighter**.

For stars, as they produce their own unchanging light, their apparent magnitude is easily calculable:
```math
m = -2.5\log_{10}\left(\frac{F}{F_0}\right)\tag{63}
```
Where $F$ is the intensity of the starlight at the observer in $\text{W}/\text{m}^2$, and $F_0$ is a constant equaling $2.518\cdot10^{-8} \text{ W}/\text{m}^2$.\
$F$ can be calculated with this formula:
```math
F = \frac{P}{4\pi R^2}\tag{64}
```
Where $P$ is the power output of the star in $\text{W}$, and $R$ is the distance from the star to the observer in $\text{m}$. This makes sense as $4\pi R^2$ is the surface area of a sphere with radius $R$, thus $F$ represents the power output $P$ being spread out over that area.

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

The brightness of planets is harder to calculate.
