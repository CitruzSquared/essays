## Chapter 11. Eclipse Patterns
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
\text{Distance to the Moon } &= 384\:399 \text{ km}\\
\text{Distance to the Sun } &= 149\:598\:023 \text{ km}\\
\text{Radius of the Moon } &= 1737.4 \text{ km}\\
\text{Radius of the Sun } &= 696\:000 \text{ km}\\
\text{Equatorial Radius of the Earth } &= 6378.137 \text{ km}\\
\text{Orbital Period of the Moon } &= 27.32 \text{ dy}\\
\text{Orbital Period of the Earth } &= 365.25 \text{ dy}\\
\text{Lunar Orbital Inclination } &= 5.14\degree\\
\end{align}
```
We have:
```math
\begin{alignat}{2}
s &= 0.259\degree & \enspace\enspace\enspace s' &= 0.267\degree\\
\pi &= 0.951\degree & \enspace\enspace\enspace \pi' &= 0.00244\degree\\

\mu &= 0.549\degree/h & \enspace\enspace\enspace \sigma &= 0.0411\degree/h\\
q &= 13.358 & \enspace\enspace\enspace I' &= 5.553\degree\\
\end{alignat}
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

If the eclipse season is very close to being one synodic month, a more precise approach is required because the nodal precession of the Moon's orbit cannot be ignored. The more precise method is shown in example $11.3$.

Therefore we have that in order for two solar eclipses to occur one month apart, they must both be partial. This is exemplified by the partial solar eclipses of $\text{July 13, } 2018$ and $\text{August 11, } 2018$.

The eclipse season lengths are tabulated here for convenience.
```math
\begin{array}{cccc} \hline \text{Eclipse Type} & & & \text{Eclipse Season Length} \\ \hline
\text{Partial Solar} & & & 33.42\text{ dy}\\
\text{Central Solar} & & & 21.31\text{ dy}\\ 
\text{Partial Penumbral Lunar} & & & 33.51\text{ dy}\\
\text{Total Penumbral Lunar} & & & 21.78\text{ dy}\\
\text{Partial Lunar} & & & 21.42\text{ dy}\\
\text{Total Lunar} & & & 9.68\text{ dy}\\ \hline
\end{array}
```
$\blacksquare$

### Eclipse Years and Draconic Months
Because the lunar nodes precess (see chapter $3$ for more detail), it does not take the Sun and Moon one orbital period each to return to a node after leaving it. The time it takes for the Sun to return to the same node is known as an *eclipse year*, and the time it takes for the Moon to return to the same node is known as a *draconic month*. They are both calculable as:
```math
T = \frac{O T_{\dot\Omega}}{T_{\dot\Omega} \pm O}\tag{11.2}
```
Where $O$ is the orbital period of the Moon or the Sun, and $T_{\dot\Omega}$ is the nodal precession period of the Moon's orbit. The top sign is to be used if the node regresses, and the bottom sign if the node advances.
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

Because the nodes regress for our Moon, we use the top sign in equation $11.2$.
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
From the conditions, we know that for a total lunar eclipse to occur, $\beta$ must be at maximum $0.429\degree$, and therefore $\xi$ must be at maximum $0.429\degree\cot(5.14\degree) = 4.77\degree$. Similarly, $\xi$ must be at maximum $10.51\degree$ for a central solar eclipse. If we assume a total lunar eclipse occurred when the Sun was $4.77\degree$ to the west of the node, after one fortnight the Sun would be at $-4.77\degree + 15.34\degree = 10.57\degree$ east of the node, slightly too far for a central solar eclipse to occur. However, with slightly different values of maximum $\beta$ (remember, these numbers do not stay constant), it could well be possible. In fact, in $2032$, there will be a total lunar eclipse on April $25$, and an annular solar eclipse a fortnight later, on May $9$.\
$\blacksquare$

#### Example 11.4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the maximum number of eclipses that can occur in one year.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Because the solar eclipse season ($33.42\text{ dy}$) is longer than a synodic month, there could be two solar eclipses in one month. In between the two solar eclipses, there would be a lunar eclipse, for a total of three eclipses at maximum per eclipse season. (Similarly, there could also be two lunar eclipses and one solar eclipse in the middle).

Assume that at the beginning of the year, the Sun passed through a lunar node and an eclipse ocurred. A fortnight later another eclipse would occur. Half an eclipse year later, the Sun would be at the opposite lunar node, and another eclipse season would start, with a maximum of three eclipses. Because an eclipse year is shorter than a year, The Sun would begin another eclipse season before the end of the year, which could produce three more eclipses, for a total of eight. However, we must count the eclipses carefully. Because an eclipse year is $346.61/29.53 = 11.74$ months long, half an eclipse year is $5.78$ months long, which rounds up to $6$ months (remember, eclipses only occur at new or full moon, meaning they can only occur separated by units of $0.5$ months), and in this scenario we would have:
1. Eclipse at month $0$
2. Eclipse at month $0.5$
3. Eclipse at month $5.5$
4. Eclipse at month $6$
5. Eclipse at month $6.5$
6. Eclipse at month $11.5$
7. Eclipse at month $12$
8. Eclipse at month $12.5$ (!)
   
