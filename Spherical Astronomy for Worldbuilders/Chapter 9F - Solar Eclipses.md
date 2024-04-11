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
We need to find $\zeta$ to find $C$ and $B$. In order to do this, we first assume $\zeta = 0$ and find two values of $Q$ by equation $9.77$ and $9.78$. Then, equation $9.28*$ gives:
```math
\begin{align}
\xi &= x - (l - i\zeta)\sin(Q)\\
\eta_1 &= (y - (l - i\zeta)\cos(Q))/ \rho_1\tag{9.28*}\\
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
These are also the extremes of the limits of partiality. Thus the northern limit of partiality extends from $17:29:30$ to $19:05:23$, and the southern limit extends from $16:32:38$ to $20:02:15$. I will give the solution for the time $18:00$ in full.

For this time, we have:
```math
a'_1 = -0.00043531 \enspace\enspace\enspace b'_1 = -0.28178103 \enspace\enspace\enspace c'_1 =  0.51976556
```
and:
```math
x = -0.30856088 \enspace\enspace\enspace y = 0.22479055 \enspace\enspace\enspace i_1 =  0.00466835  \enspace\enspace\enspace l_1 = 0.53573027 
```

We first assume $\zeta = 0$. We calculate $B$ and $C$ by equation $9.77$:
```math
\begin{alignat}{2}
B &= -0.28178103 - (0.00466835^2 + 1) \cdot 0 \cdot 0.00025898 &&= -0.28178103\\
C &= 0.51976556 - (0.00466835^2 + 1) \cdot 0 \cdot 0.26187054 \cos(0.13019636) &&= 0.51976556
\end{alignat}
```
Now, equation $9.78$ gives the first approximate values of $Q$:
```math
\begin{align}
Q_1 &= 2\arctan\left(\frac{\sqrt{-(-0.00043531)^2+(-0.28178103)^2+0.51976556^2}-0.51976556}{-0.00043531 + (-0.28178103)}\right)\\
&= -0.49604542\\
Q_2 &= 2\arctan\left(\frac{-\sqrt{-(-0.00043531)^2+(-0.28178103)^2+0.51976556^2}-0.51976556}{-0.00043531 + (-0.28178103)}\right)\\
&= 2.64407467
\end{align}
```
Using $Q_1$ in equation $9.28*$ gives:
```math
\begin{align}
\xi &= -0.30856088 - (0.53573027 - 0.00466835 \cdot 0)\sin(-0.49604542)\\
&= -0.05357934 \\
\eta_1 &= (0.22479055 - (0.53573027 - 0.00466835 \cdot 0)\cos(-0.49604542))/ 0.99670381\\
&= -0.24718378  \\
\zeta_1 &= \sqrt{1 - (-0.05357934)^2 - (-0.24718378 )^2} \\
&= 0.96748614
\end{align}
```
Which then put into $9.27$ gives:
```math
\begin{align}
\zeta &= -0.99994358 \cdot -0.24718378 \sin(0.13062939 - 0.12976473) + 0.99994358 \cdot 0.96748614 \cos(0.13062939 - 0.12976473)\\
&= 0.96764491
\end{align}
```
This value substituted into equation $9.77$ gives:
```math
\begin{alignat}{2}
B &= -0.28178103 - (0.00466835^2 + 1) \cdot 0.96764491 \cdot 0.00025898 &&= -0.28203162\\
C &= 0.51976556 - (0.00466835^2 + 1) \cdot 0.96764491 \cdot 0.26187054 \cos(0.13019636) &&= 0.26850704
\end{alignat}
```
Now, equation $9.78$ gives the second approximate values of $Q$:
```math
\begin{align}
Q_1 &= 2\arctan\left(\frac{\sqrt{-(-0.00043531)^2+(-0.28203162)^2+0.26850704^2}-0.26850704}{-0.00043531 + (-0.28203162)}\right)\\
&= -0.80884143\\
\end{align}
```
Which in $9.28*$ gives:
```math
\begin{align}
\xi &= 0.07576525 \\
\eta_1 &= -0.14239483  \\
\zeta_1 &= 0.98690594
\end{align}
```
Which in $9.27$ gives a second approximate value of $\zeta$:
```math
\zeta = 0.98697301
```
The table of repetitions is given here:
```math
\begin{array}{ccc} \hline \text{Repetition} & \zeta \enspace (Q_1) & \zeta \enspace (Q_2) \\ \hline
1 & 0.96764491 & 0.44051669\\
2 & 0.98697301 & 0.42532847\\
3 & 0.98723346 & 0.42587744\\
4 & 0.98723688 & 0.4258576\\
5 & 0.98723692 & 0.42585832\\
6 & 0.98723692 & 0.42585829\\
7 & 0.98723692 & 0.42585829\\ \hline
\end{array}
```
Now that $\zeta$ has converged, we can continue:
```math
\begin{array}{r|c|c} \hline & \zeta \enspace (Q_1) & \zeta \enspace (Q_2) \\ \hline
\zeta & 0.98723692 & 0.42585829\\
B & -0.28203669 & -0.28189132\\
C & 0.26341978 & 0.40918726\\
Q & -0.81838782 & 2.53747552 \\
(l - i\zeta)\cos(Q) & 0.36296793 > 0& -0.43927193 < 0\\
 & \text{Southern} & \text{Northern} \\
