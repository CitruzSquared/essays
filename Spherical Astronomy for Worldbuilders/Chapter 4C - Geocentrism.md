(Continued from Part B...)

### Lunar Libration
It is commonly known that only one side of the Moon ever faces the Earth, i.e. the Moon is tidally locked to the Earth. However, this does not mean we can only see exactly $50$% of the Moon. Because of the Moon's orbit is not a perfect circle, we can see a bit more than $50$% of the Moon depending on the position of the Moon, and this effect is known as *optical libration*.

The center of the lunar disk as seen from the Earth is evidently the sub-Earth point on the lunar surface. We measure the libration of the Moon with the coordinates of this sub-Earth point. To do this, consider this diagram:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/8d98a4a1-4c9c-4026-8afc-e384801c62bb" width="450"/> This diagram depicts the Moon. $K$ is the ecliptic pole, i.e. the point with ecliptic latitude of $90\degree$. $P_0$ is the rotational North pole of the Moon, i.e. the point of the axis of the Moon. Thus the angle of the arc $P_0K$ is the axial tilt of the Moon with regard to the ecliptic, which we denote $I$. $P_0$ is not a fixed point on the surface of the Moon however, unlike the true north pole of the Earth, due to the fact that the lunar orbit precesses. This precession of the lunar north pole is in such a way that the ascending node of the lunar equator with respect to the ecliptic, i.e. the point $Q$, is also the descnding node of the orbit of the  Moon with respect to the ecliptic. Therefore, if we say that the longitude of the ascending node of the orbit of the Moon is $\Omega$, the ecliptic longitude of the point $Q$ ($AQ$, where $A$ is the location of Aries) is $\Omega + 180\degree$. Because of the way the Moon's axis is tilted, it also follows that the angle $KP_0Q = 90\degree$ and the ecliptic longitude of $P_0$ is $\Omega + 90\degree$.

Let us assume that the Moon orbits perfectly uniformly along a circle around the Earth with zero inclination from the ecliptic and calculate this fictional Moon's ecliptic longitude. This is known as the Moon's mean longitude and we will denote it $L'$. Then, the mean longitude of the Earth from the Moon is $L' + 180\degree$. We will denote the point with this longitude $E_0$. Therefore, the arc $QE_0$ is $180\degree + L' - (180\degree + \Omega) = L' - \Omega$. Now, let us define a point called the *mean center of the lunar disk*, which we will denote $M$, that lies on the lunar equator with the same separation from $Q$ as $E_0$ is from $Q$. In other words:
```math
MQ = L' - \Omega \tag{4.30}
```
$M$ is a fixed point on the lunar surface, and we define the prime merdian of the Moon as the great circle $P_0M$.

Now we can define the *selenographic* longitude and latitude $(l_X, b_X)$ of any point $X$ on the lunar surface as:
```math
\begin{align}
l_X &= MP_0X\\
b_X &= 90\degree - P_0X
\end{align} \tag{4.31}
```
Now, say the true position of the sub-Earth point is $E$. If we say that the ecliptic coordinates of the Moon are $(\lambda, \beta)$, the ecliptic longitude and latitude of $E$ is $(\lambda + 180\degree, -\beta)$. Let us say that the selenographic coordinates of the point $E$ is $(l, b)$. Now, using all the quantities we have found so far, we can find that:
```math
\begin{align}
P_0E &= 90\degree - b\\
KE &= 90\degree + \beta\\
KP_0E &= 90\degree - (L' - \Omega) - l = 90\degree - L' + \Omega - l\\
P_0KE &= \lambda + 180\degree - (\Omega + 90\degree) = 90\degree - (\Omega - \lambda)\\
P_0K &= I
\end{align} \tag{4.32}
```
Now, consider the spherical triangle $P_0KE$. Applying the [spherical law of cosines](https://en.wikipedia.org/wiki/Spherical_law_of_cosines) to this triangle and using the results of equations $4.32$ gives:
```math
\begin{align}
\cos(90\degree - b) &= \cos(I)\cos(90\degree + \beta) + \sin(I)\sin(90\degree + \beta)\cos(90\degree - (\Omega - \lambda))\\
\therefore \sin(b) &= -\cos(I)\sin(\beta) + \sin(I)\cos(\beta)\sin(\Omega - \lambda) \tag{4.33-i}
\end{align}
```
Using the [first analogue formulae for the spherical law of cosines](https://proofwiki.org/wiki/Analogue_Formula_for_Spherical_Law_of_Cosines) to this triangle with $a = P_0E$ and $B = KP_0E$ gives:
```math
\begin{align}
\sin(90\degree - b)\cos(90\degree - L' + \Omega - l) &= \cos(90\degree + \beta)\sin(I) - \sin(90\degree + \beta)\cos(I)\cos(90\degree - (\Omega - \lambda))\\
\therefore \cos(b)\sin(L' - \Omega + l) &= -\sin(\beta)\sin(I) - \cos(\beta)\cos(I)\sin(\Omega - \lambda)  \tag{4.33-ii}
\end{align}
```
Using the [spherical law of sines](https://proofwiki.org/wiki/Spherical_Law_of_Sines) to this triangle gives:
```math
\begin{align}
\frac{\sin(90\degree - b)}{\sin(90\degree - (\Omega - \lambda))} &= \frac{\sin(90\degree + \beta)}{\sin(90\degree - L' + \Omega - l)}\\
\therefore \sin(90\degree - b)\sin(90\degree - L' + \Omega - l) &= \sin(90\degree + \beta)\sin(90\degree - (\Omega - \lambda))\\
\therefore \cos(b)\cos(L' - \Omega + l) &= \cos(\beta)\cos(\Omega - \lambda) \tag{4.33-iii}
\end{align} 
```
To sum up:
```math
\begin{align}
\sin(b) &= -\cos(I)\sin(\beta) + \sin(I)\cos(\beta)\sin(\Omega - \lambda)\\
\cos(b)\sin(L' - \Omega + l) &= -\sin(\beta)\sin(I) - \cos(\beta)\cos(I)\sin(\Omega - \lambda)\\
\cos(b)\cos(L' - \Omega + l) &= \cos(\beta)\cos(\Omega - \lambda)
\end{align} \tag{4.33}
```
These equations fully determine $l$ and $b$ and thus fully describe the geocentric optical libration of the Moon.
