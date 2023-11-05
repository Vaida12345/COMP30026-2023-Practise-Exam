# COMP30026 2023 Practise Exam Answer

Hey. Just want to organize the answers, for anyone needing this in the future.

*Please do not rely on the format. This is a community version, as there isn't a official one.*

# Question 1

## Part A
### Question 1
[![verified](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/verified.svg)](https://edstem.org/au/courses/12631/discussion/1670387)

> $\psi =\lnot (\lnot P \lor Q) \lor R$
> 
> $\psi = (P \land \lnot Q) \lor R$
> 
> Apparently, $\psi \models (\lnot Q\lor R)$

$\varphi=(Q \to R)$

### Question 2
![unchecked](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/unchecked.svg)

$P$

### Question 3
![unchecked](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/unchecked.svg)

> $\rho = \lnot P \lor \lnot Q \lor R$
>
> Apparently, $R \models (\lnot P \lor \lnot Q \lor R)$

$\varphi=R$

### Question 4
![unchecked](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/unchecked.svg)

$P$

## Part B
![unchecked](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/unchecked.svg)

> 1: $R \leftrightarrow S$
>
> 2: $\lnot(R\lor S)\to \lnot P$
>
> 3: $Q\to (R \oplus S)$
>
> 4: $(R\land S)\to Q$

```mathematica
In = LogicalExpand[Implies[Q, Xor[R, S]] && Implies[R && S, Q] && Equivalent[R, S] && Implies[! (R || S), ! P]]
Out = ! P && ! Q && ! R && ! S
```
Hence, by mathematica, and looking really hard, *The conditions that have been posed are unsatisfiable*.


# Question 2
[![verified](https://github.com/Vaida12345/COMP30026-2023-Practise-Exam/blob/main/Assets/verified.svg)](https://edstem.org/au/courses/12631/discussion/1679710)

## Part A

> You need to give an interpretations that makes it valid and another that makes it unsatisfiable, [read more](https://edstem.org/au/courses/12631/discussion/1687211).

Consider $\mathcal{I}(D)=\mathbb{R}$, $\mathcal{I}(P)(x,y)=(x=y)$, $F\land Q\equiv\top$.

Consider $\mathcal{I}(D)=\mathbb{R}$, $\mathcal{I}(P)(x,y)=(x<y)$, $F\land Q\equiv\bot$.

Hence, $F\land Q$ is satisfiable but not valid.

## Part B

> To show is not valid, only need to give a counter example.

Consider $\mathcal{I}(D)=\mathbb{R}$, $\mathcal{I}(P)(x,y)=(x<y)$, $F\lor Q\equiv\bot$.
