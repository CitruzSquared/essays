## VI. Horizontal Coordinates

Let's define a set of coordinates that we can use to describe the location of objects from the view of an observer on the ground.

### The Hour Angle

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/5b1c3310-b4f1-4e70-b954-f4f68287a381" width="400"/> Consider this diagram. 

This diagram depicts the celestial sphere around an observer at point $O$. The gray plane is the local horizon. $ON$, $OS$, $OE$, and $OW$, are the local directions of North, South, East, and West respectively. $N'$ and $S'$ depict the celestial poles, and thus the line $N'S'$ is the Earth's rotational axis, and therefore the plane perpendicular to $N'$ and $S'$ is the Earth's equatorial plane. Therefore, the angle $N'ON$ defines the observer's local latitude $\phi$. $Z$ and $A$ are the observer's Zenith and Nadir respectively.

The plane (or circle) $NZSA$ defines the local meridian. 

In the last chapter, we saw how we could define the sidereal time as the Western distance between Aries and the Meridian. Now we are interested in the point $P$, which may be the location of a star or a planet. We can do the same thing, and we can define the angle between the Meridian and $P$, putting West as positive again. This angle is called the [**hour angle**](https://en.wikipedia.org/wiki/Hour_angle) and is more rigorously defined as the angle between the meridian circle and the circle that goes through $P$, $N'$, and $S'$, which is called the [hour circle](https://en.wikipedia.org/wiki/Hour_circle) of $P$. This is useful as it gives us a way to describe the location of $P$, specifically how East or West it is, in comparison to the meridian.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/743585dd-02e4-41f2-ba17-18ecfa2a35cc" width="400"/> In this diagram, the Western angle between the Prime Meridian and Aries (the right ascension of the Prime Meridian) is the standard sidereal time ($\Theta$), and the Western angle between the Local Meridian and Aries (the right ascension of the Local Meridian) is the local standard time ($\Theta_L$), as we saw in the last chapter. The Eastern angle between Aries and the Star is, by definition, the right ascension of the star ($\alpha$). Furthermore, the Eastern angle between the Prime Meridian and the Local Meridian is the longitude $l$. (Eastern angle meaning the angle measured in the Eastern direction.)

The Western angle between the Prime Meridian and the Star is then known as the Standard Hour Angle of the star ($h$), and the Western angle between the Local Meridian and the Star is known as the Local Hour Angle of the star ($h_L$).

<br/>
<br/>

It is therefore evident that 
```math
h_L = \Theta_L - \alpha\tag{80}
```
and because $\Theta_L = \Theta + l$ (equations $77$ and $78$):

```math
h_L = \Theta + l - \alpha\tag{81}
```

When $h_L = 0$, the star is coincident with the meridian, and the star is at the highest point in the sky. If $h_L = 180\degree$, the star is coincident with the lower meridian, and it is at the lowest point in the sky. If the star in question is the Sun, then the times at which $h_L = 0$ and $h_L = 180\degree$ are called *apparent noon* and *apparent midnight* respectively. These are not the same as the *mean noon* and *mean midnight*, the mean values are simply the average of the apparent values over the year. (Yes, this means noon and midnight aren't always at $12:00$ and $00:00$!)

#### Example 22
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$, on solar day $175$ at local mean solar time $11:00:00$, <br/>
what was the local hour angle of star $S$, with right acension $5^h$?
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

$175\text{ dy }11:00:00$ is $175.458333\text{ dy}$.\
We need the sidereal time, so by equation $79$:
```math
\begin{align}
\Theta_L &= \frac{289.42+1}{289.42} \cdot 175.458333 - 0.5\\
&= 175\text{ sdy } 203\degree\:14'\:48.61''
\end{align}
```

Then, by equation $80$:
```math
\begin{align}
h_L &= 203\degree\:14'\:48.61'' - 5^h\\
&= 128\degree\:14'\:48.61''
\end{align}
```
$\blacksquare$

#### Example 23
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$, on some time during solar day $175$, the hour angle of star $S$, with right acension $5^h$, was $128\degree\:14'\:48.61''$. <br/>
What was the local mean solar time?
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

By equation $80$:
```math
\begin{align}
\Theta_L &= 128\degree\:14'\:48.61'' + 5^h\\
&= 203\degree\:14'\:48.61''
\end{align}
```
Then, by equation $79$ (See example $21$ for more details), we try $\Theta = 175 \text{ sdy } 203\degree$ $14'$ $48.61''$:
```math
\begin{align}
t &= (175\text{ sdy } + 203\degree\:14'\:48.61'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175.458333 \text{ dy}\\
&= 175\text{ dy }11:00:00
\end{align}
```
Which agrees with example $22$.\
$\blacksquare$

#### Example 24
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at standard time $t = 175.00 \text{  dy }$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree$ $40'$ $36.24''$. <br/>
What was the standard mean solar time of <i>apparent</i> noon on solar day $175$ at $l = 0\degree E$? <br/>
(The axial tilt $\varepsilon$ of $P$ is $25.5\degree$)
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

We mostly follow the previous example.\
Because $l = 0\degree$, $h_L = h$.
```math
h = \Theta - \alpha
```
Apparent noon is when $h_L$ of the Sun $= 0\degree$, therefore at apparent noon, $\Theta = \alpha$.\
Using equations $1$, $2,$ and $3$, and setting $\beta = 0\degree$ from the definition of the Ecliptic, we find:
```math
\Theta = \alpha = 214\degree\:52'\:37.04''.
```
Then, using the method of example $21$, we try $\Theta = 175 \text{ sdy } 215\degree$ $25'$ $50.5''$.
```math
\begin{align}
t &= (175 \text{ sdy } 214\degree\:52'\:37.04'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175.4905 \text{ dy } \\
&= 175 \text{ dy } 11:46:22
\end{align}
```
$\blacksquare$

However, in this example, $t = 175 \text{ dy } 11:46:22 \neq 175.00 \text{  dy }$! Thus, our $\lambda_{\text{Sun}}$ value would be off by some amount because the Sun would have moved during the $11h$ $46m$ $22s$.
Thus, this time only works as a preliminary approximation, and we will have to repeat our calculations if we want a better result.
#### Example 24-II
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
Using the fact that at $t = 175 \text{ dy } 11:46:22$, $\lambda_{\text{Sun}}$ was $218\degree$ $17'$ $12.78''$, <br/>
Improve the approximation of the time of apparent noon. 
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

Again, using equations $1$, $2,$ and $3$, we find:
```math
\Theta = \alpha = 215\degree\:28'\:9.28''.
```
Then repeating the method of example 21,
```math
\begin{align}
t &= (175\: \text{ sdy }\: 215\degree\:28'\:9.28'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175\: \text{ dy }\: 11:48:43
\end{align}
```
More repetition will improve our estimations even further, but they rapidly converge. (A third estimate using the longitude of the Sun at $11:48:43$ gives the time $11:48:44$.)

We can see that the time of apparent noon is not $12:00$. This difference is called the [Equation of Time](https://en.wikipedia.org/wiki/Equation_of_time), and the amount by it differs by changes throughout the year.\
$\blacksquare$

### Horizontal Coordinates
Let's now get to defining our coordinates.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/bba24e72-058d-41ad-84d5-e11d97a593d2" width="400"/> Let us say we want to describe the location of $P$. This can be done very simply with two angles, using spherical coordinates. First we drop $P$ down onto the local horizon to form $P'$. Then we can describe the position of $P$ by the angles $NOP'$ and $POP'$. The angle $NOP'$ is called the *azimuth* (denoted $A$, not to be confused with the $A$ in the diagram) and is measured from North with East as positive. The angle $POP'$ is called the *altitude* (denoted $a$). This system of coordinates is called the [*Horizonal Coordinate System*](https://en.wikipedia.org/wiki/Horizontal_coordinate_system).

The way of calculating the azimuth and altitude is again given with rotation matrices, just like in chapter $1$:
- **Equatorial to Horizontal:**
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
-\sin(\phi) & 0 & \cos(\phi) \\
0 & -1 & 0 \\ \tag{82}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
\cos(\delta) \cos(h) \\
\cos(\delta) \sin(h) \\
\sin(\delta)
\end{bmatrix}
```
Where $\phi$ is the latitude of observer and $h$ is the hour angle of $P$.

- **Horizontal to Equatorial (Does not change):**
```math
\begin{bmatrix}
\cos(\delta) \cos(h) \\
\cos(\delta) \sin(h) \\
\sin(\delta)
\end{bmatrix}
=
\begin{bmatrix}
-\sin(\phi) & 0 & \cos(\phi) \\
0 & -1 & 0 \\ \tag{83}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
```
The hour angle is used because it factors in both the rotation of the Earth and the right ascension of the star (equation $80$). 

Note that in older textbooks, the azimuth is defined starting from South and going West. This is not the IAU's definition of the azimuth anymore, and therefore the azimuth values given in older books would have to be shifted by $180\degree$ to match the modern definition.

#### Example 25
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at latitude $50\degree$, on solar day $175$ at local mean solar time $11:00:00$, <br/>
what were the horizontal coordinates of star $S$, with right acension $5^h$ and declension $+30\degree$?
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

In example $22$, we found the hour angle of $S$:
```math
h = 128\degree\:14'\:48.61''
```
Thus, using equation $82$:
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
-\sin(50\degree) & 0 & \cos(50\degree) \\
0 & -1 & 0 \\
\cos(50\degree) & 0 & \sin(50\degree)
\end{bmatrix}
\begin{bmatrix}
\cos(30\degree) \cos(128\degree\:14'\:48.61'') \\
\cos(30\degree) \sin(128\degree\:14'\:48.61'') \\
\sin(30\degree)
\end{bmatrix}
```
Thus
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
0.732080607\\
-0.680134006\\
0.038415077
\end{bmatrix}
```
Now, using equation $2$, we can find $A$ and $a$:
```math
\begin{align}
\rho &= 1 \text{ (Celestial Sphere has arbitrary radius)}\\
A &= \arctan(-0.680134006, +0.732080607)\\
&= 317\degree\:6'\:23.78''\\
a &= \arcsin(0.038415077/1)\\
&= 2\degree\:12'\:5.63''
\end{align}
```
$\blacksquare$

Using our knowledge, we can calculate the times of certain astronomical events involving certain altitudes or azimuths, questions such as:
- When does the Sun rise?
- When is the Moon's location due East?\
etc.

#### Example 26
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at standard time $t = 175.00\: \text{ dy }$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree\:40'\:36.24''$. <br/>
What was the mean solar time of sunrise on solar day $175$ at $\phi = 50\degree N$ and $l = 0\degree E$? <br/>
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

"Sunrise" means that the Sun is at the horizon, or more specifically, the Eastern horizon. This means that the altitude $a$ of the Sun is $0\degree$, and the hour angle of the sun $h$ is a negative number. (Remember, the hour angle is measured such that *West* is positive.)

Recall equation $82$.
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
-\sin(\phi) & 0 & \cos(\phi) \\
0 & -1 & 0 \\ 
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
\cos(\delta) \cos(h) \\
\cos(\delta) \sin(h) \\
\sin(\delta)
\end{bmatrix}
```

Because $z_{\text{horizontal}} = \sin(a)$, when $a = 0\degree$, $z_{\text{horizontal}} = 0$.\
So, let's set $z_{\text{horizontal}} = 0$ and solve for $h$.\
Carrying out the matrix multiplication only for $z$:
```math
\begin{align}
z_{\text{horizontal}} = 0 &= \cos(\phi)\cos(\delta) \cos(h) + 0\cdot\cos(\delta) \sin(h) + \sin(\phi)\sin(\delta)\\
&=\cos(\phi)\cos(\delta) \cos(h)+\sin(\phi)\sin(\delta)\\

\therefore \cos(h) &= -\frac{\sin(\phi)\sin(\delta)}{\cos(\phi)\cos(\delta)}\\
&=-\tan(\phi)\tan(\delta)\tag{84}
\end{align}
```
Equation $84$ is called the [Sunrise Equation](https://en.wikipedia.org/wiki/Sunrise_equation). However, it works for any celestial object, not just the Sun.\
Carrying on, we clearly need $\delta$, so, using equations $1$, $2$, and $3$, we calculate the equatorial coordinates.
```math
\begin{alignat}{4}
\delta &=-15&&\degree\:15&&'\:21.30&&''\\
\alpha &= 214&&\degree\:52&&'\:37.04&&''
\end{alignat}
```
Substituting $\phi$ and $\delta$:
```math
\displaylines{
\cos(h) = -\tan(50\degree)\tan(-15\degree\:15'\:21.3'')\\
\therefore h = \arccos(0.3250415)
}
```
Taking the negative arccosine value for $h$ (negative because sunrise), we get:
```math
h = -71\degree\:1'\:54.87''
```
From here we just need to find the mean time from the hour angle, so we follow example $23$.
```math
\displaylines{
h_L = \Theta_L - \alpha\\
\begin{align}
\therefore \Theta = \Theta_L &= h_L + \alpha  = h + \alpha\\
&=-71\degree\:1'\:54.87'' + 214\degree\:52'\:37.04''\\
&=143\degree\:50'\:42.17''\\

t &= (175\: \text{ sdy } \: 143\degree\:50'\:42.17'' + 180\degree) \cdot \frac{289.42}{290.42}\\
& = 175\: \text{ dy } \: 07:03:13
\end{align}
}
```
Just as with example $24$, this is just a preliminary approximation, and these calculations must be repeated for a more accurate time of sunrise.

At $t = 175 \text{ dy } 07:03:13$, $\lambda_\text{Sun} = 218\degree$ $2'$ $32.28''$.\
Converting to equatorial coordinates:
```math
\begin{alignat}{4}
\delta &=-15&&\degree\:23&&'\:05.06&&''\\
\alpha &= 215&&\degree\:13&&'\:54.03&&''
\end{alignat}
```
Thus the sunrise equation gives (again, taking the negative arccosine):
```math
h = -70\degree\:51'\:26.21''
```
Now we follow example $23$.
```math
\displaylines{
\begin{align}
\Theta &=144\degree\:22'\:27.82''\\
\therefore t &= 175\: \text{ dy } \: 07:05:19
\end{align}
}
```
Further repetition will better our approximations.\
$\blacksquare$

### Heliacal Rising

Because the Earth orbits the Sun, different parts of the sky are completely blocked out by the glare of the Sun in different seasons. The [heliacal rising](https://en.wikipedia.org/wiki/Heliacal_rising) of a star happens when a star becomes visible for the first time again after being blocked out by the glare of the Sun for some time.

Because the Sun's ecliptic longitude increases (i.e. the Sun moves East), the Stars with fixed right ascensions and declinations to the East of the Sun will eventually be blocked by the Sun's light, and re-emerge to the West of the Sun when it is visible again. Because a Western elongation implies a morning star, the heliacal rising happens when the Star is visible in the dawn again. The star will then rise earlier and earlier before the Sun, until it loops all the way around and becomes lost in the glare of the Sun again.

Let's try and find out when the heliacal rising of a star with right ascension $\alpha$ and declination $\delta$ will happen at a location with latitude $\phi$.

We estimate the heliacal rising to be the point when the star would rise exactly at sunrise, but in reality it is some days after this time because the Star still needs some time to be visible. Let's first say the Sun's ecliptic longitude to be $\lambda$. Then, the Sun's equatorial coordinates are given by equation $3$ (Keep in mind $\beta$ of the Sun is $0\degree$):
```math
\begin{align}
\alpha_S &= \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda))\\
\delta_S &= \arcsin(\sin(\varepsilon)\sin(\lambda))
\end{align}
```
Now we use the sunrise equation (equation $84$) to calculate the time of sunrise:
```math
\Theta_{\text{Sunrise}} = -\arccos(-\tan(\phi)\tan(\delta_S)) + \alpha_S
```
We now substitute $\alpha_S$ and $\delta_S$ with our calculations from before:
```math
\Theta_{\text{Sunrise}} = -\arccos(-\tan(\phi)\tan(\arcsin(\sin(\varepsilon)\sin(\lambda)))) + \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda))
```
Now we use the same equation to calculate the time of star rise:
```math
\Theta_{\text{Star-rise}} = -\arccos(-\tan(\phi)\tan(\delta)) + \alpha
```
These two times must equal:
```math
-\arccos(-\tan(\phi)\tan(\arcsin(\sin(\varepsilon)\sin(\lambda)))) + \arctan(\cos(\varepsilon)\sin(\lambda), \cos(\lambda)) = -\arccos(-\tan(\phi)\tan(\delta)) + \alpha \tag{85}
```
Since we know $\alpha$, $\delta$, $\phi$, and $\varepsilon$, we can solve this equation for $\lambda$. Once we have $\lambda$, we can reverse the methods of chapter $2$ to find the mean anomaly of the Earth and thus the date of heliacal rising.

#### Example 26
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

We put the values into equation $85$. The right hand side is:
```math
-\arccos(-\tan(30\degree)\tan(-16\degree\:42'\:58.02'')) + 06^h\:45^m\:08.92^s = 0.371275 \text{ rad}
```
Thus equation $85$ is:
```math
-\arccos(-\tan(30\degree)\tan(\arcsin(\sin(23.44\degree)\sin(\lambda)))) + \arctan(\cos(23.44\degree)\sin(\lambda), \cos(\lambda)) = 0.371275 \text{ rad}
```
Then we solve for $\lambda$ (a computer program was used):
```math
\lambda = 2.1139\text{ rad} = 121\degree\:7'
```
Thus $\lambda_{\text{Earth Heliocentric}} = 121\degree$ $7' + 180\degree = 301\degree$ $7'$.\
Now we follow example $4$ (Chapter $2$).
```math
\begin{align}
\nu &= 301\degree\:7' - 102\degree\:56'\:49.9''\\
&= 198\degree\:10'\:13.29''\\
\end{align}
```
$\nu$ is bigger than $180\degree$, so:
```math
\begin{align}
E &= 2\pi - \arccos\left(\frac{0.0167 + \cos(198\degree\:10'\:13.29'')}{1 + 0.0167\cos(198\degree\:10'\:13.29'')}\right)\\
&= 3.463975 \text{ rad}\\
\therefore M &= 3.463975 - 0.0167\sin(3.463975)\\
&= 3.469266 \text{ rad}\\
\therefore t &= \frac{3.469266}{2\pi}\cdot365.24\text{ dy}\\
&= 202\text{ dy }
\end{align}
```
$202\text{ dy}$ after $\text{January 3, }2024$ is $\text{July 23, }2024$. Adding about a week to give Sirius time to actually be visible, we get $\text{July 30, }2024$. This is almost exact: the heliacal rising of Sirius happens around $\text{July 30}$ to $\text{August 1}$.

The ancient Egyptians thought of this event to have immense significance simply because it coincided with the beginning of the flooding season of the Nile river by coincidence.\
$\blacksquare$
