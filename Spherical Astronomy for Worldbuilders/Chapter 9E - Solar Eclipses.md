(Continued from Part D...)
### Curve of Maximum on the Horizon
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
Then, we have:
```math
\gamma = E + \psi \tag{9.68}
```
From where we can carry on with equations $9.58$ and $9.59$ to get the longitude and latitude of the place.

Evidently, $\sin(\psi) = m\sin(M - E)/p$ cannot be greater than $1$ or less than $-1$. Here, the approximation $p = 1$ can be made and we can say that in order for points on this curve to exist, $m\sin(M - E)$ must be less than $1$ and greater than $-1$.

Also, the first equation in $9.67$ produces two values for $\psi$. the value of $\psi$ that produces $|\Delta| > |l|$ must be discarded.
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
\psi_2 \rightarrow \Delta_2 & 0.87333703 & 0.10043927
\end{array}
```
Considering $l_1 = 0.53563338$ at this time, $\Delta_2$ for $E_1$ and $\Delta_1$ for $E_2$ fail the test. Thus, the true values of $\Delta$ are $-0.10119491$ and $0.10043927$.

We now find $\gamma$ by equation $9.68$ and proceed as we did in earlier examples. We use the values of $\psi$ that passed the test.
```math
\begin{array}{r|c|c} 
E + \psi = \gamma & -1.59823666 & 0.87162496\\
\rho_1 & 0.99670449 & 0.99670449\\
\gamma' & -1.59832734 & \\
p & 0.99999751 & \\
m\sin(M - E)/p = \sin(\psi) & -0.87325579 & \\
\psi & -1.06184464 & \\
E + \psi = \gamma & -1.59824113 & \\
\gamma' & -1.59833183 & \\
\sin(\gamma') = \xi & -0.99962092 & \\
\cos(\gamma') = \eta_1 & -0.02730201 & \\
\phi_1 & -0.02730201 & \\
\theta & -1.5672176 & \\
 & \text{Sunrise}& \\
\phi & -1\degree\:34'\:10''  & \\
\lambda & 199\degree\:3'\:32'' & \\ \hline
\end{array}
```