\xi & 0.07918173 & -0.61174551\\
\eta_1 & -0.13863435 & 0.6662586   \\
\zeta_1 & 0.98717312 & 0.42645857\\
\phi_1 & -0.00886593 & 0.79824443 \\
\theta & 0.07926783 & -1.06848099\\
\phi & -0\degree\:30'\:35'' & 45\degree\:49'\:56''\\
\lambda & 274\degree\:38'\:26'' & 208\degree\:52'\:46''\\ \hline
\end{array}
```
In this manner the following table is computed:
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Limits of Partial Eclipse}\\
\begin{array}{|c|c|c|c|c|c|} \hline \text{Time} & \begin{matrix} \text{Northern} \\ \text{Latitude} \end{matrix} & \begin{matrix} \text{Northern} \\ \text{Longitude} \end{matrix} & & \begin{matrix} \text{Southern} \\ \text{Latitude} \end{matrix} & \begin{matrix} \text{Southern} \\ \text{Longitude} \end{matrix} \\ \hline
16:32:38 & & & & -38\degree\:48' &  207\degree\:58'\\
16:45 & & & & -25\degree\:56' &  247\degree\:3'\\
17:00 & & & & -18\degree\:59' &  256\degree\:43'\\
17:15 & & & & -13\degree\:23' &  262\degree\:49'\\
17:29:30 & 33\degree\:30' & 182\degree\:45' & & (1) & (1)\\
17:30 & (2) & (2) & & -8\degree\:36' &  267\degree\:23'\\
17:45 & 39\degree\:58' &  201\degree\:43' & & -4\degree\:19' &  271\degree\:12'\\
18:00 & 45\degree\:50 &  208\degree\:53' & & -0\degree\:31' &  274\degree\:38'\\
18:15 & 52\degree\:9' &  214\degree\:10' & & 2\degree\:55' &  277\degree\:57'\\
18:30 & 59\degree\:14' &  218\degree\:53' & & 6\degree\:2' &  281\degree\:19'\\
18:45 & 68\degree\:7' &  223\degree\:53' & & 8\degree\:52' &  284\degree\:56'\\
19:00 & 81\degree\:32' &  230\degree\:2' & & 11\degree\:28' &  288\degree\:59'\\
19:05:23 & 82\degree\:31' & 72\degree\:9' & & (1) & (1)\\
19:15 & & & & 13\degree\:48' &  293\degree\:46'\\
19:30 & & & & 15\degree\:51' &  299\degree\:50'\\
19:45 & & & & 17\degree\:26' &  308\degree\:19'\\
20:00 & & & & (2) & (2) \\
20:02:15 & & & & 16\degree\:49' &  331\degree\:48'\\ \hline
\end{array}
}
```
$^1$ These points were not computed for the sake of brevity.\
$^2$ While these points should exist, our numbers produce impossible results. This is due to the fact that these points are very close to the edges of the curve and our derivatives are not good enough (recall that we took $15$ minute time steps for the derivatives). With a smaller time step, and thus more accurate derivatives, this problem should disappear.\
$\blacksquare$

