## Chapter 11. Eclipse Cycles
This chapter will discuss when eclipses can occur and the patterns between them.

### Eclipse Seasons
Because eclipses only occur when the Moon is near the nodes of the orbit of the Moon, the Sun must be also near the nodes for an eclipse to occur. For solar eclipses, the Sun must be at the same node as the Moon, and for lunar eclipses, the Sun must be at the opposite node as the Moon.

Recall the conditions for eclipse: equations $9.3$, $10.2$ and $10.3$.
```math
\begin{array}{cccc} \hline \text{Eclipse Type} & & & \text{Condition} \\ \hline
\text{Partial Solar} & & & \beta < (s + s' + \pi - \pi')\sec(I')\\
\text{Central Solar} & & & \beta < (s - s' + \pi - \pi')\sec(I')\\ 
\text{Partial Penumbral Lunar} & & & \beta < (s + s' + \pi + \pi')\sec(I')\\
\text{Total Penumbral Lunar} & & & \beta < (-s + s' + \pi + \pi')\sec(I')\\
\text{Partial Lunar} & & & \beta < (s - s' + \pi + \pi')\sec(I')\\
\text{Total Lunar} & & & \beta < (-s - s' + \pi + \pi')\sec(I')\\ \hline
\end{array}
```
The duration of time that the Sun is near enough to a lunar node for these conditions to be met at conjunction is known as an *eclipse season*. These eclipse seasons vary in length due to the fact that $s$, $s'$, $\pi$, $\pi'$, and $I'$ are not constant values, but we can consider their average values, as in the following example.
#### Example 11.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Using the average values of $s$, $s'$, $\pi$, $\pi'$, and $I'$, Determine if two solar eclipses can occur one month apart. 
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Using:
```math
\begin{align}
\text{Distance to the Moon } = 384\:399 \text{ km}\\
\text{Distance to the Sun } = 149\:598\:023 \text{ km}\\
\text{Radius of the Moon } = 1737.4 \text{ km}\\
\text{Radius of the Sun } = 696\:000 \text{ km}\\
\text{Equatorial Radius of the Earth } = 6378.137 \text{ km}\\
\text{Orbital Period of the Moon } = 27.32 \text{ dy}\\
\text{Orbital Period of the Earth } = 365.25 \text{ dy}\\
\text{Lunar Orbital Inclination } = 5.14\degree\\
\end{align}
```
We have:
```math
\begin{align}
s &= 0.259\degree\\
s' &= 0.267\degree\\
\pi &= 0.951\degree\\
\pi' &= 0.00244\degree\\
\sigma &= 0.0411\degree/h\\
\mu &= 0.549\degree/h\\
q &= 13.358\\
I' &= 5.553\degree\\
\end{align}
```
Using all these values, we have for the conditions:
```math
\begin{array}{cccc} \hline \text{Eclipse Type} & & & \text{Condition} \\ \hline
\text{Partial Solar} & & & \beta < 1.482\degree\\
\text{Central Solar} & & & \beta < 0.945\degree\\ 
\text{Partial Penumbral Lunar} & & & \beta < 1.486\degree\\
\text{Total Penumbral Lunar} & & & \beta < 0.966\degree\\
\text{Partial Lunar} & & & \beta < 0.950\degree\\
\text{Total Lunar} & & & \beta < 0.429\degree\\ \hline
\end{array}
```
Where only the absolute value of $\beta$ matters.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/8cd33362-d85e-4282-995b-f62452cfa751" width="250"/> Consider this diagram, showing the region near the lunar node $N$, where $S$ and $M$ are the positions of the Sun and Moon respectively at the moment of conjunction. The distance $SM$ is $\beta$. It is evident that:
```math
SN = \beta \cot(I) \tag{11.1}
```
And therefore, for solar eclipses, since the maximum $\beta$ is $1.482\degree$, the maximum possible $SN$ is $1.482\degree\cot(5.14\degree) = 16.476\degree$, and since the Sun's longitude changes by $0.0411\degree/h = 0.986\degree/\text{dy}$, we have that it takes the Sun $16.476/0.986 = 16.71 \text{ dy}$ to traverse this distance.

