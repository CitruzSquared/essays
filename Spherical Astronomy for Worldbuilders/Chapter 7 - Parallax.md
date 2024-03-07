## VII. Parallax

Our formulae for the location of planets in the sky, and hence the values in our ephemeris, are calculated for a hypothetical observer at the center of the Earth. These values are called the *true* values. On the surface, there is a measurable difference in the values of angles compared to their true values due to the difference in viewing location, particularly for close objects such as the Moon. The actual observed angles are called the *apparent* values, and their difference is called the *parallax*. Let us see how to calculate this parallax.

### The Shape of the Earth
In order to observe from the surface of the Earth, we must know the shape of the Earth. As mentioned in chapter $3$, the Earth is roughly a squished sphere, meaning it is a spheroid. Due to the Earth's rotation, its polar radius its smaller than its equatorial radius. The amount of flattening of the Earth, called the *flattening* ($f$), is calculated with the following formula:
```math
f = \frac{a - b}{a} = 1 - \frac{b}{a}\tag{7.1}
```
Where $b =$ the polar radius, and $a =$ the equatorial radius.

Since the eccentricity $e$ of an ellipse is defined by
```math
e^2 = 1 - \frac{b^2}{a^2}
```
it follows that
```math
e^2 = 1 - (1 - f)^2
```
```math
\therefore e = \sqrt{2f - f^2}.\tag{7.2}
```

### Latitude
How do we define latitude on a spheroid?

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1b3d589b-28e2-4723-8f49-4938366bd700" width="350"/> In the diagram, where the Earth is depicted as an ellipse, we can see two ways to define the latitude of the point $P$. The *geocentric* latitude is given by the angle $PCE$, and the *geodetic* or *geographical* latitude given by the angle $POH$, where the line $OP$ is perpendicular to the tangent at $P$, $PT$, and $OH$ is parallel to $CE$.

When one refers to latitude, usually one is referring to the *geodetic* (*geographical*) latitude ($\phi$). This is the value of latitude we used in chapter $6$.

However, the geocentric latitude is more convenient in some situations.\
So, given a geodetic latitude, how do we find the geocentric latitude?

<br/>

Well, consider the equation of the ellipse with semi-major axis $a$ and semi-minor axis $b$:
```math
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1\tag{7.3}
```
Because $PO$ is perpendicular to the tangent $PT$, the slope of $PO$ must be $-1/m_{PT}$. In other words:
```math
\tan(\phi) = -\frac{d x}{d y}
```
And from the triangle $PCQ$ we can deduce:
```math
\tan(\phi') = \frac{y}{x}
```
Implicitly differentiating equation $7.3$ we obtain:
```math
\frac{y}{x} = -\frac{b^2}{a^2} \frac{d x}{d y}
```
Therefore:
```math
\tan(\phi') = \frac{b^2}{a^2} \cdot \tan(\phi).\tag{7.4}
```
It can be further proven with simple geometry that the difference between $\phi$ and $\phi'$, i.e. $\phi - \phi'$, called the *reduction in latitude*, is equal to the angle $CPO$ in the diagram.

Let us now also calculate the specific radius at latitude $\phi$, i.e. the length $PC$, labeled $\rho$ in the diagram.\
From the equation of the ellipse:
```math
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1
```
we substitute $x = \rho \cos(\phi')$ and $y = \rho \sin(\phi')$, and obtain:
```math
\begin{align}
1 &= \frac{(\rho \cos(\phi'))^2}{a^2} + \frac{(\rho \sin(\phi'))^2}{b^2}\\
a^2 b^2 &= \rho^2 (b^2 \cos^2(\phi') + a^2 \sin^2(\phi')) \\
\therefore \rho &= \frac{ab}{\sqrt{b^2 \cos^2(\phi') + a^2 \sin^2(\phi')}}\tag{7.5}\\
\end{align}
```

