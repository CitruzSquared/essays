(Continued from Part D...)
### Curve of Maximum Eclipse on the Horizon
While some places experience the beginning or end of the eclipse exactly at sunrise or sunset, some others experience maximum obscuration at sunrise or sunset. As discussed in chapter $\text{9C}$, the condition for maximum eclipse is:
```math
P' = 0\tag{9.64}
```
Expanding out $P'$ for eclipse on the horizon ($\zeta \approx \zeta_1 = 0$), we have:
```math
a' + c'\sin(Q) -b'\cos(Q) = 0 \tag{9.65}
```
This equation turns out to have two solutions:
```math
\begin{align}
Q_1 &= 2\arctan\left(\frac{\sqrt{-a'^2+b'^2+c'^2}-c'}{a' + b'}\right)\\
Q_2 &= 2\arctan\left(\frac{-\sqrt{-a'^2+b'^2+c'^2}-c'}{a' + b'}\right)
\end{align}\tag{9.66}
```
Now, let us say that the distance of the observer from the shadow axis at the moment of maximum eclipse is $\Delta$, which obviously must be less than or equal to $|l|$ as the observer must be within the shadow. Then, we can say that at maximum eclipse:
```math
\begin{align}
\Delta \sin(Q) &= x - \xi\\
\Delta \cos(Q) &= y - \eta
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
\Delta \sin(Q) &= m\sin(M) - p\sin(\gamma)\\
\Delta \cos(Q) &= m\cos(M) - p\cos(\gamma)
\end{align}
```
And if we now subtract $Q$ from all the angles, we get:
```math
\begin{align}
0 &= m\sin(M - Q) - p\sin(\gamma - Q)\\
\Delta &= m\cos(M - Q) - p\cos(\gamma - Q)\\
\end{align}
```
Now, if we put $\psi = \gamma - E$, we have:
```math
\begin{align}
\sin(\psi) &= \frac{m\sin(M - Q)}{p}\\
\Delta &= m\cos(M - Q) - p\cos(\psi)
\end{align} \tag{9.67}
```
Where $\Delta$ must be positive as it is a distance.
Then, we have:
```math
\gamma = Q + \psi \tag{9.68}
```
From where we can carry on with equations $9.58$ and $9.59$ to get the longitude and latitude of the place.

Evidently, $\sin(\psi) = m\sin(M - Q)/p$ cannot be greater than $1$ or less than $-1$. Here, the approximation $p = 1$ can be made and we can say that in order for points on this curve to exist, $m\sin(M - Q)$ must be less than $1$ and greater than $-1$. Also, the first equation in $9.67$ produces two values for $\psi$: the value of $\psi$ that produces $\Delta > |l|$ must be discarded.

To find determine at which times $m\sin(M - Q)/p$ produces mathematically possible outcomes for $\psi$, we must consider the extreme points of this curve. The extremes are the places where $\Delta = |l|$: i.e. the place experiences maximum eclipse when the place is on the boundary of the shadow of the Moon. This means that the Moon just barely grazes past the Sun in these locations and therefore are the edges of visibility of the eclipse.

When $\Delta = l$ and we have the fact that the eclipse is on the horizon, our problem is simply the problem from the last section. Therefore the extreme points of the curve of maximum eclipse on the horizon must be on the sunrise and sunset curves. Since $P'$ determines whether the eclipse is beginning, ending, or at maximum, we can look at our table of rising and setting limits (the table calculated in example $9.6$), and determine when on the rising / setting limit curves the eclipse goes from beginning to ending (or vice versa).