### Limits of Centrality
The limits of centrality are obtained exactly like the limits of partiality: simply replace the penumbral variables $i_1$, $l_1$, $a_1'$, $b_1'$, $c_1'$ with the umbral variables $i_2$, $l_2$, $a_2'$, $b_2'$, $c_2'$.

The extremes of the limits can be obtained exactly as the extremes of the penumbral limits:
1. Compute the umbral contact $U_1$, $U_2$, $U_3$, $U_4$. (Redo example $9.5$ with umbral variables.)
2. Compute the rising / setting limits for the umbra, i.e. the curves of central eclipse beginning/ending on the horizon. (Redo example $9.6$ with umbral variables.)
3. Compute the times and locations on the rising / setting limtis where $P'$ flips sign. (Redo the first part of example $9.7$ with umbral variables.)

While this more rigorous method is recommended, and even necessary for worldbuilding cases where the umbral shadow is significantly large, for cases similar to our Earth, where the umbra is very small, we would find that the umbral external and internal contacts are only a few minutes apart ($U_1$ and $U_2$, or $U_3$ and $U_4$, are both only $2$ minutes apart for the case of the $\text{April, 8, }2024$ eclipse), and therefore our time step of $15$ minutes will not be able to capture any detail. While a smaller time step would resolve this issue, we have another workaround:

The extreme points lie on the rising / setting limits, and the extreme points lie on those limits at some time in between the external and internal contacts. Also, the time between the external and internal umbral contacts is so small, that the time between the extreme points at each lobe, which is even smaller, is absolutely tiny, to the point where they occur almost at the same instant (less than a minute apart for the case of the $\text{April, 8, }2024$ eclipse). In addition, the area covered by these rising / setting limits is also very small. We can therefore say that the points on the rising / setting limits at the time midway between the contacts are close enough to the true extreme points. The time midway between the umbral contacts is well approximated by the time of contact of the center of the shadow, which we have already calculated in example $9.9$. Thus, the points on the rising / setting limits at the time of central contact can be used as the extreme points of the limits of centrality.

