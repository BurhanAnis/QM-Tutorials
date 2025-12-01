# Delta-Function Potential: Full Solution to Question 37 (Expanded)

This document collects **all** the steps and explanations for Question 37 about the one-dimensional delta-function potential, with more detailed algebra and reasoning shown explicitly.

We consider the time-independent Schrödinger equation:

\[
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + V(x)\psi(x) = E\psi(x)
\]

with

\[
V(x) = \alpha\,\delta(x).
\]

Here:
- \(m\) is the particle mass,
- \(\hbar\) is the reduced Planck constant,
- \(E\) is the energy eigenvalue,
- \(\delta(x)\) is the Dirac delta function,
- \(\alpha\) is a real constant (strength of the delta potential).

---

## (a) Bound-state solutions for \(\alpha < 0\), \(E < 0\)

### Step 1: Why is \(V(x)=0\) when \(x \neq 0\)?

By definition of the Dirac delta function:
1. \(\delta(x) = 0\) for all \(x \neq 0\),
2. \(\displaystyle \int_{-\infty}^{\infty}\delta(x)\,dx = 1\).

Since
\[
V(x) = \alpha \delta(x),
\]
it follows that for **all** \(x \neq 0\),
\[
V(x) = \alpha \delta(x) = \alpha \cdot 0 = 0.
\]

So **outside** the single point \(x=0\), the potential is zero.

### Step 2: Schrödinger equation for \(x \neq 0\)

For \(x \neq 0\), the Schrödinger equation becomes
\[
-\frac{\hbar^2}{2m}\frac{d^2\psi}{dx^2} + 0\cdot \psi(x) = E\psi(x),
\]
or simply
\[
-\frac{\hbar^2}{2m}\psi''(x) = E\psi(x).
\]

Multiply both sides by \(-\dfrac{2m}{\hbar^2}\):
\[
\psi''(x) = -\frac{2mE}{\hbar^2}\,\psi(x).
\]

### Step 3: Use that \(E<0\)

For a **bound state**, we have \(E<0\). Let us write
\[
E = -|E|, \quad |E|>0.
\]

Then
\[
-\frac{2mE}{\hbar^2}
= -\frac{2m(-|E|)}{\hbar^2}
= \frac{2m|E|}{\hbar^2} > 0.
\]

Therefore,
\[
\psi''(x) = \frac{2m|E|}{\hbar^2}\,\psi(x).
\]

### Step 4: Define \(\kappa\)

Introduce a positive constant \(\kappa\) to simplify notation:
\[
\kappa \equiv \sqrt{\frac{2m|E|}{\hbar^2}} 
= \sqrt{-\frac{2mE}{\hbar^2}} > 0.
\]

Then our differential equation is
\[
\psi''(x) = \kappa^2 \psi(x).
\]

### Step 5: Solve the differential equation

The ODE
\[
\psi''(x) = \kappa^2 \psi(x)
\]
has general solution
\[
\psi(x) = A e^{\kappa x} + B e^{-\kappa x},
\]
for **any** interval where the equation holds (here for \(x<0\) or \(x>0\)).

So we write, in the most general way:

- For \(x<0\):
  \[
  \psi(x) = A e^{\kappa x} + B e^{-\kappa x}.
  \]

- For \(x>0\):
  \[
  \psi(x) = C e^{\kappa x} + D e^{-\kappa x}.
  \]

At this stage \(A,B,C,D\) are arbitrary constants. They will be fixed by:
1. Normalizability (wavefunction must not blow up at \(|x|\to\infty\)),
2. Continuity at \(x=0\),
3. The derivative jump condition at \(x=0\) from the delta potential.

---

## (b) Derivative discontinuity and \(\eta\)

We now derive the condition on the **derivative** of \(\psi\) at \(x=0\). Start from the full Schrödinger equation:

\[
-\frac{\hbar^2}{2m}\psi''(x) + \alpha\,\delta(x)\,\psi(x) = E\psi(x).
\]

### Step 1: Integrate across a small interval around \(x=0\)