If we say that at time $t_1$, $P' = P'_1$, at time $t_2$, $P' = P'_2$, and the sign of $P'_1$ is the opposite of the sign of $P'_2$, we can find the approximate time that $P'$ flipped sign by approximating $P'$ as linear in this portion. If we let $t_0$ be the time when $P' = 0$, we find:
```math
t_0 = \frac{t_2 P'_1 - t_1 P'_2}{P'_1 - P'_2} \tag{9.69}
```
This approximation can be refined recursively, by finding the true value of $P'$ at $t_0$ and repeating the calculations (similar to the bisection method used in chapter $4$). Another way, that avoids recursive calculation, is to simply have a smaller time step which is not difficult computationally when done on a computer.

Once we have the time when $P' = 0$ on the rising/setting limits, we can simply calculate the place via the method of example $9.6$. These will be the extreme points of the curve of maximum on the horizon.

#### Example 9.7
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

We must first find the extreme points on the curve of maximum eclipse on the horizon. Looking at our computations in the previous example, we find four points where the eclipse goes from beginning to ending:
```math
\begin{array}{|c|c|}\hline \text{Time} & \epsilon & P' \\ \hline
16:30 & < 0 & -0.02759005\\
16:45 & < 0 & 0.12821353 \\ \hline
17:15 & > 0 & -0.13869916 \\
17:30 & > 0 & 0.00472722 \\ \hline
19:00 & < 0 & -0.05823664 \\
19:15 & < 0 & 0.10380897 \\ \hline
20:00 & > 0 & -0.0227394 \\
20:15 & > 0 & 0.12931085 \\ \hline
\end{array}
```
Now, using decimal hours (e.g. $16:30 = 16.5$) as our values of $t$, we can find the approximate places $P'$ flips sign for each of these intervals using equation $9.69$:
```math
\begin{alignat}{2}
t_{01} &= \frac{16.75 \cdot (-0.02759005) - 16.5 \cdot 0.12821353}{-0.02759005 - 0.12821353} &&= 16:32:38\\
t_{02} &= \frac{17.5 \cdot (-0.13869916) - 17.25 \cdot 0.00472722}{-0.13869916 - 0.00472722} &&= 17:29:30\\
t_{03} &= \frac{19.25 \cdot (-0.05823664) - 19.0 \cdot 0.10380897}{-0.05823664 - 0.10380897} &&= 19:05:23\\
t_{04} &= \frac{20.25 \cdot (-0.0227394) - 20.0 \cdot 0.12931085}{-0.0227394 - 0.12931085} &&= 20:02:15\\
\end{alignat}
```
We will not do a second approximation. (When predicting eclipses with a program, simply use smaller time steps than $15$ minutes to get more accurate answers.) Now we have to find the points on the rising and setting curve at these times. Using linearly interpolated values from the elements table in Chapter $\text{9Z}$:
```math
\begin{array}{|c|c|c|c|c|c|c|c|c|}\hline t & d & \mu & x & y & l_1 & \rho_1 & d_1 \\ \hline
16:32:38 & 0.12981883 & 1.18785924 & -1.05311448 & -0.17027728 & 0.53561349 & 0.99670349 & 0.13025064 \\
17:29:30 & 0.13006473 & 1.43597894 & -0.56856575 & 0.08686272 & 0.53569566 &  0.9967037 & 0.13049733 \\
19:05:23 & 0.13047918 & 1.8544714 & 0.24893948 & 0.52036319 & 0.53578202 & 0.99670406 & 0.13091313\\
20:02:15 & 0.13072501 & 2.10260536 & 0.73370105 & 0.77722511 & 0.53580264 & 0.99670427 & 0.13115976 \\ \hline
\end{array}
```
(Note that calculating the true elements at each of these times from the ephemeris using the method of example $9.2$ is even better and should be done when eclipse prediction is done using a program.)

