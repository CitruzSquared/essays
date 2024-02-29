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

### The Subsolar Point
In some regions of the world, there are times when the Sun is directly overhead (i.e. at the Zenith) and objects leave no shadow on the ground. This phenomenon is called the [Lahaina noon](https://en.wikipedia.org/wiki/Lahaina_Noon) and the point where this occurs on the Earth is called the [subsolar point](https://en.wikipedia.org/wiki/Subsolar_point). Let's try to find the subsolar time at any time. 

Say that at (solar) time $t$, the Sun was at right ascension $\alpha$ and declination $\delta$. The subsolar point would be the point corresponding to these equatorial coordinates. Thus the latitude of the subsolar point is simply the declination of the Sun:
```math
\phi_{\text{Subsolar}} = \delta \tag{6.7}
```
Because the declension of the Sun cannot exceed the axial tilt of the planet, Lahaina noon only occurs in regions with latitudes between $+\varepsilon$ and $-\varepsilon$ (the Tropics of Cancer and Capricorn).

If the Sun is at the Zenith, then it is also at the meridian and thus it would be the apparent noon at that place. Thus we just have to find the longitude where it is exactly apparent noon at time $t$. The hour angle of the Sun at apparent noon is $0\degree$, so that longitude would be where $\Theta_L = \alpha$ (by equation $6.1$). Thus, if we know the standard sidereal time $\Theta$ at time $t$, we can calculate the longitude by:
```math
l_{\text{Subsolar}} = \alpha - \Theta\tag{6.8}
```
Which comes from equation $6.2$.

#### Example 6.7
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the subsolar point on the Earth on $\text{May 27, } 2024$ at standard solar time $09:18$. <br/>
$\lambda = 66\degree$ $40'$, $\Theta = 24\degree$ $55'$ $27''$, $\varepsilon = 23.44\degree$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $1.3$:
```math
\begin{align}
\alpha = 4^h\:19^m\:17^s\\
\delta = 21\degree\:25'\:25''
\end{align}
```
Thus by equation $6.7$ and $6.8$:
```math
\begin{align}
\phi &= \delta = 21\degree\:25'\:25''\\
l &= \Theta - \alpha = 39\degree\:53'\:42''
\end{align}
```
Which is in Mecca, Saudi Arabia.\
$\blacksquare$


Now to find the date when Lahaina noon occurs at a specific location. We have from earlier:
```math
\delta = \phi
```
But also, by equation $1.1$ we know:
```math
\begin{align}
x_{\text{equatorial}} &= \cos(\delta)\cos(\alpha)\\
y_{\text{equatorial}} &= \cos(\delta)\sin(\alpha)\\
z_{\text{equatorial}} &= \sin(\delta)
\end{align}
```
Therefore, using equation $1.4$:
```math
z_{\text{ecliptic}} = -\sin(\varepsilon)\cos(\delta)\sin(\alpha) + \cos(\varepsilon)\sin(\delta)
```
But we also know that since $\beta$ of the Sun is $0\degree$, $z_{\text{ecliptic}} = \sin(0\degree) = 0$. Thus:
```math
\begin{align}
0 &= -\sin(\varepsilon)\cos(\delta)\sin(\alpha) + \cos(\varepsilon)\sin(\delta)\\
\therefore \sin(\alpha) &= \frac{\cos(\varepsilon)\sin(\delta)}{\sin(\varepsilon)\cos(\delta)}
\end{align}
```
So we take the arcsine. $\arcsin()$ has two solutions:
```math
\begin{align}
\alpha_1 &= \arcsin\left(\frac{\cos(\varepsilon)\sin(\delta)}{\sin(\varepsilon)\cos(\delta)}\right) \tag{6.9}\\
\alpha_2 &= 12^h - \alpha_1 \tag{6.10}
\end{align}
```
Therfore at any location, if Lahaina noon is possible, there will be two dates when this happens. (Unless one is *exactly* at the Tropic of Cancer or Capricorn. Then $\alpha_1$ works out to be equal to $\alpha_2$.)

From $\alpha$ and $\delta$ we can find $\lambda$ and then find the date by means of example $2.3$.

#### Example 6.8
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the $\lambda$ values for which there is Lahaina noon in Mecca, Saudi Arabia. <br/>
$\phi = 21\degree$ $25'$ $25''$, $l =39\degree$ $53'$ $42''$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $6.7$:
```math
\delta = \phi = 24\degree\:25'\:25''
```
Then, by equations $6.9$ and $6.10$:
```math
\begin{align}
\alpha_1 &= \arcsin\left(\frac{\cos(23.44\degree)\sin(24\degree\:25'\:25'')}{\sin(23.44\degree)\cos(24\degree\:25'\:25'')}\right)\\
&= 4^h\:19^m\:17^s\\
\alpha_2 &= 12^h - 4^h\:19^m\:17^s\\
&= 7^h\:40^m\:43^s
\end{align}
```
Then, by equation $1.4$:
```math
\begin{align}
\lambda_1 = 66\degree\:40'\\
\lambda_2 = 113\degree\:20'
\end{align}
```
$\lambda_1$ is the value of $\lambda$ from the previous example.

These can be converted to dates by following example $2.3$, and should result in dates around $\text{May 27, } 2024$ and $\text{July 15, } 2024$. At these dates, at the moment of local apparent noon at Mecca, the Sun is directly overhead Mecca, and therefore for anyone in any other place in the world where the Sun is up, their shadow would point perfectly away from Mecca. The direction of the Muslim prayer (the *Qibla*), which is in the direction of Mecca, can be determined then by the direction opposite one's shadow on these dates. Read more about this [here](https://en.wikipedia.org/wiki/Qibla_observation_by_shadows).\
$\blacksquare$

### Lighting Direction
Here is another thing we can do with horizontal coordinates: in chapter $4$, we learned how to calculate how much of a planet was visible (the phase) and even which side of the planet was illuminated. Let us now figure out specifically which direction the light was coming from.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/86eb72e3-9593-4153-8334-5f4d2d0ff113" width="400"/> In this diagram, the Sun is at point $S$, and the planet of interest is at point $P$. $Z$ is the zenith. The arc connecting the Sun and the Planet is shown. What we are interested in is in which direction is $S$ from $P$? More specifically, we are interested in the angle $ZPS$.

This can be calculated with the [spherical law of cosines](https://en.wikipedia.org/wiki/Spherical_law_of_cosines):
```math
\cos(ZPS) = \frac{\cos(ZOS) - \cos(ZOP)\cos(SOP)}{\sin(ZOP)\sin(SOP)}
```
The angle $ZOS$ and $ZOP$ are called the *zenith distances* (denoted $\zeta$) of $S$ and $P$ and can be calculated by:
```math
\zeta = 90\degree - a\tag{6.11}
```
Therefore, the equation becomes:
```math
ZPS = \arccos\left(\frac{\cos(\zeta_S) - \cos(\zeta_P) \cos(SOP)}{\sin(\zeta_P)\sin(SOP)}\right)\tag{6.12}
```
The angle $SOP$ can be calculated by equation $4.3$.

<br/>

#### Example 6.9
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Recall example $4.1$ where we calculated the phase of Venus on $\text{January 1, } 2024$. <br/>
Calculate how Venus would have looked from London, UK ($\phi = 51\degree, l = 0\degree$) at $06:00$ ($\Theta = 190\degree$ $23'$ $56.5''$).
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Recall from example $4.1$:
```math
\begin{align}
\alpha_V &= 16^h\:07^m\:26^s\\
\delta_V&=-18\degree\:57'\:52''\\
\alpha_S &= 18^h\:46^m\:38^s \\
\delta_S&=-23\degree\:0'\:10''\\
SOV &= 37\degree\:16'\:\:7.9''
\end{align}
```
Where $S$ is the Sun and $V$ is Venus.\
We found out the the phase of Venus was $78$%:
<p align="center">

  <img width="100" src="https://github.com/CitruzSquared/essays/assets/23460281/ed1b89ff-3c4c-4e04-84d7-e0658861d887">
</p>

Now, let's figure out the lighting direction. Using equation $6.1$:
```math
\begin{align}
h_V &= 190\degree\:23'\:56.5'' - 16^h\:07^m\:26^s = -51\degree\:27'\:33.5''\\
h_S &= 190\degree\:23'\:56.5'' - 18^h\:46^m\:38^s = -91\degree\:15'\:33.5''
\end{align}
```
Now, using equation $6.3$ (See example $6.4$ for more detail):
```math
\begin{align}
A_V &= 131\degree\:50'\:46.3''\\
a_V&= 6\degree\:47'\:32.0''\\
A_S &= 104\degree\:2'\:39.1''\\
a_S&= -18\degree\:26'\:47.8''\\
\end{align}
```
Thus, by equation $6.11$:
```math
\begin{align}
\zeta_V &= 90\degree - 6\degree\:47'\:32.0'' = 83\degree\:12'\:28.0''\\
\zeta_S &= 90\degree - (-18\degree\:26'\:47.8'') = 108\degree\:26'\:47.8''\\
\end{align}
```
And then finally by equation $6.12$:
```math
\begin{align}
ZVS &= \arccos\left(\frac{\cos(108\degree\:26'\:47.8'') - \cos(83\degree\:12'\:28.0'') \cos(37\degree\:16'\:\:7.9'')}{\sin(83\degree\:12'\:28.0'')\sin(37\degree\:16'\:\:7.9'')}\right)\\
&= 133\degree\:3'\:31.3''
\end{align}
```
Thus, the light was shining from an angle of $133\degree$ $3'$ $31.3''$ from the Zenith. Keeping in mind that since the Sun's azimuth is less than that of Venus, the Sun must be shining from the left:
<p align="center">
  <img width="150" src="https://github.com/CitruzSquared/essays/assets/23460281/10422092-c198-47be-a4d8-145a0d273e0c">
</p>

Comparing with [Stellarium](https://stellarium.org/) (a planetarium software):
<p align="center">
  <img width="100" src="https://github.com/CitruzSquared/essays/assets/23460281/8a470f40-b97a-46e9-acd0-25c550e6516f">
  <img width="100" src="https://github.com/CitruzSquared/essays/assets/23460281/337c923c-0f6d-48b0-9c3c-77fed37d3b43"> <br/>
  Stellarium image on the left, Stellarium image overlaid with our prediction on the right.
</p>

$\blacksquare$
