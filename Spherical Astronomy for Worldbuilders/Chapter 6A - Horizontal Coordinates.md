## VI. Horizontal Coordinates
Let's define a set of coordinates that we can use to describe the location of objects from the view of an observer on the ground.

### The Hour Angle

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/5b1c3310-b4f1-4e70-b954-f4f68287a381" width="300"/> Consider this diagram. 

This diagram depicts the celestial sphere around an observer at point $O$. The gray plane is the local horizon. $ON$, $OS$, $OE$, and $OW$, are the local directions of North, South, East, and West respectively. $N'$ and $S'$ depict the celestial poles, and thus the line $N'S'$ is the Earth's rotational axis, and therefore the plane perpendicular to $N'$ and $S'$ is the Earth's equatorial plane. Therefore, the angle $N'ON$ defines the observer's local latitude $\phi$. $Z$ and $A$ are the observer's Zenith and Nadir respectively.

The plane (or circle) $NZSA$ defines the local meridian. 

In the last chapter, we saw how we could define the sidereal time as the Western distance between Aries and the Meridian. Now we are interested in the point $P$, which may be the location of a star or a planet. We can do the same thing, and we can define the angle between the Meridian and $P$, putting West as positive again. This angle is called the [**hour angle**](https://en.wikipedia.org/wiki/Hour_angle) and is more rigorously defined as the angle between the meridian circle and the circle that goes through $P$, $N'$, and $S'$, which is called the [hour circle](https://en.wikipedia.org/wiki/Hour_circle) of $P$. This is useful as it gives us a way to describe the location of $P$, specifically how East or West it is, in comparison to the meridian.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/743585dd-02e4-41f2-ba17-18ecfa2a35cc" width="400"/> In this diagram, the Western angle between the Prime Meridian and Aries (the right ascension of the Prime Meridian) is the standard sidereal time ($\Theta$), and the Western angle between the Local Meridian and Aries (the right ascension of the Local Meridian) is the local standard time ($\Theta_L$), as we saw in the last chapter. The Eastern angle between Aries and the Star is, by definition, the right ascension of the star ($\alpha$). Furthermore, the Eastern angle between the Prime Meridian and the Local Meridian is the longitude $l$. (Eastern angle meaning the angle measured in the Eastern direction.)

The Western angle between the Prime Meridian and the Star is then known as the Standard Hour Angle of the star ($h$), and the Western angle between the Local Meridian and the Star is known as the Local Hour Angle of the star ($h_L$).

<br/>
<br/>

It is therefore evident that 
```math
h_L = \Theta_L - \alpha\tag{6.1}
```
and because $\Theta_L = \Theta + l$ (equations $5.2$ and $5.3$):

```math
\displaylines{
\begin{align}
h_L &= \Theta + l - \alpha\\
&= h + l
\end{align}
}\tag{6.2}
```

When $h_L = 0$, the star is coincident with the meridian, and the star is at the highest point in the sky. If $h_L = 180\degree$, the star is coincident with the lower meridian, and it is at the lowest point in the sky. If the star in question is the Sun, then the times at which $h_L = 0$ and $h_L = 180\degree$ are called *apparent noon* and *apparent midnight* respectively. These are not the same as the *mean noon* and *mean midnight*, the mean values are simply the average of the apparent values over the year. (Yes, this means noon and midnight aren't always at $12:00$ and $00:00$!)

#### Example 6.1
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
We need the sidereal time, so by equation $5.4$:
```math
\begin{align}
\Theta_L &= \frac{289.42+1}{289.42} \cdot 175.458333 - 0.5\\
&= 175\text{ sdy } 203\degree\:14'\:48.61''
\end{align}
```

Then, by equation $6.1$:
```math
\begin{align}
h_L &= 203\degree\:14'\:48.61'' - 5^h\\
&= 128\degree\:14'\:48.61''
\end{align}
```
$\blacksquare$

#### Example 6.2
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$, at some time during solar day $175$, the hour angle of star $S$ (with right acension $5^h$) was $128\degree\:14'\:48.61''$. <br/>
What was the local mean solar time?
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

By equation $6.1$:
```math
\begin{align}
\Theta_L &= 128\degree\:14'\:48.61'' + 5^h\\
&= 203\degree\:14'\:48.61''
\end{align}
```
We now follow example $5.3$: we try $\Theta = 175 \text{ sdy } 203\degree$ $14'$ $48.61''$:
```math
\begin{align}
t &= (175\text{ sdy } + 203\degree\:14'\:48.61'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175.458333 \text{ dy}\\
&= 175\text{ dy }11:00:00
\end{align}
```
Which agrees with example $6.1$.\
$\blacksquare$

#### Example 6.3
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
Using equations $1.1$, $1.2$, and $1.3$, and setting $\beta = 0\degree$ from the definition of the Ecliptic, we find:
```math
\Theta = \alpha = 214\degree\:52'\:37.04''.
```
Then, using the method of example $5.3$, we try $\Theta = 175 \text{ sdy } 215\degree$ $25'$ $50.5''$.
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
#### Example 6.3-II
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

Again, using equations $1.1$, $1.2$, and $1.3$, we find:
```math
\Theta = \alpha = 215\degree\:28'\:9.28''.
```
Then repeating the method of example $5.3$,
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

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/bba24e72-058d-41ad-84d5-e11d97a593d2" width="300"/> Let us say we want to describe the location of $P$. This can be done very simply with two angles, using spherical coordinates. First we drop $P$ down onto the local horizon to form $P'$. Then we can describe the position of $P$ by the angles $NOP'$ and $POP'$. The angle $NOP'$ is called the *azimuth* (denoted $A$, not to be confused with the $A$ in the diagram) and is measured from North with East as positive. The angle $POP'$ is called the *altitude* (denoted $a$). This system of coordinates is called the [*Horizonal Coordinate System*](https://en.wikipedia.org/wiki/Horizontal_coordinate_system).

The way of calculating the azimuth and altitude is again given with rotation matrices, just like in chapter $1$:
- **Equatorial to Horizontal:**
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
-\sin(\phi) & 0 & \cos(\phi) \\
0 & -1 & 0 \\ \tag{6.3}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
\cos(\delta) \cos(h) \\
\cos(\delta) \sin(h) \\
\sin(\delta)
\end{bmatrix}
```
Where $\phi$ is the latitude of observer and $h$ is the **local** hour angle of $P$.

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
0 & -1 & 0 \\ \tag{6.4}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
```
The hour angle is used because it factors in both the rotation of the Earth and the right ascension of the star (equation $6.1$). 

Note that in older textbooks, the azimuth is defined starting from South and going West. This is not the IAU's definition of the azimuth anymore, and therefore the azimuth values given in older books would have to be shifted by $180\degree$ to match the modern definition.

#### Example 6.4
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

In example $6.1$, we found the hour angle of $S$:
```math
h = 128\degree\:14'\:48.61''
```
Thus, using equation $6.3$:
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
Now, using equation $1.2$, we can find $A$ and $a$:
```math
\begin{align}
\rho &= 1 \text{ (Celestial Sphere has arbitrary radius)}\\
A &= \arctan(-0.680134006, +0.732080607)\\
&= 317\degree\:6'\:23.78''\\
a &= \arcsin(0.038415077/1)\\
&= 2\degree\:12'\:5.63''
\end{align}
```
We can see that $S$ was in the Northwest ($270\degree < A < 360\degree$) and very close to the horizon.\
$\blacksquare$

### The Sunrise Equation
Let's calculate the time of sunrise. "Sunrise" means that the Sun is at the horizon, or more specifically, the Eastern horizon. This means that the altitude $a$ of the Sun is $0\degree$, and the hour angle of the sun $h$ is a negative number. (Remember, the hour angle is measured such that *West* is positive.)

Recall equation $6.3$.
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
&=-\tan(\phi)\tan(\delta)\tag{6.5}
\end{align}
```
Equation $6.5$ is called the [Sunrise Equation](https://en.wikipedia.org/wiki/Sunrise_equation). However, it can be used to calculate the rising time of any celestial object, not just the Sun. If the positive arccosine value is taken, then the formula will calculate the setting time instead.

Notice that if $\phi > \arctan(\cot(\delta))$, then the sunrise equation predicts $\cos(h) > 1$ which is impossible. Likewise, if $\phi < -\arctan(\cot(\delta))$, then $\cos(h) < -1$ which is also impossible. This means that the object will not rise or set in these latitudes. In particular, if $\cos(h) > 1$, then the object is perpetually below the horizon. If $\cos(h) < -1$, then the object is perpetually up.

#### Example 6.5
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

To use the sunrise equation (equation $6.5$), we clearly need $\delta$, so, using equations $1.1$, $1.2$, and $1.3$, we calculate the equatorial coordinates.
```math
\begin{alignat}{4}
\delta &=-15&&\degree\:15&&'\:21.30&&''\\
\alpha &= 214&&\degree\:52&&'\:37.04&&''
\end{alignat}
```
Substituting $\phi$ and $\delta$ into equation $6.5$:
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
From here we just need to find the mean time from the hour angle, so we follow example $6.2$.
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
Just as with example $6.3$, this is just a preliminary approximation, and these calculations must be repeated for a more accurate time of sunrise.

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
Now we follow example $6.2$.
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

Note that the sunrise equation calculates when the center of the Sun (or any other object) is at the horizon. Because things have an apparent angular size in the sky, this means that the sunrise equation calculates at what hour angle exactly half of the object is visible. To calculate the precise time of first or last visibility, this angular size must be taken into account by calculating when the object's altitude would be 1 apparent radius (see chapter $4$) below the horizon (instead of the altitude being precisely $0\degree$), which we did not do here.

The equation can also be written to solve for the hour angle of an object at any altitude $a$:
```math
\cos(h) = \frac{\sin(a)-\sin(\phi)\sin(\delta)}{\cos(\phi)\cos(\delta)} \tag{6.5*}
```

Furthermore, objects near the horizon have their positions significantly altered by [atmospheric refraction](https://en.wikipedia.org/wiki/Atmospheric_refraction) (upto about $30'$ for our Earth), which depends on the density and composition of the atmosphere and the specific weather conditions of the time and location. However, this is far too complicated to go into any detail here, especially since existing formulae only apply to the Earth's atmosphere and in a worldbuilding setting they won't be accurate, so we will be assuming an airless environment in our calculations.

### The Terminator
The [*terminator*](https://en.wikipedia.org/wiki/Terminator_(solar)) is the line separating night and day at any moment in time. Let's say at standard solar time $t$, the standard sidereal time was $\Theta$. To find the terminator, we find the places where the Sun is rising or setting, i.e. we use the sunrise equation:
```math
\cos(h) = -\tan(\phi)\tan(\delta)
```
Therefore:
```math
h = \begin{cases}
-\arccos(-\tan(\phi)\tan(\delta)) & \text{ Sunrise}\\
\arccos(-\tan(\phi)\tan(\delta)) & \text{ Sunset}
\end{cases}
```
but by equation $6.2$, $h = \Theta + l - \alpha$, so:
```math
l = \begin{cases}
-\arccos(-\tan(\phi)\tan(\delta)) - \Theta + \alpha & \text{ Sunrise}\\
\arccos(-\tan(\phi)\tan(\delta)) - \Theta + \alpha & \text{ Sunset}
\end{cases}\tag{6.6}
```
#### Example 6.6
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
Find the terminator on $\text{June 21, }2023$ at standard solar time $14:56:00$. <br/>
$\lambda_{\text{Sun}} = 90\degree$, $\Theta = 133\degree$ $33'$ $1''$, and $\varepsilon = 23.44\degree$.
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

By equation $1.3$:
```math
\begin{align}
\alpha &= 90\degree\\
\delta &= 23\degree\:26'\:24''
\end{align}
```
Thus the limits of sunrise and sundown are:
```math
\phi = \pm\arctan(\cot(23\degree\:26'\:24'')) = \pm66\degree\:33'\:36''
```
Now we use equation $6.6$.\
For $\phi = 0\degree$:
```math
l = \begin{cases}
-\arccos(-\tan(0\degree)\tan(23\degree\:26'\:24'')) - 133\degree\:33'\:1'' + 90\degree & \text{ Sunrise}\\
= 226\degree\:26'\:59'' &  \text{ Sunrise} \\
\arccos(-\tan(0\degree)\tan(23\degree\:26'\:24'')) - 133\degree\:33'\:1'' + 90\degree & \text{ Sunset}\\
= 46\degree\:26'\:59'' & \text{ Sunset}
\end{cases}
```
Filling out for $66\degree$ $33'$ $36''\leq\phi\leq66\degree$ $33'$ $36''$:
```math
\begin{array}{|c|c|c|}\hline \phi & l \text{ of Sunrise} & l \text{ of Sundown}\\ \hline
66\degree\:33'\:36'' & 136\degree\:27' & 136\degree\:27'\\
60\degree & 177\degree\:47' & 95\degree\:7'\\
50\degree & 195\degree\:20' & 77\degree\:34'\\
40\degree & 205\degree\:7' & 67\degree\:47'\\
30\degree & 211\degree\:57' & 60\degree\:57'\\
20\degree & 217\degree\:22' & 55\degree\:32'\\
10\degree & 222\degree\:4' & 50\degree\:50'\\
0\degree & 226\degree\:27' & 46\degree\:27'\\
-10\degree & 230\degree\:50' & 42\degree\:4'\\
-20\degree & 235\degree\:32' & 37\degree\:22'\\
-30\degree & 240\degree\:57' & 31\degree\:57'\\
-40\degree & 247\degree\:47' & 25\degree\:7'\\
-50\degree & 257\degree\:34' & 15\degree\:20'\\
-60\degree & 275\degree\:7' & 357\degree\:47'\\
-66\degree\:33'\:36'' & 316\degree\:27' & 316\degree\:27'\\ \hline
\end{array}
```
Plotting all these points on a map and connecting the dots, we get:
<p align="center">
  <img width="450" src="https://github.com/CitruzSquared/essays/assets/23460281/26c676ad-d825-4f04-846a-e6ff4abbbbd8"> <br/>
  The Earth's terminator on $\text{June 21, }2023$ at $14:56:00$. <br/>
  It is daytime in the light part and nighttime in the dark part. <br/>
  <img width="450" src="https://github.com/CitruzSquared/essays/assets/23460281/0af4ffe1-757c-40c5-801d-9001a14c646d"> <br/>
  The Earth's terminator on $\text{June 21, }2023$ at $14:56:00$ from <a href="https://www.timeanddate.com/">timeanddate.com</a>. <br/>
  On this map, our calculations correspond to the border of the lightest shade of black. <br/>
  The Sun and Moon icons show the subsolar and sublunar points (to be discussed later).
</p>

$\blacksquare$

### The Ascending Sign
(Continued in Part B...)
