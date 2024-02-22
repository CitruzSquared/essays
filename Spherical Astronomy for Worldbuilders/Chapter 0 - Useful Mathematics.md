## Useful Mathematics

### Algebra
```math
\begin{align}
(a + b)(c + d) &= ac + ad + bc + bd \\
\frac{a}{b} = \frac{c}{d} &\implies ad = bc\\
x^0 &= 1 \\
x^{a/b} &= \sqrt[b]{x^a} \\
x^{-a} &= \frac{1}{x^a} \\
x^a\cdot x^b &= x^{a + b} \\
\left(x^a\right)^b & =x^{ab} \\
ax^2 + bx + c = 0 &\implies x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}\\
\end{align}
```

### Geometry
<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/669a9787-9f70-4c9e-89d5-e7f390f5bdbc" width="250"/>

```math
\begin{align}
\frac{\sin(A)}{a} &= \frac{\sin(B)}{b} = \frac{\sin(C)}{c}\\
c^2 &= a^2 + b^2 - 2ac\cos(C)\\
S &= \frac{1}{2}ab\sin(C)\\
A + B + C &= 180\degree \\
\end{align}
```

<br/>
<br/>
<br/>

<img align="left" src="https://github.com/CitruzSquared/essays/assets/23460281/e5e14475-0c35-41fb-affc-e0c08afefc50" width="250"/>

```math
\begin{align}
(\theta \text{ in} &\text{ radians})\\
C &= r\theta\\
S &= \frac{1}{2}r^2 \theta \\
\\
2\pi\text{ rad} &= 360\degree = 1\text{ rev} = 24^h\\
1\degree &= 60' = 3600''\\
1^h &= 60^m = 3600^s
\end{align}
```

### Trigonometry
```math
\begin{align}
\text{trig}(\alpha + n\cdot 360\degree) &= \text{trig}(\alpha)\enspace[n \in \mathbb{Z}]\\
\tan(\alpha) &= \frac{\sin(\alpha)}{\cos(\alpha)} \\
\sin(\alpha) &= -\sin(-\alpha) = -\sin(\alpha + 180\degree) = \sin(180\degree - \alpha) \\
\cos(\alpha) &= \cos(-\alpha) = -\cos(\alpha + 180\degree) = -\cos(180\degree - \alpha)\\
\tan(\alpha) &= -\tan(-\alpha) = \tan(\alpha + 180\degree) = -\tan(180\degree - \alpha)\\
\sin(\alpha) &= \cos(\alpha - 90\degree) \\
\csc(\alpha) &= \frac{1}{\sin(\alpha)}\\
\sec(\alpha) &= \frac{1}{\cos(\alpha)}\\
\cot(\alpha) &= \frac{1}{\tan(\alpha)}\\
\sin(\alpha\pm\beta) &= \sin(\alpha)\cos(\beta)\pm\cos(\alpha)\sin(\beta) \\
\cos(\alpha\pm\beta) &= \cos(\alpha)\cos(\beta)\mp\sin(\alpha)\sin(\beta) \\
\sin^2(\alpha) + \cos^2(\alpha) &= 1 \\
\tan^2(\alpha) + 1 &= \sec^2(\alpha) \\
\cot^2(\alpha) + 1 &= \csc^2(\alpha)
\end{align}
```
Two Argument Arctangent:
```math
\arctan(y, x) = \begin{cases}
\arctan(y/x) &\text{ if } x > 0 \\
\arctan(y/x) + 180\degree&\text{ if } x < 0 \text{ and } y \geq 0\\
\arctan(y/x) - 180\degree&\text{ if } x < 0 \text{ and } y < 0\\
90\degree&\text{ if } x = 0 \text{ and } y > 0 \\
-90\degree&\text{ if } x = 0 \text{ and } y < 0 \\
\text{undefined} &\text{ if } x = 0 \text{ and } y = 0
\end{cases}
```
### Calculus
```math
\begin{align}
\frac{d}{dx} f(x) &= f'(x) = \dot f\\
\frac{d}{dx} a &= 0 \\
\frac{d}{dx} x^a &= ax^{a-1} \\
\\
(x \text{ in} &\text{ radians})\\
\frac{d}{dx} \sin(x) &= \cos(x) \\
\frac{d}{dx} \cos(x) &= -\sin(x) \\
\frac{d}{dx} \tan(x) &= \sec^2(x) \\
\frac{d}{dx} \arcsin(x) &= \frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arccos(x) &= -\frac{1}{\sqrt{1-x^2}} \\
\frac{d}{dx} \arctan(x) &= \frac{1}{1 + x^2} \\
\\
\frac{d}{dx} [af(x) + bg(x)] &= af'(x) + bg'(x)\\
\frac{d}{dx} [f(x)g(x)] &= f'(x)g(x) + f(x)g'(x)\\
\frac{dy}{dx} &= \frac{dy}{du_1}\frac{du_1}{du_2}\frac{du_2}{du_3}\cdots\frac{du_{n-1}}{du_n}\frac{du_n}{dx} \\
\therefore \frac{d}{dx}[f(g(x))] &= f'(g(x))g'(x)\\
\\
\int_{a}^{b} f'(x) dx &= f(b) - f(a)
\end{align}
```
### Vectors
Most of these vector properties are nonessential to this guide.