Since  the triangle can be mirrored on the other side, we have that there is a $16.71 \cdot 2 = 33.42\text{ dy}$ period where solar eclipses are possible. Since the synodic month is only $29.53\text{ dy}$ long (see example $4.3$), it is indeed possible for two solar eclipses to occur one month apart if one occurs at the beginning of the season and the other at the end of the season. Let us now discuss the nature of these eclipses.

If we do the same analysis with central solar eclipses, we have maximum $\beta = 0.945\degree$ and thus $SN = 10.506\degree$, and thus the Sun would take $10.655\text{ dy}$ to traverse that distance, and thus there is only a $10.655 \cdot 2 = 21.31\text{ dy}$ period where central solar eclipses are possible. Since this is shorter than one month, two central eclipses of the Sun cannot occur one month apart.

If we consider the length of time $16.71\text{ dy} + 10.655\text{ dy} = 27.365\text{ dy}$, we see that this too is shorter than a synodic month, and therefore a central solar eclipse and a partial solar eclipse cannot occur one month apart.

Therefore we have that in order for two solar eclipses to occur one month apart, they must both be partial. This is exemplified by the partial solar eclipses of $\text{July 13, } 2018$ and $\text{August 11, } 2018$.

The eclipse season lengths are tabulated here for convenience.
```math
\begin{array}{cccc} \hline \text{Eclipse Type} & & & \text{Eclipse Season Length} \\ \hline
\text{Partial Solar} & & & 33.42\text{ dy}\\
\text{Central Solar} & & & 22.31\text{ dy}\\ 
\text{Partial Penumbral Lunar} & & & 33.51\text{ dy}\\
\text{Total Penumbral Lunar} & & & 21.78\text{ dy}\\
\text{Partial Lunar} & & & 21.42\text{ dy}\\
\text{Total Lunar} & & & 9.67\text{ dy}\\ \hline
\end{array}
```
$\blacksquare$

### Eclipse Years and Draconic Months
Because the lunar nodes precess (see chapter $3$), it does not take the Sun and Moon one orbital period each to return to a node after leaving it. The time it takes for the Sun to return to the same node is known as an *eclipse year*, and the time it takes for the Moon to return to the same node is known as a *draconic month*. They are both calculable as:
```math
T = \frac{O T_{\dot\Omega}}{T_{\dot\Omega} + O}\tag{11.2}
```
Where $O$ is the orbital period of the Moon or the Sun, and $T_{\dot\Omega}$ is the nodal precession period of the Moon's orbit.
#### Example 11.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Using $T_{\dot\Omega} = 6793\text{dy}$, Determine the length of the eclipse year and the draconic month.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We use equation $11.2$.
```math
\begin{alignat}{2}
EY &= \frac{365.25 \cdot 6793}{6793 + 365.25} &&= 346.61\text{ dy}\\
DM &= \frac{27.32 \cdot 6793}{6793 + 27.32} &&= 27.21\text{ dy}
\end{alignat}
```
$\blacksquare$

Because the Sun will make a whole circle relative to a lunar node in one eclipse year, we have that $SN$ in the previous diagram, which we will now denote as $\xi$, will change by $360\degree$ every eclipse year. 
#### Example 11.3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine if a central eclipse of the Sun can occur a fortnight after a total eclipse of the Moon.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

In one fortnight, $\xi$ will change by
```math
\Delta \xi = \frac{360\degree}{346.61\text{ dy}} \cdot \frac{29.53\text{dy}}{2} = 15.34\degree
```
From the conditions, we know that for a total lunar eclipse to occur, $\beta$ must be at maximum $0.429\degree$, and therefore $\xi$ must be at maximum $0.429\degree\cot(5.14\degree) = 4.77\degree$. Similarly, $\xi$ must be at maximum $10.51\degree$ for a central solar eclipse. If we assume a total lunar eclipse occurred when the Sun was $4.77\degree$ to the west of the node, after one fortnight the Sun would be at $-4.77\degree + 15.34\degree = 10.57\degree$ east of the node, slightly too far for a central solar eclipse to occur. However, with slightly different values of maximum $\beta$ (remember, these numbers do not stay constant), it could well be possible.\
$\blacksquare$

### The Saros
