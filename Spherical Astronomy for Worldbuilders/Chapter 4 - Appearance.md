# Part 2. Terrestrial Observations
In the last part, we discussed how to calculate the positions of the planets in space. Let's now discuss how they look from the Earth.

## IV. Appearance

### Apparent Radius
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/cddae410-88cf-4199-b2ee-58052fe983e2" width="300"/> How large do objects in space appear from our point of view? Well, in this diagram, an observer at point $O$ is looking at an object with center $C$ and radius $r$. The [*angular size*](https://en.wikipedia.org/wiki/Angular_diameter) (also called the *angular diameter*) is then given by the angle $AOA'$, which is $2 \cdot AOC$. The angle $AOC$, which is called the *angular radius*, is given by this formula:
```math
AOC = \arcsin\left(\frac{r}{OC}\right) \tag{54}
```
Because $AO$ makes a right angle with $AC$, the radius. Thus,
```math
AOA' = 2\arcsin\left(\frac{r}{D}\right)\tag{55}
```
where $D$ is the distance to the object, $OC$.

### Phase

Let's now calculate how much of an object would be visible.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6322b87c-a65e-4623-908e-a5a3e4aad970" width="300"/> In this diagram, $S$ is the position of the Sun, $E$ is the position of the Earth, and $P$ is a celestial body (either a planet or a moon). 

The line $LL'$ perpendicular to $SP$ and delineates the *terminator line* of $P$, or the line where night and day are separated. The line $HH'$ is perpendicular to $EP$ and shows the side of the planet visible to $E$.