Integrate both sides from \(-\varepsilon\) to \(+\varepsilon\), with \(\varepsilon>0\) small:

\[
\int_{-\varepsilon}^{+\varepsilon}
\left(
-\frac{\hbar^2}{2m}\psi''(x) + \alpha\,\delta(x)\,\psi(x)
\right) dx
=
\int_{-\varepsilon}^{+\varepsilon}
E\psi(x)\,dx.
\]

We now evaluate each term separately.

### Step 2: The \(\psi''(x)\) term

Consider
\[
\int_{-\varepsilon}^{+\varepsilon} \psi''(x)\,dx.
\]

Using the fundamental theorem of calculus,
\[
\int_{-\varepsilon}^{+\varepsilon} \psi''(x)\,dx
= \left[\psi'(x)\right]_{x=-\varepsilon}^{x=+\varepsilon}
= \psi'(+\varepsilon) - \psi'(-\varepsilon).
\]

Thus the first term in the Schrödinger equation gives

\[
-\frac{\hbar^2}{2m}
\int_{-\varepsilon}^{+\varepsilon} \psi''(x)\,dx
=
-\frac{\hbar^2}{2m}\big(\psi'(+\varepsilon) - \psi'(-\varepsilon)\big).
\]

In the limit \(\varepsilon \to 0\), we define:

\[
\psi'(0^+) \equiv \lim_{x \to 0^+}\psi'(x), \quad
\psi'(0^-) \equiv \lim_{x \to 0^-}\psi'(x),
\]

so

\[
\lim_{\varepsilon\to 0}
\left[-\frac{\hbar^2}{2m}\big(\psi'(+\varepsilon) - \psi'(-\varepsilon)\big)\right]
=
-\frac{\hbar^2}{2m}\big(\psi'(0^+) - \psi'(0^-)\big).
\]

### Step 3: The delta-function term

Now consider the second term:
\[
\int_{-\varepsilon}^{+\varepsilon} \alpha\,\delta(x)\,\psi(x)\,dx
= \alpha \int_{-\varepsilon}^{+\varepsilon} \delta(x)\,\psi(x)\,dx.
\]

By the defining property of \(\delta(x)\), for a function \(\psi(x)\) that is continuous at \(x=0\):

\[
\int_{-\varepsilon}^{+\varepsilon} \delta(x)\,\psi(x)\,dx \to \psi(0)
\quad \text{as } \varepsilon \text{ is large enough to include } x=0.
\]

Therefore, in the limit,

\[
\int_{-\varepsilon}^{+\varepsilon} \alpha\,\delta(x)\,\psi(x)\,dx \to \alpha\,\psi(0).
\]

### Step 4: The right-hand side

The right-hand side is

\[
\int_{-\varepsilon}^{+\varepsilon} E\psi(x)\,dx.
\]

Here, \(E\) is finite and \(\psi(x)\) is assumed finite and continuous at \(x=0\). The interval length is \(2\varepsilon\), so the integral is of order \(\varepsilon\). Thus,

\[
\lim_{\varepsilon\to 0}\int_{-\varepsilon}^{+\varepsilon} E\psi(x)\,dx = 0.
\]

### Step 5: Combine all terms

Putting everything together, in the limit \(\varepsilon \to 0\):

\[
-\frac{\hbar^2}{2m}\big(\psi'(0^+) - \psi'(0^-)\big) + \alpha\,\psi(0) = 0.
\]

Rearrange to solve for the jump in the derivative:

\[
-\frac{\hbar^2}{2m}\big(\psi'(0^+) - \psi'(0^-)\big)
= -\alpha\,\psi(0),
\]

so

\[
\psi'(0^+) - \psi'(0^-) = \frac{2m\alpha}{\hbar^2}\,\psi(0).
\]

The problem states this jump as

\[
\psi'(0^+) - \psi'(0^-) = \eta\,\psi(0).
\]

Comparing, we identify

\[
\boxed{\eta = \frac{2m\alpha}{\hbar^2}}.
\]

**Key point:**  
- The wavefunction \(\psi(x)\) is **continuous** at \(x=0\),  
- Its derivative \(\psi'(x)\) has a **finite jump** at \(x=0\) proportional to \(\psi(0)\).

---

## (c) Bound-state wavefunction and energy

We now use:
1. Normalizability (bound state),
2. Continuity of \(\psi\) at \(x=0\),
3. The derivative jump condition from part (b).

### Step 1: Enforce normalizability

From part (a), the general solutions were:

- For \(x<0\):
  \[
  \psi(x) = A e^{\kappa x} + B e^{-\kappa x}.
  \]

- For \(x>0\):
  \[
  \psi(x) = C e^{\kappa x} + D e^{-\kappa x}.
  \]

We require \(|\psi(x)|^2\) to be integrable on \((-\infty,\infty)\). This means \(\psi(x) \to 0\) as \(|x|\to\infty\).

#### For \(x \to -\infty\):

- \(e^{\kappa x} \to 0\) (since \(x\) is large negative),
- \(e^{-\kappa x} \to \infty\) (blows up).

So we **must** set the coefficient of the growing term to zero:
\[
B = 0.
\]

Thus, for \(x<0\),
\[
\psi(x) = A e^{\kappa x}.
\]

#### For \(x \to +\infty\):

- \(e^{\kappa x} \to \infty\) (grows),
- \(e^{-\kappa x} \to 0\) (decays).

So we must set
\[
C = 0.
\]

Thus, for \(x>0\),
\[
\psi(x) = D e^{-\kappa x}.
\]

So far we have
\[
\psi(x) =
\begin{cases}
A e^{\kappa x}, & x<0,\\[4pt]
D e^{-\kappa x}, & x>0.
\end{cases}
\]

### Step 2: Continuity at \(x=0\)

We require
\[
\psi(0^-) = \psi(0^+).
\]

Compute each side:
- For \(x<0\): \(\psi(0^-) = A e^{\kappa\cdot 0} = A\).
- For \(x>0\): \(\psi(0^+) = D e^{-\kappa\cdot 0} = D\).

So
\[
A = D.
\]

Let this common value be \(C\). Then we can write
\[
\psi(x) =
\begin{cases}
C e^{\kappa x}, & x<0,\\[4pt]
C e^{-\kappa x}, & x>0.
\end{cases}
\]

This can be written compactly using \(|x|\):

\[
\psi(x) = C e^{-\kappa |x|}.
\]

### Step 3: Apply the derivative jump condition

From part (b):
\[
\psi'(0^+) - \psi'(0^-) = \eta\,\psi(0),
\quad \eta = \frac{2m\alpha}{\hbar^2}.
\]

First compute the derivatives.

For \(x>0\):
\[
\psi(x) = C e^{-\kappa x} \quad\Rightarrow\quad
\psi'(x) = -\kappa C e^{-\kappa x},
\]
so
\[
\psi'(0^+) = -\kappa C.
\]

For \(x<0\):
\[
\psi(x) = C e^{\kappa x} \quad\Rightarrow\quad
\psi'(x) = \kappa C e^{\kappa x},
\]
so
\[
\psi'(0^-) = \kappa C.
\]

Now form the difference:
\[
\psi'(0^+) - \psi'(0^-)
= (-\kappa C) - (\kappa C)
= -2\kappa C.
\]

We also have
\[
\psi(0) = C e^{-\kappa|0|} = C.
\]

Substitute into the jump condition:
\[
-2\kappa C = \eta\,\psi(0) = \eta C.
\]

Assuming \(C \neq 0\), divide both sides by \(C\):
\[
-2\kappa = \eta.
\]

Thus,
\[
\kappa = -\frac{\eta}{2}.
\]

Since
\[
\eta = \frac{2m\alpha}{\hbar^2},
\]
we have
\[
\kappa = -\frac{1}{2}\cdot\frac{2m\alpha}{\hbar^2}
= -\frac{m\alpha}{\hbar^2}.
\]

For \(\alpha < 0\), we can write \(-\alpha = |\alpha|\), so
\[
\kappa = \frac{m|\alpha|}{\hbar^2} > 0,
\]
which is consistent with our definition of a positive \(\kappa\).

### Step 4: Energy of the bound state

We defined earlier
\[
\kappa = \sqrt{-\frac{2mE}{\hbar^2}}.
\]

Square both sides:
\[
\kappa^2 = -\frac{2mE}{\hbar^2}.
\]

Solve for \(E\):
\[
E = -\frac{\hbar^2\kappa^2}{2m}.
\]

Now substitute \(\kappa = \dfrac{m|\alpha|}{\hbar^2}\):
\[
\kappa^2 = \frac{m^2\alpha^2}{\hbar^4},
\]
so
\[
E = -\frac{\hbar^2}{2m}\cdot \frac{m^2\alpha^2}{\hbar^4}
= -\frac{m\alpha^2}{2\hbar^2}.
\]

Thus the bound-state energy is
\[
\boxed{E = -\frac{m\alpha^2}{2\hbar^2}}.
\]

### Step 5: Normalization of the bound state

We now normalize
\[
\psi(x) = C e^{-\kappa|x|}.
\]

The normalization condition is
\[
\int_{-\infty}^{\infty} |\psi(x)|^2\,dx = 1.
\]

Compute:
\begin{align*}
\int_{-\infty}^{\infty} |\psi(x)|^2 dx
&= \int_{-\infty}^{\infty} |C|^2 e^{-2\kappa |x|}\,dx \\
&= |C|^2 \left(\int_{-\infty}^{0} e^{-2\kappa |x|}\,dx + \int_{0}^{\infty} e^{-2\kappa |x|}\,dx\right).
\end{align*}

For \(x<0\), \(|x| = -x\), so
\[
\int_{-\infty}^{0} e^{-2\kappa |x|}\,dx
= \int_{-\infty}^{0} e^{-2\kappa(-x)}\,dx
= \int_{-\infty}^{0} e^{2\kappa x}\,dx.
\]

For \(x>0\), \(|x| = x\), so
\[
\int_{0}^{\infty} e^{-2\kappa |x|}\,dx
= \int_{0}^{\infty} e^{-2\kappa x}\,dx.
\]

Both integrals are equal, so
\begin{align*}
\int_{-\infty}^{\infty} |\psi(x)|^2 dx
&= |C|^2 \cdot 2 \int_{0}^{\infty} e^{-2\kappa x}\,dx.
\end{align*}

Now compute the integral:
\[
\int_{0}^{\infty} e^{-2\kappa x}\,dx
= \left[-\frac{1}{2\kappa}e^{-2\kappa x}\right]_{0}^{\infty}
= 0 - \left(-\frac{1}{2\kappa}\right)
= \frac{1}{2\kappa}.
\]

Hence
\begin{align*}
\int_{-\infty}^{\infty} |\psi(x)|^2 dx
&= |C|^2 \cdot 2 \cdot \frac{1}{2\kappa}
= \frac{|C|^2}{\kappa}.
\end{align*}

Set equal to 1:
\[
\frac{|C|^2}{\kappa} = 1
\quad\Rightarrow\quad
|C|^2 = \kappa.
\]

Choose \(C\) real and positive:
\[
C = \sqrt{\kappa}.
\]

**Final normalized bound state:**
\[
\boxed{
\psi(x) = \sqrt{\kappa}\,e^{-\kappa|x|},\quad
\kappa = \frac{m|\alpha|}{\hbar^2},\quad
E = -\frac{m\alpha^2}{2\hbar^2}.
}
\]

---

## (d) Scattering states for \(E>0\)

Now consider **scattering states** with **positive energy** \(E>0\). For \(x \neq 0\), the potential is zero, so

\[
-\frac{\hbar^2}{2m}\psi''(x) = E\psi(x).
\]

Rearrange:
\[
\psi''(x) = -\frac{2mE}{\hbar^2}\psi(x).
\]

Define
\[
k \equiv \frac{\sqrt{2mE}}{\hbar} > 0.
\]

Then
\[
\psi''(x) = -k^2 \psi(x).
\]

The general solution is a superposition of plane waves:
\[
\psi(x) = A e^{ikx} + B e^{-ikx}.
\]

### Physical interpretation of the exponentials

- \(e^{ikx}\) represents a **right-moving** plane wave (positive momentum).
- \(e^{-ikx}\) represents a **left-moving** plane wave (negative momentum).

### Scattering setup: incoming wave from the left

We assume a beam of particles:
- Coming from the left (\(x \to -\infty\)),
- Moving to the right,
- Scattering off the potential at \(x=0\),
- Partly reflected back to the left,
- Partly transmitted to the right (\(x \to +\infty\)).

Thus:

- For \(x<0\):
  - There is a **right-moving incoming** wave with amplitude \(A_i\).
  - There is a **left-moving reflected** wave with amplitude \(A_r\).
  \[
  \psi(x) = A_i e^{ikx} + A_r e^{-ikx}, \quad x<0.
  \]

- For \(x>0\):
  - We only want an **outgoing** right-moving wave (no incoming wave from \(+\infty\)), so the coefficient of \(e^{-ikx}\) is zero. The amplitude of the transmitted wave is \(A_t\):
  \[
  \psi(x) = A_t e^{ikx}, \quad x>0.
  \]

This is the standard **scattering ansatz** for a localized potential.

---

## (e) Reflection and transmission

We now find the reflection and transmission **coefficients** by applying the boundary conditions at \(x=0\).

### Step 1: Continuity of \(\psi\) at \(x=0\)

From the left:
\[
\psi(0^-) = A_i e^{ik\cdot 0} + A_r e^{-ik\cdot 0} = A_i + A_r.
\]

From the right:
\[
\psi(0^+) = A_t e^{ik\cdot 0} = A_t.
\]

Continuity requires:
\[
A_i + A_r = A_t.
\tag{1}
\]

### Step 2: Derivative jump condition

We use again
\[
\psi'(0^+) - \psi'(0^-) = \eta\,\psi(0), \quad \eta = \frac{2m\alpha}{\hbar^2}.
\]

First compute the derivatives.

For \(x<0\):
\[
\psi(x) = A_i e^{ikx} + A_r e^{-ikx},
\]
so
\[
\psi'(x) = ikA_i e^{ikx} - ikA_r e^{-ikx},
\]
and therefore
\[
\psi_<'(0) = ikA_i - ikA_r = ik(A_i - A_r).
\]

For \(x>0\):
\[
\psi(x) = A_t e^{ikx} \Rightarrow \psi'(x) = ikA_t e^{ikx},
\]
so
\[
\psi_>'(0) = ikA_t.
\]

Now compute the jump:
\[
\psi'(0^+) - \psi'(0^-)
= ikA_t - ik(A_i - A_r)
= ik(A_t - A_i + A_r).
\]

Using continuity (1), \(A_t = A_i + A_r\), we get
\begin{align*}
A_t - A_i + A_r
&= (A_i + A_r) - A_i + A_r \\
&= 2A_r.
\end{align*}

Hence,
\[
\psi'(0^+) - \psi'(0^-)
= ik \cdot 2A_r = 2ikA_r.
\]

The jump condition then reads
\[
2ikA_r = \eta\,\psi(0) = \eta(A_i + A_r).
\tag{2}
\]

### Step 3: Define reflection and transmission amplitudes

Define the **reflection amplitude** \(r\) and **transmission amplitude** \(t\) as
\[
r \equiv \frac{A_r}{A_i}, \quad t \equiv \frac{A_t}{A_i}.
\]

From (1):
\[
A_i + A_r = A_t
\quad\Rightarrow\quad
1 + r = t.
\tag{3}
\]

From (2):
\[
2ikA_r = \eta (A_i + A_r).
\]

Divide everything by \(A_i\):
\[
2ikr = \eta (1 + r).
\tag{4}
\]

### Step 4: Solve for \(r\) and \(t\)

From (4), solve for \(r\):

\begin{align*}
2ikr &= \eta + \eta r, \\
2ikr - \eta r &= \eta, \\
r(2ik - \eta) &= \eta, \\
r &= \frac{\eta}{2ik - \eta}.
\end{align*}

Using (3),
\begin{align*}
t &= 1 + r
= 1 + \frac{\eta}{2ik - \eta}
= \frac{2ik - \eta + \eta}{2ik - \eta}
= \frac{2ik}{2ik - \eta}.
\end{align*}

So, the **reflection amplitude** and **transmission amplitude** are
\[
r = \frac{\eta}{2ik - \eta}, 
\quad
t = \frac{2ik}{2ik - \eta},
\]
with \(\eta = \dfrac{2m\alpha}{\hbar^2}\).

### Step 5: Reflection and transmission coefficients

The **reflection coefficient** \(R\) is the ratio of reflected probability current to incident current. For plane waves in 1D with the same \(k\) on both sides, the probability current is proportional to \(|A|^2 k/m\), so the ratios reduce to just ratios of squared amplitudes:
\[
R = \left|\frac{A_r}{A_i}\right|^2 = |r|^2, \quad
T = \left|\frac{A_t}{A_i}\right|^2 = |t|^2.
\]

We focus first on \(T\). Since \(\eta\) is real,

\[
|2ik - \eta|^2 = (2ik - \eta)(-2ik - \eta)
= (2ik)(-2ik) - \eta(2ik) - \eta(-2ik) - \eta^2
= 4k^2 + \eta^2.
\]

The magnitude squared of the numerator of \(t\) is
\[
|2ik|^2 = (2ik)(-2ik) = 4k^2.
\]

Therefore,
\[
T = |t|^2 = \left|\frac{2ik}{2ik - \eta}\right|^2
= \frac{4k^2}{4k^2 + \eta^2}.
\]

Now substitute
\[
\eta = \frac{2m\alpha}{\hbar^2},
\quad\Rightarrow\quad
\eta^2 = \frac{4m^2\alpha^2}{\hbar^4}.
\]

Then
\begin{align*}
T &= \frac{4k^2}{4k^2 + \dfrac{4m^2\alpha^2}{\hbar^4}} \\
  &= \frac{k^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
\end{align*}

So the **transmission coefficient** is
\[
\boxed{
T = \frac{k^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}
},
\quad k = \frac{\sqrt{2mE}}{\hbar}.
\]

For the **reflection coefficient**,
\[
R = |r|^2 = \left|\frac{\eta}{2ik - \eta}\right|^2
= \frac{\eta^2}{4k^2 + \eta^2}
= \frac{\left(\dfrac{m\alpha}{\hbar^2}\right)^2}{k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
\]

One can check explicitly that
\[
R + T = 1,
\]
as required for a real, localized potential in one dimension (probability is conserved).

---

## Summary

- For \(\alpha<0\), there is exactly **one bound state** with normalized wavefunction
  \[
  \boxed{
  \psi(x) = \sqrt{\kappa}\,e^{-\kappa|x|},
  \quad
  \kappa = \frac{m|\alpha|}{\hbar^2},
  \quad
  E = -\frac{m\alpha^2}{2\hbar^2}.
  }
  \]

- For **scattering states** with \(E>0\), the wavefunction is
  \[
  \psi(x) =
  \begin{cases}
  A_i e^{ikx} + A_r e^{-ikx}, & x<0,\\[4pt]
  A_t e^{ikx}, & x>0,
  \end{cases}
  \quad k = \dfrac{\sqrt{2mE}}{\hbar}.
  \]

- The reflection and transmission **coefficients** are
  \[
  \boxed{
  R = \frac{\left(\dfrac{m\alpha}{\hbar^2}\right)^2}
           {k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2},
  \quad
  T = \frac{k^2}
           {k^2 + \left(\dfrac{m\alpha}{\hbar^2}\right)^2}.
  }
  \]

These formulas completely characterize the bound and scattering states of the one-dimensional delta-function potential.

