(Continued from Part C...)
### Contacts

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/91a468a0-a447-411d-a60f-4ee875b5f00d" width="350"/>  As the shadow of the Moon (the shaded circle) passes over the Earth (the larger circle centered on $E$), there are a few key times of interest. 

The times and points at which the shadow cone of the Moon is tangent to the Earth are known as *contacts*. There are four contacts, labeled $1$, $2$, $3$, and $4$ in the diagram:
1. First External Contact (External Ingress)
2. First Internal Contact (Internal Ingress)
3. Last Internal Contact (Internal Egress)
4. Last External Contact (External Egress)

If the shadow in question is the penumbra, these times are called $P_1$, $P_2$, $P_3$, and $P_4$ respectively, and if the shadow is the umbra, they are called $U_1$, $U_2$, $U_3$, and $U_4$ respectively.

Evidently, $P1$ and $P4$ are the times at which the eclipse begins and ends globally, and $U1$ and $U2$ are the times at which the total (or annular) eclipse begins and ends globally.

Also, notice that because the shadow cone is tangent to the Earth, at the locations of contact the eclipse must be at the local horizon. For our purposes, this means that the zenith distance of the point $Z$ (the point that points in the direction of the shadow axis) is $90\degree$, and therefore by equation $9.34$, $\zeta_1 = 0$. This means that, by equation $9.24$, for contacts:
```math
\xi^2 + \eta_1^2 = 1\tag{9.51}
```
On the fundamental plane, let's define $m$, $M$, $p$, and $\gamma$ such that:
```math
\begin{align}
m\sin(M) &= x\\
m\cos(M) &= y\\
p\sin(\gamma) &= \xi\\
p\cos(\gamma) &= \eta
\end{align} \tag{9.52}
```
Then, the distance from the center of the Earth to $(x, y)$ is $m$ and the distance to $(\xi, \eta)$ is $p$.\
Thus, at the contacts we have:
```math
m = p\pm l 
```
Where the top sign is for external contacts and the bottom is for internal contacts.\
Therefore, at contacts, we have:
```math
\begin{align}
(p \pm l)\sin(M) &= x\\
(p \pm l)\cos(M) &= y
\end{align}\tag{9.53}
```
For reasonable cases, $x$ and $y$ are very close to linear. Thus, if we say that at time $T_0$ the coordinates of the shadow of the Moon were $x_0$ and $y_0$ and their derivatives were $x'$ and $y'$, we have at time $\tau$ after $T_0$:
```math
\begin{align}
x &= x_0 + x'\tau\\
y &= y_0 + y'\tau
\end{align}
```
If we now put:
```math
\begin{align}
m_0\sin(M_0) &= x_0\\
m_0\cos(M_0) &= y_0\\
n\sin(N) &= x'\\
n\cos(N) &= y'
\end{align} \tag{9.54}
```
Then equations $9.53$ become:
```math
\begin{align}
(p \pm l)\sin(M) &= m_0\sin(M_0) + \tau n\sin(N) \\
(p \pm l)\cos(M) &= m_0\cos(M_0) + \tau n\cos(N) 
\end{align}
```
If we subtract $N$ from all angles in the above equation, we get:
```math
\begin{align}
(p \pm l)\sin(M - N) &= m_0\sin(M_0 - N)\\
(p \pm l)\cos(M - N) &= m_0\cos(M_0 - N) + \tau n
\end{align}
```
Now, if we put $\psi = M - N$, we have, for the time of contacts:
```math
\begin{align}
\sin(\psi) &= \frac{m_0\sin(M_0 - N)}{p \pm l}\\
\tau &=  \frac{(p \pm l)\cos(\psi) - m_0\cos(M_0 - N)}{n}\\
T &= T_0 \pm \tau
\end{align} \tag{9.55}
```
Where in the last equation we take the top sign for last contacts and the bottom sign for first contacts. Notice that in the first equation, for interior contacts, if $p - l$ is less than $m_0\sin(M_0 - N)$, then $\sin(\psi)$ exceeds $1$ and therefore no $\psi$ exists: this means that there are no interior contacts and there is always a part of the shadow that misses the Earth.