The angle $SPE$ is known as the [*phase angle*](https://en.wikipedia.org/wiki/Phase_angle_(astronomy)). It can be calculated as follows:

- Step 1: Calculate the angle $SEP$. \
This angle is the angular distance between the Sun and $P$ from the view of the Earth, and can be calculated from the [great circle distance formula](https://en.wikipedia.org/wiki/Great-circle_distance):
```math
SEP = \arccos(\sin(\varphi_S)\sin(\varphi_P) + \cos(\varphi_S)\cos(\varphi_P)\cos(\Delta\vartheta))\tag{56}
```
Where $\varphi_S$ and $\varphi_P$ are the declination or latitude of the Sun and $P$ respectively, and $\Delta\vartheta$ is the difference in right ascension or longitude of the Sun and $P$.

- Step 2: Calculate the distance $r$.\
This is the distance from the Sun to $P$, and can be found with the law of cosines:
```math
r = \sqrt{R^2 + \rho^2 - 2R\rho\cos(SEP)}\tag{57}
```

- Step 3: Calculate the phase angle.\
This can be done with the law of sines:
```math
\text{Phase Angle } = \arcsin(R\sin(SEP)/r)\tag{58}
```

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3d239d87-232b-45f0-9c06-a99790222a62" width="300"/> Now in this diagram, we can see that the section of $HH'$ that is illuminated by the Sun is $HA$, or $HP + PA$. $HP$ is just the planetary radius $R_P$, and $PA$ is given by $R_P\cos(LPH')$.

But, $LPH' = 90\degree - EPL$, but also $SPE = 90\degree - EPL$, so $SPE = LPH'$. Thus the section of $HH'$ illuminated by the Sun is given by $R_P + R_P\cos(SPE)$. Dividing this all by the length of $HH' = 2R_P$, we obtain:
```math
\text{Phase } = \frac{1 + \cos(SPE)}{2}\tag{59}
```
Where $\text{Phase}$ is the fraction of $P$ seen as illuminated from $E$.

<br/>
<br/>

#### Example 12
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On $\text{January 1, } 2024$, <br/>
Venus was at $\alpha = 16^h\enspace07^m\enspace26^s$ and $\delta=-18\degree\enspace57'\enspace52''$, and was at a distance $1.1882 \text{ AU}$ from the Earth. <br/>
The Sun was at $\alpha = 18^h\enspace46^m\enspace38^s$ and $\delta=-23\degree\enspace0'\enspace10''$, and was at a distance $0.9833 \text{ AU}$ from the Earth. <br/>
Given Venus' radius is $4.045\cdot10^{-5}\text{ AU}$, calculate the angular size and phase (as a percentage) of Venus on $\text{January 1, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We get the angular diameter by equation $55$:
```math
\begin{align}
\text{Angular Diameter } &= 2 \arcsin\left(\frac{4.045\cdot10^{-5}\text{ AU}}{1.1882 \text{ AU}}\right) \\
&= 14''
\end{align}
```
Now we have to find the phase:\
By equation $56$:
```math
\begin{align}
\text{Sun-Earth-Venus Angle } &= \arccos(\sin(-23\degree\enspace0'\enspace10'')\sin(-18\degree\enspace57'\enspace52'') + \\&\cos(-23\degree\enspace0'\enspace10'')\cos(-18\degree\enspace57'\enspace52'')\cos(18^h\enspace46^m\enspace38^s - 16^h\enspace07^m\enspace26^s)) \\
&= 37\degree\enspace16'\enspace\enspace7.87''
\end{align}
```
Then, by equation $57$:
```math
\begin{align}
\text{Sun-Venus Distance } &= \sqrt{1.1882^2 + 0.9833^2 - 2\cdot1.1882\cdot0.9833\cdot\cos(37\degree\enspace16'\enspace\enspace7.87'')}\\
&= 0.7205 \text{ AU}
\end{align}
```
Now, by equation $58$:
```math
\begin{align}
\text{Phase Angle } &= \arcsin(0.9833\sin(37\degree\enspace16'\enspace\enspace7.87'')/0.7205)\\
&= 55\degree\enspace44'\enspace\enspace1.61''
\end{align}
```
Then finally by equation $59$:
```math
\begin{align}
\text{Phase } &= \frac{1 + \cos(55\degree\enspace44'\enspace\enspace1.61'')}{2}\\
&= 78.2 \%
\end{align}
```
And thus Venus would look something like:
<p align="center">
  <img width="100" src="https://github.com/CitruzSquared/essays/assets/23460281/fbf93871-95be-4f74-9cbf-3089e599038f">
</p>

$\blacksquare$

### Elongation

The [*elongation*](https://en.wikipedia.org/wiki/Elongation_(astronomy)) is the difference in ecliptic longitude between an object and the Sun.
```math
\epsilon_{\text{Object}} = \lambda_{\text{Object}} - \lambda_{\text{Sun}} \tag{60}
```
This angle is expressed in a range of $(-180\degree,180\degree]$. Thus, if the elongation is positive, the object is *East* of the Sun. This means it will rise after the Sun (because the Earth rotates from West to East, things further East will become visible later), and thus also set after the Sun. This means the object will be *visible in the evening*. If the elongation is negative, the object is *West* of the Sun (Remember that ecliptic longitude is measured with East as positive), and by the same reasoning, will be *visible in the morning*. If the elongation is $\approx180\degree$, the object will be visible basically all throughout the night, and if the elongation is $\approx0\degree$, it won't be visible at all since it is too close to the Sun.

#### Example 13
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given the data from example $12$, was Venus a morning star or an evening star on $\text{January 1, } 2024$? <br/>
Use $\varepsilon = 23.44\degree$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

The data from example 12:
```math
\begin{align}
\alpha_V &= 16^h\enspace07^m\enspace26^s\\
\delta_V &= -18\degree\enspace57'\enspace52''\\
\\
\alpha_S &= 18^h\enspace46^m\enspace38^s \\
\delta_S &= \delta=-23\degree\enspace0'\enspace10''
\end{align}
```
We need the elongation, so we use equation $1$, $2$, $4$ and equation $60$:
```math
\begin{align}
\lambda_V &= 243\degree\enspace29'\enspace35.63''\\
\lambda_S &= 280\degree\enspace43'\enspace11.52''\\
\therefore \epsilon &= -37\degree\enspace13'\enspace35.89''\\
\end{align}
```
The elongation is negative, therefore it is a morning star. Thus the Eastern side of Venus would be illuminated (Venus is west of the Sun, therefore its Eastern side faces the Sun).\
$\blacksquare$

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/f54ce1cc-10c2-4dfd-a5a4-1218b70aa117" width="450"/> In this diagram, the orbit of 3 planets are shown with the Sun at the center $S$. The middle orbit is the orbit of Earth, which is denoted by $O$. The orientation is such that the direction of West to East is counterclockwise.

Let us focus on the inner planet's orbit. When the inner planet (which we will call $I$) is at $E$, its elongation is at its maximum positive value. It is the furthest possible it can be from the Sun. Thus this phenomenon is called "greatest eastern elongation". Similarly, when the inner planet is at $W$, its elongation is at its minimum value (maximum negative value), and thus this phenomenon is called its "greatest western elongation" Because these points $E$ and $W$ happen at the points where the line $OI$ is tangent to the orbit of $I$, the phase of $I$ will more or less be $50\%$ at these points. The maximum elongation can be calculated as:
```math
\epsilon_{\text{max}} = \arcsin\left(\frac{a_I}{a_O}\right) \tag{61}
```
But because orbits are not perfect circles, this formula (and also the fact that the phase of $I$ is $50$% at max elongation) is not exact, and the value of this maximum elongation will change depending on the exact orientation of the planets.

Now onto the outer planet. The outer planet cannot have a maximum elongation, its elongation can take any value between $-180\degree$ and $180\degree$. Moons that orbit the Earth also cannot have a maximum elongation. When the elongation is $90\degree$ (i.e. at the point $Q$ or $Q'$), the planet is known to be at *quadrature*. 

When the elongation of any object is $0\degree$, there is no difference in longitude between it and the Sun, and it is known to be [*in conjunction*](https://en.wikipedia.org/wiki/Conjunction_(astronomy)) with the Sun. Note that for inner planets, conjunction can happen at two points in the orbit (at the point $B$ when the phase is $\approx100$% (called the "superior conjunction), and at the point $C$ when the phase is $\approx0$% (called the inferior conjunction)). For outer planets, conjunction can only happen when it is on the far side of the Sun (point $A$). For moons, conjunction can only happen when the moon is on the near side of the Sun (phase $\approx0$%), and this is called the [*new moon*](https://en.wikipedia.org/wiki/New_moon).

When the elongation is $180\degree = -180\degree$, the object is known to be at [*opposition*](https://en.wikipedia.org/wiki/Opposition_(astronomy)) with the Sun, and can only happen with outer planets (when the outer planet is at $D$) and moons (in which case this is known as the [*full moon*](https://en.wikipedia.org/wiki/Full_moon)). Note that for outer planets, the phase is $\approx100$% at both opposition and conjunction.

Because the Moon orbits from West to East, its elongation increases as time passes. It goes from being in conjunction to the Sun to being in quadrature, then to being in opposition, then to quadrature again before going back to being in conjunction. It is easy to see that when the Moon's elongation is East, it is *waxing* (its phase is getting larger), and its elongation is West, it is *waning* (its phase is getting smaller).

### The Synodic Period
