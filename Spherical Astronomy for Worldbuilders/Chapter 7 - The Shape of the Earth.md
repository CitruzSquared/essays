## VII. The Shape of the Earth
We will now refine our calculations for observations on the surface of the Earth, so we must know the figure of the Earth.

### The Ellipsoid
As mentioned in chapter $3$, the Earth is roughly a squished sphere, meaning it is an ellipsoid (in particular, a spheroid). Due to the Earth's rotation, its polar radius its smaller than its equatorial radius. The amount of flattening of the Earth, called the *flattening* ($f$), is calculated with the following formula:
```math
f = \frac{a - b}{a} = 1 - \frac{b}{a}\tag{7.1}
```
Where $b =$ the polar radius, and $a =$ the equatorial radius.

The ellipsoid, being a solid of rotation where every vertical (merdianal) cross section is an ellipse, can be simplified to be an ellipse for most things:\
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

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/effa9c9a-6e15-446d-9c2c-43457717cccd" width="350"/> In the diagram, where the Earth is depicted as an ellipse, we can see two ways to define the latitude of the point $P$. The *geocentric* latitude is given by the angle $PCE$, and the *geodetic* or *geographical* latitude given by the angle $POH$, where the line $OP$ is perpendicular to the tangent at $P$, $PT$, and $OH$ is parallel to $CE$.

When one refers to latitude, usually one is referring to the *geodetic* (*geographical*) latitude ($\phi$). This definition is used as this definition of latitude makes sure that a perpendicular change in the observer's elevation does not change the observer's latitude. This is the value of latitude we used in chapter $6$.