We find our extreme points (using the method of example $9.6$, but the sign of $\epsilon$ to be used is already known):
```math
\begin{array}{cccc}\hline \text{Point} & \text{Time} & \text{Latitude} & \text{Longitude} \\ \hline
\text{Sunrise Southern Extreme} & 16:32:38 & -38\degree\:48'\:13'' & 207\degree\:58'\:0'' \\
\text{Sunrise Northern Extreme} & 17:29:30 & 33\degree\:29'\:55'' & 182\degree\:45'\:29'' \\
\text{Sunset Northern Extreme} & 19:05:23 & 82\degree\:31'\:16'' & 72\degree\:8'\:45'' \\
\text{Sunset Southern Extreme} & 20:02:15 & 16\degree\:49'\:18'' & 331\degree\:48'\:27'' \\ \hline
\end{array}
```
Whether the point is northern or southern is determined by the value of $\cos(Q)$ (see equation $9.10$). The $Q$ for these points was found in the same way as example $9.6$: equation $9.60$. If $\cos(Q)$ is positive, the point is northern. If $\cos(Q)$ is negative, the point is southern. If no internal contacts exist, there will only be two extremes, one per lobe, (as the sunrise and sunset lobes are connected, the curve of maximum eclipse on the horizon will extend throughout the whole eclipse), and both will be northern or both will be southern.

Now we know the curve of maximum eclipse on the horizon extends only from $16:32:38$ to $17:29:30$ for the sunrise lobe, and from $19:05:23$ to $20:02:15$ in the sunset lobe. The points in between are calculated via the method detailed above in this section: I will give the calculation for the point at time $16:45$ in full.

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
Thus, we can calculate $Q$ by equation $9.66$:
```math
\begin{align}
Q_1 &= 2\arctan\left(\frac{\sqrt{-(-0.0012427)^2+(-0.30358228)^2+(0.50818381)^2}-0.50114349}{-0.0012427 + (-0.30358228)}\right)\\
&= -0.53639649 \\
Q_2 &= 2\arctan\left(\frac{-\sqrt{-(-0.0012427)^2+(-0.30358228)^2+(0.50818381)^2}-0.50114349}{-0.0012427 + (-0.30358228)}\right)\\
&= 2.60099756
\end{align}
```
We find $\psi$ and $\Delta$ with equation $9.67$ for each value of $Q$, first approximating $p = 1$:
```math
\begin{alignat}{2}
\sin(\psi)_1 &= (0.95478937\sin(-1.69092252 - (-0.53639649)))/1 &&= -0.87325361 \\
\psi_{11} &= \arcsin(-0.87325361) &&= -1.06184017\\
\Delta_{11} &= 0.95478937\cos(-1.69092252 - (-0.53639649)) - 1\cdot\cos(-1.06184017) &&= -0.10119491\\
\psi_{12} &= \pi - \arcsin(-0.87325361) &&= 4.20343283\\
\Delta_{12} &= 0.95478937\cos(-1.69092252 - (-0.53639649)) - 1\cdot\cos(4.20343283) &&= 0.87333703\\
\\
\sin(\psi)_2 &= (0.95478937\sin(-1.69092252 - 2.60099756))/1 &&= 0.87162496 \\
\psi_{21} &= \arcsin(0.87162496) &&= 1.05850769\\
\Delta_{21} &= 0.95478937\cos(-1.69092252 - 2.60099756) - 1\cdot\cos(1.05850769) &&= -0.87990746\\
\psi_{22} &= \pi - \arcsin(0.87162496) &&= 2.08308496\\
\Delta_{22} &= 0.95478937\cos(-1.69092252 - 2.60099756) - 1\cdot\cos(2.08308496) &&= 0.10043927
\end{alignat}
```
Considering $l_1 = 0.53563338$ at this time, $\psi_{22}$ ($\psi_2$ for $Q_2$) is the only $\psi$ value that produces a positive $\Delta$ value that is less than $l$. Thus, we continue with $\psi_{22}$ and $Q_2$.
```math
\begin{array}{r|c} \hline
Q_2 + \psi_{22} = \gamma & 4.68408253 \\
\rho_1 & 0.99670449 \\
\gamma' & -1.59919632\\
p & 0.99999735 \\
m\sin(M - Q_2)/p = \sin(\psi)_2 & 0.87162727 \\
\pi - \arcsin(\sin(\psi))_2 = \psi_{22} & 2.08308025 \\
Q_2 + \psi_{22} = \gamma & 4.68407781\\
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
In the same manner the following table is computed:
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Curves of Maximum Eclipse on the Horizon}\\
\begin{array}{|c|c|c|} \hline \text{Time} & \text{Latitude} & \text{Longitude}\\ \hline
16:32:38 & -38\degree\:48' & 207\degree\:58' \\
16:45 & -1\degree\:37' & 199\degree\:4'  \\
17:00 & 12\degree\:34' & 193\degree\:26'  \\
17:15 & 23\degree\:50' & 188\degree\:2'  \\
17:29:30 & 33\degree\:30' & 182\degree\:45' \\ \hline
19:05:23 & 82\degree\:31' & 72\degree\:9 \\
19:15 & 79\degree\:44' & 27\degree\:46'  \\
19:30 & 70\degree\:41' & 359\degree\:36'  \\
19:45 & 58\degree\:21' & 346\degree\:9'  \\
20:00 & 38\degree\:20' & 336\degree\:3'  \\ 
20:02:15 & 16\degree\:49'& 331\degree\:48' \\ \hline
\end{array}
}
```
$\blacksquare$
### Greatest Eclipse
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/91a468a0-a447-411d-a60f-4ee875b5f00d" width="350"/> In this diagram, the point labeled $G$ is called the point of *greatest eclipse*. It is the point at which the distance from the center to the Earth to the center of the shadow, a variable we have been calling $m$, is minimum.

