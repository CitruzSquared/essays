(Continued from Part A...)

### The Outline of the Shadow on the Surface of the Earth

At a distance $\zeta$ above the fundamental plane, the shadow's radius is $L$. Therefore, for places on a parallel plane at the edge of the shadow, that is, for places where the eclipse is beginning or ending:
```math
\Delta = L \tag{9.16}
```
Or, using equatins $9.9$ and $9.15$:
```math
(x - \xi)^2 + (y - \eta)^2 = (l - i\zeta)^2\tag{9.17}
```
Which can also be expressed as (using equation 9.10):
```math
\displaylines{
\begin{align}
(l - i\zeta)\sin(Q) &= x - \xi\\
(l - i\zeta)\cos(Q) &= y - \eta
\end{align}
}\tag{9.18}
```
Equation $9.18$ is known as the *fundamental equation of eclipse theory*.

To convert $\xi, \eta, \zeta$ to coordinates on the surface of the Earth, we have equations $9.7$, restated here:
```math
\begin{align}
\xi &= \rho \cos(\phi') \sin(\theta) \\
\eta &= \rho \sin(\phi')\cos(d) - \rho\cos(\phi')\sin(d)\cos(\theta) \tag{9.7}\\
\zeta &= \rho \sin(\phi')\sin(d) + \rho\cos(\phi')\cos(d)\cos(\theta) 
\end{align}
```
The five equations of $9.7$ and $9.18$ involve six variables, so one of them must be a free variable. Taking $Q$ as a free variable and letting it range from $0\degree$ to $360\degree$ gives us the full outline of the shadow as $Q$ describes the angle between the place of observation and the position of the shadow, therefore we let $Q$ range free.