However, the geocentric latitude is more convenient in some situations. So, given a geodetic latitude, how do we find the geocentric latitude? Well, consider the equation of the ellipse with semi-major axis $a$ and semi-minor axis $b$:
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
\begin{align}
\frac{2x}{a^2} + \frac{2y}{b^2}\frac{dy}{dx} &= 0\\
\therefore \frac{2x}{a^2} &= -\frac{2y}{b^2}\frac{dy}{dx}\\
\therefore \frac{a^2}{x} &= -\frac{b^2}{y}\frac{dx}{dy}\\
\therefore \frac{y}{x} &= -\frac{b^2}{a^2} \frac{d x}{d y}
\end{align}
```
Therefore:
```math
\tan(\phi') = \frac{b^2}{a^2} \cdot \tan(\phi) \tag{7.4}
```
It can be further proven with simple geometry that the difference between $\phi$ and $\phi'$, i.e. $\phi - \phi'$, called the *reduction in latitude*, is equal to the angle $CPO$ in the diagram.

### The Radius of the Earth

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
\therefore \rho &= \frac{ab}{\sqrt{b^2 \cos^2(\phi') + a^2 \sin^2(\phi')}}\tag{7.5}
\end{align}
```

An alternate formula for $\rho$ is given as follows:\
From the equation of the ellipse and its derivative, substituting $1 - e^2$ for $b^2/a^2$,
```math
\displaylines{
{x^2} + \frac{y^2}{1 - e^2} = a^2\\
\frac{y}{x} = (1 - e^2) \tan(\phi)
}
```
we find:
```math
\displaylines{
y = x(1 - e^2) \tan(\phi)\\
\therefore x^2 + x^2(1 - e^2)\tan^2(\phi) = a^2\\
\therefore x^2 \left(1 + (1 - e^2)\cdot\frac{\sin^2(\phi)}{\cos^2(\phi)}\right) = a^2\\
\begin{align}
\therefore x^2 &= \frac{a^2}{1 + (1 - e^2)\cdot\frac{\sin^2(\phi)}{\cos^2(\phi)}}\\
&= \frac{a^2\cos^2(\phi)}{\cos^2(\phi) + \sin^2(\phi) - e^2\sin^2(\phi)}\\
&= \frac{a^2\cos^2(\phi)}{1 - e^2\sin^2(\phi)}\\
\therefore x &= \frac{a \cos(\phi)}{\sqrt{1 - e^2\sin^2(\phi)}}
\end{align}
}
```
And now solving for $y$:
```math
\begin{align}
y &= x(1 - e^2) \tan(\phi)\\
&= \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}\cdot(1 - e^2)\cdot\frac{\sin(\phi)}{\cos(\phi)}\\
&= \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\end{align}
```
Thus:
```math
x = \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\:\:\:\:\:\text{and}\:\:\:\:\:
y = \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
```
But, $x = \rho \cos(\phi')$ and $y = \rho \sin(\phi')$, so:
```math
\displaylines{
\begin{align}
\rho \cos(\phi') &= \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}\\
\rho \sin(\phi') &= \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\end{align}
} \tag{7.6}
```
With the addition of an auxiliary $\psi$ defined via $\sin(\psi) = e\sin(\phi) \therefore \sqrt{1-e^2\sin^2(\phi)} = \cos(\psi)$, these equations can be simplified:
```math
\begin{align}
\sin(\psi) &= e\sin(\phi)\\
\rho \cos(\phi') &= a \cos(\phi)\sec(\psi)\tag{7.7}\\
\rho \sin(\phi') &= a (1 - e^2) \sin(\phi)\sec(\psi)
\end{align}
```
We can deduce from equation $7.7$ by using the angle addition formulae
```math
\begin{align}
\rho \cos(\phi - \phi') &= \rho\cos(\phi)\cos(\phi') + \rho\sin(\phi)\sin(\phi')\\
&= a \cos^2(\phi) \sec(\psi) + a(1 - e^2) \sin^2(\phi) \sec(\psi)\\
&= a \sec(\psi) (\cos^2(\phi) + \sin^2(\phi) - e^2 \sin^2(\phi))\\
&= a \sec(\psi) (1 - e^2\sin^2(\phi)) \\
&= a \sec(\psi) (1 - \sin^2(\psi)) \\
&= a \sec(\psi) \cos^2(\psi) \\
&= a \cos(\psi)
\end{align}
```
and
```math
\begin{align}
\rho \sin(\phi - \phi') &= \rho\sin(\phi)\cos(\phi') - \rho\cos(\phi)\sin(\phi') \\
&= a \cos(\phi)\sec(\psi)\sin(\phi) - a (1 - e^2) \sin(\phi)\sec(\psi)\cos(\phi) \\
&= a \cos(\phi)\sin(\phi)\sec(\psi) (1 - (1 - e^2)) \\
&= a e^2 \cos(\phi)\sin(\phi)\sec(\psi)
\end{align}
```
Thus:
```math
\begin{align}
\rho \cos(\phi - \phi') &= a \cos(\psi)\\
\rho \sin(\phi - \phi') &= a e^2 \cos(\phi)\sin(\phi)\sec(\psi)
\end{align}\tag{7.8}
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
The reader can verify that equation $7.9$ gives the same answer.\
$\blacksquare$

### The Normal
The normal line is the line $PO$, and is the true vertical line at point $P$.\
The distance $PO$, which we denote $N$, is given as follows. From the figure above, it is evident that:
```math
CQ = N\cos(\phi) = \rho\cos(\phi')
```
and therefore,
```math
N = \frac{\rho\cos(\phi')}{\cos(\phi)} = \frac{\frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}}{\cos(\phi)} = \frac{a}{\sqrt{1 - e^2 \sin^2(\phi)}}
\tag{7.10}
```
or, by using the same auxiliary $\sin(\psi) = e\sin(\phi)$,
```math
N = a \sec(\psi)
```
Let us now find the distance between the center and the intersection point of the normal line and the axis, i.e. the distance $CO$. From the triangle $CMO$, we can see:
```math
\rho\sin(\phi - \phi') = CO \sin(90\degree - \phi)
```
and therefore:
```math
CO = \frac{\rho\sin(\phi - \phi')}{\cos(\phi)} \tag{7.11}
```
or, by $7.8$:
```math
CO = \frac{a e^2 \cos(\phi)\sin(\phi)\sec(\psi)}{\cos(\phi)} = a e^2 \sin(\phi)\sec(\psi) \tag{7.12}
```
Now we can properly account for altitude above sea level. To find the distance from the center of the earth to a point $P'$ which is at a perpendicular altitude $h$ above $P$, we first find the normal distance to the axis $N$ and the center – intersection distance $CO$. Then, we add the altitude $h$ to $N$, and then use the law of cosines to find the new geocentric distance $D$ of the point $P'$.

This all can be summarized as:
```math
D^2 = (N + h)^2 + CO^2 - 2 \cdot (N + h) \cdot CO \cdot \sin(\phi) \tag{7.13}
```

#### Example 7.2
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the geocentric distance and latitude of a point with geographic latitude $35\degree$ and altitude $100\text{ km}$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

From the last example, we know that for $\phi = 35\degree$:
```math
\begin{align}
\phi' &= 34\degree\:49'\:9.79''\\
\rho &= 6371.141\:\text{km}
\end{align}
```
Then, by equation $7.10$:
```math
N = \frac{6371.141\cos(34\degree\:49'\:9.79'')}{\cos(35\degree)} = 6385.172 \text{ km}
```
And by equation $7.11$:
```math
CO = \frac{6371.141 \sin(35\degree - 34\degree\:49'\:9.79'')}{\cos(35\degree)} = 24.518 \text{ km}
```
And now by equation $7.13$:
```math
\begin{align}
D^2 &= (6385.172 + 100)^2 + 24.518^2 - 2 \cdot (6385.172 + 100) \cdot 24.518 \cdot \sin(35\degree) = 41\:875\:656 \text{ km}^2\\
\therefore D &= 6471.140 \text{ km}
\end{align}
```
Now, by equation $7.10$:
```math
\begin{align}
6385.172 + 100 &= \frac{6471.140\cos(\phi')}{\cos(35\degree)}\\
\therefore \phi' &= \arccos\left(\frac{6485.172\cos(35\degree)}{6471.140}\right)\\
&= 34\degree\:49'\:19.82''
\end{align}
```
$\blacksquare$

### The Curvature of the Earth
In addition, the radius of curvature $R$ of a curve is given as:
```math
R = \left|\frac{(1 + y'^2)^{3/2}}{y''}\right|
```
And so for the Earth, which is an ellipse, we have from the equation of an ellipse:
```math
\begin{align}
y' &= \frac{dy}{dx} = -\frac{b^2x}{a^2y}\\
y'' &= \frac{d^2y}{dx^2} = -\frac{b^2}{a^2 y} + \frac{b^2 x}{a^2 y^2}\frac{dy}{dx} \\
&= -\frac{b^2}{a^2 y} - \frac{b^2 x}{a^2 y^2}\frac{b^2x}{a^2y} \\
&= -\frac{b^2 a^2 y^2 - b^4 x^2}{a^4 y^3} \\
&= -\frac{b^2 a^2 y^2 - b^4 a^2 (1 - y^2/b^2)}{a^4 y^3} \\
&= -\frac{b^2 a^2 y^2 - b^4 a^2 - b^2 a^2 y^2}{a^4 y^3} \\
&= -\frac{b^4}{a^2y^3}
\end{align}
```
And therefore we have:
```math
\begin{align}
R &= \frac{(1 + \frac{b^4x^2}{a^4y^2})^{3/2}}{\frac{b^4}{a^2y^3}}\\
&= \frac{(a^4y^2 + b^4x^2)^{3/2}}{a^4b^4}
\end{align}
```
When we substitute
```math
x = \frac{a \cos(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
\:\:\:\:\:\text{and}\:\:\:\:\:
y = \frac{(1 - e^2) a \sin(\phi)}{\sqrt{1-e^2\sin^2(\phi)}}
```
as well as $b^2 = a^2 (1 - e^2)$ into equation $7.14$, we obtain:
```math
\begin{align}
R &= \frac{\left(a^4\frac{(1 - e^2)^2 a^2 \sin^2(\phi)}{1-e^2\sin^2(\phi)} + b^4\frac{a^2 \cos^2(\phi)}{1-e^2\sin^2(\phi)}\right)^{3/2}}{a^4b^4}\\
&= \frac{\left(\frac{a^4(1 - e^2)^2 a^2 \sin^2(\phi) + b^4 a^2 \cos^2(\phi)}{1-e^2\sin^2(\phi)}\right)^{3/2}}{a^4b^4}\\
&= \frac{(a^4(1 - e^2)^2 a^2 \sin^2(\phi) + b^4 a^2 \cos^2(\phi))^{3/2}}{a^4b^4 (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{(b^4 a^2 \sin^2(\phi) + b^4 a^2 \cos^2(\phi))^{3/2}}{a^4b^4 (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{b^6 a^3 (\sin^2(\phi) + \cos^2(\phi))^{3/2}}{a^4b^4 (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{b^6 a^3}{a^4b^4 (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{b^2}{a (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{a^2 (1 - e^2)}{a (1-e^2\sin^2(\phi))^{3/2}}\\
&= \frac{a (1 - e^2)}{(1-e^2\sin^2(\phi))^{3/2}} \tag{7.15}
\end{align}
```
Locally therefore, the Earth can be approximated as a sphere with radius $R$. We can now calculate the altitude angle of the horizon at height $h$ above sea level.

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/709c76b6-0a8c-4d6f-b527-01b79d915f17" width="350"/> In this diagram, the Earth has been approximated as a sphere with radius $R$. The true horizon of an observer at the point $P$, which is at a height $h$ above the Earth, is given by $PT$ and not $PH$. The altitude angle of point $T$, $HPT$, is therefore given by:
```math
HPT = -(90\degree - CPT)
```
Where $CPT$ is given by:
```math
CPT = \arcsin\left(\frac{R}{R + h}\right)
```
Thus:
```math
HPT = -\left(90\degree - \arcsin\left(\frac{R}{R + h}\right)\right) = -\arccos\left(\frac{R}{R + h}\right) \tag{7.16}
```
This approximation works best when both the eccentricity of the ellipsoid and the altitude of the observer are low.

#### Example 7.3
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Find the altitude angle of the horizon of a viewer point with geographic latitude $35\degree$ and altitude $100\text{ km}$. <br/>
Use $a = 6378.137\text{ km}$ and $e = 0.081819$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $7.15$, the radius of curvature of the Earth at this latitude is:
```math
R = \frac{6378.137 (1 - 0.081819^2)}{(1-0.081819^2\sin^2(35\degree))^{3/2}} = 6356.427 \text{ km}
```
Therefore the altitude angle of the horizon is (by equation $7.16$):
```math
HPT = -\arccos\left(\frac{6356.427}{6356.427 + 100}\right) = -10\degree\:5'\:50''
```
$\blacksquare$
