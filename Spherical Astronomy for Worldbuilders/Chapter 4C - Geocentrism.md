(Continued from Part B...)

### Lunar Libration
It is commonly known that only one side of the Moon ever faces the Earth, i.e. the Moon is tidally locked to the Earth. However, this does not mean we can only see exactly $50$% of the Moon. Because of the Moon's orbit is not a perfect circle, we can see a bit more than $50$% of the Moon depending on the position of the Moon, and this effect is known as the *optical libration of the Moon*.

The center of the lunar disk as seen from the Earth is evidently the sub-Earth point on the lunar surface. We measure the libration of the Moon with the coordinates of this sub-Earth point. To do this, consider this diagram:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/8d98a4a1-4c9c-4026-8afc-e384801c62bb" width="450"/> This diagram depicts the Moon. $K$ is the ecliptic pole, i.e. the point with ecliptic latitude of $90\degree$. $P_0$ is the rotational North pole of the Moon, i.e. the point of the axis of the Moon. Thus the angle of the arc $P_0K$ is the axial tilt of the Moon with regard to the ecliptic, which we denote $I$. $P_0$ is not a fixed point on the surface of the Moon however, unlike the true north pole of the Earth, due to the fact that the lunar orbit precesses. This precession of the lunar north pole is in such a way that the ascending node of the lunar equator with respect to the ecliptic, i.e. the point $Q$, is also the descnding node of the orbit of the  Moon with respect to the ecliptic. Therefore, if we say that the longitude of the ascending node of the orbit of the Moon is $\Omega$, the ecliptic longitude of the point $Q$ ($AQ$, where $A$ is the location of Aries) is $\Omega + 180\degree$. Because of the way the Moon's axis is tilted, it also follows that the angle $KP_0Q = 90\degree$ and the ecliptic longitude of $P_0$ is $\Omega + 90\degree$.

Let us assume that the Moon orbits perfectly uniformly along a circle around the Earth with zero inclination from the ecliptic and calculate this fictional Moon's ecliptic longitude. This is known as the Moon's mean longitude, denoted by $L'$, and is given by:
```math
L' = \Omega + \omega + M \tag{4.30}
```
Where $\omega$ is the argument of periapsis and $M$ is the mean anomaly. Then, the mean longitude of the Earth from the Moon is $L' + 180\degree$. We will denote the point with this longitude $E_0$. Therefore, the arc $QE_0$ is $180\degree + L' - (180\degree + \Omega) = L' - \Omega$. Now, let us define a point called the *mean center of the lunar disk*, which we will denote $M$, that lies on the lunar equator with the same separation from $Q$ as $E_0$ is from $Q$. In other words:
```math
MQ = L' - \Omega \tag{4.31}
```
$M$ is a fixed point on the lunar surface, and we define the prime merdian of the Moon as the great circle $P_0M$.

