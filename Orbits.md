# Orbits

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

Pictured here is an ellipse. It is like a squished circle. There are two things you should know about the ellipse:  
- The semi-major axis is the long "radius" of the ellipse. The distance from the center to the vertex.  
- The foci are the points at which the distance from the co-vertex to the foci equal the length of the semi-major axis.
The focus has many properties, but I will not get into them here. 

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

### 3. The square of the orbital period is proportional to the cube of the orbital semi-major axis.

Kepler's third law states that **the orbital period is linked to the orbital semi-major axis by a power of 3/2.**  
This means that $T$, the orbital period, is proportional to $R^{3/2}$, where $R$ is the orbital semi-major axis.  
This can be written as $T = k R^{3/2}$, where $k$ is called Kepler's constant, and is dependent on the units used.

An illustration:
Earth has an orbital period of $1$ year, and the semi-major axis of its orbit around the Sun is $1$ AU.  
Since $T = k R^{3/2}$, if we input our values, $1 = k \cdot 1^{3/2}$ gives $k = 1 \text{year}^2/\text{AU}^3$.  
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
<br />
<br />

### III. Eccentricity
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

The reference plane for the Solar System is most commonly the plane of the Earth's orbit, called the Ecliptic plane.  
For orbits around the earth, the reference plane can either be the Ecliptic plane or the plane of the Equator of the Earth, called the Equatorial plane.

There are two points where the orbit meets the reference plane, called the **nodes**. If the orbit is going upward (Northward) at a node, it's called the **ascending node** (Marked A in the diagram). If it is going downward (Southward), it's called the **descending node** (Marked D in the diagram).

<br />

The line that connects the ascending and descending nodes is called the Line of Nodes.

If a reference direction (Marked X in the diagram) is given, (usually the towards the [cusp of Aries](https://en.wikipedia.org/wiki/First_point_of_Aries)), the angle between it and the ascending node (angle in the direction of the orbit, marked with red arrowheads) is called the **Longitude of Ascending Node**, and is denoted $\Omega$ (Light blue in the diagram).

The orbit must have a periapsis. Say it is at point P in the diagram.  
The angle from the ascending node to the point of periapsis, **along the plane of the orbit**, is called the **Argument of Periapsis**, and is denoted $\omega$ (Dark blue in the diagram).