Minimizing $m$ means minimizing $m^2$, and since $m^2 = x^2 + y^2$, the derivative is:
```math
\frac{d(m^2)}{dt} = 2xx' + 2yy'
```
Which needs to be $0$.\
Since we can linearly approximate $x$ and $y$ as:
```math
\begin{align}
x &= x_0 + x'\tau\\
y &= y_0 + y'\tau
\end{align}
```
The derivative of $m^2$ expands to:
```math
\frac{d(m^2)}{dt} = 2(x_0x' + x'^2\tau) + 2(y_0y' + y'^2\tau)
```
Setting this to $0$ and solving for $\tau$ gives:
```math
\tau = -\frac{x_0x' + y_0y'}{x'^2 + y'^2} \tag{9.70}
```
And then $T$ is given by $T = T_0 + \tau$.

Successive uses of equation $9.70$ refine our estimation for the time of greatest eclipse. The value of $m$ at this point, i.e. the minimum value of $m$, is called the *gamma* of the eclipse.

The location of greatest eclipse on the surface of the Earth can have two distinct cases. If central contacts exist (to be discussed in the next section), the point of greatest eclipse lies on the curve of centrality (to be discussed in the next section) at the time of greatest eclipse. If central contacts do not exist, the point of greatest eclipse lies on the curve of maximum eclipse on the horizon, at the time of greatest eclipse.
#### Example 9.8
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the time of greatest eclipse and the gamma of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We choose $T_0 = 18:00$ as a first approximation. At this time,
```math
\begin{align}
x_0 &= -0.30856088 \\
y_0 &= 0.22479055 \\
x' &= 0.51147366 \\
y' &= 0.27129112
\end{align}
```
Thus, equation $9.70$ gives:
```math
\begin{align}
\tau &= -\frac{(-0.30856088)\cdot0.51147366 + 0.22479055\cdot0.27129112}{0.51147366^2 + 0.27129112^2}\\
&= 0.28888984h \\
T &= 18:00 + 0.28888984h = 18:17:20
\end{align}
```
We now linearly interpolate for the elements for this time (again, calculating their true values would be even better):
```math
\begin{array}{|c|c|c|c|c|}\hline t & x & y & x' & y'\\ \hline
18:17:20 & -0.16080953 & 0.30312923 & 0.51154119 & 0.27119988 \\ \hline
\end{array}
```
Now, equation $9.70$ gives:
```math
\begin{align}
\tau &= -\frac{(-0.16080953)\cdot0.51154119 + 0.30312923\cdot0.27119988}{0.51154119^2 + 0.27119988^2}\\
&= 0.00015538h \\
T &= 18:17:20 + 0.00015538h = 18:17:21
\end{align}
```
The gamma is given by the $m = \sqrt{x^2 + y^2}$ at this time. Since the second approximation makes such a little difference, we will just use the $x$ and $y$ for the interpolated times above:
```math
\text{Gamma } = \sqrt{(-0.16080953)^2 + 0.30312923^2} = 0.34314288
```
$\blacksquare$
### Curve of Centrality

