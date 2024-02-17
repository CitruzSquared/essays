(continued from part A...)

### Orientation of Orbits in 3D Space
In examples $4$ and $5$, we have calculated the position of the Earth in ecliptic coordinates, which was simple because the Earth's perifocal plane was the definition of the Ecliptic plane. Other planets are not so simple. Let:
```math
\displaylines{
\begin{align}
&(p, q, s) \text{ denote the perifocal cartesian coordinates of an object}\\
&(x, y, z) \text{ denote the heliocentric ecliptic cartesian coordinates of the object}
\end{align}
}
```

#### Orbital Elements

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/22bef238-757a-4561-8d17-3b41dbf22c5b" width="350"/> This diagram depicts the orbit of a non-Earth planet $Q$ where $O$ is the location of the Sun and $P$ is the periapsis of the orbit. The direction of orbit is given by the arrow pointing from $P$ to $Q$. Thus the true anomaly $\nu$ of $Q$ is the angle $POQ$.

As one can see, the orbit is tilted upwards from the Ecliptic plane by an angle $i$, and therefore forms a line of intersection. The angle $i$ is called the [*inclination*](https://en.wikipedia.org/wiki/Orbital_inclination), and the line where the orbit crosses the ecliptic plane (the line $ND$) is known as the [*line of nodes*](https://en.wikipedia.org/wiki/Orbital_node). The point on the line of nodes where the planet is moving upwards (point $N$) is called the *ascending node* and the other point is known as the *descending node* (point $D$)

The angle $AON$ is known as the [*longitude of the ascending node*](https://en.wikipedia.org/wiki/Longitude_of_the_ascending_node) and is denoted $\Omega$, and the angle $NOP$ is known as the [*argument of periapsis*](https://en.wikipedia.org/wiki/Argument_of_periapsis) and is denoted $\omega$. Then, remembering that the $x$-axis in the ecliptic frame points towards Aries, and that the $p$-axis in the perifocal frame points towards the periapsis, the ecliptic frame can be transformed into the perifocal frame by the procedure below:
```math
\displaylines{
\begin{align}
\text{1. } & \text{Rotate the ecliptic in the direction of the orbit plane by } \Omega.\\
\text{2. } & \text{Then, rotate it upwards by } i.\\
\text{3. } & \text{Then, rotate it in the direction of the orbit by } \omega.\\
\end{align}
}
```
This results in the $x$-axis now pointing in the $p$ direction.

This can be done with rotation matrices:
- Step 1 - we rotate by $\Omega$ about the $z$-axis.
```math
A =
\begin{bmatrix}
\cos{(\Omega)} & \sin{(\Omega)}  & 0\\
-\sin{(\Omega)} & \cos{(\Omega)} & 0\\
0 & 0 & 1
\end{bmatrix}
```
- Step 2 - we rotate by $i$ about the $x$-axis (which now points in the direction of $N$).
```math
B =
\begin{bmatrix}
1 & 0 & 0\\
0 & \cos{(i)} & \sin{(i)}\\
0 & -\sin{(i)} & \cos{(i)}
\end{bmatrix}
```
- Step 3 - we rotate by $\omega$ about the $z$-axis (which now points perpendicular to the orbital plane).
```math
C =
\begin{bmatrix}
\cos{(\omega)} & \sin{(\omega)}  & 0\\
-\sin{(\omega)} & \cos{(\omega)} & 0\\
0 & 0 & 1
\end{bmatrix}
```
Now, the full rotation matrix is given by multiplying all these steps together:
```math
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
=
CBA
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
```
Actually carrying out the matrix multiplication, this is:
```math
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
=
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega  &  \sin i \sin\omega \\
  -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega &\sin i \cos\omega \\
   \sin\Omega \sin i  &  -\cos \Omega \sin i  & \cos i
 \end{bmatrix}

\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
\tag{29}
```
The reverse transformation, going from the perifocal frame to the ecliptic frame, is given by the transpose of $CBA$:
```math
\begin{bmatrix}
x \\ y \\ z
\end{bmatrix}
=
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & \sin\Omega \sin i \\
  \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega & -\cos \Omega \sin i \\
  \sin i \sin\omega & \sin i \cos\omega &  \cos i
 \end{bmatrix}
\begin{bmatrix}
p \\ q \\ s
\end{bmatrix}
\tag{30}
```
Thus the exact position of $Q$ can be calculated in ecliptic coordinates from the values $a, e, i, \Omega, \omega,$ and $\nu$, and these are called the [**orbital elements**](https://en.wikipedia.org/wiki/Orbital_elements) of $Q$.
