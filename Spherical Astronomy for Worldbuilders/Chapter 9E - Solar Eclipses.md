(Continued from Part D...)
### Curve of Maximum Eclipse on the Horizon
While some places experience the beginning or end of the eclipse exactly at sunrise or sunset, some others experience maximum obscuration at sunrise or sunset. As discussed in chapter $\text{9C}$, the condition for maximum eclipse is:
```math
P' = 0\tag{9.64}
```
Expanding out $P'$ for eclipse on the horizon ($\zeta = 0$), we have:
```math
a' + c'\sin(Q) -b'\cos(Q) = 0 \tag{9.65}
```
The solution to this equation turns out to be:
```math
Q = 2\arctan\left(\frac{\pm\sqrt{-a'^2+b'^2+c'^2}-c'}{a' + b'}\right)
```
Let us define $E$ such that:
```math
E = 2\arctan\left(\frac{\pm\sqrt{-a'^2+b'^2+c'^2}-c'}{a' + b'}\right)\tag{9.66}
```
Now, let us say that the distance of the observer from the shadow axis at the moment of maximum eclipse is $\Delta$, which obviously must be less than or equal to $|l|$ as the observer must be within the shadow. Then, we can say that at maximum eclipse:
```math
\begin{align}
\Delta \sin(E) &= x - \xi\\
\Delta \cos(E) &= y - \eta
\end{align}
```
In the above equation, we know $x$, $y$, and $E$, but we do not know $\Delta$.\
Putting 
```math
\begin{align}
m\sin(M) &= x\\
m\cos(M) &= y\\
p\sin(\gamma) &= \xi\\
p\cos(\gamma) &= \eta
\end{align}
```
as before, the above conditions become:
```math
\begin{align}
\Delta \sin(E) &= m\sin(M) - p\sin(\gamma)\\
\Delta \cos(E) &= m\cos(M) - p\cos(\gamma)
\end{align}
```
And if we now subtract $E$ from all the angles, we get:
```math
\begin{align}
0 &= m\sin(M - E) - p\sin(\gamma - E)\\
\Delta &= m\cos(M - E) - p\cos(\gamma - E)\\
\end{align}
```
Now, if we put $\psi = \gamma - E$, we have:
```math
\begin{align}
\sin(\psi) &= \frac{m\sin(M - E)}{p}\\
\Delta &= m\cos(M - E) - p\cos(\psi)
\end{align} \tag{9.67}
```
Where $\Delta$ must be positive as it is a distance.
Then, we have:
```math
\gamma = E + \psi \tag{9.68}
```
From where we can carry on with equations $9.58$ and $9.59$ to get the longitude and latitude of the place.

Evidently, $\sin(\psi) = m\sin(M - E)/p$ cannot be greater than $1$ or less than $-1$. Here, the approximation $p = 1$ can be made and we can say that in order for points on this curve to exist, $m\sin(M - E)$ must be less than $1$ and greater than $-1$.

Also, the first equation in $9.67$ produces two values for $\psi$. the value of $\psi$ that produces $\Delta > l$ must be discarded.
#### Example 9.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the curve of maximum eclipse on the horizon of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

I will give the solution for time $16:45$ in full.\
At this time, we have:
```math
\begin{align}
m &= 0.95478937 \\
M &= -1.69092252
\end{align}
```
and
```math
\begin{align}
a_1' &= -0.0012427\\
b_1' &= -0.30358228\\
c_1' &= 0.50818381
\end{align}
```
Thus, we can calculate $E$ by equation $9.66$:
```math
\begin{align}
E_1 &= 2\arctan\left(\frac{\sqrt{-(-0.0012427)^2+(-0.30358228)^2+(0.50818381)^2}-0.50114349}{-0.0012427 + (-0.30358228)}\right)\\
&= -0.53639649 \\
E_2 &= 2\arctan\left(\frac{-\sqrt{-(-0.0012427)^2+(-0.30358228)^2+(0.50818381)^2}-0.50114349}{-0.0012427 + (-0.30358228)}\right)\\
&= 2.60099756
\end{align}
```
Now, we verify if $m\sin(M - E) < 1$:
```math
\begin{array}{r|c|c}\hline  & E_1 & E_2 \\ \hline
m\sin(M - E) & -0.87325361 & 0.87162496
\end{array}
```
Both values of $E$ pass the test. We can now continue.\
We find $\psi$ and $\Delta$ with equation $9.67$:
```math
\begin{array}{r|c|c} 
m\sin(M - E) = \sin(\psi) & -0.87325361 & 0.87162496\\
\psi_1 & -1.06184017 & 1.05850769\\
\pi - \psi_1 = \psi_2 & 4.20343283 & 2.08308496\\
\psi_1 \rightarrow \Delta_1 & -0.10119491 & -0.87990746 \\
\psi_2 \rightarrow \Delta_2 & 0.87333703 & 0.10043927 \\ \hline
\end{array}
```
Considering $l_1 = 0.53563338$ at this time, $\psi_2$ for $E_2$ is the only $\psi$ value that produces a positive $\Delta$ value that is less than $l$. Thus, we continue with $\psi_2$ and $E_2$.
```math
\begin{array}{r|c} \hline
\gamma = E + \psi & 4.68408253 \\
\rho_1 & 0.99670449 \\
\gamma' & -1.59919632\\
p & 0.99999735 \\
m\sin(M - E)/p = \sin(\psi) & 0.87162727 \\
\pi - \arcsin(\sin(\psi)) = \psi & 2.08308025 \\
\gamma = E + \psi & 4.68407781\\
\gamma' & -1.59920106\\
\sin(\gamma') = \xi & -0.99959661 \\
\cos(\gamma') = \eta_1 & -0.02753202 \\
\phi_1 & -0.02816386 \\
\theta & -1.56710457 \\
 & \text{Sunrise} \\
\phi & -1\degree\:37'\:9'' \\
\lambda & 199\degree\:3'\:56'' \\ \hline
\end{array}
```
When computing the whole curve in $15$ minute intervals, we find that only between times $16:45$ and $20:00$ have $m\sin(M - E) < 1$. 
Thus the following table is computed only for those times:
```math
\begin{array}{|c|c|c|c|} \hline \text{Time} & \text{Latitude} & \text{Longitude} & \text{Obscuration} \\ \hline
16:45 & -1\degree\:37' & 199\degree\:4' & \\
17:00 & 12\degree\:34' & 193\degree\:26' & \\
17:15 & 23\degree\:50' & 188\degree\:2' & \\
17:30 & 33\degree\:45' & 182\degree\:35' & \\ \hline
19:15 & 79\degree\:44' & 27\degree\:46' & \\
19:30 & 70\degree\:41' & 359\degree\:36' & \\
19:45 & 58\degree\:21' & 346\degree\:9' & \\
20:00 & 38\degree\:20' & 336\degree\:3' & \\ \hline
\end{array}
```
