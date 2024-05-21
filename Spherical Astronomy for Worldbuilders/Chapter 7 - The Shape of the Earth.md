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

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1b3d589b-28e2-4723-8f49-4938366bd700" width="350"/> In the diagram, where the Earth is depicted as an ellipse, we can see two ways to define the latitude of the point $P$. The *geocentric* latitude is given by the angle $PCE$, and the *geodetic* or *geographical* latitude given by the angle $POH$, where the line $OP$ is perpendicular to the tangent at $P$, $PT$, and $OH$ is parallel to $CE$.

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
Note that the exact distance to the center of the Earth also depend on the elevation of the observer (and no, it is not as simple as adding the elevation to $\rho$) but we will ignore this for simplicity, especially since any realistic elevation does not compare to the radius of the Earth. 

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
\:\:\:\text{and}\:\:\:
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
With the addition of an auxiliary $\psi$ defined via $\sin(\psi) = e\sin(\phi)$, these equations can be simplified:
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
\rho \cos(\phi - \phi') &= \rho\cos(\phi)\cos(phi') + \rho\sin(\phi)\sin(\phi')\\
&= a \cos^2(\phi) \sec(\psi) + a(1 - e^2) \sin^2(\phi) \sec(\psi)\\
&= a \sec(\psi) (\cos^2(\phi) + \sin^2(\phi) - e^2 \sin^2(\phi))\\
&= a \sec(\psi) (1 - e^2\sin^2(\phi)) \\
&= a \sec(\psi) (1 - sin^2(\psi)) \\
&= a \sec(\psi) \cos^2(\psi) \\
&= a \cos(\psi)
\end{align}
```
and
```math
\begin{align}
\rho \sin(\phi - \phi') &= \rho\sin(\phi)\cos(phi') - \rho\cos(\phi)\sin(\phi') \\
&= a \cos(\phi)\sec(\psi)\sin(\phi) - a (1 - e^2) \sin(\phi)\sec(\psi)\cos(phi) \\
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
