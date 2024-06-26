(Continued from Part C...)
### Contacts

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/91a468a0-a447-411d-a60f-4ee875b5f00d" width="350"/>  As the shadow of the Moon (the shaded circle) passes over the Earth (the larger circle centered on $E$), there are a few key times of interest. 

The times and points at which the shadow cone of the Moon is tangent to the Earth are known as *contacts*. There are four contacts, labeled $1$, $2$, $3$, and $4$ in the diagram:
1. First External Contact (External Ingress)
2. First Internal Contact (Internal Ingress)
3. Last Internal Contact (Internal Egress)
4. Last External Contact (External Egress)

The point labeled $G$ is called "Greatest Eclipse" and will be discussed later.

If the shadow in question is the penumbra, the contact points are called $P_1$, $P_2$, $P_3$, and $P_4$ respectively, and if the shadow is the umbra, they are called $U_1$, $U_2$, $U_3$, and $U_4$ respectively.

Evidently, $P1$ and $P4$ are the times at which the eclipse begins and ends globally, and $U1$ and $U2$ are the times at which the total (or annular) eclipse begins and ends globally.

Also, notice that because the shadow cone is tangent to the Earth, at the locations of contact the eclipse must be at the local horizon. For our purposes, this means that the zenith distance of the point $Z$ (the point that points in the direction of the shadow axis) is $90\degree$, and therefore by equation $9.34$, $\zeta_1 = 0$. This means that, by equation $9.24$, for contacts:
```math
\xi^2 + \eta_1^2 = 1\tag{9.51}
```
On the fundamental plane, let's define $m$, $M$, $p$, and $\gamma$ such that:
```math
\displaylines{
\begin{cases}
m\sin(M) = x\\
m\cos(M) = y
\end{cases}
\enspace\enspace\enspace\enspace
\begin{cases}
p\sin(\gamma) = \xi\\
p\cos(\gamma) = \eta
\end{cases} }\tag{9.52}
```
Then, the distance from the center of the Earth to $(x, y)$ is $m$ and the distance to $(\xi, \eta)$ is $p$.\
Thus, at the contacts we have:
```math
m = p\pm l 
```
Where the top sign is for external contacts and the bottom is for internal contacts, and we use the *absolute value* of $l$ (because it is used as a distance here, the umbral shadow must also be written positive here).\
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
\displaylines{
\begin{cases}
m_0\sin(M_0) = x_0\\
m_0\cos(M_0) = y_0
\end{cases}
\enspace\enspace\enspace\enspace
\begin{cases}
n\sin(N) = x'\\
n\cos(N) = y'
\end{cases} } \tag{9.54}
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
T &= T_0 + \tau
\end{align} \tag{9.55}
```
The first equation has two solutions: we take $\psi = \arcsin()$ for last contacts and $\psi = 180\degree - \arcsin()$ for first contacts. Notice that in the first equation, for interior contacts, if $p - l$ is less than $m_0\sin(M_0 - N)$, then $\sin(\psi)$ exceeds $1$ and therefore no $\psi$ exists: this means that there are no interior contacts and there is always a part of the shadow that misses the Earth.

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
\gamma' &= \arctan(\rho_1 \sin(\gamma), \cos(\gamma))\\
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
Find the time and location of the $P_1$, $P_2$, $P_3$, and $P_4$ contacts of the solar eclipse of $\text{April 8, } 2024$.
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
\therefore M_0 &= \arctan(-0.30856086, 0.22479055) &&= -0.94118943 \text{ rad}\\
n\sin(N) &= 0.51147366 &&\\
n\cos(N) &= 0.27129112 &&\\
\therefore n &= \sqrt{0.51147366^2 + 0.27129112} &&= 0.57896820\\
\therefore N &= \arctan(0.51147366, 0.27129112) &&= 1.08311714 \text{ rad}
\end{alignat}
```
Now, taking $p = 1$ as a first approximation, for the exterior contacts, equations $9.55$ give:
```math
\begin{align}
\sin(\psi) &= \frac{0.38175987 \sin(-0.94118943 - 1.08311714)}{1 + 0.53573027}\\
&= -0.22345693\\
\psi_\text{First External} &= \pi - \arcsin(-0.22345693)\\
&= 3.3669523 \text{ rad}\\
\tau_\text{First External} &= \frac{-(1 + 0.53573027)\cos(-0.22535964) - 0.38175987\cos(-0.94118943 - 1.08311714)}{0.57896820}\\
&= -2.29656737h\\
T_\text{First External} &= 18:00 - 2.29656737h = 15:42:12\\
\\
\psi_\text{Last External} &= \arcsin(-0.22345693)\\
&= -0.22535964\text{ rad}\\
\tau_\text{Last External} &=  \frac{(1 + 0.53573027)\cos(-0.22535964) - 0.38175987\cos(-0.94118943 - 1.08311714)}{0.57896820}\\
&= 2.87434701h\\
T_\text{Last External} &= 18:00 + 2.87434701h = 20:52:28
\end{align}
```
Then by equation $9.56$ and $9.58$:\
(For the first external contact and using $\rho_1$ for $18:00$)
```math
\begin{alignat}{2}
\gamma &=  1.08311714 + 3.3669523 &&= 4.45006944\\
\gamma' &= \arctan(0.99670381 \sin(4.45006944), \cos(4.45006944)) &&= -1.83394395\\
p &= \frac{\sin(-1.83394395)}{\sin(4.45006944)} &&= 0.999777311
\end{alignat}
```
Similarly, for the last external contact:
```math
\begin{alignat}{2}
\gamma &= 1.08311714 + (-0.22535964) &&= 0.8577575\\
\gamma' &= \arctan(0.99670381 \sin(0.8577575), \cos(0.8577575)) &&= 0.85612355\\
p &= \frac{\sin(0.85612355)}{\sin(0.85612355)} &&= 0.99858559
\end{alignat}
```
Repeating this computation but using $p - l$ in equation $9.55$ gives the times for internal contact:
```math
\begin{array}{r|c|c}\hline  & P_2 & P_3 \\ \hline
m_0 & 0.38175987 & 0.38175987\\
M_0 & -0.94118943 & -0.94118943\\
n & 0.57896820 & 0.57896820\\
N & 1.08311714 & 1.08311714\\
\sin(\psi) & -0.7391599 & -0.7391599\\
\psi & 3.97341485 & -0.83182219\\
\tau & -0.25120821 & 0.82898786\\
T_0 + \tau = T & 17:44:56 & 18:49:44\\
N + \psi = \gamma & 5.05653199 & 0.25129495\\
\gamma' & -1.22560336 & 0.25050091\\
p & 0.99962314 & 0.99690667\\ \hline
\end{array}
```

