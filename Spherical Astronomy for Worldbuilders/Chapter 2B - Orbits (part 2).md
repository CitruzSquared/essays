(continued..)

What is more important though, is the reverse operation of example $4$: going from a specific time to a location. Sounds easy: $M$ is very easy to calculate, and $E$ gives us the exact coordinates $(x, y)$, and we have a relation between $M$ and $E$ by [Kepler's equation](https://en.wikipedia.org/wiki/Kepler%27s_equation) (equation $23$)!\
Unfortunately, Kepler's equation
```math
M = E - e\sin (E)
```
is [transcendental](https://en.wikipedia.org/wiki/Transcendental_function), which means $E$ cannot be solved for $M$ analytically.\
However, there is hope! We can solve for $E$ [*numerically*](https://en.wikipedia.org/wiki/Numerical_analysis).
