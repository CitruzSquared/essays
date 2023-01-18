# Beginner's guide to Orbits

This document will be discussing elliptical orbits.

## 1. Newton's Law of Gravitation
Newton's law of gravitation is the law that determines the force of gravity between two objects.  

It is given by $F = GMm/R^2$, where $M$ is the mass of the first object (in kilograms), $m$ is the mass of the second object (in kilograms), $R$ is the distance in between them (in meters), $G$ is a constant equalling $6.67 \cdot 10^{-11} {\text{ m}^3}/{\text{kg s}^2}$, and $F$ is the force in between those two objects (in Newtons).  

Everything discussed in this text stems from this equation.

## 2. Kepler's Laws of Planetary Motion
In orbital mechanics, there are 3 laws called Kepler's laws. (Because Johannes Kepler found them out).  
They can all be derived from Newton's law of gravitation, but I will not write down the derivations here.  
The laws are as follows:
### I. All orbits are elliptical, with the primary object at one of the ellipse's foci.
<img align="left" src="https://user-images.githubusercontent.com/23460281/212556101-5fc11bc9-2e65-4ea2-8aae-c8d8874aac32.png" alt="alt text" width="450" height="348"/>

Pictured here is an ellipse. It is like a squished circle. There are four things you should know about the ellipse:  
- The semi-major axis is the long "radius" of the ellipse. The distance from the center to the vertex.   
- The semi-minor axis is the short "radius" of the ellipse. The distance from the center to the co-vertex.  
- The foci are the points at which the distance from the co-vertex to the foci equal the length of the semi-major axis.  
The focus has many properties, but I will not get into them here.  
- The ellipse can be described by the equation $x^2/a^2 + y^2/b^2 = 1$, where $a$ is the semi-major axis, $b$ is the semi-minor axis, and $(0, 0)$ is the center of the ellipse.  

</br>

Kepler's first law states **that the primary body of the orbit (The body the orbit is centered around) is at one of the foci.**   

Well that's a bit of a lie. Technically its the barycenter, the center of mass of the two bodies, that is at the focus. But in cases where the two masses are incomparibly different, say the Sun and the Earth, this fact can be ignored and we can place the primary object at one of the foci.

### II. The line connecting the two bodies "sweeps" out equal areas during equal durations of time.
<img align="left" src="https://user-images.githubusercontent.com/23460281/212556615-cdeff256-7f4c-4ddd-aac4-7d70323ea0c9.gif" alt="alt text" width="450" height="300"/>

Kepler's second law states that when a body orbits another one, **the line connecting them will "sweep" out equal areas during equal durations of time.**

In the gif, the blue area is the area the planet is currently sweeping out in some fixed time interval, and Kepler's 2nd law states that the area of the blue region stays constant.

This defines the speed at which the body travels around the elliptical orbit.  

When the body is far away, it travels slowly. When it comes close, it travels quickly.