#### Example 7.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth's equatorial radius and polar radius are given as $6378.137$ $\text{km}$ and $6356.752$ $\text{km}$ respectively. <br/>
Find the radius of the Earth at geographic latitude $35\degree N$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $7.4$:
```math
\displaylines{
\tan(\phi') = \frac{6356.752^2}{6378.137^2} \cdot \tan(35\degree)\\
\therefore\phi' = 34\degree\:49'\:9.79''.
}
```
Then by equation $7.5$:
```math
\begin{align}
\rho &= \frac{ab}{\sqrt{b^2 \cos^2(\phi') + a^2 \sin^2(\phi')}}\\
&= \frac{6378.137\cdot6356.752}{\sqrt{6356.752^2 \cos^2(34\degree\:49'\:9.79'') + 6378.137^2 \sin^2(4\degree\:49'\:9.79'')}}\\
&= 6371.141\:\text{km}.
\end{align}
```
$\blacksquare$

### Apparent Equatorial Coordinates
Knowing the radius of the Earth, we can formulate the position of any point on the Earth $(p, q, s)$ in geocentric equatorial coordinates as follows:
```math
\begin{align}
p &= \rho \cos(\phi')\cos(\Theta_L)\\
q &= \rho \cos(\phi')\sin(\Theta_L)\tag{7.6} \\ 
s &= \rho \sin(\phi')
\end{align}
```
Because $\Theta_L$ is the right ascension of the local meridian. Then, given that the true cartesian coordinates of a celestial body is $(x, y, z)$, we can calculate its apparent cartesian coordinates $(x', y', z')$ by:
```math
(x', y', z') = (x - p, y - q, z - s) \tag{7.7}
```
Which can be turned back into spherical coordinates and then be used to calculate the phenomena detailed in chapter $6$.\
Naturally, if one is given the apparent coordinates then the true coordinates are:
```math
(x, y, z) = (x' + p, y' + q, z' + s) \tag{7.8}
```
The differences in $\alpha$ and $\delta$ between the true and apparent values are called the parallax in right ascension and declension respectively.

While the disparity of location between the observer and the center of the Earth significantly changes the location of closer objects (like the Sun and the planets, and in particular the Moon) it does not matter much for very far objects like the stars, and the stars can be regarded has having 0 parallax, i.e. no difference in location whatsoever.

#### Example 7.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
On $\text{January 1, } 2024$ at standard time $00:00$ ($\Theta = 100\degree$ $9'$ $9.42''$), <br/> 
the true equatorial coordinates of the Moon were $\alpha = 10^h$ $35^m$ $11.55^s$ and $\delta = +12\degree$ $45'$ $8.3''$. <br/>
Given that the distance to the Moon was $404$ $634.3 \text{ km}$, calculate its apparent equatorial coordinates from $\phi = 35\degree$ and $l = 150\degree$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

In cartesian coordinates, the Moon's true coordinates were (by equation $1.1$):
```math
\begin{alignat}{2}
x &= 404\:634.3 \cos(12\degree\:45'\:8.3'')\cos(10^h\:35^m\:11.55^s) &&= -367940.1\\
y &= 404\:634.3 \cos(12\degree\:45'\:8.3'')\sin(10^h\:35^m\:11.55^s) &&=  142728.4\\ 
z &= 404\:634.3 \sin(12\degree\:45'\:8.3'') &&= 89317.63
\end{alignat}
```
The local sidereal time was (by equation $5.3$):
```math
\Theta_L = 100\degree\:9'\:9.42'' + 150\degree = 250\degree\:9'\:9.42''
```
The radius of the Earth at $\phi = 35\degree$ ($\phi' =  34\degree$ $49'$ $9.79''$) was calculated in example $7.1$ to be $6371.141\text{ km}$. Thus, the equatorial coordinates of the point $\phi = 35\degree, l = 150\degree$ is (by equation $7.6$):
```math
\begin{alignat}{2}
p &= 6371.141 \cos(34\degree\:49'\:9.79'')\cos(250\degree\:9'\:9.42'') &&= -1775.813\\
q &= 6371.141 \cos(34\degree\:49'\:9.79'')\sin(250\degree\:9'\:9.42'') &&= -4919.741\\ 
s &= 6371.141 \sin(34\degree\:49'\:9.79'') &&= 3637.867
\end{alignat}
```
Thus, by equation $7.7$:
```math
\begin{alignat}{2}
x' &= -367940.1 - (-1775.813) &&= -366164.3\\
y' &= 142728.4 - (-4919.741) &&= 147648.1\\ 
z' &= 89317.63 - 3637.867 &&= 85679.76
\end{alignat}
```
Thus, by equation $1.2$:
```math
\begin{alignat}{2}
\alpha' &= \arctan(147648.1, -366164.3) &&= 10^h\:32^m\:9.43^s\\
\delta' &= \arcsin\left(\frac{85679.76}{\sqrt{(-366164.3)^2 + 147648.1^2 + 85679.76^2}}\right) &&= +12\degree\:14'\:38.9''
\end{alignat}
```
In a worldbuilding setting however, the cartesian coordinates of the Moon would already be known, and therefore one can skip the first step.\
$\blacksquare$

To demonstrate the difference, let's calculate the horizontal coordinates of the Moon.
#### Example 7.3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Calculate the horizontal coordinates of the Moon at the time and location from the previous example using the true and apparent coordinates.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We use equation $6.3$ with the geodetic latitude $35\degree$.\
For the true coordinates:
```math
\begin{align}
h &= 250\degree\:9'\:9.42'' - 10^h\:35^m\:11.55^s = 91\degree\:21'\:16.17''\\
\delta &= 12\degree\:45'\:8.3''
\end{align}
```
Therefore:
```math
\begin{align}
A &= 281\degree\:15'\:18.12''\\
a &= 6\degree\:11'\:2.82''\\
\end{align}
```
For the apparent coordinates:
```math
\begin{align}
h' &= 250\degree\:9'\:9.42'' - 10^h\:32^m\:9.43^s = 92\degree\:6'\:48.03''\\
\delta' &= 12\degree\:14'\:38.9''
\end{align}
```
Therefore:
```math
\begin{align}
A' &= 281\degree\:15'\:28.20''\\
a' &= 5\degree\:17'\:8.62''\\
\end{align}
```
Comparing to the real life values of $A = 281\degree, a = 5\degree$ (rounded values), it is evident that the values calculated using the apparent coordinates are what an observer standing at that location would actually see. Thus, the notion of "geocentric (true) horizontal coordinates" is merely a simplification and has no real-life meaning. That is not to say it is not useful, as we will see in the next section. \
$\blacksquare$

### Apparent Horizontal Coordinates
It is possible to calculate the apparent horizontal coordinates from the geocentric horizontal coordinates, thus removing the need to calculate the apparent right ascension and declension.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1de6400b-51a2-4e33-a0fe-5f96ce0f04f5" width="350"/> Consider a coordinate system where the origin is the place of observation $P$, the $x$-axis points northward along the meridian along the horizon, i.e. $TP$, and the $z$-axis points upward towards the Zenith, i.e. $PZ$. The $y$-axis is then the East-West line at point $P$. In this coordinate system, the position $(x', y', z')$ of an object in the sky is given as (by equation $1.1$):
```math
\begin{align}
x' &= \Delta' \cos(a')\cos(A')\\
y' &= \Delta' \cos(a')\sin(A')\\ 
z' &= \Delta' \sin(a')
\end{align}
```
Where $\Delta'$ is the apparent distance to the object. These are the apparent horizontal coordinates of the object.

Consider another coordinate system, parallel to the first but centered at the Earth's center $C$, i.e. the $x$-axis points in the direction $T'C$, and the $z$-axis points in the direction $CZ'$. The position $(x, y, z)$ of the object is given in this new coordinate system as (by equation $1.1$):
```math
\begin{align}
x &= \Delta \cos(a)\cos(A)\\
y &= \Delta \cos(a)\sin(A)\\ 
z &= \Delta \sin(a)
\end{align}
```
These are the true (geocentric) horizontal coordinates of the object.

The position $(p, q, s)$ of $P$ in the second (geocentric) system are given as:
```math
\begin{align}
p &= -\rho \sin(\phi - \phi')\\
q &= 0 \tag{7.9} \\
s &= \rho \cos(\phi - \phi')
\end{align}
```
Because $\phi - \phi' = CPO = PCZ'$. The minus sign on $p$ is due to the fact that the line $PZ$ is located closer to the equator than $CZ'$, i.e. more south in the Northern hemisphere and more north in the Southern hemisphere. Because the $x$-axis points northward, there must be a negative sign.

From equation $7.9$, the apparent horizontal coordinates can be described by equation $7.11$.
#### Example 7.4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Calculate the apparent horizontal coordinates of the Moon from $\phi = 35\degree$, given that the geocentric horizontal coordinates of the Moon at this time for this latitude was $\Delta = 404$ $634.3 \text{ km}, A = 281\degree$ $15'$ $18.12'', a = 6\degree$ $11'$ $2.82''$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

The Moon's coordinates by equation $1.1$:
```math
\begin{alignat}{2}
x &= 404\:634.3 \cos(6\degree\:11'\:2.82'')\cos(281\degree\:15'\:18.12'')&&= 78515.54\\
y &= 404\:634.3 \cos(6\degree\:11'\:2.82'')\sin(281\degree\:15'\:18.12'')&&= -394543.1\\
z &= 404\:634.3 \sin(6\degree\:11'\:2.82'') &&= 43588.73
\end{alignat}
```
We calculated in previous examples that for this latitude:
```math
\begin{align}
\rho &= 6371.141\text{ km}\\
\phi' &= 34\degree\:49'\:9.79''\\
\therefore \phi - \phi' &= 10'\:50.21''
\end{align}
```
Thus, by equation $7.9$:
```math
\begin{alignat}{2}
p &= -6371.141 \sin(10'\:50.21'') &&= -20.08377\\
q &= 0 &&\\
s &= 6371.141 \cos(10'\:50.21'') &&= 6371.109
\end{alignat}
```
Thus, by equation $7.7$:
```math
\begin{alignat}{2}
x' &= 78515.54 - (-20.08377) &&= 78535.46\\
y' &= -394543.1 - 0 &&= -394543.1\\
z' &= 43588.73 - 6371.109 &&= 37217.62
\end{alignat}
```
Thus, by equation $1.2$:
```math
\begin{alignat}{2}
A' &= \arctan(-394543.1, 78535.46) &&= 281\degree\:15'\:28.14''\\
a' &= \arcsin\left(\frac{37217.62}{\sqrt{78535.46^2 + (-394543.1)^2 + 37217.62^2}}\right) &&= 5\degree\:17'\:8.60''\\
\end{alignat}
```
Which agree with example $7.3$ within rounding error.\
$\blacksquare$

### Parallax Corrected Sunrise Equation
In chapter $6$, we derived the sunrise equation that can be used to determine the hour angle for when an object would be at the horizon. However, our formulation used the geocentric horizontal coordinates which are not what an observer on the surface would actually see. To calculate the observed hour angle, we must correct for parallax.

In order for the apparent altitude to be $0\degree$, $z'$ must be equal to $0$, and thus by equation $7.11$, $z$ must equal $s$. $z$, the geocentric horizontal z coordinate of the object is given by equation $6.3$:
```math
z = \Delta \cos(\phi) \cos(\delta) \cos(h) + \Delta \sin(\phi) \sin(\delta)
```
and $s$ is given by equation $7.9$:
```math
s = \rho \cos(\phi - \phi')
```
Equating the two and solving for $\cos(h)$ yields the parallax corrected sunrise equation:
```math
\cos(h) = \frac{\rho \cos(\phi - \phi')}{\Delta \cos(\phi) \cos(\delta)} - \tan(\phi) \tan(\delta) \tag{7.10}
```
This formula only involves geocentric coordinates for ease of calculation.

It is easy to see that if $\rho = 0$, i.e. the place of observation is the center of the Earth, this equation reduces to the regular sunrise equation. It is evident from the many examples of chapter $6$ that the uncorrected version is accurate enough for most things: obviously the stars (since they have no parallax), and even for closer objects like the Sun. However, even closer objects like the Moon can have a very significant parallax (see the next section) and therefore the parallax corrected version of the sunrise equation should be used.

### Horizontal Parallax
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/421ed255-ca91-49ad-8606-3fdb88c149d6" width="250"/> In this diagram, the place of observation is $A$, the object being observed is $S$, and the geocentric and local horizons are given by $CH$ and $AH'$ respectively. The true altitude of the star is $SCH$ and the apparent altitude is $SAH'$. Simple geometry will show that:
```math
SAH' - SCH = ASC
```
Or in other words, the parallax in altitude is equal to the angle subtended by the radius of the Earth from $S$. It is evident therefore that maximum parallax is achieved when $S$ is at the local horizon $H'$, when $S$ subtends the whole radius of the Earth. This angle is called the *horizontal parallax*, and is maximum when the radius of the Earth $CA$ is the equatorial radius, in which case it is called the *equatorial horizontal parallax* (denoted by $\pi$).

It is evident then, that:
```math
\sin(\pi) = \frac{a}{\Delta}\tag{7.11}
```
Where $a$ is the equatorial radius of the Earth and $\Delta$ is the geocentric distance to the object.
#### Example 7.5
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine the maximum possible parallax in the position of the Moon given that the Moon was $404$ $634.3 \text{ km}$ away and that the equatorial radius of the Earth is $6378.137\text{ km}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

The maximum possible parallax is the equatorial horizontal parallax, so by equation $7.11$:
```math
\begin{align}
\sin(\pi) &= \frac{6378.137}{404\:634.3}\\
\therefore \pi &= 54'\:11''
\end{align}
```
Thus the position of the Moon could vary by up to $54'$ $11''$ from the geocentric position depending on the location of the observer on the Earth.

The absolute maximum parallax of the Moon happens when the Moon is closest to the Earth. The distance from the Earth to the Moon in this case is $356$ $400\text{ km}$, therefore:
```math
\pi = \arcsin\left(\frac{6378.137}{356\:400}\right) = 1\degree\:1'\:32''
```
The Moon's position could vary from the geocentric position by more than a degree in this case.\
$\blacksquare$

### Parallax Corrected Subsolar Point
As we saw in the last section, the parallax is maximum if the object is on the horizon. Similarly, the parallax is minimum if the object is at the Zenith, so much so that on a spherical Earth, no parallax exists for an object at the Zenith. Even for an ellipsoidal Earth, the parallax in the longitude of the subsolar point is zero, and the parallax in the latitude of the subsolar point is so miniscule for a low flattening value that it is not worth calculating. However, the method of calculation is given here regardless.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/57646d94-2271-496d-a9e6-2ba3c183506b" width="300"/> Consider a meridianal slice of an ellipsoidal Earth where $N$ is the North pole and $CE$ is the line of the equator. $S$ is the position of an object a geocentric distance $\Delta$ and geocentric declination $SCE = \delta$. The point $P$ is the sub-object point, where the object appears perpendicular to the local horizon $PT$ (i.e. at the Zenith). The angle we are interested in is the angle $PQE$, the geodetic latitude of $P$.

Let's define a 2D coordinate frame where the $C$ is the origin, the $x$-axis points towards $E$, and the $y$-axis points towards $N$. Let the coordinates of $P$ in this system be $(x_0, y_0)$ and coordinates of $S$ be $(v, u)$. Then, by geometry:
```math
\begin{align}
v &= \Delta\cos(\delta)\\
u &= \Delta\sin(\delta)
\end{align}
```
Also, as found earlier (in the *Latitude* section), the derivative of equation of the ellipse is given by:
```math
\frac{y}{x} = -\frac{b^2}{a^2} \frac{d x}{d y}
```
Therefore the slope $m$ of the normal line at a point $(x_0, y_0)$ is given by:
```math
m=-\frac{dx}{dy}= \frac{a^2 y_0}{b^2 x_0}
```
Plugging $m$ into the equation of a line passing through $(x_0, y_0)$, we obtain:
```math
\begin{align}
y - y_0  &= \frac{a^2 y_0}{b^2 x_0} (x - x_0)\\
\therefore b^2 x_0(y - y_0) &= a^2 y_0(x - x_0)\\
\therefore b^2 y x_0 - b^2 x_0 y_0 &= a^2 x y_0 - a^2 y_0 x_0
\end{align}
```
Dividing both sides by $x_0 y_0$ we obtain:
```math
\begin{align}
\frac{b^2 y}{y_0} - b^2 &= \frac{a^2 x}{x_0} - a^2\\
\therefore 0 &= \frac{a^2 x}{x_0} - \frac{b^2 y}{y_0} - a^2 + b^2\tag{7.11}\\
\end{align}
```
At this point it is convenient to introduce an auxiliary variable $\theta$ such that:
```math
\displaylines{
\begin{align}
x_0 &= a\cos(\theta)\\
y_0 &= b\sin(\theta)
\end{align}
}\tag{7.12}
```
The reader can verify that this does indeed satisfy the equation for an ellipse (equation $7.3$).\
Note that $\theta$ does not represent any real angle, it is just a convenient auxiliary that parametrizes the ellipse. By plugging equations $7.12$ into equation $7.11$, the equation for the normal at $(x_0, y_0)$ is given by:
```math
ax\sec(\theta) - by\csc(\theta) - a^2 + b^2 = 0
```
This normal line must pass through $S(v, u)$. Thus, we can substitude $x$ and $y$ by $v = \Delta\cos(\delta)$ and $u = \Delta\sin(\delta)$:
```math
a\Delta\cos(\delta)\sec(\theta) - b\Delta\sin(\delta)\csc(\theta) - a^2 + b^2 = 0\tag{7.13}
```
Solving this equation for $\theta$ gives the coordinates of $P$ by equation $7.12$, which gives the geocentric latitude by $\tan(\phi') = y_0/x_0$, which finally gives the geodetic latitude by equation $7.4$. Equation $7.13$ is not easy to solve however, and the best way to solve it is by numerical approximation: the derivative is given here for use in Newton Raphson iteration.
```math
a \Delta\cos(\delta) \tan(\theta) \sec(\theta) + b \Delta\sin(\delta) \cot(\theta) \csc(\theta)\tag{7.14}
```
Using $\theta = \delta$ is a good first guess. Note that all angles must be reckoned in radians for Newton Raphson's method.\
Also note that as the flattening increases, and $\delta$ gets closer to $0$, the rate of convergence gets slower and slower and more and more iterations are needed, to the point where bisection might be better. However this should not be a problem for most planets as they have very low flatenning values.
#### Example 7.6
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Given the true declension of the Moon $\delta = 12\degree$ $45'$ $8.3''$ and the geocentric distance $\Delta = 404$ $634.3 \text{ km}$, <br/> 
find the parallax corrected latitude of the sublunar point. <br/>
Use $a = 6378.137$ $\text{km}$ and $b = 6356.752$ $\text{km}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

$\delta$ in radians is $0.2225697\text{ rad}$. We can now perform Newton iteration:
```math
\theta_{n+1} = \theta_n - \frac{a\Delta\cos(\delta)\sec(\theta_n) - b\Delta\sin(\delta)\csc(\theta_n) - a^2 + b^2}{a \Delta\cos(\delta) \tan(\theta_n) \sec(\theta_n) + b \Delta\sin(\delta) \cot(\theta) \csc(\theta_n)}
```
Using $\theta_1 = \delta$ as a first guess, this gives $\theta_2 = 0.2218684\text{ rad}$. The table of repetitions is given here:
```math
\begin{array}{cccc}\hline n & & & \theta_n \\ \hline
1 & & & 0.2225697 \\
2 & & & 0.2218684 \\
3 & & & 0.2218704 \\
4 & & & 0.2218704 \\ \hline
\end{array}
```
The geocentric latitude of $P$ are given then as:
```math
\begin{alignat}{2}
x_0 &= 6378.137\cos(0.2218704) &&= 6221.793\\
y_0 &= 6356.752\sin(0.2218704) &&= 1398.832\\
\therefore \phi' &= \arctan\left(\frac{1398.832}{6221.793}\right) &&= 12\degree\:40'\:15.6''
\end{alignat}
```
Therefore the geodetic latitude of $P$ is (by equation $7.4$):
```math
\phi = \arctan\left(\frac{6378.137^2}{6356.752^2} \tan(12\degree\:40'\:15.6'')\right) = 12\degree\:45'\:13.0''
```
Which is less than a $5$ arcsecond difference from the value given by the simple $\phi = \delta$.\
$\blacksquare$
