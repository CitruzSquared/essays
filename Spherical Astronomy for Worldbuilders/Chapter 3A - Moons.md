## III. Moons
<p align="center">
  <img width="400" src="https://github.com/CitruzSquared/essays/assets/23460281/b034af38-ac10-45b7-8e03-8736af53e270"><br/>
   Lunar Apsidal Precession.
</p>

In the previous chapter, we studied the motion of the planets, which was modeled fairly well by Keplerian motion. Moons behave mostly in the same way, but we need to account for a few extra things due to their small size and relatively small semi-major axis lengths. In particular, [**orbital precession**](https://en.wikipedia.org/wiki/Orbital_precession), the change in the orbital elements over time caused by gravitational perturbation, cannot be ignored for moons in the same way we have ignored them for the planets. 

The two precessions we must account for are:
1. [Nodal Precession](https://en.wikipedia.org/wiki/Nodal_precession)
   - The change in the location of the node line over time, which is in the opposite direction of the orbit. Hence it is also called the *node regression*.
2. [Apsidal Precession](https://en.wikipedia.org/wiki/Apsidal_precession)
   - The change in the location of the periapsis over time, which is usually in the direction of the orbit. Hence it is also called the *periapsis advance*.

While the orbits of the planets also precess, the rate of precession is so slow (in the order of a few arcminutes of change per century) that they can be ignored. For moons, these rates are much faster. Let us now learn how to calculate these precession rates.

### Change in Ω and ω
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/252eaf18-8ac0-4aba-84df-65d6bb087387" width="350"/> This image depicts the orbit of a moon $Q$ around a planet $O$. We have projected the periapsis of the orbit of the object $Q$ (the point $P$) down to the reference plane, and thus have created a new point $P'$. As we have discussed previously, the angle $NOP$ is known as the argument of periapsis and is denoted $\omega$. The angle $AOP'$ (measured in the direction of the orbit) is known as the [*longitude of periapsis*](https://en.wikipedia.org/wiki/Longitude_of_the_periapsis) and is denoted $\varpi$ (a variant of the letter $\pi$).

When discussing apsidal precession, it is usually the precession of the **longitude** of periapsis in question, not the *argument* of periapsis. However, the nodal precession simply refers to the longitude of the ascending node. \
These precession rates are not constant in reality but they can be approximated as being more or less constant. Thus, if the nodes precess at a rate $\dot\Omega$, the longitude of the ascending node at time $t$ is given as:
```math
\begin{align}
\Omega &= \Omega_0 + \int_{t_0}^{t} \dot\Omega dt\\
&=\Omega_0 + (t - t_0)\dot\Omega \tag{3.1}
\end{align}
```
Where $\Omega_0$ is the longitude of the ascending node at time $t = 0$.\
If the apses precess at a rate $\dot\varpi$, the longitude of periapsis at time $t$ is given as:
```math
\begin{align}
\varpi &= \varpi_0 + \int_{t_0}^{t} \dot\varpi dt\\
&=\omega_0 + (t - t_0)\dot\varpi \tag{3.2}
\end{align}
```
Where $\varpi_0$ is the longitude of the periapsis at time $t = 0$.\
These make sense. However, in our ephemeris calculations, we have $\omega$ and not $\varpi$. Thus we need a way of calculating $\varpi$ from $\omega$ and back. The algorithm below shows how to correctly account for the apsidal precession.

**Step 1. Calculate $\varpi_0$ from $\Omega_0$ and $\omega_0$.**

Notice that $\varpi_0 = \Omega_0 + \Lambda_0$, where $\Lambda_0 = NOP'$. $\Lambda$ then is calculated as follows:

Notice that the periapsis point $P$ is on the orbit and is an angular distance of $\omega$ away from the ascending node $N$. If we define a coordinate frame where $O$ is the origin, the $xy$-plane is the orbital plane, and the $x$-axis points towards $N$, then the spherical coordinates of $P$ are given by $(\omega_0, 0)$.

In a similar coordinate frame, where $O$ is the origin, the $x$-axis point towards $N$, but the $xy$-plane is the reference plane, the coordinates of $P$ are given by $(\Lambda_0, p_0)$ where $p_0$ is the angular distance $P'OP$ at time $t = 0$.

To transform from the first set of coordinates to the second set of coordinates, we use a rotation matrix, and thus:
```math
\begin{bmatrix}
\cos(p_0)\cos(\Lambda_0) \\
\cos(p_0)\sin(\Lambda_0) \\
\sin(p_0)
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(i) & -\sin(i) \\
0 & \sin(i) & cos(i)
\end{bmatrix}
\begin{bmatrix}
\cos(0)\cos(\omega_0) \\
\cos(0)\sin(\omega_0) \\
\sin(0)
\end{bmatrix}
```
We only care about $\Lambda$, so expanding out the terms for $\Lambda$:
```math
\begin{align}
\cos(p_0)\cos(\Lambda_0) &= \cos(0)\cos(\omega_0) = \cos(\omega_0) \\
\cos(p_0)\sin(\Lambda_0) &= \cos(0)\sin(\omega_0)\cos(i) - \sin(0)\sin(i) = \sin(\omega_0) \cos(i)
\end{align}
```
Thus:
```math
\Lambda_0 = \arctan(\sin(\omega_0) \cos(i), \cos(\omega_0))
```
And so finally:
```math
\varpi_0 = \Omega_0 + \arctan(\sin(\omega_0) \cos(i), \cos(\omega_0)) \tag{3.3}
```
**Step 2. Add the precessions**

We use equations $3.1$ and $3.2$:
```math
\begin{align}
\Omega &= \Omega_0 + (t - t_0)\dot\Omega \\
\varpi &= \varpi_0 + (t - t_0)\dot\varpi
\end{align}
```
**Step 3. Calculate the new $\omega$.**

We reverse Step 1.\
First we find the new $\Lambda$:
```math
\Lambda = \varpi - \Omega
```
In step 1, we found out that $\Lambda$ was given by
```math
\begin{align}
\Lambda &= \arctan(\sin(\omega) \cos(i), \cos(\omega)) \\
\therefore \tan(\Lambda) &= \frac{\sin(\omega)\cos(i)}{\cos(\omega)} \\
\therefore \frac{\tan(\Lambda)}{\cos(i)} &= \frac{\sin(\omega)}{\cos(\omega)}
\end{align}
```
This can be expressed as:
```math
\begin{cases}
\frac{\sin(\Lambda)}{\cos(i)} = \sin(\omega)\\
\cos(\Lambda) = \cos(\omega)
\end{cases}
```
Thus
```math
\omega = \arctan\left(\frac{\sin(\Lambda)}{\cos(i)}, \cos(\Lambda)\right)
```
And so finally:
```math
\omega = \arctan\left(\frac{\sin(\varpi - \Omega)}{\cos(i)}, \cos(\varpi - \Omega)\right).\tag{3.4}
```
We can now use the new $\Omega$ and $\omega$ in equation $2.26$ to calculate the coordinates of the moon.

Note that if $i$ is very small, then $\cos(i) \approx 1$ and equations $3.3$ and $3.4$ simplify to:
```math
\begin{align}
\varpi_0 &\approx \Omega_0 + \omega_0 \tag{3.5}\\
\omega &\approx \varpi - \Omega \tag{3.6}
\end{align}
```

#### Example 3.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Moon has an inclination value of $5.14\degree$, and that the Moon's precession values are: <br/>
$\dot\Omega = -1\text{ rev}/6793 \text{ dy}$ and $\dot\varpi = 1\text{ rev}/3233 \text{ dy}$. <br/>  
Given that on $\text{January 1, } 2020$, $\Omega = 98\degree\:8'\:24''$ and $\omega = 81\degree\:39'$, calcaulate $\Omega$ and $\omega$ on $\text{January 1, } 2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We follow the algorithm above.\
We first calculate $\varpi_0$ by equation $3.3$:
```math
\begin{align}
\varpi_0 &= \Omega_0 + \arctan(\sin(\omega_0) \cos(i), \cos(\omega_0))\\
&= 98\degree\:8'\:24'' + \arctan(\sin(81\degree\:39') \cos(5.14\degree), \cos(81\degree\:39') \\
&= 179\degree\:45'\:24.35''
\end{align}
```
We now use equations $3.1$ and $3.2$, where $(t - t_0) = 1461\text{ dy}$:
```math
\begin{align}
\Omega &= \Omega_0 + (t - t_0)\dot\Omega \\
&= 98\degree\:8'\:24'' + 1461\cdot\frac{-360\degree}{6793}\\
&= 20\degree\:42'\:47.65''\\
\varpi &= \varpi_0 + (t - t_0)\dot\varpi\\
&= 179\degree\:45'\:24.35'' + 1461\cdot\frac{360\degree}{3233}\\
&= 342\degree\:26'\:29.68''
\end{align}
```
We now find the new $\omega$ by equation $3.4$.
```math
\begin{align}
\omega &= \arctan\left(\frac{\sin(\varpi - \Omega)}{\cos(i)}, \cos(\varpi - \Omega)\right) \\
&= \arctan\left(\frac{\sin(342\degree\:26'\:29.68'' - 20\degree\:42'\:47.65'')}{\cos(5.14\degree)}, \cos(342\degree\:26'\:29.68'' - 20\degree\:42'\:47.65'')\right)\\
&= 321\degree\:36'\:57.69''
\end{align}
```
Thus, on $\text{January 1, } 2024$:
```math
\begin{align}
\Omega &= 20\degree\:42'\:47.65'\\
\omega &= 321\degree\:36'\:57.69''
\end{align}
```
Compared to the true values:
```math
\begin{align}
\Omega &= 20\degree\:45'\\
\omega &= 322\degree\:46'\:12''
\end{align}
```
We came close considering we assumed precession is uniform.\
$\blacksquare$

Furthermore, we can calculate the rate of change of $\omega$ $(\dot\omega)$ from $\dot\Omega$ and $\dot\varpi$:\
First, let's simplify the expression for $\omega$ (this expression introduces some ambiguities but it's okay for this purpose):
```math
\omega = \arctan\left(\frac{\tan(\Lambda)}{\cos(i)}\right)
```
Then,
```math
\dot\omega = \frac{\cos^2(i)}{\cos^2(i) + \tan^2(\Lambda)}\cdot\frac{\sec^2(\Lambda)}{\cos(i)}\cdot\dot\Lambda
```
But since $\Lambda = \varpi - \Omega$,
```math
\dot\omega = \frac{\cos(i)\sec^2(\varpi - \Omega)(\dot\varpi-\dot\Omega)}{\cos^2(i) + \tan^2(\varpi - \Omega)}. \tag{3.7}
```
Thus, if one wanted, they could now calculate the new $\omega$ by:
```math
\omega = \omega_0 + \int_{t_0}^{t} \dot\omega dt \tag{3.8}
```
But this is not recommended because $\dot\omega$ is a very complex function, unless in cases such as:\
If $i$ is very small, then $\cos(i) \approx 1$, and:
```math
\begin{align}
\dot\omega &\approx \frac{\sec^2(\varpi - \Omega)(\dot\varpi-\dot\Omega)}{1 + \tan^2(\varpi - \Omega)}\\
&= \dot\varpi-\dot\Omega. \tag{3.9}
\end{align}
```
Which is consistent with equation $3.6$.\
In this case where $i$ is very small so $\cos(i) \approx 1$, $\dot\omega$ can be approximated as a constant and equation $3.8$ may be used.\
Similarly, $\dot\varpi$ can be calculated from $\dot\Omega$ and $\dot\omega$:
```math
\begin{align}
\Lambda &= \arctan(\tan(\omega) \cos(i))\\
\therefore\dot\Lambda &= \frac{1}{1 + \tan^2(\omega)\cos^2(i)}\cdot\cos(i)\sec^2(\omega)\cdot\dot\omega
\end{align}
```
But since $\varpi = \Lambda + \Omega$,
```math
\dot\varpi = \frac{\cos(i)\sec^2(\omega)\dot\omega}{1 + \tan^2(\omega)\cos^2(i)} + \dot\Omega. \tag{3.10}
```
Note that if $i$ is very small, then $\cos(i) \approx 1$, and:
```math
\begin{align}
\dot\varpi &\approx \frac{\sec^2(\omega)\dot\omega}{1 + \tan^2(\omega)} + \dot\Omega \\
&= \dot\omega + \dot\Omega. \tag{3.11}
\end{align}
```
Which is consistent with equation $3.9$.
### The Two Types of Moons
This table lists some of the Solar System's most prominent moons:
```math
\begin{array}{ccccc}\hline \text{Name} & \text{Primary} & a/R & M_M/M_P & T_M/T_P \\ \hline
\text{Moon} & \text{Earth} & 60.3 & 0.01229 & 0.07480 \\
\text{Io} & \text{Jupiter} & 6.03 & 0.00005 & 0.00041 \\
\text{Europa} & \text{Jupiter} & 9.60 & 0.00003 & 0.00082 \\
\text{Ganymede} & \text{Jupiter} & 15.3 & 0.00008 & 0.00165 \\
\text{Callisto} & \text{Jupiter} & 26.9 & 0.00006 & 0.00385 \\
\text{Titan} & \text{Saturn} & 21.0 & 0.00024 & 0.00148 \\
\text{Triton} & \text{Neptune} & 14.4 & 0.00021 & 0.00010 \\ \hline
\end{array}
```
where $a$ is the semi-major axis of the moon's orbit, $R$ is the primary planet's radius, $M_M$ and $M_P$ are the masses of the moon and planet respectively, and $T_M$ and $T_P$ are the orbital periods of the moon and planet respectively.

As is apparent, our Moon is vastly different from the other moons of our solar system: our moon has much larger $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios than other moons. Turns out, these ratios have profound effects on the precession of the orbits of the moons, and thus a distinction must be made between the two kinds of moons: "Luna-type" moons, and "Io-type" moons. (Note: this is not technical terminology.)

- "Luna-type" Moons:
  * Have large $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **orbit** of the primary planet. (That is, the inclination to the planetary ecliptic is fixed.)
  * Have most of their precession resulting from the **perturbation from the Sun**.
- "Io-type" Moons:
  * Have small $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **equator** of the primary planet. (That is, the inclination to the planetary equator is fixed.)
  * Have most of their precession resulting from the **oblateness of the primary**. (That is, the equatorial bulge of the primary planet.)
    
Thus it would be more appropriate to call these moons "Orbit-aligned moons" and "Equator-aligned moons" instead.

### Orbit-Aligned Moons
Orbit aligned moons have precessions resulting from the gravitational perturbation from the Sun. It can be shown that this perturbation mostly depends on the $T_M/T_P$ ratio, which we denote by $m$.\
Solving extremely complex equations of motion (that can be found [here](https://farside.ph.utexas.edu/teaching/celestial/Celestialhtml/node97.html)) leads to these two formulae (derivation too complex to write here):
```math
\begin{align}
\dot\Omega &= -\frac{3}{4}m + \frac{9}{32}m^2 + \frac{273}{128}m^3 + \frac{9797}{2048}m^4 + \frac{199273}{24576}m^5 + \frac{6657733}{589825}m^6\cdots \tag{3.12}\\ 
\\
\dot\varpi &= \frac{3}{4}m + \frac{225}{32}m^2 + \frac{4071}{128}m^3 + \frac{265493}{2048}m^4 + \frac{12822631}{24576}m^5 + \frac{1273925965}{589824}m^6 + \frac{66702631253}{7077888}m^7 + \frac{29726828924189}{679477248}m^8 \cdots \tag{3.13}
\end{align}
```
These formulae are not exact as they ignore small terms involving $e_M^2$, $e_P^2$, $i_M^2$, and $a_M/a_P$ (not ignoring these would make the formulae unbearably complicated). Thus, for the formula to work best, these parameters for the Moon - Planet system **must be small**.

Equations $3.12$ and $3.13$ give results in units of $\text{rev}/T_P$.

Copyable version:
```
Nodal Precession = -3/4*m + 9/32*m^2 + 273/128*m^3 + 9797/2048*m^4 + 199273/24576*m^5 + 6657733/589825*m^6

Apsidal Precession = 3/4*m + 225/32*m^2 + 4071/128*m^3 + 265493/2048*m^4 + 12822631/24576*m^5 + 1273925965/589824*m^6 + 66702631253/077888*m^7 + 29726828924189/679477248*m^8
```

#### Example 3.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given that for the Moon and the Earth, <br/>
$T_M = 27.321 \text{ dy}$ and $T_P = 365.242 \text{ dy}$, <br/>
Calculate the periods of node regression and perigee advance for the Moon in $\text{dy}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

For the Moon and the Earth:
```math
\begin{align}
e_M^2 &= 0.0030\\
e_P^2 &= 0.0003\\
i_M^2 &= 0.0080 \text{ rad}^2\\
a_M/a_P &= 0.0026\\
\end{align}
```
Which are all very small, so equations $3.12$ and $3.13$ will work.\
We find that $m = 27.321/365.242 = 0.0748$. Thus, by equations $3.12$ and $3.13$:
```math
\begin{align}
\dot\Omega &= -0.0534631 \text{ rev}/\text{yr}\\
\dot\varpi &= 0.114575 \text{ rev}/\text{yr}\\
\end{align}
```
Thus,
```math
\begin{align}
\dot\Omega &= \frac{365.242\text{ dy}/\text{yr}}{-0.0534631\text{ rev}/\text{yr}} = -6831.7\text{ dy}/\text{rev}\\
\dot\varpi &= \frac{365.242\text{ dy}/\text{yr}}{0.114575\text{ rev}/\text{yr}} = 3187.8\text{ dy}/\text{rev}
\end{align}
```
These periods of $-6831.7 \text{ dy}$ and $3187.8\text{ dy}$ do not differ much from their true values of $-6793 \text{ dy}$ and $3233\text{ dy}$ (the discrepancy comes from ignoring terms involving $e_M^2$, $e_P^2$, $i^2$, and $a_M/a_P$, and from truncating the infinite formulae at six and eight terms), and they are called the *nodal precession period* and *apsidal precession period* respectively.\
$\blacksquare$

There are also more minor perturbations in the lunar orbit by the Sun, called the evection, variation, and the annual equation. Those can be read about [here](https://farside.ph.utexas.edu/teaching/celestial/Celestialhtml/node97.html) in detail.

### Equator-Aligned Moons
(Continued in Part B...)