#### Example 9.11
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the limits of totality of the solar eclipse of $\text{April 8, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We use the approximation for the extreme points. The times of central contact are $16:40:02$ and $19:54:28$. Using the elements at these times (interpolated in example $9.9$, not exactly at the contact times but should still be sufficiently accurate):
```math
\begin{array}{|c|c|c|c|c|c|c|c|}\hline t & d & \mu & x & y & i_2 & l_2 & \rho_1\\ \hline
16:41:00 & 0.12985038 & 1.21988483 & -0.99057474 & -0.13707257 & 0.00464516 & -0.01049008 & 0.99670351 \\
19:54:40 & 0.13069238 & 2.06956364 & 0.66914899 & 0.74302244 & 0.00464499 & -0.01031513 & 0.99670424 \\ \hline
t & d_1 & \rho_2 & d_2 & d' & \mu' & x' & y' \\ \hline
16:41:00 & 0.13028229 & 0.99994388 & 0.12941987 & 0.00025897 & 0.26187053 & 0.5114177 & 0.27144902 \\
19:54:40 & 0.13112703 & 0.99994315 & 0.13025915 & 0.00025898 & 0.26187148 & 0.51157069 & 0.27105629\\ \hline
\end{array}
```
we find, via the method of example $9.5$ but swapping out $l_1$ for $l_2$:
```math
\begin{array}{cccc}\hline \text{Point} & \text{Time} & \text{Latitude} & \text{Longitude} \\ \hline
\text{Sunrise Northern Extreme} & 16:40:00 & -7\degree\:15'\:47'' & 201\degree\:3'\:33'' \\
\text{Sunrise Southern Extreme} & 16:40:00 & -8\degree\:27'\:45'' & 201\degree\:13'\:8'' \\
\text{Sunset Northern Extreme} & 19:54:40 & 48\degree\:12'\:38'' & 339\degree\:52'\:46'' \\
\text{Sunset Southern Extreme} & 19:54:40 & 47\degree\:4'\:2'' & 339\degree\:32'\:42'' \\ \hline
\end{array}
```
Which are sufficiently accurate. For a more accurate computation, the rigorous method, the one we followed for the penumbra, must be used.

Now, we find the limits just like in example $9.10$, simply swapping out the penumbral variables for umbral ones, and obtain the table below.
```math
\displaylines{
\text{Solar Eclipse of April 8, 2024 – Limits of Total Eclipse}\\
\begin{array}{|c|c|c|c|c|c|} \hline \text{Time} & \begin{matrix} \text{Northern} \\ \text{Latitude} \end{matrix} & \begin{matrix} \text{Northern} \\ \text{Longitude} \end{matrix} & & \begin{matrix} \text{Southern} \\ \text{Latitude} \end{matrix} & \begin{matrix} \text{Southern} \\ \text{Longitude} \end{matrix} \\ \hline
16:41:00 & -7\degree\:16' & 201\degree\:4' & & -8\degree\:28' & 201\degree\:13'\\
16:45 & -3\degree\:55' & 215\degree\:45' & & -4\degree\:45' & 218\degree\:5'\\
17:00 & 2\degree\:6' & 229\degree\:7' & & 1\degree\:6' & 230\degree\:50'\\
17:15 & 7\degree\:9' & 236\degree\:23' & & 6\degree\:6' & 237\degree\:59'\\
17:30 & 11\degree\:51' & 241\degree\:41' & & 10\degree\:46' & 243\degree\:15'\\
17:45 & 16\degree\:22' & 246\degree\:7' & & 15\degree\:15' & 247\degree\:39'\\
18:00 & 20\degree\:46' & 250\degree\:10' & & 19\degree\:36' & 251\degree\:40'\\
18:15 & 25\degree\:6' & 254\degree\:10' & & 23\degree\:43' & 255\degree\:37'\\
18:30 & 29\degree\:24' & 258\degree\:27' & & 28\degree\:7' & 259\degree\:50'\\
18:45 & 33\degree\:41' & 263\degree\:21' & & 32\degree\:19' & 264\degree\:37'\\
19:00 & 37\degree\:57' & 269\degree\:18' & & 36\degree\:29' & 270\degree\:23'\\
19:15 & 42\degree\:8' & 277\degree\:5' & & 40\degree\:34' & 277\degree\:51'\\
19:30 & 46\degree\:7' & 288\degree\:8' & & 44\degree\:29' & 288\degree\:19'\\
19:45 & 49\degree\:21' & 306\degree\:39' & & 47\degree\:45' & 305\degree\:31'\\
19:54:40 & 48\degree\:13' & 339\degree\:53' & & 47\degree\:4' & 339\degree\:33'\\ \hline
\end{array}
}
```
$\blacksquare$

The points we have computed in examples $9.5$ through $9.11$ can be plotted on a map and curves can be drawn through them:
```math
\begin{array}{c} \\ \hline
\text{The Total Solar Eclipse of April 8, 2024} \\ \hline
\end{array}
```

<p align="center">
  <img width="500" src="https://github.com/CitruzSquared/essays/assets/23460281/5c0f1022-9ec2-426b-a51e-20b86a9004aa"> <br/>
</p>

```math
\begin{array}{c} \hline
\text{Greatest Eclipse at 18:17 UTC} \enspace\enspace\enspace\enspace \text{Gamma } = 0.3431\\
\text{Duration of Totality at Greatest Eclipse } = \text{ 4m 30.2s} \\ \hline
\end{array}
```

### A Note on Time Steps
So far in this whole chapter, the prediction of the path of the solar eclipse was made more difficult because time step we were working with was too large.

If we take small enough time steps, which is not difficult to do on a computer that automatically calculates the positions of the Sun and Moon at any arbitrary time, the calculation of all the extreme points of the various curves is rendered unnecessary. For example, in example $9.6$, the extreme points of the rising / setting limits are simply the first and last points that produce possible values of $\epsilon$. In example $9.7$ and $9.10$, the extreme points of the curves of maximum eclipse on the horizon and the curves of the limits of partial eclipse are determined by the first and last points $m\sin(M - Q)/p$ produce possible values of $\psi$, and the first and last points $\Delta$ is less than $|l|$. In example $9.9$, the central contacts are the first and last points that produce real values of $\zeta_1$. 

Thus, if we take time steps of for example $1$ second, not only do we have more accurate derivatives, we also, if we simply ignore times that give impossible solutions for points, automatically have the times of the various contacts and extreme points of curves accurate to the nearest second as those points are the first and last times that give possible solutions. The time of greatest eclipse can also be found to the nearest second by simply computing $m = \sqrt{x^2 + y^2}$ at each time and seeing when it is at minimum.

Therefore, the method of calculation of solar eclipse phenomena when taking small time steps is as follows:
1. Find a specific New Moon that produces a solar eclipse.
2. Calculate the Besselian elements at the time of New Moon.
3. Using this, calculate the first and last external penumbral contacts. This is necessary because we need the boundary times of the whole eclipse.
4. Now, beginning from the first external penumbral contact, calculate the elements at that time and calculate all the curves via methods detailed previously in this chapter, simply ignoring impossible solutions.
5. Increment by a small time step, recalculate the elements, and calculate new points until the last external penumbral contact is reached.

### Local Predictions
For local predictions, i.e. predictions for a given place, three things are of note:
1. The time of partial eclipse beginning and ending (a.k.a. the contact times of the penumbra).
2. The time of central (total/annular) eclipse beginning and ending (a.k.a. the contact times of the umbra).
3. The maximum magnitude.
4. The duration of centrality.

The first two can be obtained via successive approximation, using methods similar to example $9.5$: 
1. Calculate $\xi$, $\eta$, $\xi'$, and $\eta'$ at $T_0$ using equations $9.6$ and $9.40$.
2. Approximate $(x - \xi)$ and $(y - \eta)$ as linear, and estimate for the times when $\Delta^2 - L^2 = 0$.
3. Repeat the approximations until a satisfactory answer is reached.

The maximum magnitude can be also calculated via successive approximation by approximating for the time when $P' = 0$ and calculating the magnitude by equation $9.71$.

However, when taking small time steps, simply keeping track of $\Delta$, $L$, and $P'$ give the times of contact and maximum magnitude naturally.  The duration of centrality is simply the difference between the two umbral contacts.

### Transits and Occultations
Transits of inner planets across the Sun or occultations of stars and planets by the Moon can be modeled as solar eclipses. For transits, simply replace the Moon with the planet. For lunar occultations, simply replace the Sun with the star or planet.

For the special case of the lunar occultations of stars, because stars are infinitely far away and have zero parallax and zero angular diameter, star rays can be modeled as parallel and therefore the shadow cone becomes a shadow cylinder: $f = 0$, and so $i = \tan(f) = 0$, and so $l = L = \text{Radius of the Moon}$ (the penumbra will not exist, the star will either be fully obstructed or not), and the coordinates $z$ and $\zeta$ will not need to be used. The position of the Sun must also be considered as it is generally useless to predict lunar occultations of stars during daylight.