However, 12.5 months is $12.5 \cdot 29.53 = 369.13$ days, which is longer than a year, meaning there is no way for the eighth eclipse to fit in one year. Therefore the maximum number of eclipses that could occur is seven.

This is exemplified by the extraordinary year of $1982$:
```math
\begin{array}{ccc} \hline \text{Date} & & \text{Eclipse} \\ \hline
\text{January 9, } 1982 & & \text{Total Lunar Eclipse} \\
\text{January 25, } 1982 & & \text{Partial Solar Eclipse} \\
\text{June 21, } 1982 & & \text{Partial Solar Eclipse} \\
\text{July 6, } 1982 & & \text{Total Lunar Eclipse} \\
\text{July 20, } 1982 & & \text{Partial Solar Eclipse} \\
\text{December 15, } 1982 & & \text{Partial Solar Eclipse} \\
\text{December 30, } 1982 & & \text{Total Lunar Eclipse} \\ \hline
\end{array}
```

$\blacksquare$
### Periodicity of Eclipses and the Saros
Because eclipses occur when the Moon and Sun are at nodes, if we can determine a length of time where the Sun and Moon will end up at a node again after an eclipse occurs, we can determine that an eclipse will also occur on that date. These lengths of time are known as *eclipse cycles*.

#### Example 11.5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Using the more accurate values of: <br/>
$\text{Synodic Month } = 29.53059\text{ dy}$ and $\text{Eclipse Year } = 346.62008\text{ dy}$, <br/>
Determine the length of some eclipse cycles.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

An eclipse is followed by an eclipse of the same type (solar or lunar) only in units of synodic months. Therefore, we need to find the number of synodic months that would result in the Sun being at a node. This ensures the parameter $\xi$ is close enough for an eclipse to occur. Thus, we search for multiples of synodic months that are also multiples of eclipse years.

For example, $47$ synodic months is $47 \cdot 29.53059 = 1387.93773$ days, which is $1387.93773/346.62008 = 4.0042$ eclipse years, which has an error of $0.0042$ eclipse years off from a perfect multiple. This corresponds to a $\Delta \xi$ of $0.0042 \cdot 360\degree = 1.512\degree$. This means that every cycle, the distance of the Sun from a node changes only by $1.512\degree$, meaning favorable conditions for an eclipse are reproduced.

A list of periods with absolute $\Delta \xi$ less than $2\degree$ are listed here, computed via trial and error:
```math
\begin{array}{cccc} \hline \text{Syn. Months}& \text{Eclipse Years} & \text{Years} & \Delta\xi\\ \hline
47 & 4.0042 & 3.8 & 1.5137\degree\\
176 & 14.9945 & 14.23 & -1.9914\degree\\
223 & 18.9987 & 18.03 & -0.4777\degree\\
270 & 23.0029 & 21.83 & 1.036\degree\\
446 & 37.9973 & 36.06 & -0.9554\degree\\
493 & 42.0016 & 39.86 & 0.5583\degree\\
669 & 56.996 & 54.09 & -1.4331\degree\\ \hline
\end{array}
```
One can see that the eclipse cycle with a period of $223$ synodic months has a $\Delta\xi$ lower than the rest. This cycle is known as a *Saros* (plural *"Saroi"*) and is the standard eclipse cycle used today.

A Saros is special not only because it has a very small $\Delta\xi$ value per cycle, but because it is also an almost exact multiple of the anomalistic month (see chapter $3$ for more details; one Saros is $238.992$ anomalistic months), meaning the Moon is also at almost the same distance from the Earth after one Saros. Favorable conditions for the same kind of eclipse (total or annular) eclipse are reproduced. In addition, a Saros is also a near multiple of the solar year, having only $0.03$ years (or eleven days) of error per cycle. This means that the Earth is also nearly at the same point in its orbit after one Saros, so the axis of the Earth is tilted in the same way. This means that eclipses separated by one Saros will not only be of similar type and duration, but also trace similar paths on the ground.

