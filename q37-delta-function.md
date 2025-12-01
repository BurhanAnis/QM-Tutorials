
# Delta-Function Potential: Full Solution to Question 37

This document collects all the steps and explanations for Question 37 about the one-dimensional delta-function potential.

We consider the time-independent Schrödinger equation:

$$
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V(x)\psi(x) = E\psi(x)
$$

with

$$
V(x) = \alpha\,\delta(x)
$$

---

## (a) Bound-state solutions for $\alpha < 0$, $E < 0$

For $x \neq 0$, the potential is zero because $\delta(x) = 0$ for all $x \neq 0$:

$$
V(x) = \alpha\delta(x) = 0 \quad \text{for } x\neq 0
$$

Thus the Schrödinger equation reduces to:

$$
-\frac{\hbar^2}{2m}\psi''(x) = E\psi(x)
$$

Since $E<0$, write $E=-|E|$:

$$
\psi''(x) = \frac{2m|E|}{\hbar^2}\psi(x)
$$

Define:

$$
\kappa = \sqrt{\frac{2m|E|}{\hbar^2}} > 0
$$

Thus:

$$
\psi''(x)=\kappa^2 \psi(x)
$$

General solutions:

$$
\psi(x)=A e^{\kappa x}+B e^{-\kappa x},\quad x<0
$$

$$
\psi(x)=C e^{\kappa x}+D e^{-\kappa x},\quad x>0
$$

---

## (b) Derivative discontinuity and $\eta$

Start with:

$$
-\frac{\hbar^2}{2m}\psi''(x)+\alpha\delta(x)\psi(x)=E\psi(x)
$$

Integrate from $-\varepsilon$ to $+\varepsilon$ around $x=0$:

The first term gives:

$$
-\frac{\hbar^2}{2m}[\psi'(0^+)-\psi'(0^-)]
$$

The delta-function term gives:

$$
\alpha\psi(0)
$$

The right-hand side vanishes as $\varepsilon\to 0$.

Thus:

$$
-\frac{\hbar^2}{2m}(\psi'(0^+)-\psi'(0^-))+\alpha\psi(0)=0
$$

Rearranging:

$$
\psi'(0^+)-\psi'(0^-)=\frac{2m\alpha}{\hbar^2}\psi(0)
$$

So:

$$
\boxed{\eta=\frac{2m\alpha}{\hbar^2}}
$$

---

## (c) Bound-state wavefunction and energy

Normalizability requires:

$$
\psi(x)=Ce^{\kappa x},\quad x<0
$$

$$
\psi(x)=Ce^{-\kappa x},\quad x>0
$$

Thus:

$$
\psi(x)=Ce^{-\kappa |x|}
$$

Derivatives:

$$
\psi'(0^+)=-\kappa C,\quad \psi'(0^-)=\kappa C
$$

Jump condition:

$$
-2\kappa C=\eta C
$$

Thus:

$$
\kappa = -\frac{\eta}{2} = -\frac{1}{2}\cdot\frac{2m\alpha}{\hbar^2}
   = -\frac{m\alpha}{\hbar^2}
$$

For $\alpha<0$, this yields $\kappa=\frac{m|\alpha|}{\hbar^2}>0$.

Energy:

$$
E=-\frac{\hbar^2\kappa^2}{2m}
$$

Thus:

$$
E=-\frac{m\alpha^2}{2\hbar^2}
$$

Normalization:

$$
\int_{-\infty}^{\infty}|Ce^{-\kappa|x|}|^2 dx = 1
$$

This gives:

$$
C=\sqrt{\kappa}
$$

Final normalized state:

$$
\boxed{
\psi(x)=\sqrt{\kappa}\,e^{-\kappa|x|},\quad 
\kappa=\frac{m|\alpha|}{\hbar^2},\quad
E=-\frac{m\alpha^2}{2\hbar^2}
}
$$

---

## (d) Scattering states for $E>0$

Define:

$$
k=\frac{\sqrt{2mE}}{\hbar}>0
$$

Solutions:

$$
\psi''(x)=-k^2\psi(x)
$$

Scattering ansatz:

$$
\psi(x)=A_i e^{ikx}+A_r e^{-ikx},\quad x<0
$$

$$
\psi(x)=A_t e^{ikx},\quad x>0
$$

---

## (e) Reflection and transmission

Continuity:

$$
A_i+A_r = A_t
$$

Derivatives:

$$
\psi_<'(0)=ik(A_i-A_r)
$$

$$
\psi_>'(0)=ikA_t
$$

Jump:

$$
2ikA_r=\eta(A_i+A_r)
$$

Define:

$$
r=\frac{A_r}{A_i},\quad t=\frac{A_t}{A_i}
$$

From continuity:

$$
t=1+r
$$

From jump:

$$
2ikr=\eta(1+r)
$$

Solve:

$$
r=\frac{\eta}{2ik-\eta}
$$

$$
t=\frac{2ik}{2ik-\eta}
$$

Transmission coefficient:

$$
T=|t|^2=\frac{4k^2}{4k^2+\eta^2}
$$

Using $\eta=\frac{2m\alpha}{\hbar^2}$:

$$
\boxed{
T=\frac{k^2}{k^2+\left(\frac{m\alpha}{\hbar^2}\right)^2}
}
$$

Reflection:

$$
R=\frac{\left(\frac{m\alpha}{\hbar^2}\right)^2}{k^2+\left(\frac{m\alpha}{\hbar^2}\right)^2}
$$

---

## Summary

- One bound state for $\alpha<0$:

$$
\psi(x)=\sqrt{\kappa}e^{-\kappa|x|},\quad 
\kappa=\frac{m|\alpha|}{\hbar^2},\quad
E=-\frac{m\alpha^2}{2\hbar^2}
$$

- Scattering states:

$$
\psi(x)=A_i e^{ikx}+A_r e^{-ikx},\ x<0;\quad 
\psi(x)=A_t e^{ikx},\ x>0
$$

- Coefficients:

$$
R=\frac{\left(\frac{m\alpha}{\hbar^2}\right)^2}{k^2+\left(\frac{m\alpha}{\hbar^2}\right)^2}
$$

$$
T=\frac{k^2}{k^2+\left(\frac{m\alpha}{\hbar^2}\right)^2}
$$

