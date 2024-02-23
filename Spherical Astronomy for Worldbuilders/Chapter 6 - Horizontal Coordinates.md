## VI. Horizontal Coordinates

- **Equatorial to Horizontal:**
```math
\begin{bmatrix}
x_{\text{horizontal}} \\ y_{\text{horizontal}} \\ z_{\text{horizontal}}
\end{bmatrix}
=
\begin{bmatrix}
\sin(\phi) & 0 & -\cos(\phi) \\
0 & 1 & 0 \\ \tag{5}
\cos(\phi) & 0 & \sin(\phi)
\end{bmatrix}
\begin{bmatrix}
\cos(\delta) \cos(h) \\
\cos(\delta) \sin(h) \\
\sin(\delta)
\end{bmatrix}
```
Where $\phi =$ Latitude of Observer.



### The Hour Angle
The [hour angle](https://en.wikipedia.org/wiki/Hour_angle), as defined earlier, is the angle between the meridian plane and the hour plane. **This value is measured with West as positive.**

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/743585dd-02e4-41f2-ba17-18ecfa2a35cc" width="400"/> In the diagram, the Eastern angle between Aries and the Prime Meridian (the right ascension of the Prime Meridian) is the standard sidereal time ($\Theta$), and the Eastern angle between Aries and the Local Meridian is the local standard time ($\Theta_L$). The Eastern angle between Aries and the Star is, by definition, the right ascension of the star ($\alpha$). Furthermore, the Eastern angle between the Prime Meridian and the Local Meridian is the longitude $l$. (Eastern angle meaning the angle measured in the Eastern direction.)

The Western angle between the Prime Meridian and the Star is known as the Standard Hour Angle of the star ($h$), and the Western angle between the Local Meridian and the Star is known as the Local Hour Angle of the star ($h_L$).

<br/>
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
On planet $P$ at standard time $t = 175.00 \text{  dy }$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree$ $40'$ $36.24''$. <br/>
What was the mean Solar time of <i>apparent</i> noon on Solar day $175$ at $l = 0\degree E$? <br/>
(The axial tilt $\varepsilon$ of $P$ is $25.5\degree$)
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

Recall equation $81$:
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
\Theta = \alpha = 214\degree\:52'\:37.04''.
```
Then, using the method of Example $21$, we try $\Theta = 175 \text{ sdy } 215\degree$ $25'$ $50.5''$.
```math
\begin{align}
t &= (175\: \text{ sdy }\: 214\degree\:52'\:37.04'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175.4905\: \text{ dy } \\
&= 175\: \text{ dy } \: 11:46:22
\end{align}
```
$\blacksquare$

However, in this example, $t = 175 \text{ dy } 11:46:22 \neq 175.00 \text{  dy }$! Thus, our $\lambda_{\text{Sun}}$ value would be off by some amount because the Sun would have moved during the $11h$ $46m$ $22s$.
Thus, this time only works as a preliminary approximation, and we will have to repeat our calculations if we want a better result.
#### Example 22-II
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
Repeating the method of Example 21,
```math
\begin{align}
t &= (175\: \text{ sdy }\: 215\degree\:28'\:9.28'' + 180\degree) \cdot \frac{289.42}{290.42}\\
&= 175\: \text{ dy }\: 11:48:43
\end{align}
```
More repetition will improve our estimations even further, but they rapidly converge. (A third estimate gives the time $11:48:44$.)

We can see that the time of apparent noon is not $12:00$. This difference is called the [Equation of Time](https://en.wikipedia.org/wiki/Equation_of_time), and the amount by it differs by changes throughout the year.\
$\blacksquare$

### Horizontal Coordinates using Sidereal Time

Using our knowledge, we can calculate the times of certain astronomical events involving certain altitudes or azimuths, questions such as:
- When does the Sun rise?
- When is the Moon's location due East?\
etc.

#### Example 23
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ at standard time $t = 175.00\: \text{ dy }$, the Sun's Ecliptic Longitude $\lambda_{\text{Sun}}$ was $217\degree\:40'\:36.24''$. <br/>
What was the mean Solar time of sunrise on Solar day $175$ at $\phi = 50\degree N$ and $l = 0\degree E$? <br/>
<img width="2000" height="0">
</td>
</tbo dy >
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
Taking the negative arccosine value for h (negative because sunrise), we get:
```math
h = -71\degree\:1'\:54.87''
```
From here we just need to find the mean time from the hour angle, so we follow Example $5$.
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
Just as with Example $5$, this is just a preliminary approximation, and these calculations must be repeated for a more accurate time of sunrise.

At $t = 175 \text{ dy } 07:03:13$, $\lambda_\text{Sun} = 218\degree$ $2'$ $32.28''$.\
Converting to equatorial coordinates:
```math
\begin{alignat}{4}
\delta &=-15&&\degree\:23&&'\:5.06&&''\\
\alpha &= 215&&\degree\:13&&'\:54.03&&''
\end{alignat}
```
Thus the sunrise equation gives (again, taking the negative arccosine):
```math
h = -70\degree\:51'\:26.21''
```
Now we follow Example $5$.
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
