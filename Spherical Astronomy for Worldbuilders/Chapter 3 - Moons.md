## III. Moons
In the previous chapter, we studied the motion of the planets, which was modeled fairly well by Keplerian motion. Moons behave mostly in the same way, but we need to account for a few extra things due to their small size and relatively small semi-major axis lengths. In particular, [**orbital precession**](https://en.wikipedia.org/wiki/Orbital_precession), the change in the orbital elements over time caused by gravitational perturbation, cannot be ignored for moons in the same way we have ignored them for the planets. 

The two precessions we must account for are:
1. [Nodal Precession](https://en.wikipedia.org/wiki/Nodal_precession)
   - The change in the longitude of the ascending node $\Omega$ over time.
2. [Apsidal Precession](https://en.wikipedia.org/wiki/Apsidal_precession)
   - The change in the argument of periapsis $\omega$ over time.

While the orbits of the planets also precess, the rate of precession is so slow (in the order of a few arcminutes of change per century) that they can be ignored. For moons, these rates are much faster. Let us now learn how to calculate these precession rates.

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

As is apparent, our Moon is vastly different from the other moons of our solar system: our moon has a much larger $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios than other moons. Thus a distinction must be made between the two kinds of moons: "Io-type" moons, and "Luna-type" moons. (Note: this is not technical terminology.)

- "Io-type" Moons:
  * Have small $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **equator** of the primary planet. (That is, the inclination to the planetary equator is fixed.)
  * Have most of their precession resulting from the **oblateness of the primary**. (That is, the equatorial bulge of the primary planet.)
- "Luna-type" Moons:
  * Have large $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **orbit** of the primary planet. (That is, the inclination to the planetary ecliptic is fixed.)
  * Have most of their precession resulting from the **perturbation from the Sun**.
    
Thus it would be more appropriate to call these moons "Equator-aligned moons" and "Orbit-aligned moons" instead.

### Equator-Aligned Moons

Unfortunately, the derivation of the precession rate of satellites is too complex to be written here, but they depend on the gravitational potential field of the Earth, which can be expressed as an infinite series with coefficients involving [zonal spherical harmonics](https://en.wikipedia.org/wiki/Zonal_spherical_harmonics) $J_1, J_2, J_3, \cdots$ . Fortunately, $J_2$ is about a thousand times larger than all the other terms, so we can focus on the $J_2$ term and ignore the others. Unfortunately, $J_2$ is not easily calculable. It depends on the specific distribution of mass in the three-dimensional structure of the Earth, and the only way to truly know the value of $J_2$ is through observation of the precession rates. So what to do? 

Well, we can make a *very* crude approximation that the Earth is a perfect spheroid of uniform density throughout. Then, $J_2$ is given by:
```math
J_2 \approx \frac{2f}{3} - \frac{R_E^3 w^2}{3GM}\tag{33}
```
where $f$ is the [flattening](https://en.wikipedia.org/wiki/Flattening), calculated by the equatorial radius $R_E$ and the polar radius $R_P$ of the planet as such:
```math
f = \frac{R_E - R_P}{R_E}\tag{34}
```
$w$ is the rotational speed of the planet in $\text{rad}$,\
$G$ is the gravitational constant, and\
$M$ is the mass of the planet.

The table of $J_2$ values by planet in the Solar System is given here:
```math
\begin{array}{cccc}\hline \text{Name} & J_2 & \text{Flattening} & \text{Approximate } J_2 \\ \hline
\text{Mercury} & 60\cdot10^{-6} & 0.000900 & 600\cdot 10^{-6}\\
\text{Venus} & 4.458\cdot10^{-6} & 0.000000 & 0.02\cdot 10^{-6}\\
\text{Earth} & 1.08263\cdot10^{-3} & 0.003353 & 1.08136\cdot10^{-3} \\
\text{Mars} & 1.96045\cdot10^{-3} & 0.005890 & 2.39485\cdot10^{-3}\\
\text{Jupiter} & 14.7360\cdot10^{-3} & 0.064870 & 13.5152\cdot 10^{-3}\\
\text{Saturn} & 16.2980\cdot10^{-3} & 0.097960 & 12.5902\cdot10^{-3}\\
\text{Uranus} & 3.34343\cdot10^{-3} & 0.022930 & 5.44115\cdot10^{-3}\\
\text{Neptune} & 3.411\cdot10^{-3} & 0.017080 & 2.69509\cdot10^{-3}\\ \hline
\end{array}
```
Evidently, the approximation is very crude; however it's the best we got. Now that we have $J_2$, we can calculate the precession rates:
- Nodal Precession Rate
```math
\dot\Omega = -\left[\frac{3\sqrt{GM}J_2R_{\text{avg}}^2}{2(1-e^2)^2a^{7/2}}\right]\cos(i)\tag{35}
```
Where $G$ is the gravitational constant, $M$ and $R_{\text{avg}}$ are the mass and the average radius of the planet respectively, and $a$, $e$, and $i$ are the semi-major axis, eccentricity, and inclination of the orbit of the satellite respectively.\
Note that nodal precession is always in the direction opposite to the orbit, and therefore also called the *node regression*.
- Apsidal Precession Rate
```math
\dot\omega = -\left[\frac{3\sqrt{GM}J_2R_{\text{avg}}^2}{2(1-e^2)^2a^{7/2}}\right]\left(\frac{5}{2}\sin^2(i)-2\right)\tag{36}
```
Note that if $0\degree \leq i \leq 63.4\degree$ or $116.6\degree \leq i \leq 180\degree$, then the precession of the apses are in the direction of the orbit, and therefore apsidal precession is also called the *periapsis advance*.