See [Conservation of Angular Momentum](https://en.wikipedia.org/wiki/Angular_momentum#Conservation_of_angular_momentum)

<br />

### III. The square of the orbital period is proportional to the cube of the orbital semi-major axis.

Kepler's third law states that **the orbital period is linked to the orbital semi-major axis by a power of 3/2.**  
This means that $T$, the orbital period, is proportional to $R^{3/2}$, where $R$ is the orbital semi-major axis.  
This can be written as $T = k R^{3/2}$, where $k$ is called Kepler's constant, and is dependent on the units used.

An illustration:
Earth has an orbital period of $1$ year, and the semi-major axis of its orbit around the Sun is $1$ AU.  
Since $T = k R^{3/2}$, if we input our values, $1 = k \cdot 1^{3/2}$ gives $k = 1 \text{ year}/\text{AU}^{3/2}$.  
Venus orbits at $0.723$ AU from the Sun.  
$T = k R^{3/2}, k = 1$.   
Therefore, $T = 0.723^{3/2}$, giving $T = 0.615$ years.  
This is Venus's orbital period.

## 3. Orbital Elements
There are a few key elements that describe an orbit.  
Apsides, Eccentricity, Inclination, Nodes, and Argument of Periapsis.

### I. Apsides
<img align="left" src="https://user-images.githubusercontent.com/23460281/212558162-3907bab9-5856-40d2-ace1-bcd1fa89a61e.png" alt="alt text" width="450" height="396"/>

In an elliptical orbit, there are points at which the orbiting body is closest to the primary, and farthest from the primary.  
These are called the **periapsis** and **apoapsis** respectively.  

If we call the distance from the primary to the orbiter at periapsis $P$, and the distance at apoapsis $A$, then $(P + A)/2$ gives the length of the semi-major axis.

The line that connects the two apsides is called the Line of Apsides.

<br />
<br />
<br />
<br />
<br />
<br />
<br />

### II. Eccentricity
How do we define how elliptical an orbit is?  
Well, this is done with the eccentricity of an orbit.  
If we call the distance from the center to the foci $c$, and the length of the semi-major axis $a$, eccentricity $e$, is defined by $c/a$.  

<img align="left" src="https://user-images.githubusercontent.com/23460281/212558513-6f44c454-fcee-4da7-aa8a-c2c22f8b24b5.png" alt="alt text" width="300" height="627"/>

Eccentricity ranges from $0$ to $1$, with $0$ being a perfect circle.  
As eccentricity increases, the ellipse gets more elongated and the foci get pushed out to the vertices.  
This diagram shows ellipses of increasing eccentricity, with $e = 0$ being the first image.

<br />

Given the eccentricity $e$ and the semi-major axis $a$, one can find the distances to periapsis and apoapsis.  
If we call the distance from the primary to the orbiter at periapsis $P$, and the distance from the primary to the orbiter at apoapsis $A$, because the primary is at distance $c$ from the center of the ellipse,   
$P = a - c$ and $A = a + c$.  
Since $e = c/a$, $P = a - ae$ and $A = a + ae$.  
Which can be simplified to $P = a(1 - e)$ and $A = a(1 + e)$.

<br />

Another formula for the eccentricity can be derived as follows:  
If we call the length of the semi-minor axis $b$,  
Becase the foci are the points at which the distance from the co-vertex to the foci equal the length of the semi-major axis, by the Pythagorean theorem, 
$c^2 + b^2 = a^2$.  

Thus $c = \sqrt{a^2 - b^2}$,  
And $e = \sqrt{a^2 - b^2}/a$.  
Dividing the numerator and denominator by $a$,  
$e = \sqrt{1 - b^2/a^2}/1 = \sqrt{1 - b^2/a^2}$.

<br />

### III. Inclination, the Nodes, and the Argument of Periapsis

<img align="left" src="https://user-images.githubusercontent.com/23460281/212560350-41200278-b093-4fac-9b11-ddb54ec772b7.png" alt="alt text" width="450" height="300"/>

Orbital inclination $i$ is the angle the orbit makes from a reference plane (Green in the diagram).  

The reference plane for the Solar System is most commonly the plane of the Earth's orbit, called the Ecliptic plane. (And therefore the Earth has no inclination with respect to the Ecliptic plane).   
For orbits around the Earth, the reference plane can either be the Ecliptic plane or the plane of the Equator of the Earth, called the Equatorial plane.

There are two points where the orbit meets the reference plane, called the **nodes**. If the orbit is going upward (Northward) at a node, it's called the **ascending node** (Marked A in the diagram). If it is going downward (Southward), it's called the **descending node** (Marked D in the diagram).

<br />

The line that connects the ascending and descending nodes is called the Line of Nodes.

If a reference direction (Marked X in the diagram) is given, (usually the towards the [cusp of Aries](https://en.wikipedia.org/wiki/First_point_of_Aries)), the angle between it and the ascending node (angle in the direction of the orbit, marked with red arrowheads) is called the **Longitude of Ascending Node**, and is denoted $\Omega$ (Light blue in the diagram).

The orbit must have a periapsis. Say it is at point P in the diagram.  
The angle from the ascending node to the point of periapsis, **along the plane of the orbit**, is called the **Argument of Periapsis**, and is denoted $\omega$ (Dark blue in the diagram).


## 4. The Position of the Orbiting Body at Time = t

### I. Along the orbit

<img align="left" src="https://user-images.githubusercontent.com/23460281/212620383-b2971cfc-003a-4fbd-ad00-883590d31f7c.png" alt="alt text" width="450" height="346"/>

The position of the orbiting body can be given as $x, y$ coordinates with the origin $(0, 0)$ being placed at the focus, and the $x$ axis pointing towards periapsis.  This coordinate system is called the **periforcal coordinate system**.
The calculation of the $x, y$ coordinates is as follows:  

First it would be a great start to get a rough approximation of the position of the object.  
Disregarding Kepler's second law, we can assume the body moves in the orbit at a uniform rate.  
If we say that the orbital period is $T$, then the rate at which the body orbits is given by $2\pi/T$. This is called the mean motion.  

Then, at a time $t$, where $t = 0$ means the body is at periapsis, the angle the body has moved through is $2\pi/T \cdot t$.  
This is called the **mean anomaly** ( $M$ ).

<img align="left" src="https://user-images.githubusercontent.com/23460281/212613418-99c63c77-38f4-4f36-a7ef-6b33045bfe92.png" alt="alt text" width="450" height="450"/>

To get one step closer to calculating the coordinates and to take Kepler's second law into account, we imagine a circle around the orbit with radius equal to the semi major axis.  
The position of the body can be projected vertically onto the circle, and the angle between the projected position, the center, and periapsis ( $\angle B'CP$ ) is called the **eccentric anomaly** ( $E$ ).

Eccentric anomaly can be described by Kepler's equation:  
$M = E - e\sin E$, where $e$ is the eccentricity.  
The derivation of this equation can be seen [here](http://www.csun.edu/~hcmth017/master/node15.html).

Solving this equation for $E$ analytically is impossible due to $\sin x$ being a transcendental function, and we must approximate it.  
Luckily, [Newton's method](https://en.wikipedia.org/wiki/Newton%27s_method) allows us to approximate it with arbitrary precision extremely quickly.  
Newton's method gives:  
$E_{n+1} = (E_n - e \sin E_n - M)/(1 - e \cos E_n)$.  
We first assume $E_1 = M$. Then we plug this into the formula for $E_n$.  
We now have $E_2$, a better approximation for $E$.  
We now plug this new value back into $E_n$, and calculate $E_3$.  
Repeating this until $E_5$ is sufficient.

If we call the position of the orbiting body $(x, y)$ and the center of the circle $(0, 0)$,   
We can see that $\cos E = x/a$. (Because the radius of the circle is $a$, and $B$ and $B'$ have the same $x$ coordinate.)  
Because the ellipse can be described as $x^2/a^2 + y^2/b^2 = 1$,  
$\cos^2 E + y^2/b^2 = 1$,   
Therefore, by the Pythagorean identity $\cos^2 x + \sin^2 x = 1$,  
$\sin E = y/b$.  
Thus the coordinates of the body around the center is given by $(a \cos E, b \sin E)$.

To move the origin to the focus, recall that $e = c/a$, and therefore $c = ea$.  
Also, only the $x$ coordinate will be changed, as the focus lies on the $x$ axis.  
Thus we subtract $c$ from the $x$ coordinate.  
**Therefore the perifocal coordinates of the orbiting body is:**  
$(a \cos E - ae, b \sin E)$.  
or, in 3D space:  
$(a \cos E - ae, b \sin E, 0)$.  
Thus our problem is solved.

However, there is another way of describing our orbit. That is, with the angle the object has travelled since periapsis, and the distance from the focus to the object.  
This angle ( $\angle BFP$, denoted $\theta$ ) is called the **true anomaly**.  
It is described by the formula:  
$\cos \theta = (\cos E - e)/(1 - e\cos E)$.  
Which can also be written:  
$\theta = 2 \cdot \arctan \left(\sqrt{\frac{1+e}{1-e} \tan \frac{E}{2}}\right)$.

The distance from the focus to the orbiting body $r$ can be given as follows:  
$r = a(1 - e \cos E)$  
or  
$r = a \cdot (1 - e^2)/(1 + e \cos \theta)$.

And so the perifocal coordinates of our body can also be given as:  
$(r \cos \theta, r \sin \theta)$  
or, in 3D space:  
$(r \cos \theta, r \sin \theta, 0)$.  

### II. In a fixed reference frame

The orbit can be tilted in numerous ways.  
Therefore, knowing the position of the orbiting body in the perifocal coordinate system is not enough.  
If we wish to compare two different orbits, or determine the relative position of a body from another orbiting body, we must know their coordinates in absolute terms.  

Referring back to [3.III](https://github.com/CitruzSquared/essays/blob/main/Orbits.md#iii-inclination-the-nodes-and-the-argument-of-periapsis), we have an absolute frame of reference. The ecliptic plane for Heliocentric orbits, and the ecliptic or equatorial plane for Geocentric orbits.  
The formula for calculating the coordinates in these reference frames is as follows:  

```math
\begin{bmatrix}
  x_\text{reference} \\
  y_\text{reference} \\
  z_\text{reference}
 \end{bmatrix}
 =
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & \sin\Omega \sin i \\
  \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega & -\cos \Omega \sin i \\
  \sin i \sin\omega & \sin i \cos\omega &  \cos i
 \end{bmatrix}
 \begin{bmatrix}
  x_\text{perifocal} \\
  y_\text{perifocal} \\
  z_\text{perifocal}
 \end{bmatrix}
 ```
 Where:  
 $\Omega$ is the Longitude of Ascending Node,  
 $i$ is the Inclination,  
 and $\omega$ is the Argument of Periapsis.  
 $(x_\text{perifocal}, y_\text{perifocal}, z_\text{perifocal})$ are the $(a \cos E - ae, b \sin E, 0)$ or $(r \cos \theta, r \sin \theta, 0)$ as derived earlier.  
 $(0, 0, 0)$ are the coordinates of the primary body in the absolute frame.
 
 The result may be turned to spherical coordinates using these formulae:  
 $x = r \cos \phi \cos \lambda$  
 $y = r \cos \phi \sin \lambda$  
 $z = r \sin \phi$  
 Where:  
 $r$ is the distance from the center of the primary to the orbiting body $a(1 - e \cos E)$ or $a \cdot (1 - e^2)/(1 + e \cos \theta)$,  
 $\phi$ is the Latitude (in case of Ecliptic coordinates) or Declination (in case of Equatorial coordinates),  
 and $\lambda$ is the Longitude (in case of Ecliptic coordinates) or Right Ascension (in case of Equatorial coordinates).
 
 ## 5. Solved Example
 Let us calculate the **geocentric ecliptic coordinates** of Mars on January 19th, 2023.  
 Because we are working in geocentric coordinates, we must calculate the relative position of Mars from Earth, which requires calculation of both Mars and Earth's positions.
 
 First, need to know the orbital elements of Earth and Mars.  
 Because we are working in Ecliptic coordinates, the inclination of the Earth should be zero, but because orbits are not static, as of 2023, compared to the Earth's orbit at year 2000, Earth's orbit has these elements:
 
 Semi-major axis $a = 1$ AU  
 Semi-minor axis $b = 0.999860401599$ AU  
 Eccentricity $e = 0.0167086$  
 Orbital Period $T = 365.25636$ days  
 Inclination $i = 0.00005\degree = 8.72665 \cdot 10^{-7} \text{rad}$ (Ignorable)  
 Longitude of Ascending Node $\Omega = −11.26064\degree = -0.1965352 \text{rad}$  
 Argument of Periapsis $\omega = 114.20783\degree = 1.9933027 \text{rad}$  
 
 For Mars:  
 Semi-major axis $a = 1.52368055$ AU  
 Semi-minor axis $b = 1.51702003298$ AU  
 Eccentricity $e = 0.0934$  
 Orbital Period $T = 686.980$ days  
 Inclination $i = 1.850\degree = 0.0322886 \text{rad}$   
 Longitude of Ascending Node $\Omega = 49.57854\degree = 0.8653088 \text{rad}$  
 Argument of Periapsis $\omega = 286.5\degree = 5.00037 \text{rad}$  
 
 We also need the time elapsed since periapsis.  
 Earth reached its last periapsis on January 4th of 2023.  
 Mars reached its last periapsis on June 21st of 2022.  
 
 This means that it has been 15 days since Earth's last periapsis, and 212 days since Mars's last periapsis.
 
 *Data from Wikipedia.*
 
 ### I. Earth Calculations
 
 Now let's calculate the position of the Earth on January 19th, 2023.  
 Earth's mean motion is $2\pi/365.25636 = 0.017202124303 \text{rad}/\text{day}.$  
 At $t = 15$, the Mean Anomaly $M = 0.017202124303 * 15 = 0.258031864545 \text{rad}$.  
 Carrying out the Newton Iteration  
 $E_{n+1} = (E_n - e \sin E_n - M)/(1 - e \cos E_n)$  
 4 times gives:  
 $E = 0.262365504457$.  
 Thus the perifocal coordinates of the Earth are:   
 $(a \cos E - ae, b \sin E, 0)$  
 $= (0.94907054974, 0.259329623245, 0)$.
 
 Let's now find the rotation matrix for calculating the Earth's heliocentric ecliptic coordinates.  
 ```math
 \begin{bmatrix}
  \cos\Omega\cos\omega - \sin\Omega\cos i\sin\omega & -\cos\Omega\sin\omega - \sin\Omega\cos i\cos \omega & \sin\Omega \sin i \\
  \sin\Omega\cos\omega + \cos\Omega\cos i\sin\omega & -\sin\Omega\sin\omega + \cos\Omega\cos i\cos\omega & -\cos \Omega \sin i \\
  \sin i \sin\omega & \sin i \cos\omega &  \cos i
 \end{bmatrix}
 ```
 We can say $i = 0$ for convenience.  
 Also, since $z_{\text{perifocal}} = 0$, we can ignore the 3rd column of the matrix. (set to 0).  
 Doing the calculations, it gives:  
  ```math
 \begin{bmatrix}
 −0.224052950686 & −0.97457697248 & 0 \\
 0.97457697248 & −0.224052950686 & 0 \\
 0 & 0 & 0
 \end{bmatrix}
 ```
 
 Carrying out the matrix multiplication gives the heliocentric ecliptic coordinates of the Earth as:  
 $\oplus(-0.46537873617, 0.8668387357, 0)$.
 
 ### II. Mars Calculations 
 
 Doing the math for Mars is much the same.  
 $t = 212$, so $M = 1.93897243751$.  
 Doing the Newton Iteration,  
 $E = 2.02298507585$.  
 Therefore the perifocal coordinates are:  
 $(−0.808061647728, 1.36454877288, 0)$.  
 
 The matrix for Mars is:  
 ```math
 \begin{bmatrix}
 0.913722378184 & 0.405595108205 & 0 \\
 −0.40515835572 & 0.914006859473 & 0 \\
 −0.0309535522544 & 0.00916891689845 & 0
 \end{bmatrix}
 ```  
 Notice how the last row isnt all $0$ since $i \neq 0$.  
 Carrying out the matrix multiplication gives the heliocentric ecliptic coordinates of Mars as:  
 $M(-0.18488970329, 1.57459986701, 0.0375238127401)$. 
 
 ### III. Calculation of Geocentric Coordinates
 
 Now let's subtract the coordinates of the Earth from the coordinates of Mars to get relative position of Mars from Earth.  
 $M - \oplus = (0.28048903288, 0.707761, 0.0375238127401)$.  
 
 Now let's convert this to spherical coordinates.  
 $x = r \cos \phi \cos \lambda$  
 $y = r \cos \phi \sin \lambda$  
 $z = r \sin \phi$    
 
 Since $x, y, z$ are all multiplied by $r$, we can normalize the vector and cancel all the $r$'s.  
 $(M - \oplus)\_{\text{norm}} = (0.367981, 0.928529, 0.0492284)$.  
 Now:  
 $z = \sin \phi \implies \phi = 2\degree 49'$  
 Since $y/x = \tan \lambda$,  
 $lambda = \arctan(y/x) = 68\degree 23'$.  
 
 Therefore our calculations show that on January 19, 2023, Mars will be found at:  
 Longitude: $68\degree 23'$  
 Latitude: $2\degree 49'$  
 In the constellation of Taurus.  
 
 Consulting an ephemeris shows our calculations as exact to within $3'$ in Longitude, and $30"$ in Latitude.
 
 ## 6. Further Reading
 [Orbit](https://en.wikipedia.org/wiki/Orbit)  
 [Orbital Mechanics](https://en.wikipedia.org/wiki/Orbital_mechanics)  
 [Kepler's Laws](https://en.wikipedia.org/wiki/Kepler%27s_laws_of_planetary_motion)  
 [Kepler's Equation](https://en.wikipedia.org/wiki/Kepler%27s_equation)  
 [Equatorial Coordinates](https://en.wikipedia.org/wiki/Equatorial_coordinate_system)  
 [Ecliptic Coordinates](https://en.wikipedia.org/wiki/Ecliptic_coordinate_system)  
