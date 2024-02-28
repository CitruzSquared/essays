### Saturn in the Sky
We figured out how Venus looked in examples $4.1$ and $6.7$. Let's do something more detailed: Let's try to figure out how Saturn looked in the sky on $\text{January 1, } 2024$ at $19:00$ from London, UK ($\phi = +51\degree, l = 0\degree$).

#### 1. Data Collection
To figure out what Saturn looked like from the Earth, we must first know how Saturn looks in general:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/31cbc860-fe82-4627-9ba9-2bc59c92890b" width="350"/> First, and foremost, Saturn can be well modeled as a giant sphere, $58$ $232 \text{ km}$ in radius. 

In addition to that though, the planet has some gorgeous rings. The rings are made up of many parts, but we can generally say that the brightest parts form a disk on the plane of Saturn's equator, spanning from $92$ $000\text{ km}$ to $136$ $780\text{ km}$ from the planet's center (rings B and A).

Saturn's north pole points towards $\alpha = 2^h$ $42^m$ $21^s$, $\delta = 83\degree$ $32'$ $13''$ (*Saturn-centric* Earth equatorial coordinates).

Now that we know some things about Saturn, let's get onto things we need to know to calculate its appearance.\
The sidereal time at $19:00, \text{ January 1, } 2024$ was:
```math
\Theta = 25\degree\:55'\:58.5''
```
The geocentric locations of Saturn and the Sun were:
- Saturn ($P$):
```math
\begin{align}
\alpha_P &= 22^h\:22^m\:07.21^s\\
\delta_P &= -11\degree\:55'\:54.3''\\
\rho_P &= 1\:540\:141\:300\text{ km}
\end{align}
```
- The Sun ($S$):
```math
\begin{align}
\alpha_S &= 18^h\:45^m\:45.07^s\\
\delta_S &= -23\degree\:01'\:15.8''\\
\rho_S &= 147\:099\:700\text{ km}
\end{align}
```
Note that these values differ slightly from examples $4.1$ and $6.7$ because we used a different data set. (Why do different data sets differ on the same quantities? I do not know.)

#### 2. Vectors
In a worldbuilding setting, we would have the vector forms, not the spherical forms. Let's convert the spherical coordinates to vectors by equation $1.1$:
- Earth to Saturn Vector ($\textbf{p}$):
```math
\textbf{p}=
\begin{bmatrix}
1\:371\:517\:050\\-624\:168\:063\\-318\:418\:649
\end{bmatrix}
```
- Earth to Sun Vector ($\textbf{s}$):
```math
\textbf{s}=
\begin{bmatrix}
26\:847\:342\\-132\:696\:193\\-57\:526\:188
\end{bmatrix}
```
- Sun to Saturn Vector ($\textbf{v}$):\
This is given by $\textbf{p} - \textbf{s}$.
```math
\textbf{v}=
\begin{bmatrix}
1\:344\:669\:710\\-491\:471\:870\\-260\:892\:461
\end{bmatrix}
```
And their normalized forms (Direction vectors)
```math
\textbf{p}_d=
\begin{bmatrix}
0.89051378\\-0.405266753\\-0.20674639
\end{bmatrix}
\enspace\enspace
\textbf{s}_d=
\begin{bmatrix}
0.18251119\\-0.90208337\\-0.39106938
\end{bmatrix}
\enspace\enspace
\textbf{v}_d=
\begin{bmatrix}
0.92401427\\-0.33772384\\-0.17927700
\end{bmatrix}
```
The Sun - Saturn distance is given by the magnitude of $\textbf{v}$:
```math
|\textbf{v}| = 1\:455\:247\:779\text{ km}
```
Additionally, the direction vector pointing towards the North pole of Saturn (from the center of Saturn):
```math
\textbf{n}=
\begin{bmatrix}
0.08548148\\0.07323415\\0.99364464
\end{bmatrix}
```
#### 2. Phase
Let's calculate the phase of Saturn. We have all the distances already so we can go straight to equation $4.5$:
```math
\begin{align}
\text{Phase Angle } &= \arccos\left(\frac{1\:540\:141\:300^2 + 1\:455\:247\:779^2 - 147\:099\:700^2}{2\cdot1\:540\:141\:300\cdot1\:455\:247\:779}\right)\\
&=4\degree\:36'
\end{align}
```
Therefore, by equation $4.6$:
```math
\begin{align}
\text{Phase}\% &= \frac{1 + \cos(4\degree\:36')}{2}\cdot100\%\\
&= 99.84\%
\end{align}
```
This makes sense as planets in the far reaches of the Solar System tend to always be at full phase.
#### The Rings

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/9fb1a5ab-ba66-4f31-aa40-a117b2f0cbb3" width="350"/> In this diagram, the center of Saturn is $C$, and the rings span from $A$ to $B$. $\textbf{n}$ is the vector to the north pole, perpendicular to the plane of the rings (the equator) and the Earth is in the direction $-\textbf{p}$ (because the Earth to Saturn vector is $\textbf{p}$, the Saturn to Earth vector must be $-\textbf{p}$).

