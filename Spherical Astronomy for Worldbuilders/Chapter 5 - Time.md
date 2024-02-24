## V. Time
We will now move on to specific observations from the ground, and of great importance here is the time of events. So let us talk about how to measure time:

### Sidereal and Solar time
When measuring time, two types of time must be distinguished:
 - The [Mean Solar Time](https://en.wikipedia.org/wiki/Solar_time) (denoted $t$)
   * This is the time that bases itself off the Sun. This is the time that all of us are used to. The **average** time of noon (when the Sun is at its highest point in the sky) is $12:00$, or $.5$ (solar) days, and the **average** time of midnight (when the Sun is at its lowest point in the sky) is $00:00$, or $.0$ (solar) days. The Solar day is also called the *synodic day*
 - The [Sidereal Time](https://en.wikipedia.org/wiki/Sidereal_time) (denoted $\Theta$)
   * <ins>This is the time that bases itself off the rotation of the Earth</ins>. Contrary to popular belief, the rotation period of the Earth is not equal to one solar day. It is instead equal to one sidereal day. These two times are different due to the orbit of the Earth around the Sun. One sidereal day after some point in time, the distant stars will return to the same position in the sky, but because the Earth has orbited the sun and has moved in that time period (or, from the Earth's perspective, the Sun has moved), the Sun will have not retuend to the same position. Therefore there is a discrepancy between the two times.
   * **Sidereal time measures the amount the Earth has rotated**. Where do we start measuring it then? Well, it is measured with $0$ sidereal time being when Aries is highest in the sky. In the Northern hemisphere, this is when Aries is directly South. In the Southern hemisphere, it is when Aries is directly North.
   * We call the North-South line the "Meridian", and this can be extended as a whole circle around us. It is the circle that starts at North, goes straight up to the point right above our head (the "Zenith"), down to direct South, and down further to the point right beneath our feet (the "Nadir") and then back up to North. This is called the "Meridian circle" or "Meridian plane".
   * The sidereal time then measures how far away Aries is from this Meridian circle. Since the Earth rotates from East to West, things rise in the East and set in the West. This means that as time progreses, Aries will go away from the meridian towards West before setting beneath the horizon, and then come back up in the East later. Thus, sidereal time is measured as the distance of Aries from the Meridian with **West as positive**.
   * This further means that sidereal time could also be measured how far East the meridian is from Aries, i.e. the **right ascension of the meridian**.
   * Sidereal time is often measured in degrees.

A further investigation into the difference between the two times: as mentioned earlier, after one sidereal day, the Earth is facing the same point in the sky, and thus the stars will have returned to the same point in the sky. However, because the Earth has orbited an amount around the Sun in that time period, the Sun will not have returned to the same position in the sky. \
So how long is a solar day in comparison to a sidereal day? Well, think about it this way:
- Say at time $0$, the Prime Meridian of the Earth is facing away from the Sun, and the Sun is exactly at Aries.
- Say $n$ sidereal days after some date, the Earth is at the opposite end of its orbit.
- Then, the Prime Meridian will still be pointing towards Aries, but now it is facing the Sun instead of away. This means that there was $0.5$ more sidereal days in that time period than there were Solar days.
- Thus, there is exactly $1$ more sidereal day in $1$ year than there are Solar days.

- The same argument applies for retrograde rotation, but there is $1$ fewer sidereal days than Solar days.

Thus, since there are $Y\pm1$ sidereal days per $Y$ synodic days, where $Y$ is the length of the year in **solar days**,
```math
\text{Sidereal Day} = \frac{Y}{Y \pm 1} \cdot \text{Solar Day}\tag{76}
```
#### Example 19
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
The Earth has an orbital period of $365.2422$ Earth Solar days while Venus has an orbital period of $1.92$ Venusian Solar days. <br/>
Calculate the length of the sidereal day on Earth and Venus, keeping in mind Venus has a retrograde rotation. <br>
(The length of an Earth Solar day is $24$ hours while the length of a Venusian Solar day is $116.75$ Earth Solar days.)
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

We use equation $76$.\
Since Earth has a prograde orbit,
```math
\text{Sidereal Day Length} = \frac{Y}{Y + 1} \cdot \text{Solar Day Length}
```
Substituting the numbers,
```math
\text{Earth Sidereal Day Length} = \frac{365.2422}{365.2422 + 1} \cdot 24 h = 23h\: 56m\: 4s
```

Since Venus has a retrograde orbit,
```math
\text{Sidereal Day Length} = \frac{Y}{Y - 1} \cdot \text{Solar Day Length}
```
Substituting the numbers,
```math
\text{Venus Sidereal Day Length} = \frac{1.92}{1.92 - 1} \cdot 116.75\: \text{ dy } = 243\: \text{ dy }
```
Comparing these values to Wikipedia, we can see we are correct.\
$\blacksquare$

<br/>

* Due to random fluctuations in the rotation rate of the Earth, the length of the sidereal day fluctuates by a second or two. *We will ignore this for the purposes of worldbuilding.*

### Converting between Times

The prime meridian is the reference longitude on the Earth. This is where longitude is measured from, and it is also where the standard time is measured. All other solar times can be converted to standard time via this formula:
```math
\text{Standard Time } (t) = \text{Local Time} - \frac{l / 360\degree}{\text{Solar Day Length}}\tag{77}
```
Where $l$ is the local longitude (East is positive).\
If the time is given as an angle, the following formula is perfectly viable:
```math
\text{Standard Time } (t) = \text{Local Time} - l \tag{78}
```

<ins>The benefit to worldbuilding is that we can decide when time $0$ and when day $0$ is.</ins> **Here, we define time $0$ to be the time of Spring Equnox on the prime meridian, and we shall also, for the sake of convenience, also say that the Spring Equinox happened at exactly midnight.** This means, that at solar time (t) $= 0$, the sidereal time was exactly $-0.5$ sidereal days, as Aries (coincident with the Sun) was at midnight.

Under this presumption, the conversion from Solar time to sidereal time is very easy. Since the length of a sidereal day is exactly $Y/(Y\pm1)$ of a solar day, we just multiply the time elapsed, in days, from $t = 0$ by $(Y\pm1)/Y$ to get the sidereal time, then subtract by $0.5$ sidereal days to account for the fact that Aries was at midnight at $t = 0$.
```math
\Theta = \frac{Y \pm 1}{Y} \cdot t - 0.5 \tag{79}
```

#### Example 20
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
An observation was made on planet $P$ on solar day $175$ at solar time $05:16:34$ at $l=165\degree E$. <br/>
Calculate the standard sidereal time at the time of the observation. <br/>
(Assume a year length of $289.42$ solar days, a solar day length of $24$ hours, and prograde rotation.)
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

First, using equation $77$, we determine the standard time of observation.
```math
\begin{align}
\text{Standard Time } (t) &= 05:16:34 - \frac{165\degree/360\degree}{24h} \\
&= 05:16:34 - 11h \\
&= -1\: \text{ dy } \: 18:16:34
\end{align}
```
Where $\text{ dy }$ means Solar days.\
This means the standard time at the time of observation was solar day $174$ at $18:16:34$, or at $t = 174.7615$ days.\
Then, using equation $79$:
```math
\Theta \text{ (in days)} = \frac{289.42 + 1}{289.42} \cdot 174.7615 - 0.5 = 174.8653$
```
Thus the standard sidereal time at the time of measurement was sidereal day $174,$ $311\degree$ $31'$ $12.25''$. \
This can be interpreted as the fact that at the time of measurement, at the prime meridian, the cusp of aries had rotated $311\degree$ $31'$ $12.25''$ from the meridian, or in other words: ***the right ascension of the prime meridian was*** $311\degree$ $31'$ $12.25'' = 20^h$ $:46^m$ $4.82^s$.

Furthermore, the local sidereal time can be calculated by equation $78$:
```math
\Theta_{\text{local}} = \Theta_{\text{standard}} + l = 175\: \text{ sdy }\:116\degree\:31'\:12.25''
```
Where $\text{ sdy }$ means sidereal days.\
$\blacksquare$

To convert from sidereal time to mean solar time, it is harder. Often, from later on calculations that give us the sidereal time of an event, the whole part of the sidereal time will not be apparent. Therefore we must guess by knowing the solar date. However, equation $79$ still holds.
#### Example 21
<div align="center">
<table>
<tbo dy >
<td align="center">
<img width="2000" height="0"><br>
On planet $P$ on local solar day $175$, an observation was made at $l = 165\degree E$ at local sidereal time $116\degree$ $31'$ $12.25''.$ <br/>
Calculate the standard mean solar time.
<img width="2000" height="0">
</td>
</tbo dy >
</table>
</div>

We convert to standard sidereal time by subtracting the longitude:
```math
\text{Standard } \Theta = 116\degree\:31'\:12.25'' - 165\degree = -1\: \text{ sdy } \:311\degree\:31'\: 12.25''\tag{i}
```
We then find the sidereal day corresponding to solar day $175$:
```math
\Theta_{t=175.00} = \frac{290.42}{289.42} \cdot 175 - 0.5 = 175\: \text{ sdy }\:37\degree\:40'\:36.24''
```
Which we truncate to:
```math
\Theta_{t=175.00} = 175\: \text{ sdy } \tag{ii}
```
Combining the results from $(\text{i})$ and $(\text{ii})$, we try $\Theta = 175 \text{ sdy } -1 \text{ sdy } 311\degree$ $31'$ $12.25''$.\
Using equation $9$ with $0.5$ sidereal days $= 180\degree$,
```math
\begin{align}
t &= (174\: \text{ sdy }\: 311\degree\:31'\:12.25'' + 180\degree) \cdot \frac{289.42}{290.42} \\
&= 174.7615\: \text{ dy }\\
&= 174\: \text{ dy } \: 18:16:34
\end{align}
```
If we add $l$ to $t$, we can see we get local solar day $175$, matching with the local observation date. \
If we had gotten for this value local solar day $174$, we would try again but with $\Theta_{t=175.00}$ to be $1$ higher. (In our case, $\Theta_{t=175.00} = 176 \text{  sdy }$.)\
$\blacksquare$

