## V. Time
Let us talk about how time and date are measured in astronomy.

### Sidereal and Solar time
When measuring time, two types of time must be distinguished:
 - The [Mean Solar Time](https://en.wikipedia.org/wiki/Solar_time) (denoted $T$)
   * This is the time that bases itself off the Sun. This is the time that all of us are used to. The **average** time of noon (when the Sun is at its highest point in the sky) is $12:00$, or $.5$ (solar) days, and the **average** time of midnight (when the Sun is at its lowest point in the sky) is $00:00$, or $.0$ (solar) days. The Solar day is also called the *synodic day*
 - The [Sidereal Time](https://en.wikipedia.org/wiki/Sidereal_time) (denoted $\Theta$)
   * <ins>This is the time that bases itself off the rotation of the Earth</ins>. Contrary to popular belief, the rotation period of the Earth is not equal to one solar day. It is instead equal to one sidereal day. These two times are different due to the orbit of the Earth around the Sun. One sidereal day after some point in time, the distant stars will return to the same position in the sky, but because the Earth has orbited the sun and has moved in that time period (or, from the Earth's perspective, the Sun has moved), the Sun will have not retuend to the same position. Therefore there is a discrepancy between the two times.
   * It is defined as the angle between the local meridian (the North-South-Zenith-Nadir plane) and the hour plane of Aries (the Celestial North-Celestial South-Aries plane). Thus, $0$ **sidereal time is not when Aries is lowest in the sky, but it is when Aries is at the highest point in the sky.**
   * Sidereal time is often measured in degrees of Earth's rotation.

A further investigation into the difference between the two times: as mentioned earlier, after one sidereal day, the Earth is facing the same point in the sky, and thus the stars will have returned to the same point in the sky. However, because the Earth has orbited an amount around the Sun in that time period, the Sun will not have returned to the same position in the sky. \
So how long is a solar day in comparison to a sidereal day? Well, think about it this way:
- Say at time $0$, the Prime Meridian of the Earth is facing away from the Sun, and the Sun is exactly at Aries.
- Say $n$ sidereal days after some date, the Earth is at the opposite end of its orbit.
- Then, the Prime Meridian will still be pointing towards Aries, but now it is facing the Sun instead of away. This means that there was $0.5$ more sidereal days in that time period than there were Solar days.
- Thus, there is exactly $1$ more sidereal day in $1$ year than there are Solar days.

- The same argument applies for retrograde rotation, but there is $1$ fewer sidereal days than Solar days.

Thus, since there are $Y\pm1$ sidereal days per $Y$ synodic days, where $Y$ is the length of the year in **solar days**,
```math
\text{Sidereal Day} = \frac{Y}{Y \pm 1} \cdot \text{Solar Day}\tag{6}
```
#### Example 2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth has an orbital period of $365.2422$ Earth Solar days while Venus has an orbital period of $1.92$ Venusian Solar days. <br/>
Calculate the length of the sidereal day on Earth and Venus, keeping in mind Venus has a retrograde rotation. <br>
(The length of an Earth Solar day is $24$ hours while the length of a Venusian Solar day is $116.75$ Earth Solar days.)
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We use equation $6$.\
Since Earth has a prograde orbit,
```math
\text{Sidereal Day Length} = \frac{Y}{Y + 1} \cdot \text{Solar Day Length}
```
Substituting the numbers,
```math
\text{Earth Sidereal Day Length} = \frac{365.2422}{365.2422 + 1} \cdot 24 h = 23h\enspace 56m\enspace 4s
```

Since Venus has a retrograde orbit,
```math
\text{Sidereal Day Length} = \frac{Y}{Y - 1} \cdot \text{Solar Day Length}
```
Substituting the numbers,
```math
\text{Venus Sidereal Day Length} = \frac{1.92}{1.92 - 1} \cdot 116.75\enspace \text{dy} = 243\enspace \text{dy}
```
Comparing these values to Wikipedia, we can see we are correct.\
$\blacksquare$

<br/>

* Due to random fluctuations in the rotation rate of the Earth, the length of the sidereal day fluctuates by a second or two. *We will ignore this for the purposes of worldbuilding.*

### Converting between Times

The prime meridian is the reference longitude on the Earth. This is where longitude is measured from, and it is also where the standard time is measured. All other solar times can be converted to standard time via this formula:
```math
\text{Standard Time } (T) = \text{Local Time} - \frac{l / 360\degree}{\text{Solar Day Length}}\tag{7}
```
Where $l$ is the local longitude (East is positive).\
If the time is given as an angle, the following formula is perfectly viable:
```math
\text{Standard Time } (T) = \text{Local Time} - l \tag{8}
```

<ins>The benefit to worldbuilding is that we can decide when time $0$ and when day $0$ is.</ins> **Here, we define time $0$ to be the time of Spring Equnox on the prime meridian, and we shall also, for the sake of convenience, also say that the Spring Equinox happened at exactly midnight.** This means, that at solar time (T) $= 0$, the sidereal time was exactly $-0.5$ sidereal days, as Aries (coincident with the Sun) was at midnight.

Under this presumption, the conversion from Solar time to sidereal time is very easy. Since the length of a sidereal day is exactly $Y/(Y\pm1)$ of a solar day, we just multiply the time elapsed, in days, from $T = 0$ by $(Y\pm1)/Y$ to get the sidereal time, then subtract by $0.5$ sidereal days to account for the fact that Aries was at midnight at $T = 0$.
```math
\Theta = \frac{Y \pm 1}{Y} \cdot T - 0.5 \tag{9}
```

#### Example 3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
An observation was made on planet $P$ on solar day $175$ at solar time $05:16:34$ at $l=165\degree E$. <br/>
Calculate the standard sidereal time at the time of the observation. <br/>
(Assume a year length of $289.42$ solar days, a solar day length of $24$ hours, and prograde rotation.)
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

First, using equation $7$, we determine the standard time of observation.
```math
\begin{align}
\text{Standard Time } (T) &= 05:16:34 - \frac{165\degree/360\degree}{24h} \\
&= 05:16:34 - 11h \\
&= -1\enspace \text{dy} \enspace 18:16:34
\end{align}
```
Where $\text{dy}$ means Solar days.\
This means the standard time at the time of observation was solar day $174$ at $18:16:34$, or at $T = 174.7615$ days.\
Then, using equation $9$:
```math
\Theta \text{ (in days)} = \frac{289.42 + 1}{289.42} \cdot 174.7615 - 0.5 = 174.8653$
```
Thus the standard sidereal time at the time of measurement was sidereal day $174,\enspace311\degree\enspace31'\enspace12.25''$. \
This can be interpreted as the fact that at the time of measurement, at the prime meridian, the cusp of aries had rotated $311\degree\enspace31'\enspace12.25''$ from the meridian, or in other words: ***the right ascension of the prime meridian was*** $311\degree\enspace31'\enspace12.25'' = 20^h\enspace46^m\enspace4.82^s$.

Furthermore, the local sidereal time can be calculated by equation $8$:
```math
\Theta_{\text{local}} = \Theta_{\text{standard}} + l = 175\enspace \text{sdy}\enspace116\degree\enspace31'\enspace12.25''
```
Where $\text{sdy}$ means sidereal days.\
$\blacksquare$

To convert from sidereal time to mean solar time, it is harder. Often, from later on calculations that give us the sidereal time of an event, the whole part of the sidereal time will not be apparent. Therefore we must guess by knowing the solar date. However, equation $9$ still holds.
#### Example 4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ on local solar day $175$, an observation was made at $l = 165\degree E$ at local sidereal time $116\degree\enspace31'\enspace12.25''.$ <br/>
Calculate the standard mean solar time.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We convert to standard sidereal time by subtracting the longitude:
```math
\text{Standard } \Theta = 116\degree\enspace31'\enspace12.25'' - 165\degree = -1\enspace \text{sdy} \enspace311\degree\enspace31'\enspace 12.25''\tag{i}
```
We then find the sidereal day corresponding to solar day $175$:
```math
\Theta_{T=175.00} = \frac{290.42}{289.42} \cdot 175 - 0.5 = 175\enspace \text{sdy}\enspace37\degree\enspace40'\enspace36.24''
```
Which we truncate to:
```math
\Theta_{T=175.00} = 175\enspace \text{sdy} \tag{ii}
```
Combining the results from $(\text{i})$ and $(\text{ii})$, we try $\Theta = 175\enspace \text{sdy} -1\enspace \text{sdy} \enspace311\degree\enspace31'\enspace12.25''$.\
Using equation $9$ with $0.5$ sidereal days $= 180\degree$,
```math
\begin{align}
T &= (174\enspace \text{sdy}\enspace 311\degree\enspace31'\enspace12.25'' + 180\degree) \cdot \frac{289.42}{290.42} \\
&= 174.7615\enspace \text{dy}\\
&= 174\enspace \text{dy} \enspace 18:16:34
\end{align}
```
If we add $l$ to $T$, we can see we get local solar day $175$, matching with the local observation date. \
If we had gotten for this value local solar day $174$, we would try again but with $\Theta_{T=175.00}$ to be $1$ higher. (In our case, $\Theta_{T=175.00} = 176\enspace \text{sdy}$.)\
$\blacksquare$

### The Hour Angle
The [hour angle](https://en.wikipedia.org/wiki/Hour_angle), as defined earlier, is the angle between the meridian plane and the hour plane. **This value is measured with West as positive.**

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/743585dd-02e4-41f2-ba17-18ecfa2a35cc" width="400"/> In the diagram, the Eastern angle between Aries and the Prime Meridian (the right ascension of the Prime Meridian) is the standard sidereal time ($\Theta$), and the Eastern angle between Aries and the Local Meridian is the local standard time ($\Theta_L$). The Eastern angle between Aries and the Star is, by definition, the right ascension of the star ($\alpha$). Furthermore, the Eastern angle between the Prime Meridian and the Local Meridian is the longitude $l$. (Eastern angle meaning the angle measured in the Eastern direction.)

The Western angle between the Prime Meridian and the Star is known as the Standard Hour Angle of the star ($h$), and the Western angle between the Local Meridian and the Star is known as the Local Hour Angle of the star ($h_L$).

<br/>
<br/>
<br/>

It is therefore evident that 
```math
h_L = \Theta_L - \alpha\tag{10}
```
and because $\Theta_L = \Theta + l$ (equations $7$ and $8$):

```math
h_L = \Theta + l - \alpha\tag{11}
```

When $h_L = 0$, the star is coincident with the meridian, and the star is at the highest point in the sky. If $h_L = 180\degree$, the star is coincident with the lower meridian, and it is at the lowest point in the sky. If the star in question is the Sun, then the times at which $h_L = 0$ and $h_L = 180\degree$ are called *apparent noon* and *apparent midnight* respectively. These are not the same as the *mean noon* and *mean midnight*, the mean values are simply the average of the apparent values over the year. (Yes, this means noon and midnight aren't always at $12:00$ and $00:00$!)

#### Example 5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at standard time $T = 175.00\enspace \text{dy}$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree\enspace40'\enspace36.24''$. <br/>
What was the mean Solar time of <i>apparent</i> noon on Solar day $175$ at $l = 0\degree E$? <br/>
(The axial tilt $\varepsilon$ of $P$ is $25.5\degree$)
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Recall equation $11$:
```math
h_L = \Theta + l - \alpha
```
Because $l = 0\degree$, $h_L = h$.
```math
h = \Theta - \alpha
```
Apparent noon is when $h_L$ of the Sun $= 0\degree$, therefore at apparent noon, $\Theta = \alpha$.\
Using equations $1$, $2,$ and $3$, and setting $\beta = 0\degree$ from the definition of the Ecliptic, we find:
```math
\Theta = \alpha = 214\degree\enspace52'\enspace37.04''.
```
Then, using the method of Example $4$, we try $\Theta = 175\enspace \text{sdy}\enspace 215\degree\enspace25'\enspace50.5''$.
```math
\begin{align}
T &= (175\enspace \text{sdy}\enspace 214\degree\enspace52'\enspace37.04'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175.4905\enspace \text{dy} \\
&= 175\enspace \text{dy} \enspace 11:46:22
\end{align}
```
$\blacksquare$

However, in this example, $T = 175\enspace \text{dy} \enspace 11:46:22 \neq 175.00\enspace \text{dy}$! Thus, our $\lambda_{\text{Sun}}$ value would be off by some amount because the Sun would have moved during the $11h\enspace46m\enspace22s$.
Thus, this time only works as a preliminary approximation, and we will have to repeat our calculations if we want a better result.
#### Example 5-II
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Using the fact that at $T = 175\enspace \text{dy} \enspace 11:46:22$, $\lambda_{\text{Sun}}$ was $218\degree\enspace17'\enspace12.78''$, <br/>
Improve the approximation of the time of apparent noon. <br/>
(The calculation of $\lambda_{\text{Sun}}$ will be detailed in future chapters.)
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

Again, using equations $1$, $2,$ and $3$, we find:
```math
\Theta = \alpha = 215\degree\enspace28'\enspace9.28''.
```
Repeating the method of Example 4,
```math
\begin{align}
T &= (175\enspace \text{sdy}\enspace 215\degree\enspace28'\enspace9.28'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175\enspace \text{dy}\enspace 11:48:43
\end{align}
```
More repetition will improve our estimations even further, but they rapidly converge. (A third estimate gives the time $11:48:44$.)

We can see that the time of apparent noon is not $12:00$. This difference is called the [Equation of Time](https://en.wikipedia.org/wiki/Equation_of_time), and the amount by it differs by changes throughout the year.
$\blacksquare$

### Horizontal Coordinates using Sidereal Time

Using our knowledge, we can calculate the times of certain astronomical events involving certain altitudes or azimuths, questions such as:
- When does the Sun rise?
- When is the Moon's location due East?\
etc.

#### Example 6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at standard time $T = 175.00\enspace \text{dy}$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree\enspace40'\enspace36.24''$. <br/>
What was the mean Solar time of sunrise on Solar day $175$ at $\phi = 50\degree N$ and $l = 0\degree E$? <br/>
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

"Sunrise" means that the Sun is at the horizon, or more specifically, the eastern horizon. This means that the altitude $a$ of the Sun is $0\degree$, and the hour angle of the sun $h$ is a negative number. (Remember, the hour angle is measured such that *West* is positive.)

Recall equation $5$.
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
\sin(\phi) & 0 & -\cos(\phi) \\
0 & 1 & 0 \\
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
&=-\tan(\phi)\tan(\delta)\tag{12}
\end{align}
```
Equation $12$ is called the [Sunrise Equation](https://en.wikipedia.org/wiki/Sunrise_equation). However, it works for any celestial object, not just the Sun.\
Carrying on, we clearly need $\delta$, so, using equations $1$, $2$, and $3$, we calculate the equatorial coordinates.
```math
\begin{alignat}{4}
\delta &=-15&&\degree\enspace15&&'\enspace21.30&&''\\
\alpha &= 214&&\degree\enspace52&&'\enspace37.04&&''
\end{alignat}
```
Substituting $\phi$ and $\delta$:
```math
\displaylines{
\cos(h) = -\tan(50\degree)\tan(-15\degree\enspace15'\enspace21.3'')\\
\therefore h = \arccos(0.3250415)
}
```
Taking the negative arccosine value for h (negative because sunrise), we get:
```math
h = -71\degree\enspace1'\enspace54.87''
```
From here we just need to find the mean time from the hour angle, so we follow Example $5$.
```math
\displaylines{
h_L = \Theta_L - \alpha\\
\begin{align}
\therefore \Theta = \Theta_L &= h_L + \alpha  = h + \alpha\\
&=-71\degree\enspace1'\enspace54.87'' + 214\degree\enspace52'\enspace37.04''\\
&=143\degree\enspace50'\enspace42.17''\\

T &= (175\enspace \text{sdy} \enspace 143\degree\enspace50'\enspace42.17'' + 180\degree) \cdot \frac{289.42}{290.42}\\
& = 175\enspace \text{dy} \enspace 07:03:13
\end{align}
}
```
Just as with Example $5$, this is just a preliminary approximation, and these calculations must be repeated for a more accurate time of sunrise.

At $T = 175\enspace \text{dy} \enspace 07:03:13$, $\lambda_\text{Sun} = 218\degree\enspace2'\enspace32.28''$. (Again, the method of calculation of $\lambda_{\text{Sun}}$ will be shown in future chapters.)

Converting to equatorial coordinates:
```math
\begin{alignat}{4}
\delta &=-15&&\degree\enspace23&&'\enspace5.06&&''\\
\alpha &= 215&&\degree\enspace13&&'\enspace54.03&&''
\end{alignat}
```
Thus the sunrise equation gives (again, taking the negative arccosine):
```math
h = -70\degree\enspace51'\enspace26.21''
```
Now we follow Example $5$.
```math
\displaylines{
\begin{align}
\Theta &=144\degree\enspace22'\enspace27.82''\\
\therefore T &= 175\enspace \text{dy} \enspace 07:05:19
\end{align}
}
```
Further repetition will better our approximations.\
$\blacksquare$
<br/>
<br/>

Also, using the relation between the hour angle and the sidereal time, equation $5$ can be rewritten:
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
\sin(\phi) & 0 & -\cos(\phi) \\
0 & 1 & 0 \\ \tag{13}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
\cos(\Theta_L) & \sin(\Theta_L) & 0 \\
\sin(\Theta_L) & -\cos(\Theta_L) & 0 \\
0 & 0 & 1
\end{bmatrix}
\begin{bmatrix}
x_{\text{equatorial}} \\ y_{\text{equatorial}} \\ z_{\text{equatorial}}
\end{bmatrix}
```