From the view of the Earth, the rings look like they span the distance $A'B'$, which is the projection of $AB$ perpendicular to $\textbf{p}_d$. Thus the radii of the disks appear to be:
```math
C'A' = CA\sin(QCA)
```
but since $QCA = 90\degree - NCQ$:
```math
C'A' = CA\cos(NCQ)
```
$\cos(NCQ)$ is given by the dot product of the two direction vectors $\textbf{n}$ and $-\textbf{p}_d$:
```math
\begin{bmatrix}
0.08548148\\0.07323415\\0.99364464
\end{bmatrix}\cdot
\begin{bmatrix}
-0.89051378\\0.405266753\\0.20674639
\end{bmatrix}
=0.158989
```
Thus:
```math
\begin{align}
\text{Ring Size}_O &= 136\:780\cdot0.158989 = 21\:747\text{ km}\\
\text{Ring Size}_I &= 92\:000\cdot0.158989 = 14\:627\text{ km}
\end{align}
```
Where $O$ and $I$ stand for the outer and inner edge of the rings respectively. Note that these are just the vertical sizes, and the horizontal size is the full $136$ $780\text{ km}$ and $92$ $000\text{ km}$; i.e. the outer edge of the rings looks like an ellipse with height radius $21$ $747\text{ km}$ and width radius $136$ $780\text{ km}$, and the inner edge looks like an ellipse with height radius $14$ $627\text{ km}$ and width radius $92$ $000\text{ km}$.

#### Apparent Diameters
Let's now calculate the apparent sizes of everything from Earth.\
By equation $4.2$ (remembering to use $\arctan()$ for the rings since they are disks):
```math
\begin{align}
\text{Saturn } &= 2\arcsin\left(\frac{58\:232}{1\:540\:141\:300}\right) = 16.00''\\
\text{Inner Ring Horiz. } &= 2\arctan\left(\frac{92\:000}{1\:540\:141\:300}\right) = 24.64''\\
\text{Inner Ring Vert. } &= 2\arctan\left(\frac{14\:627}{1\:540\:141\:300}\right) = 3.92''\\
\text{Outer Ring Horiz. } &= 2\arctan\left(\frac{136\:780}{1\:540\:141\:300}\right) = 36.64''\\
\text{Outer Ring Vert. } &= 2\arctan\left(\frac{21\:747}{1\:540\:141\:300}\right) = 5.82''
\end{align}
```

