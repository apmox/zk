# Problema base numerico ODE
La relazione che governa il sistema è data da:

$$
\def\dd#1#2{{\frac{d #1}{d #2}}}
\dd{\varphi}{t} = f(\varphi, t)
$$

## Prima esercitazione
Il problema è dato da:
$$
\dd{\varphi}{t} = \lambda \varphi, \quad \lambda = -4.5,\quad \varphi(0) = 1000
$$

La cui soluzione analitica è:
$$
\varphi = \varphi (0) e^{\lambda t} = 1000 e^{-4.5t}
$$

Il metodo di Eulero esplicito porge la soluzione come:
$$
\begin{align}
\varphi_{n+1} &= \varphi_n + f(\varphi_n,t_n)\Delta t\\
 &= \varphi_n + \lambda\varphi_n\Delta t \\
\varphi_{n+1} &= (1 + \lambda\Delta t)\varphi_n
\end{align}
$$

Il metodo di Heun esplicito porge:
$$
\begin{align}
\varphi_{n+1} &= \varphi_n
  + \frac{1}{2}\Delta t f(\varphi_n,t_n)
  + \frac{1}{2}\Delta t f
    \left(\varphi_n + f(\varphi_n,t_n)\Delta t \right)\\
 &= \varphi_n
  + \frac{1}{2}\Delta t \lambda\varphi_n
  + \frac{1}{2}\Delta t f
    \left(\varphi_n + \lambda\varphi_n\Delta t \right)\\
 &= \varphi_n
  + \frac{1}{2}\Delta t \lambda\varphi_n
  + \frac{1}{2}\Delta t \lambda
    \left(\varphi_n + \lambda\varphi_n\Delta t \right)\\
 &= \varphi_n
      + \frac{1}{2}\Delta t \lambda\varphi_n
      + \frac{1}{2}\Delta t \lambda \varphi_n
      + \frac{1}{2}\Delta t^2 \lambda^2 \varphi_n\\
\varphi_{n+1} &=
  \left(1+\Delta t \lambda
  + \frac{1}{2}\Delta t^2 \lambda^2 \right)
  \varphi_n \\
\end{align}
$$

Il metodo di Crank-Nicolson porge:
$$
\begin{align}
\varphi_{n+1} &= \varphi_n
  + \frac{1}{2}
  \left(
    f(\varphi_{n+1}, t_{n+1})+ f(\varphi_n,t_n)
  \right)
  \Delta t \\
 \varphi_{n+1} &= \varphi_n
    + \frac{1}{2}
    \left(
      \lambda\varphi_{n+1}+ \lambda \varphi_n
    \right)
    \Delta t \\
\varphi_{n+1}\left(1-\frac{\lambda}{2}\Delta t\right) &= \left(1 + \frac{\lambda}{2}\Delta t\right)\varphi_n \\
\varphi_{n+1} &= \left(\frac{1+\frac{\lambda}{2}\Delta t}{1-\frac{\lambda}{2}\Delta t}\right)\varphi_n
\end{align}
$$
