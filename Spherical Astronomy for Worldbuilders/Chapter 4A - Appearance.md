# Part 2. Terrestrial Observations
In the last part, we discussed how to calculate the positions of the planets in space. Let's now discuss how they look from the Earth.

## IV. Appearance

### Apparent Size
How large do objects in space appear from our point of view?

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/cddae410-88cf-4199-b2ee-58052fe983e2" width="300"/>  Well, in this diagram, an observer at point $O$ is looking at an object with center $C$ and radius $r$. The [*angular size*](https://en.wikipedia.org/wiki/Angular_diameter) (also called the *angular diameter*) is then given by the angle $AOA'$, which is $2 \cdot AOC$. The angle $AOC$, which is called the *angular radius*, is given by this formula:
```math
AOC = \arcsin\left(\frac{r}{OC}\right) \tag{54}
```
Because $AO$ makes a right angle with $AC$, the radius. Thus,
```math
AOA' = 2\arcsin\left(\frac{r}{OC}\right)\tag{55}
```

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
This can yet again be done with the law of cosines:
```math
\text{Phase Angle } = \arccos\left(\frac{\rho^2 + r^2 - R^2}{2\rho r}\right)\tag{58}
```
Note that if all the distances are known already, then steps $1$ and $2$ can be skipped.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3d239d87-232b-45f0-9c06-a99790222a62" width="300"/> Now in this diagram, we can see that the section of $HH'$ that is illuminated by the Sun is $HA$, or $HP + PA$. $HP$ is just the planetary radius $R_P$, and $PA$ is given by $R_P\cos(LPH')$.

But, $LPH' = 90\degree - EPL$, but also $SPE = 90\degree - EPL$, so $SPE = LPH'$. Thus the section of $HH'$ illuminated by the Sun is given by $R_P + R_P\cos(SPE)$. Dividing this all by the length of $HH' = 2R_P$, we obtain:
```math
\text{Phase } = \frac{1 + \cos(SPE)}{2}\tag{59}
```
Where $\text{Phase}$ is the fraction of $P$ seen as illuminated from $E$.

<br/>
<br/>
<br/>
<br/>

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/b629786c-b9d4-4f51-a3fb-f3a0a64dded4" width="300"/> Thus in the view from $E$, the planet $P$ would look like this, and if we assume the Sun to be shining from the right:

The section between $H$ and $A'$ would be illuminated if the phase was $< 50$%,\
the section between $H$ and $P$ would be illuminated if the phase was $= 50$%, and\
the section between $H$ and $A$ would be illuminated if the phase was $> 50$%.

<br/>

