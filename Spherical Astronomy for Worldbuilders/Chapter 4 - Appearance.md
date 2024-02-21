# Part 2. Terrestrial Observations
In the last part, we discussed how to calculate the positions of the planets in space. Let's now discuss how they look from the Earth.

## IV. Appearance

### Apparent Radius
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/cddae410-88cf-4199-b2ee-58052fe983e2" width="300"/> How large do objects in space appear from our point of view? Well, in this diagram, an observer at point $O$ is looking at an object with center $C$ and radius $r$. The [*angular size*](https://en.wikipedia.org/wiki/Angular_diameter) (also called the *angular diameter*) is then given by the angle $AOA'$, which is $2 \cdot AOC$. The angle $AOC$, which is called the *angular radius*, is given by this formula:
```math
AOC = \arcsin\left(\frac{r}{OC}\right) \tag{53}
```
Because $AO$ makes a right angle with $AC$, the radius. Thus,
```math
AOA' = 2\arcsin\left(\frac{r}{D}\right)\tag{54}
```
where $D$ is the distance to the object, $OC$.

### Phase

Let's now calculate how much of an object would be visible.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6322b87c-a65e-4623-908e-a5a3e4aad970" width="300"/> In this diagram, $S$ is the position of the Sun, $E$ is the position of the Earth, and $P$ is a planet. 

The line $LL'$ perpendicular to $SP$ and delineates the *terminator line* of $P$, or the line where night and day are separated. The line $HH'$ is perpendicular to $EP$ and shows the side of the planet visible to $E$.

The angle $SPE$ is known as the [*phase angle*](https://en.wikipedia.org/wiki/Phase_angle_(astronomy)). It can be calculated as follows:

Step 1: Calculate the angle $SEP$. \
This angle is the angular distance between the Sun and $P$ from the view of the Earth, and can be calculated from the [great circle distance formula](https://en.wikipedia.org/wiki/Great-circle_distance):
```math
SEP = \arccos(\sin(\varphi_S)\sin(\varphi_P) + \cos(\varphi_S)\cos(\varphi_P)\cos(\Delta\vartheta))\tag{55}
```
Where $\varphi_S$ and $\varphi_P$ are the declination or latitude of the Sun and $P$ respectively, and $\Delta\vartheta$ is the difference in right ascension or longitude of the Sun and $P$.

Step 2: Calculate the distance $r$.\
This is the distance from the Sun to $P$, and can be found with the law of cosines:
```math
r = \sqrt{R^2 + \rho^2 - 2R\rho\cos(SEP)}\tag{56}
```

Step 3: Calculate the phase angle.\
This can be done with the law of sines:
```math
\text{Phase Angle } = \arcsin(R\sin(SEP)/r)\tag{57}
```

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3d239d87-232b-45f0-9c06-a99790222a62" width="300"/> Now in this diagram, we can see that the section of $HH'$ that is illuminated by the Sun is $HA$, or $HP + PA$. $HP$ is just the planetary radius $R_P$, and $PA$ is given by $R_P\cos(LPH')$.

But, $LPH' = 90\degree - EPL$, but also $SPE = 90\degree - EPL$, so $SPE = LPH'$. Thus the section of $HH'$ illuminated by the Sun is given by $R_P + R_P\cos(SPE)$. Dividing this all by the length of $HH' = 2R_P$, we obtain:
```math
\text{Phase } = \frac{1 + \cos(SPE)}{2}\tag{58}
```
Where $\text{Phase}$ is the fraction of $P$ seen as illuminated from $E$.

<br/>
<br/>

#### Example 11
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

We get the angular diameter by equation $54$:
```math
\begin{align}
\text{Angular Diameter } &= 2 \arcsin\left(\frac{4.045\cdot10^{-5}\text{ AU}}{1.1882 \text{ AU}}\right) \\
&= 14''
\end{align}
```
Now we have to find the phase:\
By equation $55$:
```math
\begin{align}
\text{Sun - Earth - Venus Angle} &= \arccos(\sin(-23\degree\enspace0'\enspace10'')\sin(-18\degree\enspace57'\enspace52'') + \\&\cos(-23\degree\enspace0'\enspace10'')\cos(-18\degree\enspace57'\enspace52'')\cos(18^h\enspace46^m\enspace38^s - 16^h\enspace07^m\enspace26^s)) \\
&= 37\degree\enspace16'\enspace\enspace7.87''
\end{align}
```
By equation $36$:
```math
\begin{align}
\text{Sun - Venus Distance} &= \sqrt{1.1882^2 + 0.9833^2 - 2\cdot1.1882\cdot0.9833\cdot\cos(37\degree\enspace16'\enspace\enspace7.87'')}\\
&= 0.7205 \text{ AU}
\end{align}
```
Now, by equation $57$:
```math
\begin{align}
\text{Phase Angle } &= \arcsin(0.9833\sin(37\degree\enspace16'\enspace\enspace7.87'')/0.7205)\\
&= 55\degree\enspace44'\enspace\enspace1.61''
\end{align}
```
Then finally by equation $58$:
```math
\begin{align}
\text{Phase } &= \frac{1 + \cos(55\degree\enspace44'\enspace\enspace1.61'')}{2}\\
&= 78.2 \%
\end{align}
```
Which lines up perfectly with real ephemeris data.\
$\blacksquare$

### Elongation
