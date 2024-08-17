> RE: Sats Räkneregler för nabla
> $\nabla(fg) = \nabla(f)g + f\nabla(g)$
> $\nabla \cdot (f {\bf{F}}) = \nabla f \cdot {\bf{F}} + f \nabla \cdot {\bf{F}}$
> $\nabla \times (f {\bf{F}}) = (\nabla f) \times {\bf{F}} + f (\nabla \times {\bf{F}})$
> $\nabla \cdot (\nabla \times {\bf{F}}) = 0$
> $\nabla \times (\nabla f) = \bf{0}$


Från 4:
> RE: Konservativt fält medför opeoende av vägen
> Antal att vektorfältet $\bf{F}$ är konservativt med potential $\phi$ i en öppen och sammanhängande mänd $D$.
> Låt $C: r = r(t), t \in [a,b]$ vara en kurva i D. Då håller:
>
> $\int_C\bf{F} \cdot dr = \phi(r(b)) - \phi(r(a))$
>
> Detta innebär att integralen $\int_C\bf{F} \cdot dr$ är oberoende av vägen i $D$

> RE:
> Man kan säga att potentialen $\phi$ (om den finns) är ett slags "primitiv funktion" till $\bf{F}$. I fysik och mekanik brukar man skriva definitionen med ett minustecken: $\bf{F} = \nabla\phi$, så att $\bf{F}$ pekar dit där potentialen minskar mest.

Med detta i åtanke fattar jag frågan som:
**Givet att vi har ett konservativt fält, bevisa att det existerar en skalär potential**

givet:
$\int_C\bf{F} \cdot dr = \phi(r(b)) - \phi(r(a))$
där $C: r = r(t), t \in [a,b]$
bevisa:
$\bf{F} = \nabla\phi \quad$ i $D$

https://math.stackexchange.com/questions/4710934/why-does-vec-nabla-times-vec-f-0-mean-that-exists-phi-nabla-phi-ve
https://math.stackexchange.com/questions/638099/why-curl-free-field-implies-existence-of-potential-function



### **Bonus) Insikt i $\hat{\bf N} \cdot {\bf F}dS$**

$\hat{\bf N}$ är en vektor som är **utåtriktad** från volymens yta där riktningen är ortagonal med ytan.

![alt text](images/gausscube1.png)

Dela upp $F$ till det som är parallellt/ortagonalt med $\hat{\bf N}$
![alt text](images/gausscube2.png)
$\large \hat{\bf N} \cdot {\bf F}dS = \hat{\bf N} \cdot ({\bf F}_\parallel + {\bf F}_\perp) dS$
$= (\hat{\bf N} \cdot {\bf F}_\parallel + \hat{\bf N} \cdot {\bf F}_\perp) dS$

Skalärprodukten med en ortagonal vektor är alltid noll
$= \hat{\bf N} \cdot {\bf F}_\parallel dS$

$dS$ ytan är ortagonal till $\hat{\bf N}$ och ${\bf F}_\parallel$

DIVERGENS THEOREM:
```https://www.youtube.com/watch?v=DrRsXhln4S```






### EXXA


> Bonus: Verifiera att matrismultiplikationen blev rätt
> Subsitutation $F_K^{-1} = Q$
>> $\left(
   (\nabla Q)^\top
   \cdot
   \nabla_{\hat{x}}\hat{\varphi}
   \left(
      Q(x)
   \right)
\right)_i$
>
>$\nabla Q = \Large\def\arraystretch{1.5}\begin{bmatrix}
   \frac{\partial Q_1}{\partial x_1} & \frac{\partial Q_1}{\partial x_2} & \cdots & \frac{\partial Q_1}{\partial x_n}
   \\
   \frac{\partial Q_2}{\partial x_1} & \frac{\partial Q_2}{\partial x_2} & \cdots & \frac{\partial Q_2}{\partial x_n}
   \\
   \vdots & \vdots & \ddots & \vdots
   \\
   \frac{\partial Q_n}{\partial x_1} & \frac{\partial Q_n}{\partial x_2} & \cdots & \frac{\partial Q_n}{\partial x_n}
\end{bmatrix}$
>
>$\nabla_{\hat{x}}\hat{\varphi} = \Large\def\arraystretch{1.5}\begin{bmatrix}
   \frac{\partial \varphi_1}{\partial {\hat{x}}_1} & \frac{\partial \varphi_1}{\partial {\hat{x}}_2} & \cdots & \frac{\partial \varphi_1}{\partial {\hat{x}}_n}
   \\
   \frac{\partial \varphi_2}{\partial {\hat{x}}_1} & \frac{\partial \varphi_2}{\partial {\hat{x}}_2} & \cdots & \frac{\partial \varphi_2}{\partial {\hat{x}}_n}
   \\
   \vdots & \vdots & \ddots & \vdots
   \\
   \frac{\partial \varphi_n}{\partial {\hat{x}}_1} & \frac{\partial \varphi_n}{\partial {\hat{x}}_2} & \cdots & \frac{\partial \varphi_n}{\partial {\hat{x}}_n}
\end{bmatrix}$
>
>$(\nabla Q)^\top = \Large\def\arraystretch{1.5}\begin{bmatrix}
   \frac{\partial Q_1}{\partial x_1} & \frac{\partial Q_2}{\partial x_1} & \cdots & \frac{\partial Q_n}{\partial x_1}
   \\
   \frac{\partial Q_1}{\partial x_2} & \frac{\partial Q_2}{\partial x_2} & \cdots & \frac{\partial Q_n}{\partial x_2}
   \\
   \vdots & \vdots & \ddots & \vdots
   \\
   \frac{\partial Q_1}{\partial x_n} & \frac{\partial Q_2}{\partial x_n} & \cdots & \frac{\partial Q_n}{\partial x_n}
