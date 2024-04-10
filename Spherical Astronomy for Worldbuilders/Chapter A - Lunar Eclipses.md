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
While a lunar eclipse can be modeled as a solar eclipse from the Moon, it is easier to simply consider the angular separation between the Moon and the shadow of the Earth to compute a lunar eclipse. For all intents and purposes, we can say that the shadow of the Earth is a circlular disk located at the antipode of the Sun, projected at the distance of the Moon, and thus the right ascension and declination of the center of the shadow are simply $\alpha_{\text{Sun}} + 180\degree$ and $-\delta_{\text{Sun}}$ respectively.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/9424197a-c38e-4198-9931-df3ae6f1a58b" width="175"/> In this diagram, if $S$ is the center of the Sun and $E$ is the center of the Earth, and $LM$ is the radius of the Earth's shadow at the distance of the Moon, then the apparent radius of the shadow of the Earth is $LEM$.

We further have that:
```math
\begin{align}
LEM &= BLE - LVE\\
&= BLE - (AES - EAV) \\
&= \pi - s' + \pi'
\end{align}
```
Where $\pi$ is the equatorial horizontal parallax of the Moon, $s'$ is the apparent radius of the Sun, and $\pi'$ is the equatorial horizontal parallax of the Sun.\
The above is the case for total lunar eclipse. For penumbral lunar eclipses, the apparent radius of the Earth's penumbra is given as $\pi + s' + \pi'$.

Now putting the least angular separation between the Moon and the shadow of the Earth as $\Sigma$, and the angular size of the Earth's penumbra as $f_1$ and the angular size of the umbra as $f_2$, we have:
```math
\begin{align}
f_1 &= \pi + s' + \pi'\\
f_2 &= \pi - s' + \pi'
\end{align} \tag{10.1}
```
And thus, if we put $s$ as the apparent radius of the Moon,
```math
\begin{align}
\text{For Partial Penumbral Eclipse: }\Sigma &< f_1 + s \\
\text{For Total Penumbral Eclipse: } \Sigma &< f_1 - s \\
\text{For Partial Eclipse: } \Sigma &< f_2 + s \\
\text{For Total Eclipse: } \Sigma &< f_2 - s \\
\end{align} \tag{10.2}
```
Where $\Sigma$ is given by equation $9.1$.

#### Example 10.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine if the full Moon of $\text{September, } 2024$ will result in a lunar eclipse.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We can find the time of opposition via the method of example $4.4$, but by solving for when the elongation is $180\degree$. We redefine the elongation to be expressed in the range of $[0\degree, 360\degree)$ to resolve the problem of the discontinuity, then subtract $180\degree$ from the elongation then use the method of bisection to solve for when this new value of elongation $-$ $180\degree$ is $0\degree$.

We find that the time of opposition was $\text{September 18, } 2024$, at $02:34$.
$\blacksquare$

### Computations
