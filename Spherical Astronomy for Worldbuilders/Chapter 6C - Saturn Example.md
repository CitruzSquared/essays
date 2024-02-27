### Saturn in the Sky
We figured out how Venus looked in examples $4.1$ and $6.7$. Let's do something harder: Let's try to figure out how Saturn looked in the sky on $\text{January 1, } 2024$ at $19:00$ from London, UK ($\phi = +51\degree, l = 0\degree$).

#### 1. Data Collection
To figure out what Saturn looked like from the Earth, we must first know how Saturn looks in general:

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/31cbc860-fe82-4627-9ba9-2bc59c92890b" width="350"/> First, and foremost, Saturn can be well modeled as a giant sphere, $58$ $232 \text{ km}$ in radius. 

In addition to that though, the planet has some gorgeous rings. The rings are made up of many parts, but we can generally say that the brightest parts form a disk on the plane of Saturn's equator, spanning from $74$ $500\text{ km}$ to $136$ $780\text{ km}$ from the planet's center (rings C, B, and A).

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
1\:371\:517\:050\\
-624\:168\:063\\
-318\:418\:649
\end{bmatrix}
```
- Earth to Sun Vector ($\textbf{s}$):
```math
\textbf{s}=
\begin{bmatrix}
26\:847\:342\\
-132\:696\:193\\
-57\:526\:188
\end{bmatrix}
```
- Sun to Saturn Vector ($\textbf{v}$):\
This is given by $\textbf{p} - \textbf{s}$.
```math
\textbf{v}=
\begin{bmatrix}
1\:344\:669\:710\\
-491\:471\:870\\
-260\:892\:461
\end{bmatrix}
```
And their normalized forms (Direction vectors)
```math
\textbf{p}_d=
\begin{bmatrix}
0.89051378\\
-0.405266753\\
-0.20674639
\end{bmatrix}
\enspace\enspace
\textbf{s}_d=
\begin{bmatrix}
0.18251119\\
-0.90208337\\
-0.39106938
\end{bmatrix}
\enspace\enspace
\textbf{v}_d=
\begin{bmatrix}
0.92401427\\
-0.33772384\\
-0.17927700
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
0.08548148\\
0.07323415\\
0.99364464
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
&= 99.8\%
\end{align}
```
This makes sense as planets in the far reaches of the Solar System tend to always be at full phase.
#### The Rings

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/768cf34c-71bc-4248-8227-71632f098d61" width="350"/> In this diagram, the center of Saturn is $C$, and the rings span from $A$ to $B$. $\textbf{n}$ is the vector to the north pole, perpendicular to the plane of the rings (the equator) and the Earth is in the direction $-\textbf{p}$ (because the Earth to Saturn vector is $\textbf{p}$, the Saturn to Earth vector must be $-\textbf{p}$).

From the view of the Earth, the rings look like they span the distance $A'B'$, which is the projection of $AB$ perpendicular to $\textbf{p}_d$. Thus the radii of the disks appear to be:
```math
C'B' = CB\sin(QCA)
```
but since $QCA = 90\degree - NCQ$:
```math
C'B' = CB\cos(NCQ)
```
$\cos(NCQ)$ is given by the dot product of the two direction vectors $\textbf{n}$ and $-\textbf{p}_d$:
```math
\begin{bmatrix}
0.08548148\\
0.07323415\\
0.99364464
\end{bmatrix}\cdot
\begin{bmatrix}
-0.89051378\\
0.405266753\\
0.20674639
\end{bmatrix}
=0.158989
```
Thus:
```math
\begin{align}
\text{Ring Size}_O &= 136\:780\cdot0.158989 = 21\:747\text{ km}\\
\text{Ring Size}_I &= 74\:500\cdot0.158989 = 11\:844\text{ km}
\end{align}
```
Where $O$ and $I$ stand for the outer and inner edge of the rings respectively. Note that these are just the vertical sizes, and the horizontal size is the full $136$ $780\text{ km}$ and $74$ $500\text{ km}$; i.e. the outer edge of the rings looks like an ellipse with height radius $21$ $747\text{ km}$ and width radius $136$ $780\text{ km}$, and the inner edge looks like an ellipse with height radius $11$ $844\text{ km}$ and width radius $74$ $500\text{ km}$.

#### Apparent Diameters
Let's now calculate the apparent sizes of everything from Earth.\
By equation $4.2$ (remembering to use $\arctan()$ for the rings since they are disks):
```math
\begin{align}
\text{Saturn } &= 2\arcsin\left(\frac{58\:232}{1\:540\:141\:300}\right) = 16.00''\\
\text{Inner Ring Horiz. } &= 2\arctan\left(\frac{74\:500}{1\:540\:141\:300}\right) = 19.95''\\
\text{Inner Ring Vert. } &= 2\arctan\left(\frac{11\:844}{1\:540\:141\:300}\right) = 3.17''\\
\text{Outer Ring Horiz. } &= 2\arctan\left(\frac{136\:780}{1\:540\:141\:300}\right) = 36.64''\\
\text{Outer Ring Vert. } &= 2\arctan\left(\frac{21\:747}{1\:540\:141\:300}\right) = 5.82''
\end{align}
```
