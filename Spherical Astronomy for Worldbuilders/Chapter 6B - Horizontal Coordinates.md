(Continued from Part A...)

### Heliacal Rising

Because the Earth orbits the Sun, different parts of the sky are completely blocked out by the glare of the Sun in different seasons. The [heliacal rising](https://en.wikipedia.org/wiki/Heliacal_rising) of a star happens when a star becomes visible for the first time again after being blocked out by the glare of the Sun for some time.

Because the Sun's ecliptic longitude increases (i.e. the Sun moves East), the Stars with fixed right ascensions and declinations to the East of the Sun will eventually be blocked by the Sun's light, and re-emerge to the West of the Sun when it is visible again. Because a Western elongation implies a morning star, the heliacal rising happens when the Star is visible in the dawn again. The star will then rise earlier and earlier before the Sun, until it loops all the way around and becomes lost in the glare of the Sun again.

Let's try and find out when the heliacal rising of a star with right ascension $\alpha$ and declination $\delta$ will happen at a location with latitude $\phi$.

We estimate the heliacal rising to be the point when the star would rise exactly at sunrise, but in reality it is some days after this time because the Star still needs some time to be visible. Let's first say the Sun's ecliptic longitude to be $\lambda$. Then, the Sun's equatorial coordinates are given by equation $1.3$ (Keep in mind $\beta$ of the Sun is $0\degree$):
```math
\begin{align}
\alpha_{\text{Sun}} &= \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda))\\
\delta_{\text{Sun}} &= \arcsin(\sin(\varepsilon)\sin(\lambda))
\end{align}
```
Now we use the sunrise equation (equation $6.5$) to calculate the time of sunrise:
```math
\Theta_{\text{Sunrise}} = -\arccos(-\tan(\phi)\tan(\delta_{\text{Sun}})) + \alpha_{\text{Sun}}
```
We now substitute $\alpha_{\text{Sun}}$ and $\delta_{\text{Sun}}$ with our calculations from before:
```math
\Theta_{\text{Sunrise}} = -\arccos(-\tan(\phi)\tan(\arcsin(\sin(\varepsilon)\sin(\lambda)))) + \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda))
```
Now we use the sunrise equation again to calculate the time of star rise:
```math
\Theta_{\text{Star-rise}} = -\arccos(-\tan(\phi)\tan(\delta)) + \alpha
```
These two times must equal:
```math
-\arccos(-\tan(\phi)\tan(\arcsin(\sin(\varepsilon)\sin(\lambda)))) + \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda)) = -\arccos(-\tan(\phi)\tan(\delta)) + \alpha \tag{6.6}
```
Since we know $\alpha$, $\delta$, $\phi$, and $\varepsilon$, we can solve this equation for $\lambda$. Once we have $\lambda$, we can find the mean anomaly of the Earth and thus the date of heliacal rising.

Copyable Version:
```
-arccos(-tan(phi)tan(arcsin(sin(epsilon)sin(lambda)))) + arctan(cos(epsilon)sin(lambda), cos(lambda)) = -arccos(-tan(phi)tan(delta)) + alpha
```

#### Example 6.6
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
Calculate the date of the heliacal rising of the star Sirius ($\alpha = 06^h$ $45^m$ $08.92^s$, $\delta = -16\degree$ $42'$ $58.02''$) in Egypt ($\phi = 30\degree$). <br/>
Use $\varepsilon = 23.44\degree$, $e = 0.0167$, and $T = 365.24\text{ dy}$ for the Earth. <br/>
The time of the last periapsis of Earth was $\text{January 3, }2024$.
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

We put the values into equation $6.6$. The right hand side is:
```math
-\arccos(-\tan(30\degree)\tan(-16\degree\:42'\:58.02'')) + 06^h\:45^m\:08.92^s = 0.371275 \text{ rad}
```
Thus equation $6.6$ is:
```math
-\arccos(-\tan(30\degree)\tan(\arcsin(\sin(23.44\degree)\sin(\lambda)))) + \arctan(\cos(23.44\degree)\sin(\lambda), \cos(\lambda)) = 0.371275 \text{ rad}
```
Then we solve for $\lambda$ (a computer program was used):
```math
\lambda = 2.1139\text{ rad} = 121\degree\:7'
```
Thus $\lambda_{\text{Earth Heliocentric}} = 121\degree$ $7' + 180\degree = 301\degree$ $7'$ (Equation $1.5$).\
Now we follow example $2.3$.
```math
\begin{align}
\nu &= 301\degree\:7' - 102\degree\:56'\:49.9''\\
&= 198\degree\:10'\:13.29''\\
\end{align}
```
$\nu$ is bigger than $180\degree$, so we take the negative arccosine in equation $2.16$:
```math
\begin{align}
E &= - \arccos\left(\frac{0.0167 + \cos(198\degree\:10'\:13.29'')}{1 + 0.0167\cos(198\degree\:10'\:13.29'')}\right) + 2\pi\\
&= 3.463975 \text{ rad}\\
\therefore M &= 3.463975 - 0.0167\sin(3.463975)\\
&= 3.469266 \text{ rad}\\
\therefore t &= \frac{3.469266}{2\pi}\cdot365.24\text{ dy}\\
&= 202\text{ dy }
\end{align}
```
$202\text{ dy}$ after $\text{January 3, }2024$ is $\text{July 23, }2024$. Adding about $10$ days to give Sirius time to actually be visible, we get $\text{August 2, }2024$. This is almost exact: the heliacal rising of Sirius happens around $\text{August 1}$ in Egypt.

The ancient Egyptians thought of this event to have immense significance because it happened just before the beginning of the flooding season of the Nile river (around late Summer) by coincidence. Read more about this [here](https://en.wikipedia.org/wiki/Sopdet).\
$\blacksquare$

### Lighting Direction