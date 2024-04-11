## 10. Lunar Eclipses
Lunar eclipses happen when the Earth casts a shadow on the Moon. As it is a phenomenon that really changes the appearance of the Moon, anywhere on the Earth that can see the Moon during a lunar eclipse will see it, unlike solar eclipses. This makes the discussion of lunar eclipses much simpler than the discussion of solar eclipses.

### Penumbral, Partial, and Total Lunar Eclipses
The Earth has two shadows: the penumbra and umbra. Depending on which parts of the shadow the Moon passes through, the eclipse can be categorized in four ways:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/edf30659-ca55-4ea9-af22-675bb076c4fa" width="250"/> In this diagram, the penumbra of the Earth is the lightly shaded region (the larger shaded circle) and the umbra is the heavily shaded region (the smaller shaded circle). Depending on the position of the Moon, ($1$, $2$, $3$, or $4$), the eclipse can be categorized as:

1. Partial Penumbral Eclipse
2. Partial (Umbral) Eclipse
3. Total (Umbral) Eclipse
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

Now putting the least angular separation between the Moon and the shadow of the Earth as $\Sigma$, and the angular radius of the Earth's penumbra as $f_1$ and the angular radius of the umbra as $f_2$, we have:
```math
\begin{align}
f_1 &= \pi + s' + \pi'\\
f_2 &= \pi - s' + \pi'
\end{align} \tag{10.1}
```
And if we define:
```math
\begin{align}
L_1 = f_1 + s\\
L_2 = f_1 - s\\
L_3 = f_2 + s\\
L_4 = f_2 - s
\end{align} \tag{10.2}
```
We have, if we put $s$ as the apparent radius of the Moon,
```math
\begin{align}
\text{Condition for Partial Penumbral Eclipse: }\Sigma &< L_1\\
\text{Condition for Total Penumbral Eclipse: } \Sigma &< L_2\\
\text{Condition for Partial Eclipse: } \Sigma &< L_3\\
\text{Condition for Total Eclipse: } \Sigma &< L_4\\
\end{align} \tag{10.3}
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

We find that the time of opposition was $\text{September 18, } 2024$, at $02:36$. At this time:
```math
\begin{align}
\lambda_\text{Moon} &=355\degree\:20'\:41.65''\\
\lambda_\text{Sun} &=175\degree\:20'\:41.65''\\
\beta_\text{Moon} &= -1\degree\:0'\:15.19''\\
\Delta_\text{Moon} &= 357\:484.36 \text{ km}\\
\Delta_\text{Sun} &= 150\:315\:226.07\text{ km}
\end{align}
```
Also:
```math
\begin{align}
\text{Earth's equatorial radius } &=6378.137 \text{ km}\\
\text{Moon's radius } &= 1737.4 \text{ km}\\
\text{Sun's radius } &= 696\:000 \text{ km}\\
I &= 5.14\degree
\end{align}
```
Thus by equations $4.1$ and $8.6$:
```math
\begin{alignat}{2}
s &= \arcsin\left(\frac{1737.4}{357\:484.36}\right) &&= 16'\:42.5''\\
s' &= \arcsin\left(\frac{696\:000}{150\:315\:226.07}\right) &&= 15'\:55.07''\\
\pi &= \arcsin\left(\frac{6378.137}{357\:484.36}\right) &&= 1\degree\:1'\:20.32''\\
\pi' &= \arcsin\left(\frac{6378.137}{150\:315\:226.07}\right) &&= 8.75''
\end{alignat}
```
Therefore, by equation $10.1$ and $10.2$:
```math
\begin{alignat}{2}
f_1 &= 1\degree\:1'\:20.32'' + 15'\:55.07'' + 8.75'' &&= 1\degree\:17'\:24.13''\\
f_2 &= 1\degree\:1'\:20.32'' - 15'\:55.07'' + 8.75'' &&= 0\degree\:45'\:34''
\end{alignat}
```
```math
\begin{alignat}{2}
L_1 &= 1\degree\:17'\:24.13'' + 16'\:42.5'' &&= 1\degree\:34'\:6.6''\\
L_2 &= 1\degree\:17'\:24.13'' - 16'\:42.5'' &&= 1\degree\:0'\:41.67''\\
L_3 &= 0\degree\:45'\:34'' + 16'\:42.5'' &&= 1\degree\:2'\:16.47''\\
L_4 &= 0\degree\:45'\:34'' - 16'\:42.5'' &&= 0\degree\:28'\:51.54''
\end{alignat} 
```
To find $\Sigma$, we need $q$ (equations $9.1$ and $9.2$), and therefore we need $\sigma$ and $\mu$, the derivatives of longitudes of the Sun and Moon. We take one hour as the time step.\
At $03:36$:
```math
\begin{align}
\lambda_{\text{Moon}} &=355\degree\:58'\:39.95''\\
\lambda_{\text{Sun}} &=175\degree\:22'\:54.53''
\end{align}
```
Therefore:
```math
\begin{align}
\mu &= \frac{355\degree\:58'\:39.95'' - 355\degree\:20'\:41.65''}{1h} = 37.97'/h\\
\sigma &= \frac{175\degree\:22'\:54.53'' - 175\degree\:20'\:41.65''}{1h} = 2.21'/h
\end{align}
```
Therefore, by equation $9.2$:
```math
\begin{align}
q &= \frac{37.97}{2.21} = 17.181\\
\therefore I' &= \arctan\left(\frac{17.181}{17.181 - 1} \tan(5.14\degree)\right) = 5.456\degree
\end{align}
```
Therefore, by equation $9.1$, $\Sigma$ is:
```math
\Sigma = -1\degree\:0'\:15.19'' \cos(5.456\degree) = -59'\:58.81''
```
But, being a distance, $\Sigma$ must be positive, so we take the absolute value. Comparing the value of $\Sigma$ to the values of $L$, we can see that:
```math
L_4 < \Sigma < L_3
```
And therefore, by equation $10.3$, a partial eclipse of the Moon will occur.\
$\blacksquare$

### Besselian Elements
If we have that:
```math
\begin{align}
v, u, w &= \text{The normalized geocentric equatorial cartesian coordinates of the Moon}\\
\alpha, \delta &= \text{The geocentric equatorial spherical coordinates of the Sun}
\end{align}
```
Then the direction of the shadow is simply given by the opposite direction to the Sun: $a = \alpha + 180\degree$, and $d = -\delta$. The coordinate transformation to the fundamental plane is identical to equation $9.5$:
```math
\displaylines{
a = \alpha + 180\degree \enspace\enspace\text{and}\enspace\enspace d = -\delta\\ \\
R = \begin{bmatrix}
-\sin(a) & \cos(a) & 0\\
-\cos(a) \sin(d) & -\sin(a) \sin(d) & \cos(d) \tag{10.4}\\
\cos(a) \cos(d) & \sin(a) \cos(d) & \sin(d)
\end{bmatrix}
}
```
And then the Moon's coordinates in the fundamental frame is given by:
```math
\begin{bmatrix}
x\\y\\z
\end{bmatrix} = R \begin{bmatrix}
v\\ u \tag{10.5}\\ w
\end{bmatrix}
```
We use the normalized (i.e. magnitude of vector $=$ $0$) coordinates of the Moon because we are dealing with angular distances in the celestial sphere, not true distances as in chapter $9$. If we express angles in radians, angular distances correspond to arc lengths on the sphere.

And thus we have the Besselian elements for lunar eclipses: $x$, $y$, $x'$, $y'$, $s$, $L_1$, $L_2$, $L_3$, and $L_4$, where all angles ($a$, $d$, $s$, $f$, $L$) are expressed in radians.

#### Example 10.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the Besselian elements for the lunar eclipse of $\text{September 18, } 2024$ for the time $02:30$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>
