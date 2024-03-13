# Part 3. Eclipses

## IX. Solar Eclipses

### Condition for Eclipse
A solar eclipse can only happen if the Moon and the Sun are in the sky in the same position, i.e. only at new Moon. Not all new moons result in a solar eclipse however, due to the inclination of the Moon's orbit to the Ecliptic.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/7bda2d9e-5464-4488-9f92-8359beaccd5c" width="250"/> Consider this diagram. In this diagram, the line $SN$ is the ecliptic and $MN$ is the orbit of the Moon, and therefore $N$ is the lunar orbital (descending) node. Therefore the Moon moves along $MN$ and the Sun moves along $SN$ at a slower pace. 

Say $M$ and $S$ are the positions of the Moon and Sun respectively at the time of ecliptic conjunction, and $M'$ and $S'$ are the positions of the Moon and Sun at their least true separation. 

<br/>

However, an easier way of looking at this is by fixing the Sun in one place and considering the *relative motion* of the Moon to the Sun.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1193b087-f038-455d-a898-a5e8db00faad" width="250"/> In this diagram, the Sun has been fixed in place, and therefore the Moon now travels along an altered orbit $MN'$. $M'$ is still the position of the Moon at its least true separation with the Sun.

Let us put
```math
\begin{align}
\beta &= \text{ The Moon's ecliptic latitude at conjunction }= SM\\
\Sigma &= \text{ The least true separation between the Sun and Moon }= SM'\\
I &= \text{ The inclination of the Moon's orbit to the ecliptic } = SNM\\
I' &= \text{ The inclination of the Moon's orbit to the ecliptic keeping the Sun fixed } = SN'M\\
\end{align}
```

Then, by geometry we have $MSM' = I'$. Therefore:
```math
\Sigma = \beta \cos(I') \tag{9.1}
```
But also,
```math
\tan(I') = \frac{SN}{SN'} \tan(I)
```
If we put
```math
\begin{align}
\sigma &= \text{ The Sun's motion in longitude}\\
\mu &= \text{ The Moon's motion in longitude}\\
t &= \text{ The time it takes for the Moon to reach the node}\\
\end{align}
```
Then,
```math
\begin{align}
SN &= \mu t\\
SN' &= (\mu - \sigma)t\\
\therefore \frac{SN}{SN'} &= \frac{\mu t}{\mu t - \sigma t}
\end{align}
```
Dividing both the numerator and denominator by $\sigma t$ and setting $\sigma /\mu = q$, we get:
```math
\begin{align}
\frac{SN}{SN'} &= \frac{\lambda}{\lambda - 1}\\
\therefore \tan(I') &= \frac{q}{q - 1} \tan(I) \tag{9.2}
\end{align}
```
The apparent least true separation from somewhere on the surface of the Earth may differ from $\Sigma$ however by up to the difference in parallax of the two bodies, so if we put:
```math
\begin{align}
\pi &= \text{ The Moon's equatorial horizontal parallax}\\
\pi' &= \text{ The Sun's equatorial horizontal parallax}\\
\end{align}
```
we get:
```math
\text{least apparent separation } = \Sigma - (\pi - \pi')
```
An eclipse will occur if this least apparent separation is less than the sum of the apparent radii of the Sun and the Moon (i.e. the Sun and the Moon overlap). If we put:
```math
\begin{align}
s &= \text{ The Moon's apparent radius}\\
s' &= \text{ The Sun's apparent radius}\\
\end{align}
```
We have in the case of eclipse:
```math
\Sigma - (\pi - \pi') < s + s'
```
or:
```math
\beta < (s + s' + \pi - \pi')\sec(I') \tag{9.3}
```
This is the condition for solar eclipse.
#### Example 9.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine if the new Moon of $\text{April, } 2024$ will result in a solar eclipse.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We can find via the method of example $4.4$ that the new Moon occured on $\text{April 8, } 2024$ at $18:21$. At this time:\
```math
\begin{align}
\lambda_\text{Conjunction} &=19\degree\:4'\:12.19''\\
\beta_\text{Moon} &= 0\degree\:20'\:52.53''\\
\Delta_\text{Moon} &= 359\:807.95 \text{ km}\\
\Delta_\text{Sun} &= 149\:823\:425.56\text{ km}
\end{align}
```
Also:
```math
\begin{align}
\text{Earth's equatorial Radius } &=6378.137 \text{ km}\\
\text{Moon's Radius } &= 1737.4 \text{ km}\\
\text{Sun's Radius } &= 696\:000 \text{ km}\\
I &= 5.14\degree
\end{align}
```
Thus by equations $4.1$ and $8.6$:
```math
\begin{alignat}{2}
s &= \arcsin\left(\frac{1737.4}{359\:807.95}\right) &&= 16'\:35.99''\\
s' &= \arcsin\left(\frac{696\:000}{149\:823\:425.56}\right) &&= 15'\:58.2''\\
\pi &= \arcsin\left(\frac{6378.137}{359\:807.95}\right) &&= 1\degree\:0'\:56.55''\\
\pi' &= \arcsin\left(\frac{6378.137}{149\:823\:425.56}\right) &&= 8.78''
\end{alignat}
```
To determine $q$, we need $\sigma$ and $\mu$, the derivatives of longitude of the Sun and Moon. We take one hour as the time step.\
At $19:21$:
```math
\begin{align}
\lambda_{\text{Moon}} &=19\degree\:41'\:40.88''\\
\therefore \mu &= \frac{19\degree\:41'\:40.88'' - 19\degree\:4'\:12.19''}{1h} = 37.48'/h\\
\lambda_{\text{Sun}} &=19\degree\:6'\:34.7''\\
\therefore \sigma &= \frac{19\degree\:6'\:34.7'' - 19\degree\:4'\:12.19''}{1h} = 2.38'/h\\
\end{align}
```
Therefore:
```math
\begin{align}
q &= \frac{37.48}{2.38} = 15.7479\\
\therefore I' &= \arctan\left(\frac{15.7479}{15.7479 - 1} \tan(5.14\degree)\right) = 5.486\degree
\end{align}
```
Therefore:
```math
\begin{align}
(s + s' + \pi - \pi')\sec(I') &= (16'\:35.99'' + 15'\:58.2'' + 1\degree\:0'\:56.55'' - 8.78'')\sec(5.486\degree) \\
&=1\degree\:33'\:47.73''
\end{align}
```
Which is greater than $\beta_\text{Moon}$ at conjunction. Therefore, a solar eclipse will occur.\
There is a shorter way of doing this: we can precalculate the minimum possible value of $(s + s' + \pi - \pi')\sec(I')$, and if $\beta_\text{Moon}$ at conjunction is less than this minimum value, a solar eclipse must surely occur. We can also precalculate the maximum possible value of $(s + s' + \pi - \pi')\sec(I')$, and if $\beta_\text{Moon}$ at conjunction is greater than this maximum value, a solar eclipse will surely not occur. If it is in between these two values, the full calculation is required.\
$\blacksquare$