In these formulae, we have everything we need except $p$. Because $(\xi, \eta)$ must be on the edge of the Earth, $p$ must be very close to $1$ and we can start with $p = 1$ as a first approximation. Once getting the first approximation for $\psi$, we have $M = N + \psi$, but also since at the contacts $(x, y)$ and $(\xi, \eta)$ must be on the same line (see diagram), $M = \gamma$ and thus:
```math
\gamma = N + \psi \tag{9.56}
```
Now, if we put $\xi = \sin(\gamma')$, then by equation $9.51$, $\eta_1 = \cos(\gamma')$, and then because $\eta = \rho_1\eta_1$ (equation $9.23$), we have:
```math
\begin{align}
p\sin(\gamma) &= \sin(\gamma')\\
p\cos(\gamma) &= \rho_1\cos(\gamma')
\end{align}\tag{9.57}
```
From these we can deduce:
```math
\begin{align}
\tan(\gamma') &= \rho_1\tan(\gamma)\\
p &= \frac{\sin(\gamma')}{\sin(\gamma)} = \frac{\rho_1\cos(\gamma')}{\cos(\gamma)}
\end{align}\tag{9.58}
```
Which yields a second approximation for $p$ which yields another value of $\psi$. As many repetitions can be taken until convergence is reached. After repetition, a value for $\gamma'$ gives:
```math
\begin{align}
\xi &= \sin(\gamma')\\
\eta_1 &= \cos(\gamma') \tag{9.59}\\
\zeta_1 &= 0
\end{align}
```
From which equations $9.29$ and $9.30$ give the location of contact on the surface of the Earth.
#### Example 9.5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the time and location of the $P_1$, $P_2$, $P_3$, and $P_4$ contacts for the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Elements will be taken from previous examples and all angles will be given in radians.\
We will take $T_0 = 18:00$. Equations $9.54$ give:
```math
\begin{alignat}{2}
m_0\sin(M_0) &= -0.30856086 &&\\
m_0\cos(M_0) &= 0.22479055 &&\\
\therefore m_0 &= \sqrt{(-0.30856086)^2 + 0.22479055^2} &&= 0.38175987\\
\therefore M &= \arctan(-0.30856086, 0.22479055) &&= -0.94118943 \text{ rad}\\
n\sin(N) &= 0.51147366 &&\\
n\cos(N) &= 0.27129112 &&\\
\therefore n &= \sqrt{0.51147366^2 + 0.27129112} &&= 0.57896820\\
\therefore N &= \arctan(0.51147366, 0.27129112) &&= 1.08311714 \text{ rad}
\end{alignat}
```
Now, taking $p = 1$ as a first approximation, for $P_1$, equations $9.55$ give:
```math
\begin{align}
\sin(\psi) &= \frac{0.38175987 \sin(-0.94118943 - 1.08311714)}{1 + 0.53573027}\\
&= -0.22345693\\
\therefore \psi &= -0.22535964\text{ rad}\\
\tau &=  \frac{(1 + 0.53573027)\cos(-0.22535964) - 0.38175987\cos(-0.94118943 - 1.08311714)}{0.57896820}\\
&= 2.87434701h\\
T_\text{First External} &= 18:00 - 2.87434701h = 15:07:32\\
T_\text{Last External} &= 18:00 + 2.87434701h = 20:52:28
\end{align}
```
Then by equation $9.56$ and $9.58$:
```math
\begin{alignat}{2}
\gamma &= 1.08311714 + -0.22345693 &&= 0.8577575\\
\gamma' &= \arctan(0.99670381 \tan(0.8577575)) &&= 0.85612355\\
p &= \frac{\sin(0.85612355)}{\sin(0.8577575)} &&= 0.99858559
\end{alignat}
```
Rounding the contact times to the nearest minute,
```math
\begin{array}{ccc}\hline \text{Element} & 15:08 & 20:52 \\ \hline
d & 0.12945233 & 7\degree\:27'\:48.33''\\
x & -1.77450619 & -0.18070657 \
y & -0.5533137 & 0.29258104 \\
\mu & 1.57092161 & 93\degree\:39'\:8.07''\\
i_1 & 0.00466849  & 0.53574486 \\
l_1 & 0.53544889 & 0.53574486 \\
x' (\Delta t = \pm 15m) & 0.53571408 & 0.53574486 \\
y' (\Delta t = \pm 15m) & -0.00904516 & -0.00901454\\ \hline
\end{array}
```
