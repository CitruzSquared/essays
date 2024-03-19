(Continued from Part B...)
### Beginning / Ending Condition
We have found the locations on the edge of the shadow but not if the eclipse is about to begin or about to end in those places. If at time $t$ a point is on the edge of the shadow, then whether the point is inside or outside the shadow at the next instant time $t + dt$ will determine if the eclipse was beginning or ending at that place. This can be expressed in terms of equation $9.16$: the eclipse is beginning or ending depending on $\Delta$ is becoming greater or less than $L$ at time $t + dt$. We can express this as the derivative of the function $\Delta^2 - L^2$: *if the derivative is positive then the distance is increasing and the eclipse is ending. If the derivative is negative then the distance is decreasing and the eclipse is beginning.*

Note: this section is extremely mathematically dense. Skip to example $9.4$ if the solution is all you are interested in.

It is very useful now to define some vectors. Let the vector $\boldsymbol{\varrho}$ be defined as the position of the observer in the fundamental frame:
```math
\boldsymbol{\varrho} = 
\begin{bmatrix}
\xi \\ \eta \\ \zeta \tag{9.35}
\end{bmatrix}
```
And $\textbf{r}$ be defined as the position of the Moon's shadow at the level of the observer:
```math
\textbf{r} = 
\begin{bmatrix}
x\\ y \\ \zeta \tag{9.36}
\end{bmatrix}
```
Now the vector pointing from the shadow to the observer $\boldsymbol{\Delta}$ can be defined as:
```math
\boldsymbol{\Delta} = \textbf{r} - \boldsymbol{\varrho} = \begin{bmatrix}
x - \xi \\ y - \eta \\ 0
\end{bmatrix} \tag{9.37}
```
The magnitude of $\boldsymbol{\Delta}$ is $\Delta$ (equation $9.9$).

Now, $\Delta^2 - L^2$ becomes:
```math
\boldsymbol{\Delta}\cdot\boldsymbol{\Delta} - L^2
```
Taking the derivative (which we will denote by $P$) with respect to time, we get:
```math
P = 2\boldsymbol{\Delta}\cdot\boldsymbol{\Delta}' - 2LL'
```
Which, because $|\boldsymbol{\Delta}| = L$ at the instant $t$, we can reduce to:
```math
P = L(\boldsymbol{\hat{\Delta}}\cdot\boldsymbol{\Delta}' - L')
```
Where $\boldsymbol{\hat{\Delta}}$ is the unit vector in the direction of $\boldsymbol{\Delta}$. The $2$ was omitted since only the sign of the derivative is important.\
If we now set:
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\boldsymbol{\Delta}' - L' 
```
Then
```math
P = LP' \tag{9.38}
```
And so can see that *if* $P'$ *and* $L$ *have like signs, then* $P$ *is positive and the eclipse is ending. If* $P'$ *and* $L$ *have opposite signs, then* $P$ *is negative and the eclipse is beginning*. Let us now develop the quantity $P'$.

We can safely say that $i$ is constant and therefore:
```math
L' = l' - i\zeta'
```
Also, By equation $9.37$,
```math
\boldsymbol{\Delta}' = \textbf{r}' - \boldsymbol{\varrho}'
```
Therefore:
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\textbf{r}' - \boldsymbol{\hat{\Delta}}\cdot\boldsymbol{\varrho}' - (l'- i\zeta') \tag{9.39}
```
So we need to develop the quantities in the right hand side.