When the shadow of the Moon passes over the Earth, the line the center of the shadow makes on the Earth is called the *curve of centrality* or *central curve*. Therefore the points on this curve have distance $0$ from the center of the shadow. Thus, equation $9.10$ become the extremely simple:
```math
\begin{align}
\xi &= x\\
\eta &= y
\end{align}
```
Therefore, we have (by equation $9.23$ and $9.24$):
```math
\begin{align}
\xi &= x\\
\eta_1 &= \frac{y}{\rho_1}\\
\zeta_1 &= 1 - \xi^2 - \eta_1^2
\end{align} \tag{9.70}
```
From which we continue with equations $9.29$ and $9.30$.

To find the times and locations at which the curve of centrality starts and ends, we can repeat the method of finding contacts in example $9.5$ while setting $l = 0$. This makes the double sign in equation $9.55$ obsolete and therefore there are only two contacts of the center with the Earth (if they even exist).

To find the duration of totality or annularity along the line (denoted $T_c$), we use the fact that time is distance divided by speed and that time must be positive. Thus:
```math
T_c = \left|\frac{2L_2}{v}\right| = \left|\frac{2(l_2 - i_2\zeta)}{v}\right| \tag{9.71}
```
Where $v$ is simply the speed at which the place of observation is moving with respect to the shadow, or:
```math
v^2 = (x' - \xi')^2 + (y' - \eta')^2 \tag{9.72}
```
With $\xi'$ and $\eta'$ being calculated by equation $9.40$:
```math
\begin{align}
\xi' &= \mu' (-\eta\sin(d) + \zeta\cos(d))\\
\eta' &= \mu' \xi \sin(d) - d'\zeta
\end{align}
```
But since we have $\xi = x$ and $\eta = y$ on the central curve, we can write:
```math
\begin{align}
\xi' &= \mu' (-y\sin(d) + \zeta\cos(d))\\
\eta' &= \mu' x \sin(d) - d'\zeta
\end{align} \tag{9.73}
```
#### Example 9.9
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the curve of centrality of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