Now we can define the *selenographic* longitude and latitude $(l_X, b_X)$ of any point $X$ on the lunar surface as:
```math
\begin{align}
l_X &= MP_0X\\
b_X &= 90\degree - P_0X
\end{align} \tag{4.32}
```
Now, say the true position of the sub-Earth point is $E$. If we say that the ecliptic coordinates of the Moon are $(\lambda, \beta)$, the ecliptic longitude and latitude of $E$ is $(\lambda + 180\degree, -\beta)$. Let us say that the selenographic coordinates of the point $E$ is $(l, b)$. Now, using all the quantities we have found so far, we can find that:
```math
\begin{align}
P_0E &= 90\degree - b\\
KE &= 90\degree + \beta\\
KP_0E &= 90\degree - (L' - \Omega) - l = 90\degree - L' + \Omega - l\\
P_0KE &= \lambda + 180\degree - (\Omega + 90\degree) = 90\degree - (\Omega - \lambda)\\
P_0K &= I
\end{align} \tag{4.33}
```
Now, consider the spherical triangle $P_0KE$. Applying the [spherical law of cosines](https://en.wikipedia.org/wiki/Spherical_law_of_cosines) to this triangle and using the results of equations $4.32$ gives:
```math
\begin{align}
\cos(P_0E) &= \sin(P_0K)\cos(KE) + \sin(P_0K)\sin(KE)\cos(P_0KE)\\
\therefore \cos(90\degree - b) &= \cos(I)\cos(90\degree + \beta) + \sin(I)\sin(90\degree + \beta)\cos(90\degree - (\Omega - \lambda))\\
\therefore \sin(b) &= -\cos(I)\sin(\beta) + \sin(I)\cos(\beta)\sin(\Omega - \lambda) \tag{4.34-i}
\end{align}
```
Using the [first analogue formula for the spherical law of cosines](https://proofwiki.org/wiki/Analogue_Formula_for_Spherical_Law_of_Cosines) to this triangle with $a = P_0E$ and $B = KP_0E$ gives:
```math
\begin{align}
\sin(P_0E)\cos(KP_0E) &= \cos(KE)\sin(P_0K) - \sin(KE)\cos(P_0K)\cos(P_0KE)\\
\therefore \sin(90\degree - b)\cos(90\degree - L' + \Omega - l) &= \cos(90\degree + \beta)\sin(I) - \sin(90\degree + \beta)\cos(I)\cos(90\degree - (\Omega - \lambda))\\
\therefore \cos(b)\sin(L' - \Omega + l) &= -\sin(\beta)\sin(I) - \cos(\beta)\cos(I)\sin(\Omega - \lambda)  \tag{4.34-ii}
\end{align}
```
Using the [spherical law of sines](https://proofwiki.org/wiki/Spherical_Law_of_Sines) to this triangle gives:
```math
\begin{align}
\frac{\sin(P_0E)}{\sin(P_0KE)} &= \frac{\sin(KE)}{\sin(KP_0E)}\\
\therefore\frac{\sin(90\degree - b)}{\sin(90\degree - (\Omega - \lambda))} &= \frac{\sin(90\degree + \beta)}{\sin(90\degree - L' + \Omega - l)}\\
\therefore \sin(90\degree - b)\sin(90\degree - L' + \Omega - l) &= \sin(90\degree + \beta)\sin(90\degree - (\Omega - \lambda))\\
\therefore \cos(b)\cos(L' - \Omega + l) &= \cos(\beta)\cos(\Omega - \lambda) \tag{4.34-iii}
\end{align} 
```
To sum up:
```math
\begin{align}
\sin(b) &= -\cos(I)\sin(\beta) + \sin(I)\cos(\beta)\sin(\Omega - \lambda)\\
\cos(b)\sin(L' - \Omega + l) &= -\sin(\beta)\sin(I) - \cos(\beta)\cos(I)\sin(\Omega - \lambda)\\
\cos(b)\cos(L' - \Omega + l) &= \cos(\beta)\cos(\Omega - \lambda)
\end{align} \tag{4.34}
```
These equations fully determine $l$ and $b$ and thus fully describe the geocentric optical libration of the Moon.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/06f33473-be13-4289-a60b-0dfe00e8ce70" width="450"/> Another angle of interest however, is the position angle of the axis of rotation of the Moon, i.e. the angle $PEP_0$, where $P$ is the celestial north pole. This angle shows how tilted the selenographic north pole of the Moon looks from the Earth's perspective, and is denoted $c$.

First, note that we can separate this angle into two and write $c = PEK + KEP_0$. Also, note that the angle between the ecliptic pole and the celestial pole is the axial tilt of the Earth, so $KP = \varepsilon$. Furthermore, note that angle $EKP$ is the ecliptic longitude of the celestial north pole minus the ecliptic longitude of the point $E$, i.e. $EKP = 90\degree - (\lambda + 180\degree) = -90\degree - \lambda = 270\degree - \lambda$.

First let's find $PEK$. In the triangle $PEK$, we can use the [four parts formula](https://proofwiki.org/wiki/Four-Parts_Formula) with $a = KE$ and $C = EKP$ to write:

```math
\begin{align}
\cos(KE)\cos(EKP) &= \sin(KE)\cot(KP) - \sin(EKP)\cot(PEK)\\
\therefore \cos(90\degree + \beta)\cos(270\degree - \lambda) &= \sin(90\degree + \beta)\cot(\varepsilon) - \sin(270\degree - \lambda)\cot(PEK)\\
\therefore \sin(\beta)\sin(\lambda) &= \cos(\beta)\cot(\varepsilon) + \cos(\lambda)\cot(PEK)\\
\therefore \cot(PEK) &= \frac{\sin(\beta)\sin(\lambda) - \cos(\beta)\cot(\varepsilon)}{\cos(\lambda)}\\
&= \sin(\beta)\tan(\lambda) - \cos(\beta)\cot(\varepsilon)\sec(\lambda)\\
\therefore PEK &= \text{arccot}(\sin(\beta)\tan(\lambda) - \cos(\beta)\cot(\varepsilon)\sec(\lambda)) \tag{4.35-i}
\end{align} 
```
Next, in the triangle $KEP_0$, since point $P_0$ has ecliptic longitude $\Omega + 90\degree$, $EKP_0 = \lambda + 180\degree - (\Omega + 90\degree) = \lambda - \Omega + 90\degree$. Now we can use the [four parts formula](https://proofwiki.org/wiki/Four-Parts_Formula) with $a = KE$ and $C = EKP_0$ to write:
```math
\begin{align}
\cos(KE)\cos(EKP_0) &= \sin(KE)\cot(KP_0) - \sin(EKP_0)\cot(KEP_0)\\
\therefore \cos(90\degree + \beta)\cos(\lambda - \Omega + 90\degree) &= \sin(90\degree + \beta)\cot(I) - \sin(\lambda - \Omega + 90\degree)\cot(KEP_0)\\
\therefore \sin(\beta)\sin(\lambda - \Omega) &= \cos(\beta)\cot(I) - \cos(\lambda - \Omega)\cot(KEP_0)\\
\therefore \cot(KEP_0) &= \frac{\sin(\beta)\sin(\lambda - \Omega) - \cos(\beta)\cot(I)}{-\cos(\lambda - \Omega)}\\
&= -\sin(\beta)\tan(\lambda - \Omega) + \cos(\beta)\cot(I)\sec(\lambda - \Omega)\\
&= \sin(\beta)\tan(\Omega - \lambda) + \cos(\beta)\cot(I)\sec(\Omega - \lambda)\\
\therefore KEP_0 &= \text{arccot}(\sin(\beta)\tan(\Omega - \lambda) + \cos(\beta)\cot(I)\sec(\Omega - \lambda)) \tag{4.35-ii}
\end{align} 
```
Therefore,
```math
c = \text{arccot}(\sin(\beta)\tan(\lambda) - \cos(\beta)\cot(\varepsilon)\sec(\lambda)) + \text{arccot}(\sin(\beta)\tan(\Omega - \lambda) + \cos(\beta)\cot(I)\sec(\Omega - \lambda)) \tag{4.36}
```
Together with the apparent size and the phase, the libration angles $l$, $b$, and $c$ fully describe the look of the Moon from the Earth.

#### Example 4.9
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that, for the Moon, on $\text{July 22, } 2024$ at time $00:00$, the mean longitude was $L' = 310\degree$ $29'$, the ecliptic coordinates were $\lambda = 307\degree$ $21'$ and $\beta = -4\degree$ $27'$, and the longitude of the ascending node was $\Omega = 8\degree$ $47'$, find the libration angles $l$, $b$, and $c$. <br/>
  Use $I = 1.54\degree$ and $\varepsilon = 23.44\degree$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Equation $4.34$ gives:
```math
\begin{align}
\sin(b) &= -\cos(1.54\degree)\sin(-4\degree\:27') + \sin(1.54\degree)\cos(-4\degree\:27')\sin(8\degree\:47' - 307\degree\:21')\\
&= 0.101093\\
\therefore b &= \arcsin(0.101093) = 5\degree\:48'\\
\\
\cos(b)\sin(L' - \Omega + l) &= -\sin(-4\degree\:27')\sin(1.54\degree) - \cos(-4\degree\:27')\cos(1.54\degree)\sin(8\degree\:47' - 307\degree\:21')\\
&= -0.873212\\
\cos(b)\cos(L' - \Omega + l) &= \cos(-4\degree\:27')\cos(8\degree\:47' - 307\degree\:21')\\
&= 0.476739\\
\therefore L' - \Omega + l &= \arctan(-0.873212, 0.476739) = 298\degree\:38'\\
\therefore l &= 298\degree\:38' + 8\degree\:47' - 310\degree\:29' = -3\degree\:4'
\end{align}
```
For $c$, equations $4.35$ give:
```math
\begin{align}
PEK &= \text{arccot}(\sin(-4\degree\:27')\tan(307\degree\:21') - \cos(-4\degree\:27')\cot(23.44\degree)\sec(307\degree\:21'))\\
&= -15\degree\:10'\\
KEP_0 &= \text{arccot}(\sin(-4\degree\:27')\tan(8\degree\:47' - 307\degree\:21') + \cos(-4\degree\:27')\cot(1.54\degree)\sec(8\degree\:47' - 307\degree\:21'))\\
&= 44'
\end{align}
```
Thus $c = -15\degree$ $10' + 44' = -14\degree$ $6'$. \
Drawn, this looks like (see next section for guide on how to draw):
<p align="center">
  <img width="425" src="https://github.com/CitruzSquared/essays/assets/23460281/6bdd62ac-0320-48e5-9bf8-3ed22c610bf0"> <br/>
  The lunar axis is tilted from celestial North by $c = -14\degree$ $6'$ (negative means to the West). <br/> The center of the disk of the Moon, $E$, is at selenographic coordinates $(l, b) = (-3\degree$ $4',$ $5\degree$ $48'$). <br/> North is at the top and East is to the left. <br/> 
  <br/>
  <img width="250" src="https://github.com/CitruzSquared/essays/assets/23460281/42fdbe22-55dd-4f62-b9d9-b41a82d2ad2d">      
  <img width="250" src="https://github.com/CitruzSquared/essays/assets/23460281/0dda0325-ee82-4834-b8a5-6b84dacd5d36"> <br/>
  Left: simulated view of the Moon with the calculated libration angles. <br/>
  Right: simulated view of the Moon from NASA (<a href="https://www.youtube.com/watch?v=dyDIogWH9uE">Source</a>; $l$, $b$, $c = -3\degree$ $25'$, $5\degree$ $49'$, $-14\degree$ $22'$). <br/>
  The error is due to differing ephemeris data. <br/>
  Note that the extreme right side of the NASA image is dark because the Moon was at $99.4$% phase. <br/> The left image does not take this into account.
</p>

$\blacksquare$

### Tip on Drawing Spheres
When drawing a sphere with the center of the disk at coordinates $(l, b)$, follow this guide.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/a6dbdbf6-3991-4faf-88f5-6ed91f799b6f" width="400"/> This diagram shows a sphere centered at $l = -30\degree$ and $b = 30\degree$. $E$ is the center of the disk, and $P$ is the north pole. 

- Let the radius of the white circle be $r$.
- The red ellipse, the equatorial circle, has semi-minor axis $EA = r\sin(b)$.
- The green ellipse, the meridional circle, has semi-minor axis $EB = r\cos(b)\sin(l)$, and is tilted by $TEB = -\arctan(\sin(b)\tan(l))$ (negative $=$ clockwise).
- To account for the position angle of the axis (the libration angle $c$), tilt this whole diagram by $c$ (negative $=$ clockwise).

Because the two ellipses intersect at $4$ points, and only one of them is the true location of the zero point $M$, care must be taken to determine the correct intersection point.

If $b$ is positive, the north pole will be visible (as in this case). if $b$ is negative, the north pole will be hidden behind the sphere.