Let us first calculate $\boldsymbol{\varrho}'$, which involves $\xi'$, $\eta'$, and $\zeta'$. If the observer is at geocentric equatorial coordinates
```math
\begin{bmatrix}
\rho \cos(\phi')\cos(\Theta_L)\\\rho \cos(\phi')\sin(\Theta_L) \\\rho \sin(\phi')
\end{bmatrix}
```
Then they are rotating about the $z$-axis as $\Theta_L$ changes. Thus the rotational velocity vector in equatorial coordinates is:
```math
\begin{bmatrix}
0\\0 \\d\Theta/dt
\end{bmatrix}
```
Because $d\Theta_L/dt = d\Theta/dt + d/dt (l) = d\Theta/dt$.
But we want the velocity vector relative to the shadow axis. The shadow axis (in equatorial coordinates) is also rotating about the $x$ and $z$ axes:
```math
\begin{bmatrix}
-dd/dt\\0 \\da/dt
\end{bmatrix}
```
See equation $9.5$ for rationale of the signs.\
Now we can subtract the two vectors and obtain for the relative rotation vector (in equatorial coordinates):
```math
\boldsymbol{\omega}_E = \begin{bmatrix}
dd/dt\\0 \\d\Theta/dt - da/dt
\end{bmatrix} =
 \begin{bmatrix}
d'\\0 \\\mu'
\end{bmatrix}
```
To transform into fundamental coordinates, we only need to multiply by a rotation about the equatorial $x$ axis by $90\degree - d$ since the transformation about the $z$ axis by $a - 90\degree$ does not change anything about the rotation vector. Therefore:
```math
\boldsymbol{\omega} = \begin{bmatrix}
1 & 0 & 0 \\
0 & \cos(90\degree - d) & \sin(90\degree - d) \\
0 & -\sin(90\degree - d) & \cos(90\degree - d)
\end{bmatrix} \begin{bmatrix}
d'\\0 \\\mu'
\end{bmatrix}=
\begin{bmatrix}
d'\\ \cos(d)\mu'\\ \sin(d)\mu'
\end{bmatrix}
```
The cartesian velocity vector in the fundamental frame is then the cross product of the fundamental rotation vector and the fundamental position vector:
```math
\boldsymbol{\varrho}' = \begin{bmatrix}
\xi'\\ \eta' \\ \zeta'
\end{bmatrix} =
\boldsymbol{\omega} \times \boldsymbol{\varrho} =
\begin{bmatrix}
d'\\ \cos(d)\mu'\\ \sin(d)\mu'
\end{bmatrix}
\times
\begin{bmatrix}
\xi\\ \eta \\ \zeta
\end{bmatrix} =
\begin{bmatrix}
\mu'(-\eta\sin(d) + \zeta\cos(d))\\
\mu'\xi\sin(d) - d'\zeta\\
-\mu'\xi\cos(d) + d'\eta
\end{bmatrix} \tag{9.40}
```
We can substitute $\boldsymbol{\varrho}' = \boldsymbol{\omega} \times \boldsymbol{\varrho}$ into equation $9.39$: 
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\textbf{r}' - \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times \boldsymbol{\varrho}) - (l'- i\zeta')
```
Using equation $9.37$ we can write:
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\textbf{r}' - \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times (\textbf{r} - \boldsymbol{\Delta})) - (l'- i\zeta') \tag{9.41}
```
The second term $\boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times (\textbf{r} - \boldsymbol{\Delta}))$ can be expanded as:
```math
\begin{align}
\boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times (\textbf{r} - \boldsymbol{\Delta})) &= \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times \textbf{r} - \boldsymbol{\omega}\times\boldsymbol{\Delta})\\
&= \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times \textbf{r}) - \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega}\times\boldsymbol{\Delta})
\end{align}
```
The second term, the scalar triple product $\boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega}\times\boldsymbol{\Delta})$, is:
```math
\boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega}\times\boldsymbol{\Delta}) = \boldsymbol{\omega}\cdot(\boldsymbol{\Delta}\times\boldsymbol{\hat{\Delta}}) = \boldsymbol{\omega}\cdot\textbf{0} = 0
```
Thus, 
```math
\boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times (\textbf{r} - \boldsymbol{\Delta})) = \boldsymbol{\hat{\Delta}}\cdot(\boldsymbol{\omega} \times \textbf{r}) \tag{9.42}
```
$\boldsymbol{\omega} \times \textbf{r}$ is:
```math
 \boldsymbol{\omega} \times \textbf{r} =
\begin{bmatrix}
d'\\ \cos(d)\mu'\\ \sin(d)\mu'
\end{bmatrix}
\times
\begin{bmatrix}
x \\ y \\ \zeta
\end{bmatrix} =
\begin{bmatrix}
\mu'(-y\sin(d) + \zeta\cos(d))\\
\mu'x\sin(d) - d'\zeta\\
-\mu'x\cos(d) + d'y
\end{bmatrix}  = \mu' \begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix}
- \zeta \begin{bmatrix}
-\mu'\cos(d)\\ d'\\ -d'y/\zeta
\end{bmatrix}
\tag{9.43}
```
For the third term of equation $9.41$, notice that in equation $9.40$ we can write $\zeta'$ as a vector dot product:
```math
\zeta' = -\mu'\xi\cos(d) + d'\eta = \begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot\begin{bmatrix}
\xi \\ \eta \\ \zeta
\end{bmatrix} = \begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \boldsymbol{\varrho} = \begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot (\textbf{r} - \boldsymbol{\Delta})\tag{9.44}
```
To finish, we have from equation $9.10$ and $9.16$:
```math
\boldsymbol{\Delta} = (l - i\zeta)\boldsymbol{\hat{\Delta}} = (l - i\zeta) \begin{bmatrix}
\sin(Q) \\ \cos(Q) \\ 0
\end{bmatrix}\tag{9.45}
```
Substituting equations equation $9.45$ into equation $9.44$ and $9.42$, $9.43$, and $9.44$ into equation $9.41$, we have:
```math
\begin{align}
P' &= \boldsymbol{\hat{\Delta}}\cdot \left(\textbf{r}' - \mu' \begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix}
+ \zeta \begin{bmatrix}
-\mu'\cos(d)\\ d'\\ -d'y/\zeta
\end{bmatrix} \right) - l' + i \begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot (\textbf{r} - (l - i\zeta)\boldsymbol{\hat{\Delta}})\\
&= \boldsymbol{\hat{\Delta}}\cdot \textbf{r}' - \mu' \boldsymbol{\hat{\Delta}}\cdot\begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix} + \zeta \boldsymbol{\hat{\Delta}}\cdot\begin{bmatrix}
-\mu'\cos(d)\\ d'\\ -d'y/\zeta
\end{bmatrix} - l' + i\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \textbf{r} - li\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \boldsymbol{\hat{\Delta}} + i^2\zeta\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \boldsymbol{\hat{\Delta}}
\end{align}
```
If we collect the terms as $\boldsymbol{\hat{\Delta}}\cdot$ and $\zeta\boldsymbol{\hat{\Delta}}\cdot$, we get:
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\left(\textbf{r}' - \mu'\begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix} - li\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} \right) + \zeta \boldsymbol{\hat{\Delta}}\cdot\left(\begin{bmatrix}
-\mu'\cos(d)\\ d'\\ -d'y/\zeta
\end{bmatrix} + i^2 \begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\right) - l' + i\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \textbf{r} \tag{9.46}
```
Because the third element of $\boldsymbol{\hat{\Delta}}$ is $0$ (see equations $9.37$ and $9.45$),
```math
\boldsymbol{\hat{\Delta}}\cdot\begin{bmatrix}
-\mu'\cos(d)\\ d'\\ -d'y/\zeta
\end{bmatrix} = \boldsymbol{\hat{\Delta}}\cdot\begin{bmatrix}
-\mu'\cos(d)\\ d'\\ 0
\end{bmatrix}
```
And therefore we can write equation $9.46$ as:
```math
P' = \boldsymbol{\hat{\Delta}}\cdot\left(\textbf{r}' - \mu'\begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix} - li\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} \right) + \zeta (i^2 + 1) \boldsymbol{\hat{\Delta}}\cdot\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} - l' + i\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \textbf{r}
```
Which, when all the vectors are substituted in, becomes:
```math
P' = \begin{bmatrix}
\sin(Q) \\ \cos(Q) \\ 0
\end{bmatrix}\cdot\left(\begin{bmatrix}
x '\\ y' \\ \zeta'
\end{bmatrix} - \mu'\begin{bmatrix}
-y\sin(d)\\ x\sin(d)\\ -x\cos(d)
\end{bmatrix} - li\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} \right) + \zeta (i^2 + 1) \begin{bmatrix}
\sin(Q) \\ \cos(Q) \\ 0
\end{bmatrix}\cdot\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} - l' + i\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix}\cdot \begin{bmatrix}
x \\ y \\ \zeta
\end{bmatrix}\tag{9.47}
```
Even though $P'$ now involves all known variables, for the sake of brevity it is conventional to define three new variables $a'$, $b'$, and $c'$ such that $P'$ can be written as:
```math
P' = \begin{bmatrix}
\sin(Q) \\ \cos(Q) \\ 0
\end{bmatrix}\cdot\begin{bmatrix}
c' \\ -b' \\ 0
\end{bmatrix} + \zeta (i^2 + 1) \begin{bmatrix}
\sin(Q) \\ \cos(Q) \\ 0
\end{bmatrix}\cdot\begin{bmatrix}
-\mu'\cos(d) \\ d' \\ 0
\end{bmatrix} + a' \tag{9.48}
```
Matching equation $9.48$ to equation $9.47$, we get for $a'$, $b'$, and $c'$:
```math
\begin{align}
a' &= -l' + \mu' i x\cos(d) + yid'\\
b' &= -y' + \mu' x \sin(d) + lid' \tag{9.49}\\
c' &= x' + \mu'y\sin(d) + li\mu'\cos(d)
\end{align}
```
These variables do not depend on $Q$ and therefore can be calculated along with the Besselian elements.
Now, expanding out equation $9.48$ we get:
```math
P' = c'\sin(Q) - b'\cos(Q) - \zeta (i^2 + 1)\mu'\cos(d)\sin(Q) + \zeta (i^2 + 1)d'\cos(Q) + a'
```
Collecting terms as $\sin(Q)$ and $\cos(Q)$, we obtain:
```math
P' = a' + \sin(Q)(c' - (i^2 + 1)\zeta \mu'\cos(d)) + \cos(Q)(-b' + (i^2 + 1)\zeta d') \tag{9.50}
```
Equation $9.50$ is known as the *second fundamental equation of eclipse theory*. Note that the approximations $id' = 0$ and $i^2 + 1 = 1$ may be made here without much loss of precision (in most reasonable cases), which gives:
```math
P' = a' + \sin(Q)(c' - \zeta_1 \mu'\cos(d)) + \cos(Q)(-b' + \zeta_1 d') \tag{9.50*}
```
With
```math
\begin{align}
a' &= -l' + \mu' i x\cos(d) \\
b' &= -y' + \mu' x \sin(d) \tag{9.49*}\\
c' &= x' + \mu'y\sin(d) + li\mu'\cos(d)
\end{align}
```
Also, $\zeta$ can also be substituted for $\zeta_1$ in either equation $9.50$ or $9.50*$ if wanted.

Notice that if $P' = 0$, then by equation $9.38$, $P = 0$ and therefore the eclipse is *beginning and ending at the same time*. This means that the observer is right at the point where the Moon just barely grazes the Sun, and therefore is on the limit of visibility of eclipse. This will be important later.

#### Example 9.4
<div align="center">
<table>
<tbody>
<td align="center">
<img width="2000" height="0"><br>
Determine whether the eclipse was beginning or ending at the point for $Q = 90\degree$ determined in the last example.
<img width="2000" height="0">
</td>
</tbody>
</table>
</div>

The relevant Besselian elements are:
```math
\begin{align}
d &= 7\degree\:27'\:34.93''\\
x &= -0.30856088 \:R_E\\
y &= 0.22479055 \:R_E\\
i_1 &= 0.0046683\\
l_1 &= 0.53573027 \:R_E\\
d' &= 0.00025898 \text{ rad}/h\\
x' &= 0.51147366 \: R_E/h\\
y' &= 0.27129112 \:R_E/h\\
\mu' &= 0.26187054 \text{ rad}/h\\
l_1' &= 0.00006156 \: R_E/h
\end{align}
```
Also, $\zeta$ for $Q = 90\degree$ was:
```math
\zeta = 0.48984331
```
We first find $a'$, $b'$, and $c'$ by equation $9.49$:
```math
\begin{align}
a' &= -0.00006156 + 0.26187054 \cdot0.0046683 \cdot(-0.30856088)\cos(7\degree\:27'\:34.93'') + 0.22479055\cdot0.0046683\cdot0.00025898\\
&= -0.000435308\\
b' &= -0.27129112 + 0.26187054 \cdot(-0.30856088) \sin(7\degree\:27'\:34.93'') + 0.53573027\cdot0.0046683\cdot0.00025898\\
&= -0.28178103\\
c' &= 0.51147366 + 0.26187054\cdot0.22479055\sin(7\degree\:27'\:34.93'') + 0.53573027\cdot 0.0046683\cdot0.26187054\cos(7\degree\:27'\:34.93'')\\
&= 0.51976555
\end{align}
```
Then we find $P'$ by equation $9.50$:
```math
\begin{align}
P' &= -0.000435308 + \sin(90\degree)(0.51976555 - (0.0046683^2 + 1)\cdot0.48984331\cdot 0.26187054\cos(7\degree\:27'\:34.93''))\\
& + \cos(90\degree)(-(-0.28178103) + (0.0046683^2 + 1)\cdot0.48984331\cdot 0.00025898)\\
&= 0.39213761 > 0
\end{align}
```
Since $P' > 0$ and $L > 0$ (penumbra), $P > 0$ by equation $9.38$ and therefore the eclipse was ending.\
$\blacksquare$

### Contacts
(Continued in Part D...)