This is exemplified by this series of three solar eclipses, separated by one Saros each:
<p align="center">
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/7b65d51c-c22f-46aa-a1ab-8fd53728e8a8"> 
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/303ca1c4-020b-4de7-bff8-e29321cc0abd"> 
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/5739cb4d-5ffb-4a82-a521-bfe90a0c6fca"> <br/>
   Because a Saros is $223$ months $=$ $6585.324$ days, the Earth rotates by $0.324$ of a full turn (about $120\degree$) between each eclipse in a Saros. This causes eclipses separated by one saros to occur in places separated by about $120\degree$ in longitude. <br/> A chain of eclipses separated by a Saros each is called a <i>Saros series</i>. The above shows three members in the solar Saros series number $139$. <br/>
   There are many Saros series active at the same time at any given time.
</p>

For comparison, a cycle called an *Utting Cycle* exists, with an even smaller $\Delta \xi$ than a Saros:
```math
\begin{array}{cccc} \hline \text{Syn. Months} & \text{Eclipse Years} &  \text{Anom. Months}& \text{Years} & \Delta\xi\\ \hline
3803 & 323.9998 & 4075.7274 & 307.47 & -0.0749\degree \\ \hline
\end{array}
```
However, because it is not a near multiple of an anomalistic month, and because it is not as close of a multiple of a year, the characteristics and paths of the eclipses separated by an Utting Cycle each are not similar.

<p align="center">
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/c21614a7-790e-4616-9104-a2fcf5ad08d2"> 
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/303ca1c4-020b-4de7-bff8-e29321cc0abd"> 
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/d44b4480-3153-4e4a-b6b7-c54d7d2f13cf"> <br/>
</p>  

However, because two Utting cycles are $307.47 \cdot 2 = 614.94$ years, which is a near multiple of a year, every two Utting cycles there will be an eclipse with a similar shaped path. (However, because the anomalistic month still does not match, the duration and type of eclipse will not match.)

$\blacksquare$

Despite the $\Delta\xi$ error for Saros cycles being very small, it still exists and therefore Saros series die out eventually.
#### Example 11.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the length and number of members in a solar Saros series.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We determined in example $11.1$ that for a solar eclipse, the maximum $\xi$ is $16.476\degree$ and for a central solar eclipse, the maximum $\xi$ is $10.506\degree$. Because each Saros period has a $\Delta\xi$ of $-0.4777\degree$, the number of members is:
```math
\text{Num. Members } = \frac{2\cdot 16.476}{|-0.4777|} + 2 = 71
```
And of these, 
```math
\text{Num. Central Members } = \frac{2\cdot 10.506}{|-0.4777|} + 2 = 46
```
are central eclipses. This means that on average, we should expect solar saros series to consist of $12$ (or $13$) partial eclipses followed by $45$ central eclipses followed by $13$ (or $12$) partial eclipses. This is a crude approximation however, as it ignores the variation in all variables, and every saros series is quite different from each other. (In reality, most Saros series have about $70$ to $73$ members (but can range from $69$ to $87$), and the number of central eclipses in each vary significantly, ranging from $39$ to $59$, with $43$ being most common.)

In addition, since there are about $69$ members in a Saros series, every Saros series lasts about
```math
(71 - 1)\cdot223\text{ mo }\cdot29.53059 \frac{\text{ dy }}{\text{ mo }}\cdot\frac{1\text{ yr}}{365.25\text{ dy}} = 1262\text{ years}
```
In reality, Saros series take about $1250$ to $1300$ years from start to finish.

An example of a full solar Saros series (Solar Saros $139$) is shown below:
<p align="center">
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/d71c3bce-4f25-4675-9fdb-b7627b4b584c"> <br/>
   Solar Saros $139$ has $71$ members, $7$ partial eclipses followed by $55$ central eclipses followed by $9$ partial eclipses, and lasts for $1262$ years.
</p>

And for completion, an example of a full lunar Saros series (Lunar Saros $118$) is shown below:
<p align="center">
  <img width="300" src="https://github.com/CitruzSquared/essays/assets/23460281/2c6256f9-85b6-4634-b151-1bd2ecd80e90"> <br/>
   Lunar Saros $118$ has $73$ members, $9$ penumbral eclipses followed by $7$ partial eclipses followed by $28$ total eclipses followed by $8$ partial eclipses followed by $21$ penumbral eclipses, and lasts for $1298$ years.
</p>

$\blacksquare$

The factors that influence the characteristics of eclipse cycles can be summarized as follows:
1. Small $\Delta \xi$ : Many members and longevity of series.
2. Multiple of anomalistic month: Members have similar type and duration.
3. Multiple of solar year: Members have similar shaped paths. (However, this is not enough, $235$ synodic months is almost exactly $19$ solar years ($18.9998$ years to be exact), a cycle known as the *Metonic Cycle*, but does not result in eclipses with a similar path due to its extremely large $\Delta \xi$ of $7.5683 \degree$.)
