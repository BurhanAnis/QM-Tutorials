
# Delta-Function Potential: Full Solution to Question 37

This document collects all the steps and explanations for Question 37 about the one-dimensional delta-function potential.

We consider the time-independent Schrödinger equation
\begin{equation}
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V(x)\psi(x) = E\psi(x),
\end{equation}
with
\begin{equation}
V(x) = \alpha\,\delta(x).
\end{equation}

---

## (a) Bound-state solutions for \(\alpha < 0\), \(E < 0\)

For \(x \neq 0\), the potential is zero because \(\delta(x) = 0\) for all \(x \neq 0\). Thus,
\begin{equation}
V(x) = \alpha \delta(x) = 0 \quad \text{for } x \neq 0.
\end{equation}

Therefore, in the regions \(x<0\) and \(x>0\), the Schrödinger equation reduces to that of a free particle:
\begin{equation}
-\frac{\hbar^2}{2m}\psi''(x) = E\psi(x).
\end{equation}

We are seeking a **bound state**, so the energy satisfies \(E<0\). Write
\begin{equation}
E < 0, \quad E = -|E|.
\end{equation}
Then the equation becomes
\begin{equation}
\psi''(x) = -\frac{2mE}{\hbar^2}\,\psi(x) = \frac{2m|E|}{\hbar^2}\,\psi(x).
\end{equation}

Define
\begin{equation}
\kappa \equiv \sqrt{-\frac{2mE}{\hbar^2}} = \sqrt{\frac{2m|E|}{\hbar^2}} > 0.
\end{equation}
The differential equation is
\begin{equation}
\psi''(x) = \kappa^2 \psi(x),
\end{equation}
whose general solution is a linear combination of exponentials.

Thus, in the two regions we can write
\begin{align}
\psi(x) &= A e^{\kappa x} + B e^{-\kappa x}, \quad x < 0, \\[4pt]
\psi(x) &= C e^{\kappa x} + D e^{-\kappa x}, \quad x > 0.
\end{align}

These constants are constrained by normalizability and the boundary conditions at \(x=0\), which will be enforced in later parts.

---

## (b) Derivative discontinuity and the constant \(\eta\)

We start from the full Schrödinger equation with the delta potential:
\begin{equation}
-\frac{\hbar^2}{2m} \psi''(x) + \alpha\,\delta(x)\,\psi(x) = E\psi(x).
\end{equation}

To understand the effect of the delta function, integrate this equation from \(-\varepsilon\) to \(+\varepsilon\) around \(x=0\), and then take the limit \(\varepsilon \to 0\):
\begin{equation}
\int_{-\varepsilon}^{+\varepsilon} \left(-\frac{\hbar^2}{2m}\psi''(x)\right) dx
+ \int_{-\varepsilon}^{+\varepsilon} \alpha\,\delta(x)\,\psi(x)\,dx
= \int_{-\varepsilon}^{+\varepsilon} E\psi(x)\,dx.
\end{equation}

### First term

