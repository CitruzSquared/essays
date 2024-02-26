### Saturn in the Sky
Let's try to figure out how Saturn looked in the sky on $\text{January 1, } 2024$ at $19:00$ from London, UK ($\phi = +51\degree, l = 0\degree$).

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

#### 2. Apparent Size
Let's first calculate how big Saturn looks.\
Saturn's apparent size ($AS$) by equation $4.2$:
```math
\text{AS}_P = 2\arcsin\left(\frac{58\:232}{1\:540\:141\:300}\right) = 15.60''
```
The rings:
```math
\begin{align}
\text{AS}_I &= 2\arcsin\left(\frac{74\:500}{1\:540\:141\:300}\right) = 19.95''\\
\text{AS}_O &= 2\arcsin\left(\frac{136\:780}{1\:540\:141\:300}\right) = 36.64''
\end{align}
```
Where $I$ and $O$ stand for the inner edge and the outer edge of the rings respectively.

#### 3. Phase
Let's now calculate how much of Saturn is visible.\
By equation $4.3$, the Sun-Earth-Saturn angle ($SEP$) is:
```math
\begin{align}
\Delta \alpha &= 22^h\:22^m\:07.21^s - 18^h\:45^m\:45.07^s = 3^h\:36^m\:22.14^s\\
\therefore SEP &= \arccos(\sin(-11\degree\:55'\:54.3'')\sin(-23\degree\:01'\:15.8'')+\cos(-11\degree\:55'\:54.3'')\cos(-23\degree\:01'\:15.8'')\cos(3^h\:36^m\:22.14^s))\\
&= 52\degree\:29'\:6.99''
\end{align}
```
The Sun-Saturn distance ($r$) is given then by equation $4.4$:
```math
\begin{align}
r &= \sqrt{(147\:099\:700)^2 + (1\:540\:141\:300)^2 - 2\cdot147\:099\:700\cdot1\:540\:141\:300\cdot\cos(52\degree\:29'\:6.99'')}\\
&= 1\:455\:247\:779\text{ km}
\end{align}
```
And then the phase angle ($SPE$) is given by equation $4.5$:
```math
\begin{align}
SPE &= \arccos\left(\frac{1\:540\:141\:300^2 + 1\:455\:247\:779^2 - 147\:099\:700^2}{2\cdot1\:540\:141\:300\cdot1\:455\:247\:779}\right)\\
&= 4\degree\:35'\:55.69''
\end{align}
```
And then finally the phase is given by equation $4.6$:
```math
\begin{align}
\text{Phase}\% &= \frac{1 + \cos(4\degree\:35'\:55.69'')}{2} \cdot 100\%\\
&= 99.84\%
\end{align}
```
Which makes sense as outer planets tend to always be near full phase.

#### 4. Elongation
We can see that the right ascension of Saturn is greater than the right ascension of the Sun, and therefore the ecliptic longitude would probably also be greater. Therefore the elongation would probably be positive and thus Saturn would be an evening star with its western face illuminated. We do not need to calculate the specific elongation.

#### 5. Horizontal Coordinates