#### Shadow of Saturn on its Rings
Now would be a great time to familiarize oneself with [vector projection](https://en.wikipedia.org/wiki/Vector_projection). 

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/e98ab018-21b8-4ab8-b807-e05c880c39bb" width="350"/> Let's approximate the shadow of Saturn on its rings as a straight line shadow in the direction of a vector $\textbf{a}$ like the diagram. Because $\textbf{a}$ is in the same direction as Saturn is from the Sun ($\textbf{v}_d$) but in the plane of the rings (Saturn's equator), its the projection of $\textbf{v}_d$ onto Saturn's equator, and since Saturn's equator is perpendicular to the North pole vector $\textbf{n}$, $\textbf{a}$ is the "rejection" of $\textbf{v}_d$ from $\textbf{n}$.

The rejection can be calculated as follows:
```math
\textbf{a} = \textbf{v}_d - \text{proj}_{\textbf{n}}\textbf{v}_d
```
Where $\text{proj}_{\textbf{n}}\textbf{v}_d$ is the projection of $\textbf{v}_d$ onto $\textbf{n}$:
```math
\text{proj}_{\textbf{n}}\textbf{v}_d = (\textbf{n}\cdot\textbf{v}_d)\textbf{n}
```
Carrying out the math,
```math
\begin{align}
\text{proj}_{\textbf{n}}\textbf{v}_d = \left(
\begin{bmatrix}
0.08548148\\0.07323415\\0.99364464
\end{bmatrix}\cdot
\begin{bmatrix}
0.92401427\\-0.33772384\\-0.17927700
\end{bmatrix}
\right)
\begin{bmatrix}
0.08548148\\0.07323415\\0.99364464
\end{bmatrix}
=
\begin{bmatrix}
-0.01058983\\-0.00907257\\-0.12309711
\end{bmatrix}\\
\\ \therefore
\textbf{a} =
\begin{bmatrix}
0.92401427\\-0.33772384\\-0.17927700
\end{bmatrix} -
\begin{bmatrix}
-0.01058983\\-0.00907257\\-0.12309711
\end{bmatrix}
=
\begin{bmatrix}
0.93460409\\-0.32865127\\-0.05617989
\end{bmatrix}
\end{align}
```
Which, when normalized becomes:
```math
a=
\begin{bmatrix}
0.94185956\\-0.33120264\\-0.05661602
\end{bmatrix}
```
So the shadow points in the direction of $\textbf{a}$ in Saturn-centric Earth Equatorial coordinates.

#### Orientation of Saturn
To determine the plane of Saturn's equator from the Earth's view, let us define new coordinate axes such that the $x$-axis points towards Saturn. To do this:
1. We first rotate by $22^h$ $22^m$ $07.21^s$ (the right ascension of Saturn) about the $z$-axis.
```math
R_1 = \begin{bmatrix}
\cos(22^h\:22^m\:07.21^s) & \sin(22^h\:22^m\:07.21^s) & 0 \\
-\sin(22^h\:22^m\:07.21^s) & \cos(22^h\:22^m\:07.21^s) & 0 \\
0 & 0 & 1
\end{bmatrix}
```
2. Then, we rotate by $-11\degree$ $55'$ $54.3''$ (the declension of Saturn) about the $y$-axis.
```math
R_2 = \begin{bmatrix}
\cos(-11\degree\:55'\:54.3'') & 0 & -\sin(-11\degree\:55'\:54.3'')\\
0 & 1 & 0\\
\sin(-11\degree\:55'\:54.3'') & 0 & \cos(-11\degree\:55'\:54.3'')
\end{bmatrix}
```
3. The total rotation is given by the matrix product $R_2 R_1$, which when calculated gives:
```math
R = \begin{bmatrix}
0.89051378 & -0.40526675 & -0.20674639\\
0.41421607 & 0.91017858 & 0\\
0.18817613 & -0.08563768 & 0.97839457
\end{bmatrix}
```
The reverse rotation is given by the transpose $R^T$:
```math
R^T = \begin{bmatrix}
0.89051378 & 0.41421607 & 0.18817613 \\
-0.40526675 & 0.91017858 & -0.08563768\\
-0.20674639 & 0 & 0.97839457
\end{bmatrix}
```
We can verify the matrix by doing the simple calculation which transforms the vector $\textbf{p}$ into our new coordinate frame:
```math
R\cdot \textbf{p} =\begin{bmatrix}
0.89051378 & -0.40526675 & -0.20674639\\
0.41421607 & 0.91017858 & 0\\
0.18817613 & -0.08563768 & 0.97839457
\end{bmatrix}
\begin{bmatrix}
1\:371\:517\:050\\-624\:168\:063\\-318\:418\:649
\end{bmatrix} =
\begin{bmatrix}
1\:540\:141\:300\\0\\0
\end{bmatrix}
```
And we can see we get an answer solely in the $x$-axis, which is the expected answer. Note that this transformation does not affect the grid rotation (i.e. the grid will still be pointing straight up and down and straight left and right) because we did not rotate about the $x$-axis.

We can now transform the North pole vector $\textbf{n}$:
```math
R\cdot\textbf{n} = \begin{bmatrix}
0.89051378 & -0.40526675 & -0.20674639\\
0.41421607 & 0.91017858 & 0\\
0.18817613 & -0.08563768 & 0.97839457
\end{bmatrix}
\begin{bmatrix}
0.08548148\\0.07323415\\0.99364464
\end{bmatrix}=
\begin{bmatrix}
-0.15898937\\0.10206395\\0.98199049
\end{bmatrix}
```
We can see that the $x$ coordinate is negative and therefore the north pole vector is pointing towards the Earth.

We can also transform the shadow vector $\textbf{a}$:
```math
R\cdot\textbf{a} = \begin{bmatrix}
0.89051378 & -0.40526675 & -0.20674639\\
0.41421607 & 0.91017858 & 0\\
0.18817613 & -0.08563768 & 0.97839457
\end{bmatrix}
\begin{bmatrix}
0.94185956\\-0.33120264\\-0.05661602
\end{bmatrix}=
\begin{bmatrix}
0.9846695\\0.08867982\\0.15020611
\end{bmatrix}
```
The $x$ coordinate is positive so the shadow vector is pointing away from us (to be expected).

We can project these vectors onto the viewing plane (the $yz$-plane) by simply removing the $x$ component:
```math
\textbf{n}_p = \begin{bmatrix}
0\\0.10206395\\0.98199049
\end{bmatrix}
\enspace\enspace
\textbf{a}_p = \begin{bmatrix}
0\\0.08867982\\0.15020611
\end{bmatrix}
```
When "zoomed in" into an object enough, the spherical grid can be approximated by a regular grid. (see [small angle approximation](https://en.wikipedia.org/wiki/Small-angle_approximation)). Therefore we can treat these as planar vectors since we are dealing with angles in the arcseconds. Let's multiply $\textbf{n}'$ by $8.00''$ (the angular radius of Saturn; half of the value we calculated earlier) to see where the North pole lies in our view.
```math
8.00''\textbf{n}_p = \begin{bmatrix}
0''\\0.81651164''\\7.85592395''
\end{bmatrix}
```
Remembering that the positive $y$-axis lies to the left, (the positive $y$-axis is left of the positive $x$-axis), we can treat this vector as simple coordinates, and thus, We can start drawing out the shape of Saturn:

<p align="center">
  <img width="200" src="https://github.com/CitruzSquared/essays/assets/23460281/caa11f62-25de-44f3-bceb-971543cd4f09"> <br/>
  $C$ and $N$ are the center and North pole of Saturn respectively. <br/> The phase is not drawn because it is close to $100$%.
</p>

Using the fact that the equator is perpendicular to the line $NC$, we can draw the rings too (using the angular sizes from before):

<p align="center">
  <img width="400" src="https://github.com/CitruzSquared/essays/assets/23460281/1b106d84-4a18-4544-aa62-cb2786a434ec"> <br/>
  The line through $C$ that is perpendicular to $NC$ is the axis of the ellipses of the rings. <br/> The rings are seen from above because the North pole faces the Earth.
</p>

We can now also draw the shadow of Saturn on its rings. Drawing a line along the vector $\textbf{a}_p$ starting at either edge of Saturn's equator:

<p align="center">
  <img width="400" src="https://github.com/CitruzSquared/essays/assets/23460281/33643fc1-a5ee-41c3-99d4-d729d91b89dc"> <br/>
  The two lines outline the shadow.
</p>

#### Horizontal Coordinates
Finally, we have to figure out how the planet looked from London at the specified time. The overall features would look the same, but tilted by some amount. We can find out the tilt of the equatorial grid in relation to the horizontal grid in the same way we found the lighting direction in example $6.7$: we can find the direction to the Celestial North pole after transforming to horizontal coordinates.

First, we need the hour angles of both Saturn and the Celestial North Pole. We have $\Theta$ and $\alpha_\text{Saturn}$ from before. The Celestial pole lies at $\alpha = 0^h$, $\delta = 90\degree$. Thus:
```math
\begin{align}
h_P &= 25\degree\:55'\:58.5'' - 22^h\:22^m\:07.21^s = 50\degree\:24'\:10.35''\\
h_{NP} &= 25\degree\:55'\:58.5'' - 0^h = 25\degree\:55'\:58.5''
\end{align}
```
Where $P$ is Saturn and $NP$ is the Celestial North pole.\
Thus, the horizontal coordinates are (by equation $6.3$ with $\phi = 51\degree$):
```math
\begin{align}
A_P &= 230\degree\:48'\:18.8''\\
a_P &= 13\degree\:24'\:7.0''\\
A_{NP} &= 0\degree\\
a_{NP} &= 51\degree
\end{align}
```
Now we follow example $6.7$.\
The angle between Saturn and the Celestial North Pole is simply their difference in declinations $90\degree - \delta_P$:
```math
90\degree - \delta_P = 101\degree\:55'\:54.3''
```
And the zenith distances are:
```math
\begin{align}
\zeta_P &= 90\degree - 13\degree\:24'\:7.0'' = 76\degree\:36'\:53.0''\\
\zeta_{NP} &= 90\degree - 51\degree = 39\degree\\
\end{align}
```
Therefore, by equation $6.8$:
```math
\begin{align}
\text{Tilt } &= \arccos\left(\frac{\cos(39\degree) - \cos(76\degree\:36'\:53.0'')\cos(101\degree\:55'\:54.3'')}{\sin(76\degree\:36'\:53.0'')\sin(101\degree\:55'\:54.3'')}\right)\\
&= 29\degree\:54'\:1.7''\\
\end{align}
```
So Saturn is tilted by $29\degree$ $54'$ $1.7''$ from the vertical, keeping in mind that the celestial pole is to the right (the celestial pole is in the North and Saturn (Azimuth = $230\degree$) is in the Southwest). Thus:

<p align="center">
  <img width="500" src="https://github.com/CitruzSquared/essays/assets/23460281/4e396ea1-9af5-44f5-b3e1-97b8436ab1b4"> <br/>
  Saturn from London, UK on $\text{January 1, } 2024$ at $19:00$.
</p>

Comparing with [Stellarium](https://stellarium.org/):

<p align="center">
  <img width="400" src="https://github.com/CitruzSquared/essays/assets/23460281/10263da7-5aa5-4487-999a-faf9131aea3e"> 
  <img width="400" src="https://github.com/CitruzSquared/essays/assets/23460281/9b9931f1-5534-44ec-b861-bc93e76aa766"> <br/>
  Stellarium image on the left, Stellarium image overlaid with our prediction on the right.
</p>
