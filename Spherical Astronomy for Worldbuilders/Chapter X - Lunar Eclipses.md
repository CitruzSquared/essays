## 10. Lunar Eclipses
Lunar eclipses happen when the Earth casts a shadow on the Moon. As it is a phenomenon that really changes the appearance of the Moon, anywhere on the Earth that can see the Moon during a lunar eclipse will see it, unlike solar eclipses. This makes the discussion of lunar eclipses much simpler than the discussion of solar eclipses.

### Penumbral, Partial, and Total Lunar Eclipses
The Earth has two shadows: the penumbra and umbra. Depending on which parts of the shadow the Moon passes through, the eclipse can be categorized in four ways:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/edf30659-ca55-4ea9-af22-675bb076c4fa" width="250"/> In this diagram, the penumbra of the Earth is the lightly shaded region (the larger shaded circle) and the umbra is the heavily shaded region (the smaller shaded circle). Depending on the position of the Moon, ($1$, $2$, $3$, or $4$), the eclipse can be categorized as:

1. Partial Penumbral Eclipse
2. Partial Eclipse
3. Total Eclipse
4. Total Penumbral Eclipse

However, because penumbral eclipses are hardly noticeable, both $1$ and $4$ are simply collectively referred to as "penumbral eclipses", and the distinction between partial and total penumbral eclipse is usually not made.

### Conditions for Eclipse
A lunar eclipse can only happen when the Moon is on the opposite side of the Earth from the Sun, i.e. they only happen during full moons. We can say that the shadow of the Earth is a circlular disk projected at the distance of the Moon.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/9424197a-c38e-4198-9931-df3ae6f1a58b" width="175"/> In this diagram, if $S$ is the center of the Sun and $E$ is the center of the Earth, and $LM$ is the radius of the Earth's shadow at the distance of the Moon, then the apparent radius of the shadow of the Earth is $LEM$.

We further have that:
```math
\begin{align}
LEM &= BLE - LVE\\
&= BLE - (AES - EAV) \\
&= \pi - s' + \pi'
\end{align}
```
Where $\pi$ is the equatorial horizontal parallax of the Moon, $s'$ is the apparent radius of the Sun, and $\pi'$ is the equatorial horizontal parallax of the Sun.

Since the Moon and the Earth's shadow are at the same distance from the Earth, their parallaxes are equal (and thus no relative parallax) and therefore the least separation of the Moon and shadow $\Sigma$ must be:
```math
\Sigma < (\pi - s' + \pi') + s
```
Which, using equation $9.1$, becomes:
```math
\beta < (\pi - s' + \pi' + s)\sec(I') \tag{10.1}
```
Where $\beta$ is the ecliptic latitude of the Moon at the moment of opposition.

The above is the case for total lunar eclipse. For penumbral lunar eclipses, the apparent radius of the Earth's shadow can be expressed as $\pi + s' + \pi'$ and thus the condition for eclipse is:
```math
\beta < (\pi + s' + \pi' + s)\sec(I') \tag{10.2}
```

#### Example 10.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine if the full Moon of $\text{November, } 2021$ will result in a lunar eclipse.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We can find via the method of example $4.4$, but by solving for when the elongation is $180\degree$ (or the time when elongation $-$ $180\degree = 0$) the new Moon occured on $\text{November 19, } 2021$ at $08:57$. We now do similar calculations as example $9.1$, and find that:
```math
(\pi + s' + \pi' + s)\sec(I') < \beta < (\pi - s' + \pi' + s)\sec(I') 
```
Thus a partial eclipse of the Moon would occur.\
$\blacksquare$

### Computations
A lunar eclipse can be modeled as an eclipse of the Sun by the Earth from the Moon's perspective. Thus, we can calculate the Besselian elements just like solar eclipses, except we use the Moon as the reference.

The direction of the axis of the shadow, given by the quantities $G$, $a$, and $d$, are now simply the direction of the Sun from the Earth, and $a$ and $d$ are just the geocentric right ascension and declination of the Sun.

Using these, the Besselian elements can be calculated (with distances being in units of the radius of the Moon), and the times of contact can be calculated in exactly the same way as example $9.5$. If we model the Moon as a sphere (which for all intents and purposes, is accurate), the need for successive approximations of $p$ become unnecessary and $p = 1$ for all cases. Calculating the exact latitude and longitude of contact is largely unnecessary, and only the times are needed.

Once the times of contact are found, anywhere on the Earth that can see the Moon at these times, which can be found by the method of example $6.6$, using the parallax corrected sunrise equation (equation $8.5$) for more accuracy.

The degree of obscuration of the Moon can be calculated as:
```math
\text{Magnitude} = \frac{l - m}{2k}
```
Where $l$ is the radius of the shadow of the Earth, using $l_1$ for penumbral magnitude and $l_2$ for umbral magnitude, $m$ is $\sqrt{x^2 + y^2}$, and $k$ is the radius of the Moon.