\end{bmatrix}$
>
>ex: rad $i = 1$ blir:

$\begin{bmatrix}
   \displaystyle\sum_{i=1}^n \frac{\partial \varphi_i}{\partial \hat{x}_1} \cdot \frac{\partial Q_i}{\partial x_1} &
   \displaystyle\sum_{i=1}^n \frac{\partial \varphi_i}{\partial \hat{x}_2} \cdot \frac{\partial Q_i}{\partial x_1} &
   \cdots &
   \displaystyle\sum_{i=1}^n \frac{\partial \varphi_i}{\partial \hat{x}_n} \cdot \frac{\partial Q_i}{\partial x_1}
\end{bmatrix}$





# 8 Basfunktioneras derivator
Sats ang. basfunktionerna fanns inte med i 2019 boken

> RE: 1D
> En kontinuerlig styckvis linjär funktion $U(x)$ är entydligt bestämd  av sida nodvärden $U_i = U(x_i)$. För att beskriva U(x) inför vi *basfunktionerna* $\phi_i(x)$, en för varje nod $x_i$. Funktionera $\phi_i(x)$ bestäms av att det är kontinuerliga, styckvis linjära, samt att
> $\phi_i(x_j) = \begin{cases}
   1 &\text{om } i = j \\
   0 &\text{om } i \ne j
\end{cases}$
> Funktionen $U(x)$ kan nu bkrivas som en linjär kombination av basfunktionerna:
> $U(x) = \displaystyle\sum_{i=1}^N U_i\phi_i(x)$, med koeffcienterna $U_i = U(x_i)$
>
>> Obs att
>> $U(x_j) = \displaystyle\sum_{i=1}^N U_i\phi_i(x_j) = U_j$
>> efterssom $\phi_i(x_j) = \begin{cases}
   1 &\text{om } i = j \\
   0 &\text{om } i \ne j
\end{cases}$ innebär det att endast en term (där $i=j$) blir kvar i summan
>
> Vi har nu en formel som uttrycker $U(x)$ med hjälp av nodväderna. Vi ska nu bestämma de okända nodvärderna $U_i$ så att $U(x)$ blir en approximatic lösning till randvärdesproblemet (3.5). Vi andäner den svaga formulering (3.14).
>
>> RE: 3.5 (Definition 3.1 randvärdesproblem)
>> Finn $u$ sådam att:
>> $-D(aDu) = f\quad$ för $x \in I = (0,L)$
>> $aD_Nu+k(u-u_A) = g\quad$ för $x = 0,L$
>
>> RE: 3.14 (Definition 3.2 Sag formulering)
>> Finn en funktion $u$ sådan att ekvationen
>> $\int_0^L aDuDvdx + k_0u(0)v(0) + k_Lu(L)v(L)$
>> $= \int_0^L fvdx + (k_0u_0+g_0)v(0) + (k_Lu_L + g_L)v(L)$
>
> För att det inte ska bli så mycket att skriva genomför vi detta i fallet då $k_0 = k_l = 0, g_0 = g_l = 0$:
> $\int_0^L aDuDvdx = \int_0^L fvdx\quad$ (för alla $v$)
> Istället för $u(x)$ sätter vi in ansatsen $U(x) = \sum_{i=1}^N U_i\phi_i(x)$ och väljer testfunktionerna $v = \phi_j$
> Vi får
> $\displaystyle\sum_{i=1}^N U_i \int_0^L aD\phi_iD\phi_kdx = \int_0^L f\phi_jdx$
>
> Med betäckningarna
> $a_{ij} = a_{ji} = \int_0^L aD\phi_iD\phi_kdx,\quad b_j=\int_0^L f\phi_jdx$
> blir detta
> $\displaystyle\sum_{i=1}^N a_{ji} U_i = b_j,\quad j=1,\cdots,N$
> dvs på matrisform:
> $AU = b$
>
> Detta är ett linjärt ekvationssystem av N ekvationer för N obekanta. Matrisen
> $A = \left\{ a_{ij} \right\}^N_{i,j=1} = \left\{ \int_0^L aD\phi_iD\phi_kdx \right\}^N_{i,j=1}$
> Kallas *styvhetsmatris* (*stiffnes matrix*). Jämför med stångens ekvations där a = EA är materialsets styvhet. Styvhetsmatrisen är symmetrisk, ($a_{ji} = a_{ij}$), och *tridiagonal*
> $$A = \def\arraystretch{1.5}\begin{bmatrix}
   \ast   & \ast   & 0      & \cdots & 0 \\
   \ast   & \ast   & \ast   & \ddots & \vdots \\
   0      & \ast   & \ast   & \ast   & 0 \\
   \vdots & \ddots & \ast   & \ast   & * \\
   0      & \cdots & 0      & \ast   & *
\end{bmatrix}$$
>
>> RE: motsvarande för 2d
>> $\displaystyle\sum_{i=1}^N U_i
\underbrace{\iint_D a \nabla\phi_i \cdot \nabla\phi_j dA}_{\large a_{ji}}
= \underbrace{\iint_D f\phi_jdA}_{\large b_{j}}
,\quad j=1,\cdots,N$
>> Blir igen:
>> $AU = b$

> RE: basfunktionerna
> $\left\{ \phi_i \right\}^N_{i=1}$

**Sats att bevisa?**
> Basfunktionernas derivator...?

**Bevis**
Då basfunktionerna är styckvis linjära är deras derivata styckvisa konstanter?
Fattar inte frågan utan att veta vad satsen är.