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
where $a$ is the semi-major axis of the moon, $R$ is the primary planet's radius, $M_M$ and $M_P$ are the masses of the moon and planet respectively, and $T_M$ and $T_P$ are the orbital periods of the moon and planet respectively.

As is apparent, our Moon is vastly different from the other moons of our solar system: our moon has a much larger $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios than other moons. Thus two kinds of moons must be distinguished: "Io-type" moons, and "Luna-type" moons. (Note: this is not technical terminology.)

- "Io-type" Moons:
  * Have small $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **equator** of the primary planet. (That is, the inclination to the planetary equator is fixed.)
  * Have most of their precession resulting from the oblateness of the primary. (That is, the equatorial bulge of the primary planet.)
- "Luna-type" Moons:
  * Have large $a/R$, $M_M/M_P$, and $T_M/T_P$ ratios.
  * Have orbits aligned to the **orbit** of the primary planet. (That is, the inclination to the planetary ecliptic is fixed.)
  * Have most of their precession resulting from the perturbation from the Sun.
    
Thus it would be more appropriate to call these moons "Equator-aligned moons" and "Ecliptic-aligned moons" instead.
