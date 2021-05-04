# Navier Stokes equations in differential form
Fluid motion is described by the Navier-Stokes equations which in differential form are described as:
$$
\def\dede#1#2{{\frac{\partial #1}{\partial #2}}}
\def\deded#1#2{{\frac{\partial}{\partial #2}\left(#1\right)}}
\begin{align}
  \dede{\rho}{t} &=
    - \dede{\rho u_j}{ x_j}
  \\
  \dede{\rho u_i}{t} &=
    - \deded{\rho u_i u_j + p \delta_{ij}}{x_j}
    + \dede{\sigma_{ij}}{x_j}
  \\
  \frac{\partial \rho E}{\partial t} &=
    - \deded{(\rho E + p) u_j}{x_j}
    + \deded{\lambda \dede{T}{x_j}}{x_j}
    + \dede{(\sigma_{ij} u_i)}{x_j}
\end{align}
$$
where:
$$
  \sigma_{ij} = \mu \left( \dede{u_i}{x_j} + \dede{u_j}{x_i} - \frac{2}{3}\dede{u_s}{x_s} \right)
$$