First we have to determine the central contacts. We repeat the method of example $9.5$ but set $l = 0$ in equation $9.55$. Taking $T_0 = 18:00$ and $p = 1$ as a first approximation, we find:
```math
\begin{array}{r|c|c} \hline & \text{First Contact} & \text{Last Contact} \\ \hline
\tau & -1.33343322 & 1.91121291 \\
T & 16:41:00 & 19:54:40 \\
p & 0.99993787 & 0.99817491 \\ \hline
\end{array}
```
We now linearly interpolate for the elements for these times (again, calculating their true values would be even better):
```math
\begin{array}{|c|c|c|c|c|c|c|c|}\hline t & d & \mu & x & y & i_2 & l_2 & \rho_1\\ \hline
16:40:00 & 0.12985038 & 1.21988483 & -0.99057474 & -0.13707257 & 0.00464516 & -0.00913349 & 0.99670351 \\
19:54:40 & 0.13069238 & 2.06956364 & 0.66914899 & 0.74302244 & 0.00464499 & -0.00895854 & 0.99670424 \\ \hline
t & d_1 & \rho_2 & d_2 & d' & \mu' & x' & y' \\ \hline
16:41:00 & 0.13028229 & 0.99994388 & 0.12941987 & 0.00025897 & 0.26187053 & 0.5114177 & 0.27144902 \\
19:54:40 & 0.13112703 & 0.99994315 & 0.13025915 & 0.00025898 & 0.26187148 & 0.51157069 & 0.27105629\\ \hline
\end{array}
```
Now repeating the calculations for the contacts, we obtain:
```math
\begin{array}{r|c|c} \hline & \text{First Contact} & \text{Last Contact} \\ \hline
T_0 & 16:40:00 & 19:54:40 \\
\tau & 0.00052253 & -0.00321216 \\
T & 16:40:02 & 19:54:28 \\
\gamma' & -1.70807333 & 0.73085298 \\
\phi & -7\degree\:49'\:27'' & 47\degree\:40'\:46'' \\
\lambda & 201\degree\:8'\:2'' & 339\degree\:41'\:25'' \\ \hline
\end{array}
```
Now that we know the curve of centrality extends from $16:40:02$ to $19:54:28$, we can compute the curve. I will give the calculation for the point at time $18:00$ in full.

At this time, the elements are:
```math
\begin{array}{|c|c|c|c|c|c|c|c|}\hline t & d & \mu & x & y & i_2 & l_2 & \rho_1\\ \hline
18:00 &  0.13019636 & 1.56907269 & -0.30856088 & 0.22479055 & 0.0046451 & -0.00902906 & 0.99670381\\ \hline
t & d_1 & \rho_2 & d_2 & d' & \mu' & x' & y' \\ \hline
18:00 & 0.13062939 & 0.99994358 & 0.12976473  & 0.00025898 & 0.26187054 & 0.51147366 & 0.27129112 \\ \hline
\end{array}
```
equation $9.70$ gives:
```math
\begin{alignat}{2}
\xi &= -0.30856088 &&\\
\eta_1 &= \frac{0.22479055}{0.99670381} &&= 0.22553395\\
\zeta_1 &= 1 - (-0.30856088)^2 - (0.22553395)^2 &&= 0.85392462
\end{alignat}
```
Then, equations $9.29$ and $9.30$ give:
```math
\begin{align}
\phi_1 &= 0.34143872\\
\theta &= -0.36100439\\
\phi &= 19\degree\:37'\:26''\\
\lambda &= 249\degree\:24'\:53''\\
\end{align}
```
Now to find the central duration. Equation $9.27$ gives $\zeta$:
```math
\begin{align}
\zeta &= -0.99994358 \cdot 0.22553395 \sin(0.13062939 - 0.12976473) + 0.99994358 \cdot 0.85392462\cos(0.13062939 - 0.12976473) \\
&= 0.85368112
\end{align}
```
Equation $9.73$ gives $\xi'$ and $\eta'$:
```math
\begin{align}
\xi' &= 0.26187054 (-0.22479055\sin(0.13019636) + 0.85368112\cos(0.13019636))\\
&= 0.21401936\\
\eta' &= 0.26187054 \cdot (-0.30856088) \sin(0.13019636) - 0.00025898\cdot0.85368112\\
&= -0.01071163
\end{align}
```
Now, equation $9.72$ gives $v$:
```math
\begin{alignat}{2}
v^2 &= (0.51147366 - 0.21401936)^2 + (0.27129112 - (-0.01071163))^2 &&= 0.16800461 \\
\therefore v &= \sqrt{0.16800461} &&= 0.40988365
\end{alignat}
```
Then equation $9.71$ gives the central duration:
```math
T_c = \left|\frac{2(-0.00902906 - 0.0046451 \cdot 0.85368112)}{0.40988365}\right| = 0.06340577h
```
The result is in hours because all our derivatives are in units of hours. When converted to minutes and seconds, $T_c$ is:
```math
T_c = 3m\:48s
```