Rounding the contact times to the nearest minute the Besselian elements are (using the method of example $9.2$): (For a more accurate calculation, calculate Besselian elements at exactly those times we calculated. We only round here because the ephemeris we are using only gives minute precision.)
```math
\begin{array}{c|cc|cc}\hline \text{Element} & 15:42:00 & 20:52:00 & 17:45:00 & 18:50:00 \\ \hline
d & 0.12959946 & 0.13094043 & 0.13013186 & 0.13041266\\
\mu & 0.9667687 & 2.31976942 & 1.50360469 & 1.78729814\\
\rho_1 & 0.9967033 & 0.99670446 & 0.99670376 & 0.996704\\
d_1 & 0.13003055 & 0.13137588 & 0.13056468 & 0.13084639\\
x & -1.48485233 & 1.15791302 & -0.4364434 & 0.11772183 \\
y & -0.39946392 & 1.00188386 & 0.15693548 & 0.45082482  \\
i_1 & 0.00466846  & 0.00466819 & 0.00466835 & 0.0046683 \\
l_1 & 0.53552115 & 0.53580193 & 0.53571408 & 0.53577271  \\
x' (t \pm 0.25h) & 0.51119288 & 0.51145248 & 0.51158452 & 0.51156302 \\
y' (t \pm 0.25h) & 0.27151022 & 0.27085576 & 0.27138506 & 0.2712357\\ \hline
\end{array}
```
Now we are ready for a second approximation using the new elements at each time and the new values of $p$:
```math
\begin{array}{r|c|c|c|c}\hline  & P_1 & P_4 & P_2 & P_3\\ \hline
T_0 & 15:42:00 & 20:52:00 & 17:45:00 & 18:50:00 \\
m_0 & 1.53764686 & 1.53118707 & 0.46380123 & 0.46594147\\
M_0 & -1.83360014 & 0.8575154 & -1.22561432 & 0.25542194\\
n & 0.57882291 & 0.57874561 & 0.57911016 & 0.57902118\\
N & 1.08255544 & 1.08376454 & 1.08306354 & 1.08327401\\
\text{(For reference) } p & 0.999777311 & 0.99858559 & 0.99962314 & 0.99690667\\
\sin(\psi) & -0.22387431 & -0.22385595 & -0.73972339 & -0.74415818\\
\psi & 3.36738053 & -0.22576904  & 3.97425185 & -0.83927375\\
\tau & 0.00416269 & 0.00567428 & -0.00027673 & -0.01235072\\
T_0 + \tau = T & 15:42:15 & 20:52:20 & 17:44:59 & 18:49:15
\end{array}
```
Evidently, the first approximation is correct to a few seconds: the first approximation is good enough for most reasonable cases. We will not calculate new Besselian elements for the new times, we will just use the ones after the first approximation.
From here:
```math
\begin{array}{r|c|c}\text{(For reference) } N & 1.08255544 & 1.08376454 & 1.08306354 & 1.08327401\\
\text{(For reference) } \psi & 3.36738053 & -0.22576904 & 3.97425185 & -0.83927375\\
N + \psi = \gamma & 4.44993597 & 0.8579955 & 5.05731539 & 0.24400026\\
\gamma' \enspace(9.58) & -1.83407792 & 0.85636199 & -1.22481794 & 0.24322743\\
\sin(\gamma') = \xi& -0.96554114 & 0.75546398 & -0.94074412 & 0.24083631\\
\cos(\gamma') = \eta_1& -0.26025046 & 0.65519018 & 0.33911725 & 0.97056575\\
\phi_1 \enspace(9.29)& -0.26100683 & 0.70698473 & 0.34291188 & 1.29522234\\
\theta \enspace(9.29)& -1.53586099 &  1.68392198 & -1.61769396 &  2.05487427  \\
\phi \enspace(9.30)& -15\degree\:0'\:9'' & 40\degree\:36'\:8'' & 19\degree\:42'\:30'' & 74\degree\:15'\:40''\\
\lambda \enspace(9.30)& 216\degree\:36'\:36'' & 323\degree\:34'\:7'' & 181\degree\:9'\:46'' & 15\degree\:19'\:52''\\ \hline
\end{array}
```
Our answers can be arranged in a table: 
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Contacts of Penumbra}\\
\begin{array}{cccc}\hline \text{Event} & \text{Contact} &\text{Time} & \text{Latitude} & \text{Longitude}\\ \hline
\text{First External Contact} & P_1& 15:42:15 & -15\degree\:0'\:9'' & 216\degree\:36'\:36'' \\
\text{First Internal Contact} & P_2& 17:44:59 & 19\degree\:42'\:30'' & 181\degree\:9'\:46'' \\
\text{Last Internal Contact}  & P_3& 18:49:15 & 74\degree\:15'\:40'' & 15\degree\:19'\:52'' \\
\text{Last External Contact}  & P_4& 20:52:20 & 40\degree\:36'\:8'' & 323\degree\:34'\:7'' \\ \hline
\end{array}
}
```
We could make a third and more accurate approximation, but for the sake of brevity I will stop at two. For another method of calculation of the internal contacts, see chapter $\text{9F}$, in the section *A Note on Time Steps*.\
$\blacksquare$

Only now that we know that this eclipse began globally at $15:42$ and ended at $20:52$, can we calculate the Besselian elements for the entire eclipse and tabulate them. The elements for the times in between the tabulated values can then be found via simple interpolation. If one is writing a program to predict eclipses however, tabulation and interpolation is unnecessary, simply start at the beginning time, calculate the elements and the coordinates of the location of the shadow of the Moon at that time (especially the special locations to be discussed hereafter), then increment the time by a preselected $\Delta t$ (the smaller the better).

The Besselian elements for this eclipse, calculated at $15$ minute intervals using methods detailed previously, can be found in Chapter $\text{9Z}$.

### Rising and Setting Limits
In the last section we discussed how at the moment of contact at the location of contact, the shadow cone is tangent to the Earth and therefore the eclipse in those locations would be on the horizon. In particular, the contacts are:
1. First External Contact
   - The first place on the Earth at which the eclipse begins at sunrise.
2. First Internal Contact
   - The last place on the Earth at which the eclipse ends at sunrise.
3. Last Internal Contact
   - The first place on the Earth at which the eclipse begins at sunset.
4. Last External Contact
   - The last place on the Earth at which the eclipse ends at sunset.

Between the contacts, there are a whole set of points where the eclipse either begins or ends exactly at sunrise or sunset: returning to equation $9.52$, we can write equation $9.18$ as:
```math
\begin{align}
(l - i\zeta)\sin(Q) &= m \sin(M) - p\sin(\gamma)\\
(l - i\zeta)\cos(Q) &= m \cos(M) - p\cos(\gamma)
\end{align}
```
From the fact that $\zeta_1 = 0$ when the eclipse is on the horizon, we can write $\zeta = \zeta_1 = 0$ and therefore:
```math
\begin{align}
l\sin(Q) &= m \sin(M) - p\sin(\gamma)\\
l\cos(Q) &= m \cos(M) - p\cos(\gamma)
\end{align}\tag{9.60}
```
If we add the squares of both equations, we get:
```math
\begin{align}
l^2 &= m^2 - 2mp \sin(M)\sin(\gamma) - 2mp\cos(M)\cos(\gamma) + p^2\\
l^2 &= m^2 + p^2 - 2mp\cos(M - \gamma)\\
l^2 - m^2 - p^2 &= -2mp\cos(M - \gamma)\\
l^2 - m^2 - p^2 + 2mp &= -2mp\cos(M - \gamma) + 2mp\\
\frac{l^2 - (m - p)^2}{2mp} &= 1 - \cos(M - \gamma)\\
\frac{l^2 - (m - p)^2}{2mp} &= 2\sin^2((M - \gamma)/2)\\
\frac{(l - m + p)(l + m - p)}{4mp} &= \sin^2((M - \gamma)/2)\\
\end{align}
```
If we now set $\epsilon = M - \gamma$, we have:
```math
\sin(\epsilon/2) = \pm\sqrt{\frac{(l - m + p)(l + m - p)}{4mp}} \tag{9.61}
```
Where $\epsilon/2$ can always be taken as less than $90\degree$. Once we have $\epsilon$, we can get $\gamma$ by:
```math
\gamma = M + \epsilon \tag{9.62}
```
And then carry on with equations $9.58$ and $9.59$ to get the latitude and longitude of the place. Now, because of the double sign on equation $9.61$, we can see that there are two points where the eclipse is beginning or ending on the horizon at any moment in time between the internal and external contacts. Determining whether the Sun is rising or setting at the point calculated can be done by comparing $\theta$, the hour angle of the eclipse. Remembering that the hour angle is measured such that West is positive, if the hour angle $\theta$ is less than $180\degree$, the eclipse is happening at sunset. If the hour angle is more than $180\degree$ (or between $-180\degree$ and $0\degree$), the eclipse is happening at sunrise. Determining if the eclipse is beginning or ending can be done just like example $9.4$, but since we have $\zeta = 0$, equation $9.50$ simplifies to:
```math
P' = a' + c'\sin(Q) - b'\cos(Q) \tag{9.63}
```
Where we have $Q$ by equation $9.60$.

Because the points at which the eclipse is in progress during sunrise or sunset can only exist between external and internal contact, if there are no internal contacts during an eclipse (as is frequently so), then there will always be points where the eclipse is in progress at the horizon and therefore the lines of beginning/ending at sunrise/sunset extend throughout the whole eclipse. If internal contacts exist, the points where the eclipse begins/ends at sunrise and the points at which the eclipse begins/ends at sunset form two distinct areas on the globe. 

#### Example 9.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the rising and setting limits of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Because we have internal contacts in this eclipse, the rising / setting limits will form two distinct areas:
- The sunrise lobe between $P_1$ and $P_2$
- The sunset lobe between $P_3$ and $P_4$

I will give the calculation of the limiting points for the time $16:00$ in full.\
For this time, we have:
```math
\begin{align}
\mu &= 1.04533016 \\
x &= m\sin(M) = -1.3314264 \\
y &= m\cos(M) = -0.31802844 \\
l_1 &= 0.53555609\\
\rho_1 &= 0.99670336 \\
d_1 &= 0.13010879
\end{align}
```
From this we can deduce, in the same manner as example $9.5$:
```math
\begin{align}
m &= 1.36888215 \\
M &= -1.80526591
\end{align}
```
Using $p = 1$ as a first estimate, we can calculate $\epsilon$ via equation $9.61$:
```math
\begin{align}
\sin(\epsilon/2) &= \pm\sqrt{\frac{(0.53555609 - 1.36888215 + 1)(0.53555609 + 1.36888215 - 1)}{4 \cdot 1.36888215}}\\
&= \pm0.16592441\\
\therefore \epsilon_1 &= 2\arcsin(0.16592441) = 0.33339068\\
\therefore \epsilon_2 &= 2\arcsin(-0.16592441) = -0.33339068
\end{align}
```
Now, we can find $\gamma$ with equation $9.62$, then $\gamma'$ and then a better approximation for $p$ with equation $9.58$:
```math
\begin{array}{r|c|c}\hline  & \epsilon > 0 & \epsilon < 0 \\ \hline
M + \epsilon = \gamma & -1.47187523 & -2.13865659 \\
\gamma' & -1.47155018 & -2.14015486 \\
p & 0.99996769 &  0.99904305 
\end{array}
```
Now we substitute this value of $p$ into equation $9.61$:
```math
\begin{array}{r|c|c} \sin(\epsilon/2) & 0.16591397 & -2.13865659 \\
\epsilon & 0.33336951 & -0.33276149 \\
M + \epsilon = \gamma & -1.4718964 &  -2.1380274 \\
\gamma' & -1.47157142 & -2.13952479 
\end{array}
```
And now with this sufficiently accurate value of $\gamma'$ we can get the longitude and latitude of the point with equations $9.59$, $9.29$, and $9.30$:
```math
\begin{array}{r|c|c} \sin(\gamma') = \xi & -0.99508125 & -0.84258646 \\
\cos(\gamma') = \eta_1 & 0.09906216 & -0.53856111 \\
\phi_1 & 0.0983835 &  -0.56333528 \\
\theta & -1.58371166 & -1.48805765 \\
 & \text{Sunrise} & \text{Sunrise}\\
\phi & 5\degree\:39'\:21'' &  -32\degree\:21'\:49'' \\
\lambda & 209\degree\:22'\:1'' & 214\degree\:50'\:51''\\ \hline
\end{array}
```
These points we just calculated are these two points (marked red) on this map:
<p align="center">
  <img width="250" src="https://github.com/CitruzSquared/essays/assets/23460281/cb85358d-a578-45f0-ad8a-c871c2391b5d"> <br/>
</p>

The fact that they are both for sunrise is to be expected since $16:00$ is between $P_1$ and $P_2$ and therefore falls in the sunrise lobe.

To determine whether the eclipse is beginning or ending at these points, we have (for $16:00$):
```math
\begin{align}
a_1' &= -0.00172705\\
b_1' &= -0.31653541\\
c_1' &= 0.50114349
\end{align}
```
Thus:
```math
\begin{array}{r|c|c}\hline  & \epsilon > 0 & \epsilon < 0 \\ \hline
p\sin(\gamma) & -0.99508123 & -0.84258487 \\
p\cos(\gamma) & 0.09873559 & -0.53678465 \\ 
x - p\sin(\gamma) = l\sin(Q) \enspace(9.60) & -0.33634517 & -0.48884153 \\
y - p\cos(\gamma) = l\cos(Q) \enspace(9.60) & -0.41676403 & 0.21875621 \\
Q & -2.46257385 & -1.15002398 \\
P' \enspace(9.63) & - 0.56278455 & - 0.32986385\\
P' < 0 \text{ and } l > 0 & \text{Beginning} & \text{Beginning}\\ \hline
\end{array}
```
Note that here, we could have gotten a more accurate value for $Q$ by calculating a more accurate value for $p$ using the value of $\gamma'$ we calculated earlier, but this is wholly unnecessary when only the algebraic sign of $P'$ is necessary. (In fact, the fact that we did not do this correction is why $p\sin(\gamma)$ very slightly differs from the value of $\xi$ we found earlier.)

In the same manner the following table is computed:
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Rising and Setting Limits – Sunrise Lobe}\\
\begin{array}{|c|c|c|ccc|c|c|c|ccc|}\hline \text{Time} & \text{Latitude} & \text{Longitude} & & & & & \text{Latitude} & \text{Longitude} & & & \\ \hline
15:42:15 & -15\degree\:0' & 216\degree\:37' & \text{Begins} & \text{at} & \text{Sunrise} && & & & &\\
15:45 & -7\degree\:6' & 214\degree\:47' & \text{Begins} & \text{at} & \text{Sunrise} && -22\degree\:23' & 216\degree\:56' & \text{Begins} & \text{at} & \text{Sunrise} \\
16:00 & 5\degree\:39' & 209\degree\:22' & \text{Begins} & \text{at} & \text{Sunrise} && -32\degree\:22' & 214\degree\:51' & \text{Begins} & \text{at} & \text{Sunrise} \\
16:15 & 13\degree\:26' & 204\degree\:34' & \text{Begins} & \text{at} & \text{Sunrise} && -36\degree\:46' & 211\degree\:57' & \text{Begins} & \text{at} & \text{Sunrise} \\
16:30 & 19\degree\:36' & 199\degree\:56' & \text{Begins} & \text{at} & \text{Sunrise} && -38\degree\:41' & 208\degree\:36' & \text{Begins} & \text{at} & \text{Sunrise} \\
16:45 & 24\degree\:45' & 195\degree\:24' & \text{Begins} & \text{at} & \text{Sunrise} && -38\degree\:24' & 204\degree\:48' & \text{Ends} & \text{at} & \text{Sunrise} \\
17:00 & 29\degree\:1' & 190\degree\:57' & \text{Begins} & \text{at} & \text{Sunrise} && -35\degree\:29' & 200\degree\:27' & \text{Ends} & \text{at} & \text{Sunrise} \\
17:15 & 32\degree\:15' & 186\degree\:37' & \text{Begins} & \text{at} & \text{Sunrise} && -28\degree\:45' & 195\degree\:28' & \text{Ends} & \text{at} & \text{Sunrise} \\
17:30 & 33\degree\:29' & 182\degree\:38' & \text{Ends} & \text{at} & \text{Sunrise} && -15\degree\:34' & 189\degree\:41' & \text{Ends} & \text{at} & \text{Sunrise} \\
17:44:59 & 19\degree\:43' & 181\degree\:10' & \text{Ends} & \text{at} & \text{Sunrise} && & & & & \\ \hline
\end{array}
}
```
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Rising and Setting Limits – Sunset Lobe}\\
\begin{array}{|c|c|c|ccc|c|c|c|ccc|}\hline \text{Time} & \text{Latitude} & \text{Longitude} & & & & & \text{Latitude} & \text{Longitude} & & & \\ \hline
18:49:15 & 74\degree\:16' & 15\degree\:20' & \text{Begins} & \text{at} & \text{Sunset} && & & & &\\
19:00 & 46\degree\:5' & 352\degree\:56' & \text{Begins} & \text{at} & \text{Sunset} && 82\degree\:30' & 69\degree\:48' & \text{Begins} & \text{at} & \text{Sunset} \\
19:15 & 30\degree\:7' & 345\degree\:43' & \text{Begins} & \text{at} & \text{Sunset} && 82\degree\:28' & 64\degree\:46' & \text{Ends} & \text{at} & \text{Sunset} \\
19:30 & 21\degree\:48' & 340\degree\:36' & \text{Begins} & \text{at} & \text{Sunset} && 81\degree\:39' & 41\degree\:11' & \text{Ends} & \text{at} & \text{Sunset} \\
19:45 & 17\degree\:50' & 336\degree\:16' & \text{Begins} & \text{at} & \text{Sunset} && 79\degree\:15' & 17\degree\:39' & \text{Ends} & \text{at} & \text{Sunset} \\
20:00 & 16\degree\:46' & 332\degree\:22' & \text{Begins} & \text{at} & \text{Sunset} && 75\degree\:20' & 0\degree\:14' & \text{Ends} & \text{at} & \text{Sunset} \\
20:15 & 18\degree\:1' & 328\degree\:47' & \text{Ends} & \text{at} & \text{Sunset} && 70\degree\:6' & 347\degree\:39' & \text{Ends} & \text{at} & \text{Sunset} \\
20:30 & 21\degree\:34' & 325\degree\:34' & \text{Ends} & \text{at} & \text{Sunset} && 63\degree\:19' & 337\degree\:46' & \text{Ends} & \text{at} & \text{Sunset} \\
20:45 & 28\degree\:49' & 323\degree\:0' & \text{Ends} & \text{at} & \text{Sunset} && 53\degree\:23' & 329\degree\:3' & \text{Ends} & \text{at} & \text{Sunset} \\
20:52:20 & 40\degree\:36' & 323\degree\:34' & \text{Ends} & \text{at} & \text{Sunset} && & & & & \\ \hline
\end{array}
}
```
Notice that the first and last points of each lobe are always the contacts.\
$\blacksquare$

Note that computing the rising and setting limits for the umbra (and therefore determining where on the Earth totality or annularity begins or ends at sunrise or sunset) is also possible. However, while theoretically possible, the area of totality on the horizon is so small on the Earth that it is of almost no importance. However, if in a worldbuilding scenario the Moon appeared larger in the sky and therefore the umbral shadow larger, this may be of significance and worth calculating. The method of calculation is identical to that of examples $9.5$ and $9.6$, simply change all the penumbral variables to umbral ones. (This involves calculating the umbral contacts $U_1$, $U_2$, $U_3$, and $U_4$: essentially repeating all of examples $9.5$ and $9.6$.) Therefore, we will not be calculating the rising and setting limits of the umbra here.

### Curve of Maximum Eclipse on the Horizon
(Continued in Part E...)