$\textbf{e}_1$, $\textbf{e}_2$, and $\textbf{e}_3$ are unit basis vectors.\
$\theta$ is the angle between $\textbf{v}$ and $\textbf{u}$.
```math
\begin{align}
\textbf{v} &= \begin{bmatrix}
v_1 \\ v_2 \\ v_3
\end{bmatrix} = v_1\textbf{e}_1 + v_2\textbf{e}_2 + v_3\textbf{e}_3 \\
|\textbf{v}| &= \sqrt{v_1^2 + v_2^2 + v_3^3} \\
a\textbf{v} + b\textbf{u} &= \begin{bmatrix}
av_1 + bu_1 \\ av_1 + bu_2 \\ av_3 + bu_3
\end{bmatrix}\\
\textbf{v}\cdot\textbf{u} &= v_1u_1 + v_2u_2 + v_3u_3 \\
&= \textbf{u}\cdot\textbf{v}\\
&= |\textbf{v}||\textbf{u}|\cos(\theta)\\
\textbf{v}\cdot\textbf{v} &= |\textbf{v}|^2\\
\textbf{v}\times\textbf{u} &= \begin{bmatrix}
v_2u_3-v_3u_2 \\ v_3u_1-v_1u_3 \\ v_1u_2-v_2u_1
\end{bmatrix}\\
&= -\textbf{u}\times\textbf{v}\\
|\textbf{v}\times\textbf{u}| &= |\textbf{v}||\textbf{u}|\sin(\theta)\\
\textbf{v}\times\textbf{v} &= \textbf{0}\\
\textbf{v}\cdot(\textbf{v}\times\textbf{u}) &= 0 = \textbf{u}\cdot(\textbf{v}\times\textbf{u}) \\
\\
\textbf{v}\cdot(\textbf{u}\times\textbf{w}) &= \textbf{u}\cdot(\textbf{w}\times\textbf{v}) = \textbf{w}\cdot(\textbf{v}\times\textbf{u})\\
\textbf{v}\times(\textbf{u}\times\textbf{w}) &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{v}\cdot\textbf{u})\textbf{w}\\
(\textbf{v}\times\textbf{u})\times\textbf{w} &= (\textbf{v}\cdot\textbf{w})\textbf{u}-(\textbf{u}\cdot\textbf{w})\textbf{v}
\end{align}
```
### Matrices
```math
\begin{align}
c \begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
+
d \begin{bmatrix}
b_1 & b_2 & b_3 \\
b_4 & b_5 & b_6 \\
b_7 & b_8 & b_9
\end{bmatrix}
&=
\begin{bmatrix}
ca_1 + db_1 & ca_2 + db_2 & ca_3 + db_3 \\
ca_4 + db_4 & ca_5 + db_5 & ca_6 + db_6 \\
ca_7 + db_7 & ca_8 + db_8 & ca_9 + db_9
\end{bmatrix}\\
\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
\begin{bmatrix}
b_1 \\ b_2 \\ b_3
\end{bmatrix}
&=
\begin{bmatrix}
a_1b_1 + a_2b_2 + a_3b_3 \\
a_4b_1 + a_5b_2 + a_6b_3 \\
a_7b_1 + a_8b_2 + a_9b_3
\end{bmatrix}\\
\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}
\begin{bmatrix}
b_1 & b_2 & b_3 \\
b_4 & b_5 & b_6 \\
b_7 & b_8 & b_9
\end{bmatrix}
&=
\begin{bmatrix}
a_1b_1 + a_2b_4 + a_3b_7 & a_1b_2 + a_2b_5 + a_3b_8 & a_1b_3 + a_2b_6 + a_3b_9 \\
a_4b_1 + a_5b_4 + a_6b_7 & a_4b_2 + a_5b_5 + a_6b_8 & a_4b_3 + a_5b_6 + a_6b_9 \\
a_7b_1 + a_8b_4 + a_9b_7 & a_7b_2 + a_8b_5 + a_9b_8 & a_7b_3 + a_8b_6 + a_9b_9
\end{bmatrix}\\
\\
AB &\neq BA\\
\\
\begin{bmatrix}
a_1 & a_2 & a_3 \\
a_4 & a_5 & a_6 \\
a_7 & a_8 & a_9
\end{bmatrix}^T
&=
\begin{bmatrix}
a_1 & a_4 & a_7 \\
a_2 & a_5 & a_8 \\
a_3 & a_6 & a_9
\end{bmatrix}
\end{align}
```
Rotation Matrices:
```math
\textbf{v}_{\text{rotated}} = R\textbf{v}_{\text{original}}
```
```math
R_x = 
\begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(\theta) & -\sin(\theta) \\
0 & \sin(\theta) & \cos(\theta)
\end{bmatrix},
\enspace\enspace
R_y = 
\begin{bmatrix}
\cos(\theta) & 0 & \sin(\theta)\\
0 & 1 & 0\\
-\sin(\theta) & 0 & \cos(\theta)
\end{bmatrix},
\enspace\enspace
R_z = 
\begin{bmatrix}
\cos(\theta) & -\sin(\theta) & 0 \\
\sin(\theta) & \cos(\theta) & 0 \\
0 & 0 & 1
\end{bmatrix}
```