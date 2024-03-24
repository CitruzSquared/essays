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
