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

Evidently, $\sin(\psi) = m\sin(M - Q)/p$ cannot be greater than $1$ or less than $-1$. Here, the approximation $p = 1$ can be made and we can say that in order for points on this curve to exist, $m\sin(M - Q)$ must be less than $1$ and greater than $-1$. Also, the first equation in $9.67$ produces two values for $\psi$. the value of $\psi$ that produces $\Delta > l$ must be discarded.

To find determine at which times $m\sin(M - Q)/p$ produces mathematically possible outcomes for $\psi$, we must consider the extreme points of this curve. The extremes are the places where $\Delta = l$: i.e. the place experiences maximum eclipse when the place is on the boundary of the shadow of the Moon. This means that the Moon just barely grazes past the Sun in these locations and therefore are the edges of visibility of the eclipse.

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
We are not going to do a second approximation. Now we have to find the points on the rising and setting curve at these times.\
Using linearly interpolated values from the elements table in Chapter $\text{9Z}$:
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
\begin{array}{|c|c|c|c|c|c|c|c|c|}\hline \text{Point} & \text{Time} & \text{Latitude} & \text{Longitude} \\ \hline
\text{Sunrise Southern Extreme} & 16:32:38 & -38\degree\:48'\:13'' & 207\degree\:58'\:0'' \\
\text{Sunrise Northern Extreme} & 17:29:30 & 33\degree\:29'\:55'' & 182\degree\:45'\:29'' \\
\text{Sunset Northern Extreme} & 19:05:23 & 82\degree\:31'\:16'' & 72\degree\:8'\:45'' \\
\text{Sunset Southern Extreme} & 20:02:15 & 16\degree\:49'\:18'' & 331\degree\:48'\:27'' \\ \hline
\end{array}
```
Whether the point is northern or southern is determined by the value of $\cos(Q)$ (see equation $9.10$). The $Q$ for these points was found in the same way as example $9.6$: equation $9.60$. If $\cos(Q)$ is positive, the point is northern. If $\cos(Q)$ is negative, the point is southern. If no internal contacts exist, there will only be two extremes, one per lobe, (as the sunrise and sunset lobes are connected, the curve of maximum eclipse on the horizon will extend throughout the whole eclipse), and both will be northern or both will be southern.

Now we know the curve of maximum eclipse on the horizon extends only from $16:32:38$ to $17:29:30$ for the sunrise lobe, and from $19:05:23$ to $20:02:15$ in the sunset lobe. The points in between are calculated via the method outlined in this chapter: I will give the calculation for the point at time $16:45$ in full.

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
Now, we verify if $m\sin(M - Q) < 1$:
```math
\begin{array}{r|c|c}\hline  & Q_1 & Q_2 \\ \hline
m\sin(M - Q) & -0.87325361 & 0.87162496
\end{array}
```
Both values of $Q$ pass the test. We can now continue.\
We find $\psi$ and $\Delta$ with equation $9.67$:
```math
\begin{array}{r|c|c} 
m\sin(M - Q) = \sin(\psi) & -0.87325361 & 0.87162496\\
\psi_1 & -1.06184017 & 1.05850769\\
\pi - \psi_1 = \psi_2 & 4.20343283 & 2.08308496\\
\psi_1 \rightarrow \Delta_1 & -0.10119491 & -0.87990746 \\
\psi_2 \rightarrow \Delta_2 & 0.87333703 & 0.10043927 \\ \hline
\end{array}
```
Considering $l_1 = 0.53563338$ at this time, $\psi_2$ for $Q_2$ is the only $\psi$ value that produces a positive $\Delta$ value that is less than $l$. Thus, we continue with $\psi_2$ and $Q_2$.
```math
\begin{array}{r|c} \hline
\gamma = Q + \psi & 4.68408253 \\
\rho_1 & 0.99670449 \\
\gamma' & -1.59919632\\
p & 0.99999735 \\
m\sin(M - Q)/p = \sin(\psi) & 0.87162727 \\
\pi - \arcsin(\sin(\psi)) = \psi & 2.08308025 \\
\gamma = Q + \psi & 4.68407781\\
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
\begin{array}{|c|c|c|c|} \hline \text{Time} & \text{Latitude} & \text{Longitude} & \text{Obscuration} \\ \hline
16:32:38 & -38\degree\:48' & 207\degree\:58' \\
16:45 & -1\degree\:37' & 199\degree\:4' & \\
17:00 & 12\degree\:34' & 193\degree\:26' & \\
17:15 & 23\degree\:50' & 188\degree\:2' & \\
17:29:30 & 33\degree\:30' & 182\degree\:45' \\ \hline
19:05:23 & 82\degree\:31' & 72\degree\:9' \\
19:15 & 79\degree\:44' & 27\degree\:46' & \\
19:30 & 70\degree\:41' & 359\degree\:36' & \\
19:45 & 58\degree\:21' & 346\degree\:9' & \\
20:00 & 38\degree\:20' & 336\degree\:3' & \\ 
20:02:15 & 16\degree\:49'& 331\degree\:48' \\ \hline
\end{array}
}
```
