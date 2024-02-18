(Continued from Part A...)

### Kepler's Second Law
We have discussed Kepler's first and third laws. Now let us tackle his second law, which states that the area sweeped out by a planet over a unit time must stay constant.

The area of a sector with radius $r$ and central angle $\theta$ is given by:
```math
S = \frac{1}{2}r^2 \theta
```
And therefore the area sweeped out by a planet over a small increment $d\nu$ of true anomaly is:
```math
dS = \frac{1}{2} r^2 d\nu
```
And therefore the area sweeped out per unit time is
```math
\frac{dS}{dt} = \frac{r^2}{2}\frac{d\nu}{dt}
```
And this must stay constant.\
Because the area of an ellipse is $\pi a b$,
```math
T \frac{dS}{dt} = T\frac{r^2}{2}\frac{d\nu}{dt} = \pi a b
```
where $T$ is the orbital period.\
Therefore:
```math
r^2 \frac{d\nu}{dt} = \frac{2\pi a b}{T} 
```
now, denoting $2\pi/T$ as $n$ (this quantity is called the [mean motion](https://en.wikipedia.org/wiki/Mean_motion)), we obtain:
```math
r^2 \nu' = nab = na^2\sqrt{1 - e^2}\tag{22}
```

Now, recall equation $20$:
```math
r = a(1 - e\cos (E))
```
Differentiating both sides with respect to time gives us:
```math
r' = ae\sin(E)E' \tag{23}
```
Now recall equation $18$:
```math
\begin{align}
r &= \frac{a(1 - e^2)}{1 + e\cos(\nu)} \\
\therefore\frac{1}{r} &= \frac{1 + e\cos(\nu)}{a(1 - e^2)}
\end{align}
```
Differentiating both sides of this equation we obtain:
```math
\begin{align}
-\frac{r'}{r^2} = -\frac{e \sin (\nu) \nu'}{a(1 - e^2)} \\
\therefore r' = \frac{e\sin(\nu)r^2\nu'}{a(1 - e^2)} \tag{24}
\end{align}
```
Now we substitute equation $22$ in equation $24$:
```math
r' = \frac{nae\sin(\nu)}{\sqrt{1 - e^2}}
```
Equating this with equation $23$:
```math
\begin{align}
ae\sin(E)E' &= \frac{nae\sin(\nu)}{\sqrt{1 - e^2}}\\
E' &= \frac{n\sin(\nu)}{\sqrt{1 - e^2}\sin(E)}
\end{align}
```
But $\sqrt{1 - e^2}\sin(E)$ is just $y_{\text{perifocal}}/a$ by equation $19$, and $y_{\text{perifocal}} = r\sin(\nu)$ by equation $17$, so:
```math
\begin{align}
E' &= \frac{n\sin(\nu)}{r\sin(\nu)/a}\\
\therefore rE' &= na
\end{align}
```
Now, substituting equation $20$ for $r$:
```math
(1 - e\cos (E)) E' = n
```
Integrating over time on both sides yields:
```math
E - e\sin(E) = nt + c.
```
If we measure $t$ from the time of periapsis, then when $t = 0$, $E - e\sin(E) = 0$ since $E = 0$ at periapsis. Therefore $c. = 0$.\
Let's also denote $nt$ as $M$. We call this quantity the [*mean anomaly*](https://en.wikipedia.org/wiki/Mean_anomaly):
```math
M = nt = \frac{2\pi}{T}\cdot t\tag{25}
```
Now the equation becomes:
```math
M = E - e\sin (E) \tag{26}
```
Which is known as [**Kepler's Equation**](https://en.wikipedia.org/wiki/Kepler%27s_equation). This equation allows us to relate $E$ and $M$, thus relating $E$ and $t$, which allows us to finally calculate the motion of the planets. Keep in mind that we **must** use radians for $M$ and $E$.

#### Example 4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The orbital period of the Earth $T = 365.2422\text{ dy}$, and the eccentricity of its orbit is $0.0167$. <br/>
Additionally, when it is at periapsis, its heliocentric ecliptic longitude is $102\degree\enspace56'\enspace49.9''$. <br/>
Given that the time of perihelion in $2024$ was $\text{January 3, }2024\enspace 00:38$, <br/>
calculate the time of Spring Equinox in the Northern Hemisphere in $2024$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Because ecliptic coordinates are based on the Earth's orbital plane, it effectively is equal to the Earth's perifocal coordinate frame, except that the $x$-axis is rotated from the direction of perihelion to the direction of Aries. Therefore, we can use our perifocal equations in the ecliptic frame without much trouble.

Spring Equinox in the Northern Hemisphere is defined as $\lambda_{\text{Sun, Geocentric}} = 0\degree$, therefore (by equation $5$) it occurs when $\lambda_{\text{Earth, Heliocentric}} = 180\degree$. Thus, the true anomaly of the Earth at the time of Northern Spring Equinox is:
```math
\begin{align}
\nu &= 180\degree - 102\degree\enspace56'\enspace49.9''\\
&= 77\degree\enspace3'\enspace50.1''
\end{align}
```
Now, by equation $21$:
```math
\begin{align}
\cos (E) &= \frac{e + \cos(\nu)}{1 + e\cos(\nu)}\\
&= \frac{0.0167 + \cos(77\degree\enspace3'\enspace50.1'')}{1 + 0.0167\cos(77\degree\enspace3'\enspace50.1'')}\\
&= 0.239855411\\
\therefore E &= 1.3285794 \text{ rad}
\end{align}
```
Now, by Kepler's equation (equation $26$):
```math
\begin{align}
M &= E - e\sin (E)\\
&= 1.3285794 - 0.0167 \sin (1.3285794)\\
&= 1.3123669 \text{ rad}
\end{align}
```
Therefore, by the definition of $M$ (equation $25$):
```math
\begin{align}
M &= \frac{2\pi}{T}\cdot t\\
\therefore t &= \frac{TM}{2\pi}\\
&=\frac{365.2422\text{ dy} \cdot 1.3123669}{2\pi}\\
&= 76 \text{ dy}\enspace6h\enspace55m
\end{align}
```
$76\text{ dy}\enspace6h\enspace55m$ after $\text{January 3, }2024\enspace00:38$ is $\text{March 19, }2024\enspace07:33$.\
Comparing to the true time ($\text{March 20, }2024\enspace03:07$), we can see that we are very close. The discrepancy comes from rounding error and the fact that the motion of the Earth is not a true two body problem.\
$\blacksquare$

However what we really want is the reverse operation of example $4$: going from a specific time to a location. Sounds easy: $M$ is very easy to calculate, and $E$ gives us the exact coordinates $(x, y)$, and we have a relation between $M$ and $E$ by [Kepler's equation](https://en.wikipedia.org/wiki/Kepler%27s_equation) (equation $26$)!\
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
x_{n + 1} = x_n - \frac{f(x_n)}{f'(x_n)}. \tag{27}
```
Clearly, we need to find $f'(E)$.
```math
\frac{df}{dE} =  1 - e \cos (E)
```
By plugging all the values into equation $27$, we obtain:
```math
E_{n + 1} = E_n - \frac{E_n - e\sin(E_n) - M}{1 - e\cos(E_n)} \tag{28}
```
which we can use to iteratively obtain better and better approximations of $E$, which we can then use to find the coordinates of the planet.
#### Example 5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth has orbital period $T = 365.2422\text{ dy}$, its orbit has semi-major axis $a = 149.6 \text{ Gm}$, and its eccentricity $e = 0.0167$. <br/>
Find the heliocentric ecliptic longitude of the Earth at $t = 76 \text{ dy}\enspace6h\enspace55m$ past periapsis, <br/>
given that when the Earth at periapsis, its heliocentric ecliptic longitude is $102\degree\enspace56'\enspace49.9''$
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Due to the definition of the ecliptic coordinate frame, we can use our perifocal equations in it without much trouble. (See example $4$.)\
We first calculate $M$ by equation $25$:
```math
\begin{align}
M &= \frac{2\pi}{365.2422\text{ dy}} \cdot 76 \text{ dy}\enspace6h\enspace55m \\
&= 1.3123669\text{ rad}
\end{align}
```
We now perform the Newton iteration. We first guess $E_1 = M$, and obtain $E_2$ by equation $28$.
```math
\begin{align}
E_2 &= M - \frac{M - e\sin(M) - M}{1 - e\cos(M)}\\
&= 1.3285815 \text{ rad}
\end{align}
```
We perform it again, now using $E_2$ for $E_n$.
```math
\begin{align}
E_3 &= E_2 - \frac{E_2 - e\sin(E_2) - M}{1 - e\cos(E_2)}\\
&= 1.3285794 \text{ rad}
\end{align}
```
Here is the table of repetitions:
```math
\begin{array}{ccc}\hline n & & E_n \\ \hline
1 & & 1.3123669 \\
2 & & 1.3285815 \\
3 & & 1.3285794 \\
4 & & 1.3285794 \\ \hline
\end{array}
```
As we can see, $E$ has quickly converged onto $1.3285794\text{ rad}$. In general it can be assumed that $E_4$ or $E_5$ will be enough.\
We can now calculate $(x, y)$ with equation $19$:
```math
\begin{align}
x_{\text{perifocal}} &= a \cos (E) - ae\\
&= 149.6 \cos(1.3285794) - 149.6 \cdot 0.0167 \\
&= 33.384 \text{ Gm}\\
\\
y_{\text{perifocal}} &= b \sin (E)\\
&= a\sqrt{1 - e^2} \sin (E)\\
&= 149.6 \sqrt{1 - 0.0167^2} \sin(1.3285794)\\
&= 145.213 \text{ Gm}
\end{align}
```
Then, by equation $17$, the true anomaly is:
```math
\arctan(145.213, 33.384) = 77\degree\enspace3'\enspace10.27''
```
Which, when added with the ecliptic longitude of the periapsis $102\degree\enspace56'\enspace49.9''$ gives:
```math
\lambda_{\text{Earth, Heliocentric}} = 180\degree\enspace17''
```
Which agrees with example $4$. (The $17''$ is due to stray rounding error.)\
$\blacksquare$

#### Proof of Kepler's Second Law
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Prove that the area of an orbit sweeped out by a planet per unit time is constant. <br/>
Disclaimer: the proof is mathematically dense and there is no need to know it. <br/>
It is advised for the average reader to skip this investigation.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/9bc1d922-bfd0-4609-9013-0a1171e846c5" width="200"/> In this diagram, the motion of a planet $P$ has been depicted. $\textbf{r}$ is its position vector, and $d\textbf{r}$ is the small change in position over a small unit time $dt$. The angle between $\textbf{r}$ and $d\textbf{r}$ has been called $s$.

The area of this triangle $dA$ well represents the small area that is sweeped out by the planet over a small time $dt$. This area is given by:
```math
dA = \frac{1}{2}rdr\sin(s)
```
where $r$ and $dr$ are the magnitudes of $\textbf{r}$ and $d\textbf{r}$ respectively. This can be written in vector form as:
```math
d\textbf{A} = \frac{1}{2}\textbf{r}\times d\textbf{r}
```
dividing by $dt$ to get the area swept out per unit time,
```math
\frac{d\textbf{A}}{dt} = \frac{1}{2}\textbf{r}\times \frac{d\textbf{r}}{dt}
```
Kepler's second law states that this quantity $d\textbf{A}/dt$ must be constant, which means that $d^2\textbf{A}/dt^2 = \textbf{0}$.\
Calculating $d^2\textbf{A}/dt^2 = 0$:
```math
\begin{align}
\frac{d^2\textbf{A}}{dt^2} &= \frac{1}{2}(\frac{d\textbf{r}}{dt}\times\frac{d\textbf{r}}{dt} + \textbf{r}\times \frac{d^2\textbf{r}}{dt^2})\\
&= \frac{1}{2}(\textbf{v}\times\textbf{v} + \textbf{r}\times\textbf{a})\\
&= \frac{1}{2}\textbf{r}\times\textbf{a}
\end{align}
```
where $\textbf{v}$ and $\textbf{a}$ are the velocity and acceleration of $P$ respectively.\
However, it has been shown previously (in the proof of Kepler's first law) that $\textbf{r}$ is parallel to $\textbf{a}$ and therefore
```math
\frac{d^2\textbf{A}}{dt^2} = \frac{1}{2}\textbf{r}\times\textbf{a} = \textbf{0}.
```
Which proves Kepler's second law.\
$\blacksquare$

### Orientation of Orbits in 3D Space
(Continued in Part C...)
