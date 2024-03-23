(Continued From Part E...)
### Limits of Partiality
There are generally two limits at which partial eclipses can be observed, one in the North and one in the South. In the case that there are no internal contacts, only one of the two will exist. As discussed in the *Curve of Maximum Eclipse on the Horizon* section, The limit of visibility of an eclipse is given by two conditions:
```math
\begin{align}
P' &= 0 \\
\Delta &= l
\end{align}
```
Which means that the moment of maximum eclipse occurs when the point of observation is just on the edge of the shadow – meaning the shadow of the Moon only barely grazes past this point. To solve the first of these conditions, recall the expression for $P'$ (equation $9.50$):
```math
P' = a' + (c' - (i^2 + 1)\zeta \mu'\cos(d))\sin(Q) + (-b' + (i^2 + 1)\zeta d')\cos(Q)
```
In this equation, if we set:
```math
\begin{align}
C &= c' - (i^2 + 1)\zeta \mu' \cos(d) \\
B &= b' - (i^2 + 1)\zeta d'
\end{align} \tag{9.77}
```
Then, we have for $P'$:
```math
P' = a' + C\sin(Q) - B\cos(Q)
```
Which is of the same form as equation $9.65$, and thus the solutions are:
```math
\begin{align}
Q_1 &= 2\arctan\left(\frac{\sqrt{-a'^2+B^2+C^2}-C}{a' + B}\right)\\
Q_2 &= 2\arctan\left(\frac{-\sqrt{-a'^2+B^2+C^2}-C}{a' + B}\right)
\end{align}\tag{9.78}
```
We need to find $\zeta$ to find $C$ and $B$. In order to do this, we first assume $\zeta = 0$ and find two values of $Q$ by equation $9.77$ and $9.78$. Then, equation $9.28$ gives:
```math
\begin{align}
\xi &= x - (l - i\zeta_1)\sin(Q)\\
\eta_1 &= (y - (l - i\zeta_1)\cos(Q))/ \rho_1\tag{9.28}\\
\zeta_1^2 &= 1 - \xi^2 - \eta_1^1
\end{align}
```
From which equation $9.27$ gives a second approximation of $\zeta$:
```math
\zeta = -\rho_2\eta_1\sin(d_1-d_2) + \rho_2\zeta_1\cos(d_1-d_2) \tag{9.27}
```
Repeatedly applying equations $9.28$ and $9.27$ until convergence, we can now use the final value in equation $9.77$ and $9.78$ for the accurate value of $Q$. Once $Q$ has been found, apply equation $9.28$ once more, from which equation $9.29$ and $9.30$ give the latitude and longitude of the place.

Since there are two values of $Q$, two points can be found. If $(l - i\zeta)\cos(Q)$ for that point is negative, the point belongs to the northern limit. If $(l - i\zeta)\cos(Q)$ is positive, it belongs to the southern limit. The extreme points of these curves are the points where $\zeta = 0$, which we have already found as the northern and southern extremes of the curve of maximum eclipse on the horizon. The northern limit of partiality will connect the two northern extremes of the curve of maximum eclipse on the horizon, and the southern limit will connect the two southern extremes.

#### Example 9.10
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the limits of partiality of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Recall from example $9.7$ when we computed the extremes of the curve of maximum eclipse on the horizon:
```math
\begin{array}{cccc}\hline \text{Point} & \text{Time} & \text{Latitude} & \text{Longitude} \\ \hline
\text{Sunrise Southern Extreme} & 16:32:38 & -38\degree\:48'\:13'' & 207\degree\:58'\:0'' \\
\text{Sunrise Northern Extreme} & 17:29:30 & 33\degree\:29'\:55'' & 182\degree\:45'\:29'' \\
\text{Sunset Northern Extreme} & 19:05:23 & 82\degree\:31'\:16'' & 72\degree\:8'\:45'' \\
\text{Sunset Southern Extreme} & 20:02:15 & 16\degree\:49'\:18'' & 331\degree\:48'\:27'' \\ \hline
\end{array}
```
These are also the extremes of the limits of partiality.