However, we run into a problem: when using equations $9.7$, we need $\rho$ to find $\phi'$, but since $\rho$ depends on $\phi'$, we cannot determine $\rho$ until $\phi'$ is found. [Friedrich Bessel](https://en.wikipedia.org/wiki/Friedrich_Bessel) found a clever workaround to this problem:\
If $\phi$ is the geodetic latitude and distances are measured in units of Earth equatorial radii (such that $a = 1$), then we have equations $7.6$:
```math
\rho \cos(\phi') = \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\enspace\enspace\text{ and }\enspace\enspace
\rho \sin(\phi') = \frac{(1 - e^2) \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
```
Where $e$ is the eccentricity of the Earth ellipsoid.\
If we define $\phi_1$ such that:
```math
\cos(\phi_1) = \rho \cos(\phi') = \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
```
we have:
```math
\sin(\phi_1) = \sqrt{1 - \cos^2(\phi_1)} = \frac{\sin(\phi) \sqrt{1 - e^2}}{\sqrt{1-e^2\sin^2(\phi)}}
```
or:
```math
\begin{align}
\cos(\phi_1) &= \rho \cos(\phi')\\
\sqrt{1 - e^2}\sin(\phi_1) &= \rho \sin(\phi')\tag{9.19}\\
\therefore \tan(\phi) &= \frac{\tan(\phi_1)}{\sqrt{1 - e^2}}
\end{align}
```
Now, equations $9.7$ become:
```math
\begin{align}
\xi &= \cos(\phi_1) \sin(\theta) \\
\eta &= \sin(\phi_1)\cos(d)\sqrt{1 - e^2} - \cos(\phi_1)\sin(d)\cos(\theta)\tag{9.20}\\
\zeta &= \sin(\phi_1)\sin(d)\sqrt{1 - e^2} + \cos(\phi_1)\cos(d)\cos(\theta) 
\end{align}
```
Let
```math
\begin{align}
\rho_1 \sin(d_1) &= \sin(d)\\
\rho_1 \cos(d_1) &= \cos(d)\sqrt{1 - e^2}\\
\tag{9.21}\\
\rho_2 \sin(d_2) &= \sin(d)\sqrt{1 - e^2}\\
\rho_2 \cos(d_2) &= \cos(d)\\
\end{align}
```
Note that the subscripts do not mean penumbra and umbra here: they are just there to distinguish the variables.\
Now, equations $9.20$ become:
```math
\begin{align}
\xi &= \cos(\phi_1) \sin(\theta) \\
\eta &= \rho_1\sin(\phi_1)\cos(d_1) - \rho_1\cos(\phi_1)\sin(d_1)\cos(\theta)\tag{9.22}\\
\zeta &= \rho_2\sin(\phi_1)\sin(d_2) + \rho_2\cos(\phi_1)\cos(d_2)\cos(\theta) 
\end{align}
```
If we put:
```math
\eta_1 = \frac{\eta}{\rho_1} \tag{9.23}
```
And put $\zeta_1$ such that:
```math
\xi^2 + \eta_1^2 + \zeta_1^2 = 1 \tag{9.24}
```
Then:
```math
\begin{align}
\zeta_1^2 &= 1 - \xi^2 - \frac{\eta^2}{\rho_1^2}\\
&= 1 - \cos^2(\phi_1) \sin^2(\theta) - \sin^2(\phi_1)\cos^2(d_1) + 2\sin(\phi_1)\cos(d_1)\cos(\phi_1)\sin(d_1)\cos(\theta) - \cos^2(\phi_1)\sin^2(d_1)\cos^2(\theta)
\end{align}
```
Let us ignore the $2\sin(\phi_1)\cos(d_1)\cos(\phi_1)\sin(d_1)\cos(\theta)$ term for now. Carrying out algebra for the rest of the terms:
```math
\begin{align}
& 1 - \cos^2(\phi_1) \sin^2(\theta) - \sin^2(\phi_1)\cos^2(d_1) - \cos^2(\phi_1)\sin^2(d_1)\cos^2(\theta)\\
= & 1 - \cos^2(\phi_1) (1 - \cos^2(\theta)) - \sin^2(\phi_1)(1 - \sin^2(d_1)) - \cos^2(\phi_1)\sin^2(d_1)\cos^2(\theta)\\
= & 1 - \cos^2(\phi_1) - \cos^2(\phi_1)\cos^2(\theta) - \sin^2(\phi_1) - \sin^2(\phi_1)\sin^2(d_1) - \cos^2(\phi_1)\sin^2(d_1)\cos^2(\theta)\\
= & -\sin^2(\phi_1)\sin^2(d_1) + \cos^2(\phi_1)\cos^2(\theta) - \cos^2(\phi_1)\sin^2(d_1)\cos^2(\theta)\\
= & -\sin^2(\phi_1)\sin^2(d_1) + \cos^2(\phi_1)\cos^2(\theta) - \cos^2(\phi_1)\cos^2(\theta)(1 - \cos^2(d_1))\\
= & -\sin^2(\phi_1)\sin^2(d_1) + \cos^2(\phi_1)\cos^2(\theta) - \cos^2(\phi_1)\cos^2(\theta) + \cos^2(\phi_1)\cos^2(\theta)\cos^2(d_1)\\
= & -\sin^2(\phi_1)\sin^2(d_1) + \cos^2(\phi_1)\cos^2(\theta)\cos^2(d_1)
\end{align}
```
When we add back the term we ignored, we find that the result is a perfect square.
```math
\begin{align}
\zeta_1^2 &= -\sin^2(\phi_1)\sin^2(d_1) + 2\sin(\phi_1)\sin(d_1)\cos(\phi_1)\cos(d_1)\cos(\theta) + \cos^2(\phi_1)\cos^2(d_1)\cos^2(\theta)\\
&= (\sin(\phi_1)\sin(d_1) + \cos(\phi_1)\cos(d_1)\cos(\theta))^2
\end{align}
```
Thus:
```math
\zeta_1 = \sin(\phi_1)\sin(d_1) + \cos(\phi_1)\cos(d_1)\cos(\theta)
```
Therefore, equations $9.22$ can be further simplified to:
```math
\begin{align}
\xi &= \cos(\phi_1) \sin(\theta) \\
\eta_1 &= \sin(\phi_1)\cos(d_1) - \cos(\phi_1)\sin(d_1)\cos(\theta)\tag{9.25}\\
\zeta_1 &= \sin(\phi_1)\sin(d_1) + \cos(\phi_1)\cos(d_1)\cos(\theta) 
\end{align}
```
If we multiply the second equation by $-\sin(d_1)$ and the third by $\cos(d_1)$ and sum them, we obtain:
```math
\cos(\phi_1)\cos(\theta) = -\eta_1\sin(d_1) + \zeta_1\cos(d_1) \tag{9.26 i}
```
Similarly, if we multiply the second equation by $\cos(d_1)$ and the third by $\sin(d_1)$ and sum them, we obtain:
```math
\sin(\phi_1) = \eta_1\cos(d_1) + \zeta_1\sin(d_1) \tag{9.26 ii}
```
If we substitute equation $9.26$ into the equation for $\zeta$ in equation $9.22$ we get:
```math
\begin{align}
\zeta &= \rho_2(\eta_1\cos(d_1) + \zeta_1\sin(d_1))\sin(d_2) + \rho_2\cos(d_2)(-\eta_1\sin(d_1) + \zeta_1\cos(d_1))\\
&= \rho_2\eta_1\cos(d_1)\sin(d_2) + \rho_2\zeta_1\sin(d_1)\sin(d_2) - \rho_2\eta_1\cos(d_2)\sin(d_1) + \rho_2\zeta_1\cos(d_2)\cos(d_1)\\
&= -\rho_2\eta_1\sin(d_1-d_2) + \rho_2\zeta_2\cos(d_1-d_2)\tag{9.27}
\end{align}
```
For planets with low flattening values, $\zeta_1$ varies so little from $\zeta$ that we may substitute it for $\zeta$ in the equation for $L$. Therefore our problem now takes the following form. We first have equations $9.18$ (with equation $9.23$ substituted in) and $9.24$:
```math
\begin{align}
(l - i\zeta_1)\sin(Q) &= x - \xi\\
(l - i\zeta_1)\cos(Q) &= y - \rho_1\eta_1\tag{9.28}\\
\xi^2 + \eta_1^2 + \zeta_1^2 &= 1
\end{align}
```
Which fully determine $\xi$, $\eta_1$ and $\zeta_1$ for any value of $Q$. Now, from $\xi$, $\eta_1$ and $\zeta_1$ we can use equations $9.25$ and $9.26$:
```math
\begin{align}
\cos(\phi_1)\sin(\theta) &= \xi \\
\cos(\phi_1)\cos(\theta) &= -\eta_1\sin(d_1) + \zeta_1\cos(d_1)\tag{9.29}\\
\sin(\phi_1) &= \eta_1\cos(d_1) + \zeta_1\sin(d_1)
\end{align}
```
Which fully determine $\phi_1$ and $\theta$. The actual geodetic latitude and longitude of the place are then given by equations $9.19$ and $6.2$:
```math
\displaylines{
\begin{align}
\tan(\phi) &= \frac{\tan(\phi_1)}{\sqrt{1 - e^2}}\\
\lambda &= \mu - \theta
\end{align}
}\tag{9.30}
```
In order to solve equation $9.28$, let $\beta$ and $\gamma$ be defined such that:
```math
\displaylines{
\begin{align}
\sin(\beta)\sin(\gamma) &= x - l\sin(Q)\\
\sin(\beta)\cos(\gamma) &= \frac{y - l\cos(Q)}{\rho_1}\\
\end{align}
}\tag{9.31}
```
Then, we have:
```math
\begin{align}
\xi &= \sin(\beta)\sin(\gamma) + i\zeta_1\sin(Q)\\
\eta_1 &= \sin(\beta)\cos(\gamma) + \frac{i\zeta_1\cos(Q)}{\rho_1}
\end{align}
```
Substituting these into the last equation of $9.28$, we have:
```math
\begin{align}
(\sin(\beta)\sin(\gamma) + i\zeta_1\sin(Q))^2 + \left(\sin(\beta)\cos(\gamma) + \frac{i\zeta_1\cos(Q)}{\rho_1}\right)^2 + \zeta_1^2 &= 1\\
\sin^2(\beta)\sin^2(\gamma) + 2i\zeta_1\sin(\beta)\sin(\gamma)\sin(Q) + i^2\zeta_1^2\sin^2(Q) + \sin^2(\beta)\cos^2(\gamma) + \frac{2i\zeta_1\sin(\beta)\cos(\gamma)\cos(Q)}{\rho_1} + \frac{i^2\zeta_1^2\cos^2(Q)}{\rho_1^2} + \zeta_1^2 &= 1\\
-\cos^2(\beta) + 2i\zeta_1\sin(\beta)\sin(\gamma)\sin(Q) + i^2\zeta_1^2\sin^2(Q) + \frac{2i\zeta_1\sin(\beta)\cos(\gamma)\cos(Q)}{\rho_1} + \frac{i^2\zeta_1^2\cos^2(Q)}{\rho_1^2} + \zeta_1^2 &= 0
\end{align} 
```
Rearranging the terms, we get a quadratic in $\zeta_1$:
```math
\left(1 + i^2\sin^2(Q) + \frac{i^2\cos^2(Q)}{\rho_1^2}\right)\zeta_1^2 + \left(2i\sin(\beta)\sin(\gamma)\sin(Q) + \frac{2i\sin(\beta)\cos(\gamma)\cos(Q)}{\rho_1}\right)\zeta_1 -\cos^2(\beta) = 0 \tag{9.32}
```
All the coefficients involve known numbers. If the approximation $\rho_1 = 1$ is to be taken, this equation simplifies down to:
```math
(1 + i^2)\zeta_1^2 + 2i\sin(\beta)\sin(Q-\gamma)\zeta_1 - \cos^2(\beta) = 0 \tag{9.32*}
```
There are two solutions to these quadratics. To find the correct one, let us first say:
```math
Z = \text{ the zenith distance of the point Z (the point in the direction of the shadow axis).}
```
Then, since $Z$ points to right ascension $a$ and declination $d$, the hour angle of this point is $\mu - a = \theta$, and thus, via the third equation of equation $6.3$ (using the fact that zenith distance $= 90\degree -$ altitude (equation $6.16$)):
```math
\cos(Z) = \sin(\phi)\sin(d) + \cos(\phi)\cos(d)\cos(\theta)
```
If we multiply both sides by $\sqrt{1 - e^2} / \left(\rho_1 \sqrt{1 - e^2 \sin^2(\phi)}\right)$, we see that we obtain the formula for $\zeta_1$ in equation $9.25$. Thus:
```math
\cos(Z) = \zeta_1\rho_1\frac{\sqrt{1 - e^2 \sin^2(\phi)}}{\sqrt{1 - e^2}} = \zeta_1\rho_1\frac{\sin(\phi)}{\sin(\phi_1)} \tag{9.33}
```
As $\rho_1\sin(\phi)/\sin(\phi_1)$ is a positive quantity, $\cos(Z)$ and $\zeta_1$ have the same sign. But since we need the eclipse to be visible, $Z$ cannot be more than $90\degree$ (or else the eclipse would be below the horizon) and thus $\cos(Z) > 0$ and therefore we can say that $\zeta_1 > 0$.
