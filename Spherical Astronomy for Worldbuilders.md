## Introduction
**Astrology**, which is a method of divination by observing the stars, can be a very important part of worldbuilding. The basis of astrology is *Spherical Astronomy*, the science of observing the sky. This post will serve as a guide to spherical astronomy for the worldbuilder.

# Part 1. The Basics
Before we can start calculating the locations of stars and planets, we must get ourselves familiar with the bases of all our calculations.
## I. The Celestial Sphere
The most important thing in spherical astronomy is the location of celestial objects as seen from Earth. From the Earth, the sky appears to be a great dome all around us, and this is called the [Celestial Sphere](https://en.wikipedia.org/wiki/Celestial_sphere). This is a large sphere of arbitrary radius (commonly just put to 1) that surrounds the Earth that all the stars and planets are projected onto. There are two lines (circles in actuality) of great importance on the Celestial Sphere.

- **The [Celestial Equator](https://en.wikipedia.org/wiki/Celestial_equator)**
  * This is the circle on the celestial sphere obtained by projecting the Earth's equator onto the celestial sphere. If one were standing on the equator of the Earth, the celestial equator would appear to be a great circle passing right above the observer, going from East to West.
- **The [Ecliptic](https://en.wikipedia.org/wiki/Ecliptic)**
  * This is the circle the Sun appears to make in the sky over the course of a year. In other words, it is the plane of the orbit of the Earth. Due to the axial tilt ($\varepsilon$) of $23.44\degree$ of the Earth, the ecliptic and the celestial equator make an angle of $23.44\degree$ in the sky. Because the Solar System is more or less flat, all the planets, including the Moon, more or less lie on this ecliptic line.
 <br />
 
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3f19e0a6-0121-40a5-bd6d-9ccf522d8804" width="250"/> Because the ecliptic is tilted with respect to the equator, there are two points at which these two great circles meet. The point at which the ecliptic goes from being below the equator to above the equator is known as the [Cusp of Aries](https://en.wikipedia.org/wiki/First_point_of_Aries) (also known as the Vernal Equinox or the First Point of Aries), which, ironically, now lies in Pisces due to the slow (a period of about $26000$ years) precession of the axial tilt of the Earth. (*For the purposes of worldbuilding, this "axial precession" will be ignored.*) This point is of special importance as it is the place at which almost all angular measurements are made with respect to. This point is called the *Equinox point* because, if the Sun is located at it, the sun is passing directly over the equator, and the length of daytime will be exacly $1/2$ of a day ($12$ hours) all across the globe. The *Vernal* comes from the fact that, because the Sun is travelling towards the Northern direction, it is Spring time in the Northern Hemisphere when this event occurs (Vernal means Spring in Latin).

<br/>

## II. Coordinates
Evidently the best way to locate a point on the Celestial *Sphere* is with [*spherical* coordinates](https://en.wikipedia.org/wiki/Spherical_coordinate_system). This is a coordinate system based on three values:
```math
\begin{align}
\varphi &= \text{the vertical angle,}
\\ \theta &= \text{the horizontal angle,}
\\ \rho &= \text{the radius.}
\end{align}
```
$\rho$ is the distance from the origin to the point in question, $\theta$ is the angle East from North, and $\varphi$ is the angle of altitude from the $xy$-plane. (Note in mathematics and physics (and the diagram on Wikipedia), instead of $\varphi$ being the angle above the $xy$-plane, it is the complement of that angle, the angle down from the $z$-axis.) Thus, $\theta$ ranges from $0\degree$ to $360\degree$, and $\varphi$ from $-90\degree$ to $90\degree$.

This coordinate system can be thought of as the longitude-latitude system of Earth, where $\theta$ is the longitude, and $\varphi$ is the latitude.
Using trigonometry, one can find the radius of the latitude circle of a sphere with radius $\rho$ is $\rho \cos(\varphi)$ (View figure), so:
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/6d9a1a2f-885a-4f94-98df-4e0814da6e90" width="250"/>

```math
\begin{align}
x &= \rho \cos(\varphi) \cos(\theta)
\\ y &= \rho \cos(\varphi) \sin(\theta) \tag{1}
\\ z &= \rho \sin(\varphi)
\end{align}
```
Where $x$, $y$, and $z$ are the cartesian coordinates of the point described by $\rho$, $\theta$, and $\varphi$.\
The reverse transformation, also derived by simple geometry, is given below:
```math
\begin{align}
\rho &= \sqrt{x^2 + y^2 + z^2}
\\ \theta &= \arctan(y, x) \tag{2}
\\ \varphi &= \arcsin(z / \rho)
\end{align}
```
Where $\arctan(y, x)$ is the [two argument arctangent](https://en.wikipedia.org/wiki/Atan2), used to avoid tangent ambiguity.

There are three coordinate systems in wide use. The [Equatorial Coordinate System](https://en.wikipedia.org/wiki/Equatorial_coordinate_system), the [Ecliptic Coordinate System](https://en.wikipedia.org/wiki/Ecliptic_coordinate_system). and the [Horizontal Coordinate System](https://en.wikipedia.org/wiki/Horizontal_coordinate_system).

- **The Equatorial Coordinate System**
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Right Ascension* and *Declination* and are denoted $\alpha$ and $\delta$ respectively.
   * The Right Ascension is measured in the plane of the Celestial Equator from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Celestial Equator such that positive is North.
   * The Right Ascension has a peculiar unit, the angle is measured by *hours*, *minutes*, and *seconds*, where $24$ hours is one revolution, $60$ minutes is one hour, and $60$ seconds is one minute.
   * The points of $+90\degree$ and $-90\degree$ Declination are called the *North* and *South* [*Celestial Poles*](https://en.wikipedia.org/wiki/Celestial_pole) respectively. These points can be thought of as the points in the sky right above True North and True South of Earth. From the view of an observer on the Earth, the celestial poles are always in the direction of North and South. Indeed, the reason the North Star always points North is because it is located so close to the North Celestial Pole (Declension $+89\degree 16'$).
- **The Ecliptic Coordinate System**
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Ecliptic Longitude* and *Ecliptic Latitude* and are denoted $\lambda$ and $\beta$ respectively.
   * The Ecliptic Longitude is measured in the plane of the Ecliptic from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Ecliptic such that positive is North.
   * By definition of the Ecliptic, the Ecliptic Latitude of the Sun is always $0\degree$.
- **The Horizontal Coordinate System**
   * This system is unique in that it measures the points as viewed from an actual observer on the Earth, and instead of the reference plane (*xy*-plane) being fixed circles on the Celestial Sphere, it is the horizon of the observer.
   * In the Horizontal Coordinate System, the angles $\theta$ and $\varphi$ are called the *Azimuth* and *Altitude* and are denoted $A$ and $a$ respectively.
   * The Azimuth is measured in the plane of the horizon from North with East as the positive direction. Altitude is measured perpendicular from the horizon such that it is positive when objects are above the horizon.
   * In the Horizontal Coordinate System, the point vertically upwards from the origin is called the *Zenith* and the point vertically below is called the *Nadir*.
   * There are two more planes of importance in the Horizontal Coordinate System other than the horizon:
     * The [Meridian Plane (Circle)](https://en.wikipedia.org/wiki/Meridian_(astronomy)): The plane (or circle) that stretches from North to South while passing through the Zenith and Nadir.
     * The [Hour Plane (Circle)](https://en.wikipedia.org/wiki/Hour_circle): The plane (or circle) that stretches from Celestal North to Celestial South while passing through an object of note.
     * The angle between the Meridian plane and the Hour plane is called the [Hour angle](https://en.wikipedia.org/wiki/Hour_angle), denoted by $h$.

### Coordinate Transformations
Coordinate transformations between the three coordinate systems are given via rotation matrix multiplications.

- **Ecliptic to Equatorial:**
```math
\begin{bmatrix}
x_{\text{equatorial}} \\ y_{\text{equatorial}} \\ z_{\text{equatorial}}
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos{\varepsilon} & -\sin{\varepsilon} \\
0 & \sin{\varepsilon} & \cos{\varepsilon}  \tag{3}
\end{bmatrix}
\begin{bmatrix}
x_{\text{ecliptic}} \\ y_{\text{ecliptic}} \\ z_{\text{ecliptic}}
\end{bmatrix}
```
The $x$ coordinate stays the same as the ecliptic and equatorial coordinate systems have the same $x$-axis: the direction of Vernal Equinox.

- **Equatorial to Ecliptic:**
```math
\begin{bmatrix}
x_{\text{ecliptic}} \\ y_{\text{ecliptic}} \\ z_{\text{ecliptic}}
\end{bmatrix}
=
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos{\varepsilon} & \sin{\varepsilon} \\
0 & -\sin{\varepsilon} & \cos{\varepsilon}  \tag{4}
\end{bmatrix}
\begin{bmatrix}
x_{\text{equatorial}} \\ y_{\text{equatorial}} \\ z_{\text{equatorial}}
\end{bmatrix}
```
Again, the $x$ coordinate stays the same as the ecliptic and equatorial coordinate systems have the same $x$-axis: the direction of Vernal Equinox.

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

These cartesian coordinates can be transformed to spherical coordinates by equation $2$.

### Example
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On $\text{January }2,\:2024$, the Moon's right ascension was $11^{h}\enspace 19^{m}\enspace 30.12^{s}$ and its declination was $+07\degree\enspace 21'\enspace 42.9''.$ <br/>
 Calculate its ecliptic coordinates. (Use $\varepsilon = 23.44\degree$)<br>
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We first convert the sexagesimal notation to degrees:
```math
\begin{alignat}{3}
\alpha &= 11^{h}\enspace 19^{m}\enspace &&30.12^{s} &&= 169.8755\degree \\
\delta &= 07\degree\enspace 21'\enspace &&42.9'' &&= 7.3619\degree
\end{alignat}
```
Keeping in mind that $1^{h}$ is $360\degree/24 = 15\degree$.\
We then convert the equatorial coordinates given to equatorial cartesian coordinates ($\rho = 1$ because the celestial sphere is of arbitrary radius) using equation $1$:
```math
\begin{alignat}{2}
x &= \cos(\delta)\cos(\alpha) &&= -0.976313\\
y &= \cos(\delta)\sin(\alpha) &&= 0.174339\\
z &= \sin(\delta) &&= 0.128136
\end{alignat}
```
Next, we carry out the matrix multiplication (equation $4$):
```math
\begin{alignat}{3}
x_{\text{ecliptic}} &= 1 \cdot x + 0 \cdot y &&+ 0 \cdot z && = -0.976313 \\
y_{\text{ecliptic}} &= 0 \cdot x + \cos{\varepsilon} \cdot y &&+ \sin{\varepsilon} \cdot z &&= 0.210923 \\
z_{\text{ecliptic}} &= 0 \cdot x - \sin{\varepsilon} \cdot y &&+ \cos{\varepsilon} \cdot z &&= 0.0482118
\end{alignat}
```
We then convert to spherical coordinates with $\rho = 1$ using equation $2$.
```math
\begin{alignat}{2}
\lambda &= \arctan(0.210923,-0.976313) &&=  167\degree\enspace48'\enspace32.97''\\
\beta &= \arcsin(0.0482118/1) &&= \enspace\enspace2\degree\enspace45'\enspace48.24''
\end{alignat}
```
$\blacksquare$

## III. Time
When measuring time, two types of time must be distinguished:
 - The [Mean Solar Time](https://en.wikipedia.org/wiki/Solar_time)
   * This is the time that bases itself off the Sun. This is the time that all of us are used to. The **average** time of noon (when the Sun is at its highest point in the sky) is $12:00$, or $.5$ (solar) days, and the **average** time of midnight (when the Sun is at its lowest point in the sky) is $00:00$, or $.0$ (solar) days. The Solar day is also called the *synodic day*
 - The [Sidereal Time](https://en.wikipedia.org/wiki/Sidereal_time) (denoted $\Theta$)
   * <ins>This is the time that bases itself off the rotation of the Earth</ins>. Contrary to popular belief, the rotation period of the Earth is not equal to one solar day. It is instead equal to one sidereal day. These two times are different due to the orbit of the Earth around the Sun. One sidereal day after some point in time, the distant stars will return to the same position in the sky, but because the Earth has orbited the sun and has moved in that time period (or, from the Earth's perspective, the Sun has moved), the Sun will have not retuend to the same position. Therefore there is a discrepancy between the two times.
   * It is defined as the angle between the local meridian (the North-South-Zenith-Nadir plane) and the hour plane of Aries (the Celestial North-Celestial South-Aries plane). Thus, $0$ **sidereal time is not when Aries is lowest in the sky, but it is when Aries is at the highest point in the sky.**
   * Some thought will reveal that during the course of one orbit of the Earth, there is *exactly* one more sidereal day on Earth than there are solar days. If the Earth had a retrograde rotation, There would be one less sidereal day than there are solar days.
   * Sidereal time is often measured in degrees of Earth's rotation.
### Example
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


Since Earth has a prograde orbit,
```math
\text{Sidereal Day} = \frac{\text{Year Length}}{\text{Year Length} + 1} \cdot \text{Solar Day} \tag{6}
```
Substituting the numbers,
```math
\text{Earth Sidereal Day} = \frac{365.2422}{365.2422 + 1} \cdot 24 h = 23h\enspace 56m\enspace 4s
```

Since Venus has a retrograde orbit,
```math
\text{Sidereal Day} = \frac{\text{Year Length}}{\text{Year Length} - 1} \cdot \text{Solar Day} \tag{7}
```
Substituting the numbers,
```math
\text{Venus Sidereal Day} = \frac{1.92}{1.92 - 1} \cdot 116.75\enspace dy = 243\enspace dy
```
Comparing these values to Wikipedia, we can see we are correct.\
$\blacksquare$

<br/>

* Due to random fluctuations in the rotation rate of the Earth, the length of the sidereal day fluctuates by a second or two. *We will ignore this for the purposes of worldbuilding.*

### Time Conversions

The prime meridian is the reference longitude on the Earth. This is where longitude is measured from, and it is also where the standard time is measured. All other solar times can be converted to standard time via this formula:
```math
\text{Standard Time } (T) = \text{Local Time} - \frac{l / 360\degree}{\text{Solar Day Length}}\tag{8}
```
Where $l$ is the local longitude (East is positive).\
If the time is given as an angle, the following formula is perfectly viable:
```math
\text{Standard Time } (T) = \text{Local Time} - l \tag{9}
```

<ins>The benefit to worldbuilding is that we can decide when time $0$ and when day $0$ is.</ins> **Here, we define time $0$ to be the time of Spring Equnox on the prime meridian, and we shall also, for the sake of convenience, also say that the Spring Equinox happened at exactly midnight.** This means, that at solar time (T) $= 0$, the sidereal time was exactly $-0.5$ sidereal days, as Aries (coincident with the Sun) was at midnight.

Under this presumption, the conversion from Solar time to sidereal time is very easy. Since the length of a sidereal day is exactly $Y/(Y\pm1)$ of a solar day, where $Y$ is the length of a year **in solar days**, we just multiply the time elapsed, in days, from $T = 0$ by $(Y\pm1)/Y$ to get the sidereal time, then subtract by $0.5$ sidereal days to account for the fact that Aries was at midnight at $T = 0$.
```math
\Theta = \frac{Y \pm 1}{Y} \cdot T - 0.5 \tag{10}
```

### Example
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
An observation was made on planet $P$ on solar day $175$ at solar time $05:16:35$ at $l=165\degree E$. <br/>
Calculate the standard sidereal time at the time of the observation. <br/>
(Assume a year length of $289.42$ solar days, a solar day length of $24$ hours, and prograde rotation.)
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

First, using equation $8$, we determine the standard time of observation.
```math
\begin{align}
\text{Standard Time } (T) &= 05:16:35 - \frac{165\degree/360\degree}{24h} \\
&= 05:16:35 - 11h \\
&= -1\enspace dy \enspace 18:16:35
\end{align}
```
This means the standard time at the time of observation was solar day $174$ at $18:16:35$, or at $T = 174.7615$ days.\
Then, using equation $10$:
```math
\Theta \text{ (in days)} = \frac{289.42 + 1}{289.42} \cdot 174.7615 - 0.5 = 174.8653$
```
Thus the standard sidereal time at the time of measurement was sidereal day $174,\enspace311\degree\enspace31'\enspace12.25''$. \
This can be interpreted as the fact that at the time of measurement, at the prime meridian, the cusp of aries had rotated $311\degree\enspace31'\enspace12.25''$ from midnight, or in other words: ***the right ascension of the prime meridian was*** $311\degree\enspace31'\enspace12.25'' = 20^h\enspace46^m\enspace4.82^s$.

Furthermore, the local sidereal time can be calculated by equation $9$:
```math
\Theta_{\text{local}} = \Theta_{\text{standard}} + l = 175\enspace sdy\enspace116\degree\enspace31'\enspace12.25''
```
Where $sdy$ means sidereal days.\
$\blacksquare$

To convert from sidereal time to mean solar time, it is harder. Often, from later on calculations that give us the sidereal time of an event, the whole part of the sidereal time will not be apparent. Therefore we must guess by knowing the solar date. However, equation $10$ still holds.
### Example
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
\text{Standard } \Theta = 116\degree\enspace31'\enspace12.25'' - 165\degree = -1\enspace sdy \enspace311\degree\enspace31'\enspace 12.25''\tag{i}
```
We then find the sidereal day corresponding to solar day $175$:
```math
\Theta_{T=175.00} = \frac{290.42}{289.42} \cdot 175 - 0.5 = 175\enspace sdy\enspace37\degree\enspace40'\enspace36.24''
```
Which we truncate to:
```math
\Theta_{T=175.00} = 175\enspace sdy \tag{ii}
```
Combining the results from $(\text{i})$ and $(\text{ii})$, we try $\Theta = 175\enspace sdy -1\enspace sdy \enspace311\degree\enspace31'\enspace12.25''$.\
Using equation $10$ with $0.5$ sidereal days $= 180\degree$,
```math
\begin{align}
T &= (174\enspace sdy\enspace 311\degree\enspace31'\enspace12.25'' + 180\degree) \cdot \frac{289.42}{290.42} \\
&= 174.7615\enspace dy\\
&= 174\enspace dy \enspace 18:16:35
\end{align}
```
If we add $l$ to $T$, we can see we get local solar day $175$, matching with the local observation date. \
If we had gotten for this value local solar day $174$, we would try again but with $\Theta_{T=175.00}$ to be $1$ higher. (In our case, $\Theta_{T=175.00} = 176\enspace sdy$.)\
$\blacksquare$

### The Hour Angle
The [hour angle](https://en.wikipedia.org/wiki/Hour_angle), as defined earlier, is the angle between the meridian plane and the hour plane. This value is measured with West as positive.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/743585dd-02e4-41f2-ba17-18ecfa2a35cc" width="400"/> In the diagram, the Eastern angle between Aries and the Prime Meridian (the right ascension of the Prime Meridian) is the standard sidereal time ($\Theta$), and the Eastern angle between Aries and the Local Meridian is the local standard time ($\Theta_L$). The Eastern angle between Aries and the Star is, by definition, the right ascension of the star ($\alpha$). Furthermore, the Eastern angle between the Prime Meridian and the Local Meridian is the longitude $l$. (Eastern angle meaning the angle measured in the Eastern direction.)

The Western angle between the Prime Meridian and the Star is known as the Standard Hour Angle of the star ($h$), and the Western angle between the Local Meridian and the Star is known as the Local Hour Angle of the star ($h_L$).

<br/>
<br/>
<br/>

It is therefore evident that 
```math
h_L = \Theta_L - \alpha\tag{11}
```
and because $\Theta_L = \Theta + l$ (equations $8$ and $9$):

```math
h_L = \Theta + l - \alpha\tag{12}
```

When $h_L = 0$, the star is coincident with the meridian, and the star is at the highest point in the sky. If $h_L = 180\degree$, the star is coincident with the lower meridian, and it is at the lowest point in the sky. If the star in question is the Sun, then the times at which $h_L = 0$ and $h_L = 180\degree$ are called *apparent noon* and *apparent midnight* respectively. These are not the same as the *mean noon* and *mean midnight*, the mean values are simply the average of the apparent values over the year. (Yes, this means noon and midnight aren't always at $12:00$ and $00:00$!)
