## VII. Parallax

Our formulae for the location of planets in the sky, and hence the values in our ephemeris, are calculated for a hypothetical observer at the center of the Earth. These values are called the *true* values. On the surface, there is a measurable difference in the values of angles compared to their true values due to the difference in viewing location, particularly for close objects such as the Moon. The actual observed angles are called the *apparent* values, and their difference is called the *parallax*. Let us see how to calculate this parallax.

### The Shape of the Earth
In order to observe from the surface of the Earth, we must know the shape of the Earth. As mentioned in chapter $3$, the Earth is roughly a squished sphere, meaning it is a spheroid. Due to the Earth's rotation, its polar radius its smaller than its equatorial radius. The amount of flattening of the Earth, called the *flattening* ($f$), is calculated with the following formula:
```math
f = \frac{a - b}{a}\tag{7.1}
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
\therefore e = \sqrt{2c - f^2}.\tag{7.2}
```

### Latitude
How do we define latitude on a spheroid?

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1b3d589b-28e2-4723-8f49-4938366bd700" width="350"/> In the diagram, where the Earth is depicted as an ellipse, we can see two ways to define the latitude of the point $P$. The *geocentric* latitude is given by the angle $PCE$, and the *geodetic* or *geographical* latitude given by the angle $POH$, where the line $OP$ is perpendicular to the tangent at $P$, $PT$.

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
And from the triangle $PCQ$,
```math
\tan(\phi') = \frac{y}{x}
```
Implicitly differentiating equation $7.3:
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
We can substitute $b^2 = a^2(1 - e^2)$, where $e =$ eccentricity of the Earth, and obtain:
```math
\begin{align}
\rho &= \frac{ab}{\sqrt{a^2(1 - e^2) \cos^2(\phi') + a^2 \sin^2(\phi')}}\\
&= \frac{b}{\sqrt{(1 - e^2) \cos^2(\phi') + \sin^2(\phi')}}\\
&= \frac{b}{\sqrt{\cos^2(\phi') + \sin^2(\phi') - e^2 \cos^2(\phi')}}\\
&= \frac{b}{\sqrt{1 - e^2 \cos^2(\phi')}}\tag{7.6}
\end{align}
```

An alternate formula is given as follows:\
From the equation of the ellipse and its derivative, substituting $1 - e^2$ for $b^2/a^2$,
```math
\displaylines{
{x^2} + \frac{y^2}{1 - e^2} = a^2\\
\frac{y}{x} = (1 - e^2) \tan(\phi)
}
```
we find:
```math
x = \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\:\:\:\text{and}\:\:\:
y = \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
```
But, $x = \rho \cos(\phi')$ and $y = \rho \sin(\phi')$, so:
```math
\begin{align}
\rho \cos(\phi') &= \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}\\
\rho \sin(\phi') &= \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\end{align}
```
With the addition of an auxiliary $\psi$, these equations can be simplified:
```math
\begin{align}
\sin(\psi) &= e\sin(\phi)\\
\rho \cos(\phi') &= a \cos(\phi)\sec(\psi)\tag{7.7}\\
\rho \sin(\phi') &= a (1 - e^2) \sin(\phi)\sec(\psi)
\end{align}
```
We can deduce from equation $7.7$ by using the angle addition formulae
```math
\displaylines{
\begin{align}
\rho \cos(\phi - \phi') &= a \cos(\psi)\\
\rho \sin(\phi - \phi') &= a e^2 \cos(\phi)\sin(\phi)\sec(\psi)
\end{align}
}\tag{7.8}
```
By multiplying the 2nd line of equation $7.7$ with the 1st line of equation $7.8$, we obtain:
```math
\rho = a \sqrt{\frac{\cos(\phi)}{\cos(\phi')\cos(\phi-\phi')}}\tag{7.9}
```

#### Example 7.1
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth's equatorial radius and polar radius are given as $6378.137\:\text{km}$ and $6356.752\:\text{km}$ respectively. <br/>
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
A solution by equation $7.6$ or equation $7.9$ is also valid of course.\
$\blacksquare$

### Apparent Coordinates
Knowing the radius of the Earth, we can formulate the position of any point on the Earth in geocentric equatorial coordinates as follows:
```math
\begin{align}
x &= \rho \cos(\phi')\cos(\Theta_L)\\
y &= \rho \cos(\phi')\sin(\Theta_L)\tag{7.10} \\ 
z &= \rho \sin(\phi')
\end{align}
```
Because $\Theta_L$ is the right ascension of the local meridian. Then, given that the true cartesian equatorial coordinates of a celestial body is $(p, q, s)$, we can calculate its apparent cartesian equatorial coordinates $(p', q', s')$ by:
```math
(p', q', s') = (p - x, q - y, s - z) \tag{7.11}
```
Which can be turned back into spherical coordinates and then be used to calculate the phenomena detailed in chapter $6$.

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
p &= 404\:634.3 \cos(12\degree\:45'\:8.3'')\cos(10^h\:35^m\:11.55^s) &&= -367940.1\\
q &= 404\:634.3 \cos(12\degree\:45'\:8.3'')\sin(10^h\:35^m\:11.55^s) &&=  142728.4\\ 
s &= 404\:634.3 \sin(12\degree\:45'\:8.3'') &&= 89317.63
\end{alignat}
```
The local sidereal time was (by equation $5.3$):
```math
\Theta_L = 100\degree\:9'\:9.42'' + 150\degree = 250\degree\:9'\:9.42''
```
The radius of the Earth at $\phi = 35\degree$ ($\phi' =  34\degree$ $49'$ $9.79''$) was calculated in example $7.1$ to be $6371.141\text{ km}$. Thus, the equatorial coordinates of the point $\phi = 35\degree, l = 150\degree$ is (by equation $7.10$):
```math
\begin{alignat}{2}
x &= 6371.141 \cos(34\degree\:49'\:9.79'')\cos(250\degree\:9'\:9.42'') &&= -1775.813\\
y &= 6371.141 \cos(34\degree\:49'\:9.79'')\sin(250\degree\:9'\:9.42'') &&= -4919.741\\ 
z &= 6371.141 \sin(34\degree\:49'\:9.79'') &&= 3637.867
\end{alignat}
```
Thus, by equation $7.11$:
```math
\begin{alignat}{2}
p' &= -367940.1 - (-1775.813) &&= -366164.3\\
q' &= 142728.4 - (-4919.741) &&= 147648.1\\ 
s' &= 89317.63 - 3637.867 &&= 85679.76
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
Make calculate the horizontal coordinates of the Moon at the time and location from the previous example using the true and apparent coordinates.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

We use equation $6.3$.\
For the true coordinates:
```math
\begin{align}
h_L &= 250\degree\:9'\:9.42'' - 10^h\:35^m\:11.55^s = 91\degree\:21'\:16.17''\\
A &= 281\degree\:15'\:18.12''\\
a &= 6\degree\:11'\:2.82''\\
\end{align}
```
For the apparent coordinates:
```math
\begin{align}
h_L &= 250\degree\:9'\:9.42'' - 10^h\:32^m\:9.43^s = 92\degree\:6'\:48.03''\\
A &= 281\degree\:15'\:28.20''\\
a &= 5\degree\:17'\:8.62''\\
\end{align}
```
Comparing to the real life values of $A = 281\degree, a = 5\degree$ (rounded values), it is evident that the values using the apparent coordinates are what an observer standing at that location would actually see.\
$\blacksquare$

### Horizontal Parallax