#### Example 12
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On $\text{January 1, } 2024$, <br/>
Venus was at $\alpha = 16^h\:07^m\:26^s$ and $\delta=-18\degree\:57'\:52''$, and was at a distance $1.1882 \text{ AU}$ from the Earth. <br/>
The Sun was at $\alpha = 18^h\:46^m\:38^s$ and $\delta=-23\degree\:0'\:10''$, and was at a distance $0.9833 \text{ AU}$ from the Earth. <br/>
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
\text{Sun-Earth-Venus Angle } &= \arccos(\sin(-23\degree\:0'\:10'')\sin(-18\degree\:57'\:52'') + \\&\cos(-23\degree\:0'\:10'')\cos(-18\degree\:57'\:52'')\cos(18^h\:46^m\:38^s - 16^h\:07^m\:26^s)) \\
&= 37\degree\:16'\:\:7.87''
\end{align}
```
Then, by equation $57$:
```math
\begin{align}
\text{Sun-Venus Distance } &= \sqrt{1.1882^2 + 0.9833^2 - 2\cdot1.1882\cdot0.9833\cdot\cos(37\degree\:16'\:\:7.87'')}\\
&= 0.7205 \text{ AU}
\end{align}
```
Now, by equation $58$:
```math
\begin{align}
\text{Phase Angle } &= \arccos\left(\frac{1.1882^2 + 0.7205^2 - 0.9833^2}{2\cdot1.1882\cdot0.7205}\right)\\
&= 55\degree\:43'\:\:57.60''
\end{align}
```
Then finally by equation $59$:
```math
\begin{align}
\text{Phase } (\%) &= \frac{1 + \cos(55\degree\:43'\:\:57.60'')}{2} \cdot 100\% \\
&= 78.2 \%
\end{align}
```
And thus Venus would look something like:
<p align="center">

  <img width="100" src="https://github.com/CitruzSquared/essays/assets/23460281/ed1b89ff-3c4c-4e04-84d7-e0658861d887">
</p>

Where the bright side faces in the direction of the Sun. (This *is* truly how Venus looked on that day, but flipped – the Sun was shining from the left.) \
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
\alpha_V &= 16^h\:07^m\:26^s\\
\delta_V &= -18\degree\:57'\:52''\\
\\
\alpha_S &= 18^h\:46^m\:38^s \\
\delta_S &= \delta=-23\degree\:0'\:10''
\end{align}
```
We need the elongation, so we use equation $1$, $2$, $4$ and equation $60$:
```math
\begin{align}
\lambda_V &= 243\degree\:29'\:35.63''\\
\lambda_S &= 280\degree\:43'\:11.52''\\
\therefore \epsilon &= -37\degree\:13'\:35.89''\\
\end{align}
```
The elongation is negative, therefore it is a morning star. Additionally, it would be the Eastern side of Venus that would be illuminated (Venus is west of the Sun, therefore its Eastern side faces the Sun).\
$\blacksquare$

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/f54ce1cc-10c2-4dfd-a5a4-1218b70aa117" width="450"/> In this diagram, the orbit of 3 planets are shown with the Sun at the center $S$. The middle orbit is the orbit of Earth, which is denoted by $O$. The orientation is such that the direction of West to East is counterclockwise.

Let us focus on the inner planet's orbit. When the inner planet (which we will call $I$) is at $E$, its elongation is at its maximum positive value. It is the furthest possible it can be from the Sun. Thus this phenomenon is called "greatest eastern elongation". Similarly, when the inner planet is at $W$, its elongation is at its minimum value (maximum negative value), and thus this phenomenon is called its "greatest western elongation" Because these points $E$ and $W$ happen at the points where the line $OI$ is tangent to the orbit of $I$, the phase of $I$ will more or less be $50\%$ at these points. The maximum elongation can be calculated as:
```math
\epsilon_{\text{max}} = \arcsin\left(\frac{a_I}{a_O}\right) \tag{61}
```
But because orbits are not perfect circles, this formula (and also the fact that the phase of $I$ is $50$% at max elongation) is not exact, and the value of this maximum elongation will change depending on the exact orientation of the planets.

Now onto the outer planet. The outer planet cannot have a maximum elongation, its elongation can take any value between $-180\degree$ and $180\degree$. Moons that orbit the Earth also cannot have a maximum elongation. When the elongation is $90\degree$ (i.e. at the point $Q$ or $Q'$), the planet is known to be at *quadrature*. 

When the elongation of any object is $0\degree$, there is no difference in longitude between it and the Sun, and it is known to be [*in conjunction*](https://en.wikipedia.org/wiki/Conjunction_(astronomy)) with the Sun. Note that for inner planets, conjunction can happen at two points in the orbit (at the point $B$ when the phase is $\approx100$% (called the "superior conjunction), and at the point $C$ when the phase is $\approx0$% (called the inferior conjunction)). For outer planets, conjunction can only happen when it is on the far side of the Sun (point $A$). For moons, conjunction can only happen when the moon is on the near side of the Sun (phase $\approx0$%), and this is called the [*new Moon*](https://en.wikipedia.org/wiki/New_moon).

When the elongation is $180\degree = -180\degree$, the object is known to be at [*opposition*](https://en.wikipedia.org/wiki/Opposition_(astronomy)) with the Sun, and can only happen with outer planets (when the outer planet is at $D$) and moons (in which case this is known as the [*full Moon*](https://en.wikipedia.org/wiki/Full_moon)). Note that for outer planets, the phase is $\approx100$% at both opposition and conjunction.

Because the Moon orbits from West to East, its elongation increases as time passes. It goes from being in conjunction to the Sun to being in quadrature, then to being in opposition, then to quadrature again before going back to being in conjunction. It is easy to see that when the Moon's elongation is East, it is *waxing* (its phase is getting larger), and its elongation is West, it is *waning* (its phase is getting smaller).

In addition, if the orbit of a planet has $0\degree$ inclination with respect to the ecliptic, the Sun-Earth-Planet angle of equation $56$ is just equal to the elongation.

### The Synodic Period

The time it takes for the elongation to repeat is called the *synodic period*. This is also the time it takes for the phases to repeat as the phases depend on elongation (the Sun-Earth-Object angle can be approximated as the elongation). Because the elongation depends on the location on both the object and the Earth, the formula involves both periods:
```math
T_{P \text{ Synodic}} = \left|\frac{T_E T_P}{T_E - T_P}\right|\tag{62}
```
where $T$ denotes the sidereal period, and $E$ denotes the Earth, and $P$ denotes the object.\
This formula is not exact as the orbits of the planets are not perfect circles. However it gives the average value.

Evidently, the Earth does not have a synodic orbital period.

#### Example 14
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given their sidereal orbital periods, calculate the synodic period (with respect to Earth) for every planet in the Solar System and the Moon.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

The sidereal periods are given as such:
```math
\begin{array}{cc}\hline \text{Name} & \text{Sidereal Period} \\ \hline
\text{Mercury} & 87.969 \text{ dy} \\
\text{Venus} & 224.70 \text{ dy} \\
\text{Earth} & 365.24 \text{ dy} \\
\text{Moon} & 27.321 \text{ dy} \\
\text{Mars} & 686.98 \text{ dy} \\
\text{Jupiter} & 4332.6 \text{ dy} \\
\text{Saturn} & 10755  \text{ dy} \\
\text{Uranus} & 30688 \text{ dy} \\
\text{Neptune} & 60195 \text{ dy} \\ \hline
\end{array}
```

The synodic orbital period is given by equation $62$ and $63$. So for Mercury:
```math
\begin{align}
T_{\text{Mercury Synodic}} &= \frac{365.24 \cdot 87.969}{365.24 - 87.969}\\
&= 115.88\text{ dy}
\end{align}
```

Doing this for all the planets:
```math
\begin{array}{ccc}\hline \text{Name} & \text{Sidereal Period} & \text{Synodic Period} \\ \hline
\text{Mercury} & 87.969 \text{ dy} & 115.88\text{ dy} \\
\text{Venus} & 224.70 \text{ dy} & 583.96\text{ dy}  \\
\text{Earth} & 365.24 \text{ dy} & -  \\
\text{Moon} & 27.321 \text{ dy} & 29.530\text{ dy}  \\ 
\text{Mars} & 686.98 \text{ dy} & 779.86\text{ dy}  \\
\text{Jupiter} & 4332.6 \text{ dy} & 398.86\text{ dy}  \\
\text{Saturn} & 10755  \text{ dy} & 378.08\text{ dy}  \\
\text{Uranus} & 30688 \text{ dy} & 369.64\text{ dy}  \\
\text{Neptune} & 60195 \text{ dy} & 367.47\text{ dy}  \\\hline
\end{array}
```
You can see that the longer the sidereal period is for a planet compared to the Earth's, the closer the synodic period for that planet is to the Earth year. This makes sense because if a planet has a very long orbital period, it is effectively stationary, and then the only factor affecting its elongation is the Earth's orbit.

Additionally, the synodic period of the Moon $(29.53 \text{ dy})$, by definition of the synodic period, is the average time it takes for the Moon to go from new Moon to new Moon, or from full Moon to full Moon. This is known as the lunar month, and is the basis of the length of the month in many calendar systems around the world, such as the Islamic, Jewish, and Chinese calendars.\
$\blacksquare$

Applying the synodic period formula for two far-out planets gives the (very) approximate time between two conjunctions of those two planets.

### Solving for Time of Conjunction
Because the motion of the planets is very complicated, we cannot exactly solve for the time when two bodies are at the same ecliptic longitude. However, we can use numerical methods to get arbitrarily close.

We cannot use the Newton method as we did in chapter $2$ because we do not know the derivative of the function we are going to solve for (the difference in longitude between two objects at time $t$). Thus, we have to use a more crude method: [bisection](https://en.wikipedia.org/wiki/Bisection_method).

Bisection works as follows:\
To find the solution of an equation $f(t) = 0$,
- Step 1. Find two values of $t$, $a$ and $b$, such that the sign of $f(a)$ is the opposite of the sign of $f(b)$.\
If $f(t)$ is continuous between $a$ and $b$, this guarantees that a solution is in between $a$ and $b$.
- Step 2. Find the midpoint of $a$ and $b$, which we will call $c$.
- Step 3. Find $f(c)$ and compare its sign to $f(a)$ and $f(b)$. \
If $\text{sign}(f(c)) = \text{sign}(f(a))$, set $a = c$.\
If $\text{sign}(f(c)) = \text{sign}(f(b))$, set $b = c$.
- Step 4. Repeat steps $2$ and $3$ until you reach a value of $f(c)$ close enough to $0$.

#### Example 15
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the time of the first new Moon of $2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

A Lunar Ephemeris can be found [here](https://astropixels.com/ephemeris/moon/moon2024.html). This ephemeris has a column for lunar events, but we will ignore this as this data is not available to us in a worldbuilding setting.

- We use bisection to solve for when the elongation of the Moon is $0\degree$.
  
We first set $a = \text{ January 1, } 2024$ as the first new Moon of 2024 could not have been before this date.\
The elongation on this date was $-124.0\degree$. (We would have to calculate the elongation in a fictional setting as an ephemeris would not be available.) Therefore we need the elongation at time $b$ to be positive.

We set $b$ to be $a + 0.5\text{ Synodic Period}$, because then, the elongation would be $\approx -124.0\degree + 180\degree$, which is a positive number.\
Note that if we subtracted $0.5\text{ Synodic Period}$ instead, the elongation would be $\approx -124.0\degree - 180\degree = -304\degree = 56\degree$, which is also a positive number, but this does not work as $f(t)$ (the elongation at time $t$) is not continuous in this region. (There is a jump from $-180\degree$ to $180\degree$).

Now we calculate $b$ to be $\text{ January 16, } 2024$, and the elongations at $a$ and $b$ were:
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 1, } 2024 & -124.0\degree \\
b & \text{ January 16, } 2024 & +61.8\degree \\ \hline
\end{array}
```
Now we find $c$, be the midpoint of $a$ and $b$, to be $\text{ January 8, } 2024$.
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 1, } 2024 & -124.0\degree \\
b & \text{ January 16, } 2024 & +61.8\degree \\ \hline
c & \text{ January 8, } 2024 & -45.7\degree \\ \hline
\end{array}
```
The sign of the elongation at time $c$ is the same as the sign at time $a$, so we set $a = c$:
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 8, } 2024 & -45.7\degree \\
b & \text{ January 16, } 2024 & +61.8\degree \\ \hline
\end{array}
```
Now we repeat the steps: we find the midpoint $c$ and the elongation at $c$ again:
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 8, } 2024 & -45.7\degree \\ 
b & \text{ January 16, } 2024 & +61.8\degree \\ \hline
c & \text{ January 12, } 2024 & +8.5\degree \\  \hline
\end{array}
```
Now the sign of the elongation at time $c$ is equal to the sign at time $b$, so we set $b = c$:
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 8, } 2024 & -45.7\degree \\
b & \text{ January 12, } 2024 & +8.5\degree \\ \hline
\end{array}
```
We repeat again. We find $c$ and compare signs of the elongation:\
$c = \text{ January 10, } 2024, \epsilon = -20.6\degree$, set $a = c$.
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 10, } 2024 & -20.6\degree \\
b & \text{ January 12, } 2024 & +8.5\degree \\ \hline
\end{array}
```
Repeat once more:
$c = \text{ January 11, } 2024, \epsilon = -8.4\degree$, set $a = c$.
```math
\begin{array}{ccc}\hline \text{t} & \text{Date} & \text{Elongation} \\ \hline
a & \text{ January 11, } 2024 & -8.4\degree \\
b & \text{ January 12, } 2024 & +8.5\degree \\ \hline
\end{array}
```
The ephemeris does not go into hourly detail so we must stop here and say the new Moon happened at some time in between $\text{ January 11, } 2024$ and $\text{ January 12, } 2024$, i.e. some time during the day of $\text{ January 11, } 2024$, but we can go one step into the blind and calculate $c$ one more time for some extra precision: $c = \text{ January 11, } 2024$ at $12:00$. (We are remarkably close, the new Moon was on $\text{ January 11, } 2024$ at $11:59$.)

In a worldbuilding setting, we can calculate the elongation at times $a$, $b$, and $c$ at any detail we want using the methods from chapters $2$ and $3$ (we would not have to round to the nearest day, because we would not be using a pre-made ephemeris). Thus we can repeat this process **to arbitrary precision**.

We could have just simply calculated the elongation at even time intervals starting from $\text{ January 1, } 2024$, but that is very inefficient and only guarantees precesion up to the size of the time intervals we are taking. Therefore, bisection is better.

The time of conjunction (or any elongation, not just conjunction) of any two bodies can be calculated this way.\
$\blacksquare$

### Brightness
(Continued in Part B...)
