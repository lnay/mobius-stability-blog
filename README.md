---
title: My Document
author: Someone
date: 7 May 2022
header-includes: |
    \newcommand\RR{\mathbb{R}}
    \newcommand\CC{\mathbb{C}}
    \newcommand\ZZ{\mathbb{Z}}
    \newcommand\PP{\mathbb{P}}
    \newcommand\centralcharge{\mathcal{Z}}
    \newcommand\gltworplustilde{\widetilde{\mathrm{GL}_2}(\RR)^{+}}
    \newcommand\gltworplus{\mathrm{GL}_2(\RR)^{+}}
    \newcommand\Heven{H_{\mathrm{even}}^{\mathrm{alg}}}
    \newcommand\ppas{\mathbb{T}}
    \newcommand\isotropcherntoztwo{\Gamma}
    \newcommand\isotropchern{\gamma}
...

# Mobius transforms on Bridgeland stability conditions

## Copy of proof (not self contained, to be changed)

This is a copy of the proof from my thesis for the underlying theorem in the above about the autoequivalences
of the derived category acting of stability conditions modulo $\gltworplustilde$,
via Mobius transforms.
It does not contain its context from the containing section in my thesis,
I'll likely revisit this to make it self-contained.

First, note that the action of autoequivalences of the triangulated category
on the space of stability conditions
commutes with the action of $\gltworplustilde$
So the action of cohomological Fourier-Mukai transforms
on stability conditions, does descend to an action on stability
conditions modulo $\gltworplustilde$.
Furthermore, Proposition gives us that
the stability conditions given by the parametrisation in Definition
can be chosen as representatives


Next, Proposition
gives that the stability conditions are determined by their
central charge up to even shifts, so modulo $\gltworplustilde$,
they are determined uniquely.
Therefore, we need only consider the action of $\Phi^H$ on central
charges $\centralcharge \colon \Heven(\ppas) \to \CC$
modulo $\gltworplustilde$ (which reduces to an action of
$\gltworplus$).
The central charges of the stability conditions
$\sigma_{\alpha, \beta}$ are given by
$\centralcharge_{\beta + i\alpha}$
when using the notation defined in the following.

\begin{align*}
    \frac{
        \left\{
            v \in \Heven(\ppas) \otimes_\ZZ \CC
            \colon \Delta(v) = 0
        \right\}
    }{\CC^{*}}
    &\to
    \frac{
        \hom_{\ZZ}(\Heven(\ppas), \CC)
    }{\gltworplus}
    \\
    \left[
        v
    \right]
    &\mapsto
    [
        \left< v, \_ \right>
    ]
\end{align*}

Next note that $\isotropcherntoztwo$
from Definition
descends to the bijection
\begin{align*}
    [\isotropcherntoztwo] \colon
    \frac{
        \left\{
            v \in \Heven(\ppas) \otimes_\ZZ \CC
            \colon \Delta(v) = 0
        \right\}
    }{\CC^{*}}
    &\to
    \CC\PP^2
    \\
    [\exp(z \ell)]
    &\mapsto
    \begin{pmatrix}
        1 \\ z
    \end{pmatrix}
    \\
    [(0, 0, 1)]
    &\mapsto
    \begin{pmatrix}
        0 \\ 1
    \end{pmatrix}
    .
\end{align*}

These can be composed to give
\begin{align*}
    f \colon
    \CC\PP^2
    &\to
    \frac{
        \hom_{\ZZ}(\Heven(\ppas), \CC)
    }{\gltworplus}
    \\
    \left[
        u
    \right]
    &\mapsto
    \left[
        \left<
            \exp( \isotropcherntoztwo^{-1}(u) \ell),
            \_
        \right>
    \right]
\end{align*}
so that the equivalence class
$f\left(
\left[
\begin{pmatrix}
    1 & \beta + i\alpha
\end{pmatrix}^T
\right]
\right)$
contains the central charge for $\sigma_{\alpha, \beta}$.
Finally, note that $\Phi^H$ descends to a projective linear map
$\left[\Phi^H\right]$ on $\CC\PP^2$
(which are naturally identified with Möbius transformations).

With this notation, we now have a clean way of describing the action
of $\Phi^H$ on the central charges of the stability conditions
(modulo $\gltworplus$), which are contained in the image of $f$.
This action shall be related to the action of
$\left[\Phi^H\right]$ on $\CC\PP^2$:

\begin{align*}
    \Phi^H \cdot f([u])
    &=
    \left[
    \left<
        u, (\Phi^H)^{-1}(\_)
    \right>
    \right]
    \\
    &=
    \left[
    \left<
        \Phi^H(u), \_
    \right>
    \right]
    \\
    &= f\left(\left[\Phi^H\right]([u])\right)
\end{align*}
Now consider the action
$\left[\Phi^H\right]$ on the preimage of the central charges
for $\sigma_{\alpha, \beta}$.
Take $z = \beta + i\alpha$:
\begin{align*}
    \left[\Phi^H\right]
    \left(
        \left[
            \begin{pmatrix}
                1 \\ z
            \end{pmatrix}
        \right]
    \right)
    &=
    \left[
        \begin{pmatrix}
            a + b z \\ c + d z
        \end{pmatrix}
    \right]
    \\ &
    =
    \left[
        \begin{pmatrix}
            1 \\ \dfrac{c + d z}{a + b z}
        \end{pmatrix}
    \right]
\end{align*}
This therefore prooves the action of $\Phi^H$ on the
equivalence classes of stability conditions in the
statement of the theorem.
