## VII. Parallax

Our formulae for the location of planets in the sky, and hence the values in our ephemeris, are calculated for a hypothetical observer at the center of the Earth. These values are called the *true* values. On the surface, there is a measurable difference in the values of angles compared to their true values due to the difference in viewing location, particularly for close objects such as the Moon. The actual observed angles are called the *apparent* values, and their difference is called the *parallax*. Let us see how to calculate this parallax.

### The Shape of the Earth
In order to observe from the surface of the Earth, we must know the shape of the Earth. The Earth is roughly a squished sphere, meaning it is a spheroid. Due to the Earth's rotation, its polar radius its smaller than its equatorial radius. The amount of flattening of the Earth, called the *compression* ($c$), is calculated with the following formula:
```math
c = 1 - \frac{b}{a}\tag{14}
```
Where $b =$ the polar radius, and $a =$ the equatorial radius.

Since the eccentricity $e$ of an ellipse is defined by
```math
e^2 = 1 - \frac{b^2}{a^2}
```
it follows that
```math
e^2 = 1 - (1 - c)^2
```
```math
\therefore e = \sqrt{2c - c^2}.\tag{15}
```

### Latitude
How do we define latitude on a spheroid?

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/1b3d589b-28e2-4723-8f49-4938366bd700" width="350"/> In the diagram, where the Earth is depicted as an ellipse, we can see two ways to define the latitude of the point $P$. The *geocentric* latitude is given by the angle $PCE$, and the *geodetic* or *geographical* latitude given by the angle $POH$, where the line $OP$ is perpendicular to the tangent at $P$, $PT$.

When one refers to latitude, usually one is referring to the *geodetic* (*geographical*) latitude ($\phi$). For geographical reasons, when mapping the Earth, this definition of latitude is more convenient.

However, with astronomy, often the geocentric latitude ($\phi'$) is more convenient.\
So, given a geodetic latitude, how do we find the geocentric latitude?

<br/>

Well, consider the equation of the ellipse with semi-major axis $a$ and semi-minor axis $b$:
```math
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1\tag{16}
```
Because $PO$ is perpendicular to the tangent $PT$, the slope of $PO$ must be $-1/m_{PT}$. In other words:
```math
\tan(\phi) = -\frac{d x}{d y}
```
And from the triangle $PCQ$,
```math
\tan(\phi') = \frac{y}{x}
```
Implicitly differentiating equation $16$:
```math
\frac{y}{x} = -\frac{b^2}{a^2} \frac{d x}{d y}
```
Therefore:
```math
\tan(\phi') = \frac{b^2}{a^2} \cdot \tan(\phi).\tag{17}
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
\therefore \rho &= \frac{ab}{\sqrt{b^2 \cos^2(\phi') + a^2 \sin^2(\phi')}}\tag{18}\\
\end{align}
```
We can substitute $b^2 = a^2(1 - e^2)$, where $e =$ eccentricity of the Earth, and obtain:
```math
\begin{align}
\rho &= \frac{ab}{\sqrt{a^2(1 - e^2) \cos^2(\phi') + a^2 \sin^2(\phi')}}\\
&= \frac{b}{\sqrt{(1 - e^2) \cos^2(\phi') + \sin^2(\phi')}}\\
&= \frac{b}{\sqrt{\cos^2(\phi') + \sin^2(\phi') - e^2 \cos^2(\phi')}}\\
&= \frac{b}{\sqrt{1 - e^2 \cos^2(\phi')}}\tag{19}
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
\enspace\enspace\enspace\text{and}\enspace\enspace\enspace
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
\rho \cos(\phi') &= a \cos(\phi)\sec(\psi)\tag{20}\\
\rho \sin(\phi') &= a (1 - e^2) \sin(\phi)\sec(\psi)
\end{align}
```
We can deduce from equation $20$ by using the angle addition formulae
```math
\displaylines{
\begin{align}
\rho \cos(\phi - \phi') &= a \cos(\psi)\\
\rho \sin(\phi - \phi') &= a e^2 \cos(\phi)\sin(\phi)\sec(\psi)
\end{align}
}\tag{21}
```
By multiplying the 2nd line of equation $20$ with the 1st line of equation $21$, we obtain:
```math
\rho = a \sqrt{\frac{\cos(\phi)}{\cos(\phi')\cos(\phi-\phi')}}\tag{22}
```

#### Example 7
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
The Earth's equatorial radius and polar radius are given as $6378.137\enspace\text{km}$ and $6356.752\enspace\text{km}$ respectively. <br/>
Find the radius of the Earth at geographic latitude $35\degree N$.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

By equation $17$:
```math
\displaylines{
\tan(\phi') = \frac{6356.752^2}{6378.137^2} \cdot \tan(35\degree)\\
\therefore\phi' = 34\degree\enspace49'\enspace9.79''.
}
```
Then by equation $18$:
```math
\begin{align}
\rho &= \frac{ab}{\sqrt{b^2 \cos^2(\phi') + a^2 \sin^2(\phi')}}\\
&= \frac{6378.137\cdot6356.752}{\sqrt{6356.752^2 \cos^2(34\degree\enspace49'\enspace9.79'') + 6378.137^2 \sin^2(4\degree\enspace49'\enspace9.79'')}}\\
&= 6371.141\enspace\text{km}.
\end{align}
```
Or by equation $22$:
```math
\begin{align}
\rho &= a \sqrt{\frac{\cos(\phi)}{\cos(\phi')\cos(\phi-\phi')}}\\
&= 6378.137 \sqrt{\frac{\cos(35\degree)}{\cos(34\degree\enspace49'\enspace9.79'')\cos(35\degree-34\degree\enspace49'\enspace9.79'')}}\\
&= 6371.141\enspace\text{km}.
\end{align}
```
A solution by equation $19$ is also valid of course.\
$\blacksquare$