Use the fundamental theorem of calculus:
\begin{equation}
\int_{-\varepsilon}^{+\varepsilon} \psi''(x)\,dx
= \left[\psi'(x)\right]_{-\varepsilon}^{+\varepsilon}
= \psi'(+\varepsilon) - \psi'(-\varepsilon).
\end{equation}

So the first term is
\begin{equation}
-\frac{\hbar^2}{2m}\big(\psi'(+\varepsilon) - \psi'(-\varepsilon)\big)
\xrightarrow[\varepsilon\to 0]{}
-\frac{\hbar^2}{2m} \big(\psi'(0^+) - \psi'(0^-)\big).
\end{equation}

### Second term (delta function)

Using the defining property of the delta function,
\begin{equation}
\int_{-\varepsilon}^{+\varepsilon} \delta(x)\,\psi(x)\,dx \approx \psi(0),
\end{equation}
assuming \(\psi(x)\) is continuous at \(x=0\). Thus,
\begin{equation}
\int_{-\varepsilon}^{+\varepsilon} \alpha\,\delta(x)\,\psi(x)\,dx \approx \alpha \psi(0).
\end{equation}

### Right-hand side

The right-hand side,
\begin{equation}
\int_{-\varepsilon}^{+\varepsilon} E\psi(x)\,dx,
\end{equation}
is proportional to the length of the interval \(2\varepsilon\), and both \(E\) and \(\psi(x)\) are finite at \(x=0\). Therefore,
\begin{equation}
\lim_{\varepsilon\to 0} \int_{-\varepsilon}^{+\varepsilon} E\psi(x)\,dx = 0.
\end{equation}

### Combine everything

Putting all pieces together and taking the limit \(\varepsilon \to 0\), we obtain
\begin{equation}
-\frac{\hbar^2}{2m} \big(\psi'(0^+) - \psi'(0^-)\big) + \alpha \psi(0) = 0.
\end{equation}

Rearranging:
\begin{equation}
\psi'(0^+) - \psi'(0^-) = \frac{2m\alpha}{\hbar^2}\,\psi(0).
\end{equation}

The problem states that the derivative discontinuity can be written as
\begin{equation}
\psi'(0^+) - \psi'(0^-) = \eta\,\psi(0).
\end{equation}
Comparing with the previous expression, we identify
\begin{equation}
\boxed{\eta = \frac{2m\alpha}{\hbar^2}}.
\end{equation}

The wavefunction \(\psi(x)\) itself remains continuous at \(x=0\); it is only the derivative that is discontinuous.

---

## (c) Bound-state wavefunction and energy for \(\alpha < 0\)

From (a), imposing normalizability (decay at \(|x|\to\infty\)) sets
\begin{align}
\psi(x) &= A e^{\kappa x}, \quad x<0 \quad (\text{discard the growing } e^{-\kappa x} \text{ as } x\to -\infty), \\
\psi(x) &= D e^{-\kappa x}, \quad x>0 \quad (\text{discard the growing } e^{\kappa x} \text{ as } x\to +\infty).
\end{align}

Continuity of \(\psi(x)\) at \(x=0\) gives
\begin{equation}
\psi(0^-) = \psi(0^+) \quad \Rightarrow \quad A = D.
\end{equation}

Let this common value be \(C\), so we can write
\begin{equation}
\psi(x) =
\begin{cases}
C e^{\kappa x}, & x<0, \\[4pt]
C e^{-\kappa x}, & x>0.
\end{cases}
\end{equation}

Equivalently,
\begin{equation}
\psi(x) = C e^{-\kappa |x|}.
\end{equation}

### Apply the derivative jump condition

We now use the discontinuity condition from part (b):
\begin{equation}
\psi'(0^+) - \psi'(0^-) = \eta\,\psi(0).
\end{equation}

Compute the derivatives at \(x=0\):
- For \(x>0\):
  \begin{equation}
  \psi(x) = C e^{-\kappa x} \Rightarrow \psi'(x) = -\kappa C e^{-\kappa x} \Rightarrow \psi'(0^+) = -\kappa C.
  \end{equation}
- For \(x<0\):
  \begin{equation}
  \psi(x) = C e^{\kappa x} \Rightarrow \psi'(x) = \kappa C e^{\kappa x} \Rightarrow \psi'(0^-) = \kappa C.
  \end{equation}

Thus,
\begin{equation}
\psi'(0^+) - \psi'(0^-) = (-\kappa C) - (\kappa C) = -2\kappa C.
\end{equation}

Also,
\begin{equation}
\psi(0) = C e^{-\kappa |0|} = C.
\end{equation}

The jump condition says
\begin{equation}
-2\kappa C = \eta\,\psi(0) = \eta C.
\end{equation}

Assuming \(C \neq 0\), we have
\begin{equation}
-2\kappa = \eta.
\end{equation}

Therefore,
\begin{equation}
\kappa = -\frac{\eta}{2}.
\end{equation}

Recalling \(\eta = \dfrac{2m\alpha}{\hbar^2}\), we get
\begin{equation}
\kappa = -\frac{1}{2}\cdot \frac{2m\alpha}{\hbar^2} = -\frac{m\alpha}{\hbar^2}.
\end{equation}

For \(\alpha < 0\), this gives
\begin{equation}
\kappa = \frac{m|\alpha|}{\hbar^2} > 0,
\end{equation}
as required.

### Energy of the bound state

By definition,
\begin{equation}
\kappa = \sqrt{-\frac{2mE}{\hbar^2}}.
\end{equation}
So
\begin{equation}
\kappa^2 = -\frac{2mE}{\hbar^2} \quad \Rightarrow \quad E = -\frac{\hbar^2 \kappa^2}{2m}.
\end{equation}

Substitute \(\kappa = \dfrac{m|\alpha|}{\hbar^2}\):
\begin{equation}
E = -\frac{\hbar^2}{2m}\left(\frac{m^2\alpha^2}{\hbar^4}\right)
= -\frac{m\alpha^2}{2\hbar^2}.
\end{equation}

Thus, the bound-state energy is
\begin{equation}
\boxed{E = -\frac{m\alpha^2}{2\hbar^2}}.
\end{equation}

### Normalization of the bound state

We have
\begin{equation}
\psi(x) = C e^{-\kappa|x|}.
\end{equation}

Normalize:
\begin{equation}
\int_{-\infty}^{\infty} |\psi(x)|^2\,dx = 1.
\end{equation}

Compute the integral:
\begin{align}
\int_{-\infty}^{\infty} |\psi(x)|^2\,dx
&= \int_{-\infty}^{\infty} |C|^2 e^{-2\kappa |x|}\,dx \\
&= |C|^2 \cdot 2 \int_{0}^{\infty} e^{-2\kappa x}\,dx \\
&= |C|^2 \cdot 2 \cdot \frac{1}{2\kappa} \\
&= \frac{|C|^2}{\kappa}.
\end{align}

Setting this equal to 1 gives
\begin{equation}
\frac{|C|^2}{\kappa} = 1 \quad \Rightarrow \quad |C|^2 = \kappa.
\end{equation}

Choosing \(C\) real and positive,
\begin{equation}
C = \sqrt{\kappa}.
\end{equation}

The normalized bound state is therefore
\begin{equation}
\boxed{
\psi(x) = \sqrt{\kappa}\,e^{-\kappa|x|}, 
\quad \kappa = \frac{m|\alpha|}{\hbar^2}, 
\quad E = -\frac{m\alpha^2}{2\hbar^2}.
}
\end{equation}

---

## (d) Scattering states for \(E>0\)

Now take \(E>0\). For \(x\neq 0\), the potential is again zero, so
\begin{equation}
-\frac{\hbar^2}{2m}\psi''(x) = E\psi(x).
\end{equation}
Rewriting,
\begin{equation}
\psi''(x) = -\frac{2mE}{\hbar^2}\psi(x).
\end{equation}

Define
\begin{equation}
k \equiv \frac{\sqrt{2mE}}{\hbar} > 0.
\end{equation}

Then
\begin{equation}
\psi''(x) = -k^2 \psi(x),
\end{equation}
whose general solutions are plane waves
\begin{equation}
\psi(x) = A e^{ikx} + B e^{-ikx}.
\end{equation}

We consider a scattering setup in which a particle comes in from the left:
- On the left of the potential (\(x<0\)), there is an **incoming** right-moving wave and a **reflected** left-moving wave.
- On the right (\(x>0\)), there is only a **transmitted** right-moving wave (no incoming wave from \(+\infty\)).

Thus we write
\begin{align}
\psi(x) &= A_i e^{ikx} + A_r e^{-ikx}, \quad x<0, \\[4pt]
\psi(x) &= A_t e^{ikx}, \quad x>0,
\end{align}
where
- \(A_i\) is the incident amplitude,
- \(A_r\) is the reflected amplitude,
- \(A_t\) is the transmitted amplitude.

This is the standard scattering ansatz for a localized potential in one dimension.

---

## (e) Reflection and transmission coefficients

We now use two conditions at \(x=0\):

1. **Continuity of \(\psi\)**:
   \begin{equation}
   \psi(0^-) = \psi(0^+).
   \end{equation}
2. **Derivative jump condition**:
   \begin{equation}
   \psi'(0^+) - \psi'(0^-) = \eta\,\psi(0), \quad \eta = \frac{2m\alpha}{\hbar^2}.
   \end{equation}

### Continuity of \(\psi\)

At \(x=0\):
\begin{align}
\psi(0^-) &= A_i e^{ik\cdot 0} + A_r e^{-ik\cdot 0} = A_i + A_r, \\
\psi(0^+) &= A_t e^{ik\cdot 0} = A_t.
\end{align}

Continuity implies
\begin{equation}
A_i + A_r = A_t.
\tag{1}
\end{equation}

### Derivative jump condition

Compute the derivatives:
- For \(x<0\):
  \begin{equation}
  \psi_<'(x) = ikA_i e^{ikx} - ikA_r e^{-ikx} \Rightarrow \psi_<'(0) = ik(A_i - A_r).
  \end{equation}
- For \(x>0\):
  \begin{equation}
  \psi_>'(x) = ikA_t e^{ikx} \Rightarrow \psi_>'(0) = ikA_t.
  \end{equation}

Thus,
\begin{equation}
\psi'(0^+) - \psi'(0^-)
= ikA_t - ik(A_i - A_r)
= ik(A_t - A_i + A_r).
\end{equation}

Using (1), \(A_t = A_i + A_r\), we find
\begin{equation}
A_t - A_i + A_r = (A_i + A_r) - A_i + A_r = 2A_r,
\end{equation}
so
\begin{equation}
\psi'(0^+) - \psi'(0^-) = 2ikA_r.
\end{equation}

The jump condition gives
\begin{equation}
2ikA_r = \eta\,\psi(0) = \eta(A_i + A_r).
\tag{2}
\end{equation}

### Solve for reflection and transmission amplitudes

Introduce the dimensionless ratios
\begin{equation}
r \equiv \frac{A_r}{A_i}, \quad t \equiv \frac{A_t}{A_i}.
\end{equation}

From (1):
\begin{equation}
A_i + A_r = A_t \quad \Rightarrow \quad 1 + r = t.
\tag{3}
\end{equation}

From (2):
\begin{equation}
2ikA_r = \eta(A_i + A_r).
\end{equation}
Divide by \(A_i\):
\begin{equation}
2ik\,r = \eta(1 + r).
\tag{4}
\end{equation}

Solve (4) for \(r\):
\begin{align}
2ik\,r &= \eta + \eta r, \\
(2ik - \eta) r &= \eta, \\
r &= \frac{\eta}{2ik - \eta}.
\end{align}

Then from (3):
\begin{align}
t &= 1 + r
= 1 + \frac{\eta}{2ik - \eta}
= \frac{2ik - \eta + \eta}{2ik - \eta}
= \frac{2ik}{2ik - \eta}.
\end{align}

So the **reflection amplitude** and **transmission amplitude** are
\begin{equation}
r = \frac{\eta}{2ik - \eta}, \quad
t = \frac{2ik}{2ik - \eta},
\end{equation}
with \(\eta = \dfrac{2m\alpha}{\hbar^2}\).

### Reflection and transmission coefficients

The reflection and transmission coefficients are the ratios of reflected and transmitted probability currents to the incident current. For plane waves with the same \(k\) on both sides, the currents are proportional to \(|A|^2 k\), so
\begin{equation}
R = \left|\frac{A_r}{A_i}\right|^2 = |r|^2, \quad
T = \left|\frac{A_t}{A_i}\right|^2 = |t|^2.
\end{equation}

Since \(\eta\) is real,
\begin{equation}
|2ik - \eta|^2 = (2ik - \eta)(-2ik - \eta) = 4k^2 + \eta^2.
\end{equation}

For the transmission coefficient,
\begin{equation}
T = |t|^2 = \left|\frac{2ik}{2ik - \eta}\right|^2
= \frac{4k^2}{4k^2 + \eta^2}.
\end{equation}

Using \(\eta = \dfrac{2m\alpha}{\hbar^2}\),
\begin{equation}
\eta^2 = \frac{4m^2\alpha^2}{\hbar^4},
\end{equation}
so we can also write
\begin{equation}
T = \frac{4k^2}{4k^2 + \dfrac{4m^2\alpha^2}{\hbar^4}}
= \frac{k^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
\end{equation}

Thus the transmission coefficient is
\begin{equation}
\boxed{
T = \frac{k^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}}, 
\quad k = \frac{\sqrt{2mE}}{\hbar}.
\end{equation}

Similarly, the reflection coefficient is
\begin{equation}
R = |r|^2 = \left|\frac{\eta}{2ik - \eta}\right|^2
= \frac{\eta^2}{4k^2 + \eta^2}
= \frac{\left(\dfrac{m\alpha}{\hbar^2}\right)^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
\end{equation}

Clearly,
\begin{equation}
R + T = 1,
\end{equation}
as expected for a real, localized potential in one dimension.

---

### Final Summary

- For \(\alpha<0\), there is exactly one bound state with normalized wavefunction
  \begin{equation}
  \psi(x) = \sqrt{\kappa}\,e^{-\kappa|x|}, 
  \quad \kappa = \frac{m|\alpha|}{\hbar^2},
  \end{equation}
  and energy
  \begin{equation}
  E = -\frac{m\alpha^2}{2\hbar^2}.
  \end{equation}

- For scattering states with \(E>0\), the wavefunction is
  \begin{equation}
  \psi(x) =
  \begin{cases}
  A_i e^{ikx} + A_r e^{-ikx}, & x<0, \\[4pt]
  A_t e^{ikx}, & x>0,
  \end{cases}
  \quad k = \dfrac{\sqrt{2mE}}{\hbar},
  \end{equation}
  with reflection and transmission coefficients
  \begin{equation}
  R = \frac{\left(\dfrac{m\alpha}{\hbar^2}\right)^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}, 
  \qquad
  T = \frac{k^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
  \end{equation}
