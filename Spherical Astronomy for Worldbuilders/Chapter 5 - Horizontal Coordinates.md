
Before we can start calculating the locations of stars and planets, we must get ourselves familiar with the bases of all our calculations and coordinate systems.

## I. Coordinates
Let us begin by talking about how objects are even located in space.

### The Celestial Sphere
The most important thing in spherical astronomy is the location of celestial objects as seen from Earth. From the Earth, the sky appears to be a great dome all around us, and this is called the [Celestial Sphere](https://en.wikipedia.org/wiki/Celestial_sphere). This is a large sphere of arbitrary radius (commonly just put to 1) that surrounds the Earth that all the stars and planets are projected onto. There are two lines (circles in actuality) of great importance on the Celestial Sphere.

- **The [Celestial Equator](https://en.wikipedia.org/wiki/Celestial_equator)**
  * This is the circle on the celestial sphere obtained by projecting the Earth's equator onto the celestial sphere. If one were standing on the equator of the Earth, the celestial equator would appear to be a great circle passing right above the observer, going from East to West.
- **The [Ecliptic](https://en.wikipedia.org/wiki/Ecliptic)**
  * This is the circle the Sun appears to make in the sky over the course of a year. In other words, it is the plane of the orbit of the Earth. Due to the axial tilt ($\varepsilon$) of $23.44\degree$ of the Earth, the ecliptic and the celestial equator make an angle of $23.44\degree$ in the sky. Because the Solar System is more or less flat, all the planets, including the Moon, more or less lie on this ecliptic line.
 <br />
 
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/3f19e0a6-0121-40a5-bd6d-9ccf522d8804" width="250"/> Because the ecliptic is tilted with respect to the equator, there are two points at which these two great circles meet. The point at which the ecliptic goes from being below the equator to above the equator is known as the [Cusp of Aries](https://en.wikipedia.org/wiki/First_point_of_Aries) (also known as the Vernal Equinox or the First Point of Aries), which, ironically, now lies in Pisces due to the slow (a period of about $26000$ years) precession of the axial tilt of the Earth. (*For the purposes of worldbuilding, this "axial precession" will be ignored.*) This point is of special importance as it is the place at which almost all angular measurements are made with respect to. This point is called the *Equinox point* because, if the Sun is located at it, the sun is passing directly over the equator, and the length of daytime will be exacly $1/2$ of a day ($12$ hours) all across the globe. The *Vernal* comes from the fact that, because the Sun is travelling towards the Northern direction, it is Spring time in the Northern Hemisphere when this event occurs (Vernal means Spring in Latin).

<br/>
<br/>

### Coordinate Axes
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

- [**The Equatorial Coordinate System**](https://en.wikipedia.org/wiki/Equatorial_coordinate_system)
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Right Ascension* and *Declination* and are denoted $\alpha$ and $\delta$ respectively.
   * The Right Ascension is measured in the plane of the Celestial Equator from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Celestial Equator such that positive is North.
   * The Right Ascension has a peculiar unit, the angle is measured by *hours*, *minutes*, and *seconds*, where $24$ hours is one revolution, $60$ minutes is one hour, and $60$ seconds is one minute.
   * The points of $+90\degree$ and $-90\degree$ Declination are called the *North* and *South* [*Celestial Poles*](https://en.wikipedia.org/wiki/Celestial_pole) respectively. These points can be thought of as the points in the sky right above True North and True South of Earth. From the view of an observer on the Earth, the celestial poles are always in the direction of North and South. Indeed, the reason the North Star always points North is because it is located so close to the North Celestial Pole (Declension $+89\degree 16'$).
- [**The Ecliptic Coordinate System**](https://en.wikipedia.org/wiki/Ecliptic_coordinate_system)
   * In the Equatorial Coordinate System, the angles $\theta$ and $\varphi$ are called the *Ecliptic Longitude* and *Ecliptic Latitude* and are denoted $\lambda$ and $\beta$ respectively.
   * The Ecliptic Longitude is measured in the plane of the Ecliptic from the Cusp of Aries with East as the positive direction. Declination is measured perpendicular from the Ecliptic such that positive is North.
   * By definition of the Ecliptic, the Ecliptic Latitude of the Sun is always $0\degree$.
- [**The Horizontal Coordinate System**](https://en.wikipedia.org/wiki/Horizontal_coordinate_system)
   * This system is unique in that it measures the points as viewed from an actual observer on the Earth, and instead of the reference plane (*xy*-plane) being fixed circles on the Celestial Sphere, it is the horizon of the observer.
   * In the Horizontal Coordinate System, the angles $\theta$ and $\varphi$ are called the *Azimuth* and *Altitude* and are denoted $A$ and $a$ respectively.
   * The Azimuth is measured in the plane of the horizon from North with East as the positive direction. Altitude is measured perpendicular from the horizon such that it is positive when objects are above the horizon.
   * In the Horizontal Coordinate System, the point vertically upwards from the origin is called the *Zenith* and the point vertically below is called the *Nadir*.
   * There are two more planes of importance in the Horizontal Coordinate System other than the horizon:
     * The [Meridian Plane (Circle)](https://en.wikipedia.org/wiki/Meridian_(astronomy)): The plane (or circle) that stretches from North to South while passing through the Zenith and Nadir.
     * The [Hour Plane (Circle)](https://en.wikipedia.org/wiki/Hour_circle): The plane (or circle) that stretches from Celestal North to Celestial South while passing through an object of note.
     * The angle between the Meridian plane and the Hour plane is called the [Hour angle](https://en.wikipedia.org/wiki/Hour_angle), denoted by $h$.

### Coordinate Transformations
[Coordinate transformations](https://en.wikipedia.org/wiki/Astronomical_coordinate_systems#Converting_coordinates) between the three coordinate systems are given via rotation matrix multiplications.

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

#### Example 1
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
