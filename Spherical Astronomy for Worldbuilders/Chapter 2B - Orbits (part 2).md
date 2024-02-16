(continued..)

However what we really want is the reverse operation of example $4$: going from a specific time to a location. Sounds easy: $M$ is very easy to calculate, and $E$ gives us the exact coordinates $(x, y)$, and we have a relation between $M$ and $E$ by [Kepler's equation](https://en.wikipedia.org/wiki/Kepler%27s_equation) (equation $23$)!\
Unfortunately, Kepler's equation
```math
M = E - e\sin (E)
```
is [transcendental](https://en.wikipedia.org/wiki/Transcendental_function), which means $E$ cannot be solved for $M$ analytically.\
However, there is hope! We can solve for $E$ [*numerically*](https://en.wikipedia.org/wiki/Numerical_analysis). 

First we rearrange the equation:
```math
E - e \sin (E) - M = 0
```
We then define $f$ as a function of $E$ to be $f(E) = E - e \sin (E) - M$. Then we juse need to find the root of $f(E) = 0$.\
We use the [Newton–Raphson method](https://en.wikipedia.org/wiki/Newton%27s_method), given by the iterative equation
```math
x_{n + 1} = x_n - \frac{f(x)}{f'(x)}. \tag{24}
```
Clearly, we need to find $df/dE$.
```math
\frac{d}{dE} f(E) =  1 - e \cos (E)
```
By plugging all the values into equation $24$, we obtain:
```math
E_{n + 1} = E_n - \frac{E_n - e\sin(E_n) - M}{1 - e\cos(E_n)} \tag{25}
```
which we can use to iteratively obtain better and better approximations of $E$, which we can then use to find the coordinates of the planet.
#### Example 5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth has orbital period $T = 365\text{ dy}\enspace5h\enspace48m\enspace46s$, its orbit has semi-major axis $a = 149.6 \text{ Gm}$, and its eccentricity $e = 0.0167$. <br/>
Find the heliocentric ecliptic longitude of the Earth at $t = 77 \text{ dy}\enspace5h\enspace8m$ past periapsis, <br/>
given that when the Earth at periapsis, its heliocentric ecliptic longitude is $102\degree\enspace56'\enspace49.9''$
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We first calculate M by equation $22$:
```math
\begin{align}
M &= \frac{360\degree}{365\text{ dy}\enspace5h\enspace48m\enspace46s} \cdot77 \text{ dy}\enspace5h\enspace8m \\
&= 76\degree\enspace6'\enspace20.811''
\end{align}
```
We now perform the Newton iteration. We first guess $E_1 = M$, and obtain $E_2$ by equation $25$.
```math
\begin{align}
E_2 &= M - \frac{M - e\sin(M) - M}{1 - e\cos(M)}\\
&= 76\degree\enspace7'\enspace19.397''
\end{align}
```
We perform it again, now using $E_2$ for $E_n$.
```math
\begin{align}
E_3 &= E_2 - \frac{E_2 - e\sin(E_2) - M}{1 - e\cos(E_2)}\\
&= 76\degree\enspace7'\enspace19.175''
\end{align}
```
Here is the table of repetitions:
```math
\begin{array}{ccc}\hline n & & E_n \\ \hline
1 & & 76\degree\enspace6'\enspace20.811'' \\
2 & & 76\degree\enspace7'\enspace19.397'' \\
3 & & 76\degree\enspace7'\enspace19.175'' \\
4 & & 76\degree\enspace7'\enspace19.176'' \\
5 & & 76\degree\enspace7'\enspace19.176'' \\ \hline
\end{array}
```
As we can see, $E$ has quickly converged onto $76\degree\enspace7'\enspace19.176''$. In general it can be assumed that $E_5$ will be enough.\
We can now calculate $(x, y)$ with equation $19$:
```math
\begin{align}
x &= a \cos (E) - ae\\
&= 149.6 \cos(76\degree\enspace7'\enspace19.18'') - 149.6 \cdot 0.0167 \\
&= 33.384 \text{ Gm}\\
\\
y &= b \sin (E)\\
&= a\sqrt{1 - e^2} \sin (E)\\
&= 149.6 \sqrt(1 - 0.0167^2) \sin(76\degree\enspace7'\enspace19.18'')\\
&= 145.213 \text{ Gm}
\end{align}
```
Thus, the Earth's longitude with respect to its periapsis is:
```math
\arctan(145.213, 33.384) = 77\degree\enspace3'\enspace10.27''
```
Which, when added with the ecliptic longitude of the periapsis $102\degree\enspace56'\enspace49.9''$ gives:
```math
\lambda_{\text{Heliocentric}} \text{ of the Earth} = 180\degree\enspace(+ 0.17'')
```
Which agrees with example $4$. (The $0.17''$ is due to stray rounding error.)\
$\blacksquare$

#### Proof of Kepler's Equation

### Orientation of the Orbit in Space
