# On the Incompatibility of the Gram and Weil Completions

**Hauteville House**  
*October 2025*

---

Let $D = -i\frac{d}{dx}$ and $P$ the Fourier multiplier $-i\,\mathrm{sgn}(\xi)$ on $L^2_0(\mathbb R)$. For $\psi \in C_c^\infty(\mathbb R)$, define

\[
Q_0(\psi,\psi) = \frac{1}{\pi}\|\psi'\|_{L^2}^2,
\qquad
U\psi = \pi^{-1/2}\widehat{P_{D\psi}}.
\]

The form $Q_0$ is positive definite; its completion is a Hilbert space $\mathcal H_0$ of functions with one derivative in $L^2$. The construction is unconditional and contains no arithmetic data.

Define the Weil functional

\[
\begin{aligned}
W(f) = &\int_{\mathbb R} f(x)(e^{x/2}+e^{-x/2})\,dx \\
&- \sum_{n\ge 1} \frac{\Lambda(n)}{\sqrt n} [f(\log n)+f(-\log n)] \\
&- (\log 4\pi + \gamma) f(0) \\
&- \int_0^\infty [f(x)+f(-x)-2e^{-x/2}f(0)] \frac{e^{x/2}}{e^x-e^{-x}}\,dx,
\end{aligned}
\]

and from it the quadratic form

\[
Q_W(\psi,\psi) = W(\psi * \tilde\psi).
\]

Weil's criterion asserts

\[
\tag{1}
RH \iff Q_W(\psi,\psi) \ge 0 \text{ for all } \psi \in C_c^\infty(\mathbb R).
\]

When $Q_W \ge 0$, the completion of $C_c^\infty(\mathbb R)$ under $Q_W$ is a Hilbert space $\mathcal H_W$. Under RH, $\mathcal H_0$ and $\mathcal H_W$ coincide and the norms are equivalent up to a constant factor.

The purpose of this note is to prove that $Q_0 \neq Q_W$ on $C_c^\infty(\mathbb R)$, and therefore, by (1), that $\neg RH$.

---

Localize to functions supported in $(-a,a)$. Denote

\[
Q_W^a(\psi) = Q_W(\psi), \qquad \mathrm{supp}\,\psi \subset (-a,a),
\]

and let $A_a$ be the self-adjoint operator associated with the Friedrichs extension of $Q_W^a$. The operator $A_a$ has discrete spectrum bounded below. Its lowest eigenvalue

\[
\lambda(a) = \inf \sigma(A_a)
\]

is continuous in $a$, and $\lambda(a) > 0$ for sufficiently small $a$. Moreover, $a < b$ implies $\lambda(b) \le \lambda(a)$ because the support classes are nested. Thus, if $Q_W \ge 0$ (equivalently, if RH holds), we have $Q_W^a > 0$ for every $a$ and $\lambda(a)$ is a positive, nonincreasing function. The family $a \mapsto A_a$ is the canonical one-parameter evolution, and $\lambda(a)$ is the monotone quantity.

---

Separate the localized Weil form into its archimedean part and its arithmetic part:

\[
q_a[u] = q_{\infty,a}[u] - p_a[u],
\qquad
p_a[u] = 2\sum_{\log n < 2a} \frac{\Lambda(n)}{\sqrt n} \Re\langle T_{\log n}^{(a)} u, u\rangle,
\]

where $q_{\infty,a}$ is the logarithmic archimedean part. The prime sum is finite; because truncated translations are contractions, $|p_a[u]| \le 2B(a)\|u\|^2$ with $B(a) = \sum_{\log n < 2a} \Lambda(n)/\sqrt n$, so $p_a$ is a bounded form perturbation. Consequently $D(q_a) = D(q_{\infty,a})$: all domain regularity is archimedean.

For every active shift $h_n = \log n$ with $h_n < 2a$, define the defect operator

\[
d_n^{(a)} v = (T_{h_n} - I)v,
\]

where $T_{h_n}$ denotes translation with zero extension to $\mathbb R$. The arithmetic contribution to the Weil form decomposes as

\[
P_a[v] = 2\sum_{n \le e^{2a}} \frac{\Lambda(n)}{\sqrt n} \Re\langle T_{h_n}v,v\rangle
= 2C(a)\|v\|^2 - \mathfrak D_a[v],
\]

where $C(a) = \sum_{n \le e^{2a}} \frac{\Lambda(n)}{\sqrt n}$ and

\[
\tag{2}
\mathfrak D_a[v] = \sum_{n \le e^{2a}} \frac{\Lambda(n)}{\sqrt n} \|d_n^{(a)} v\|^2
\]

is the arithmetic defect. The defect Gram tensor

\[
\tag{3}
\mathsf G_{mn}^{(a)}(v) = \langle d_m^{(a)} v, d_n^{(a)} v\rangle
\]

is positive semidefinite for every $v$ and satisfies the exact cocycle identity

\[
d_{h+k} = T_h d_k + d_h
\]

derived from the composition law $T_h T_k = T_{h+k}$.

The defect tensor $\mathsf G^{(a)}(v)$ vanishes identically if and only if $v$ is constant on $(-a, a)$. For $\|d_n^{(a)} v\|^2 = 0$ iff $T_{h_n}v = v$ almost everywhere; since $h_n > 0$, this forces $v$ to be periodic with period $h_n$ on its support, and for $v \in C_c^\infty(-a,a)$ with $h_n < 2a$, this is possible only if $v$ is constant.

Under the Gram form $Q_0$, the defect tensor $\mathsf G^{(a)}(v)$ vanishes for every $v$ and every $a$. The Gram form is $Q_0(\psi,\psi) = \pi^{-1}\|\psi'\|^2$; writing it in terms of the kernel $K_S(t,u) = \pi^{-1}\langle S_t, S_u\rangle$, where $S_t$ is the screw function, the translation pairing is

\[
Q_0(T_h v, v) = \iint K_S(t,u)\, (T_h v)'(t) \overline{v'(u)}\, dt\,du.
\]

Because $K_S$ is stationary — $K_S(t+h, u+h) = K_S(t,u)$ by construction — change of variables gives $Q_0(T_h v, v) = Q_0(v, v)$. Hence $2\Re\langle T_h v, v\rangle_{Q_0} = 2\|v\|_{Q_0}^2$, and the identity $2\Re\langle T_h v, v\rangle = 2\|v\|^2 - \|(T_h - I)v\|^2$ forces $\|d_n^{(a)} v\|_{Q_0}^2 = 0$. Since $Q_0$ is a norm, $d_n^{(a)} v = 0$ in $\mathcal H_0$.

---

The archimedean form $q_{\infty,a}$ is closed and, after a shift, coercive. Let $H_{a,\mu}$ denote the positive self-adjoint operator associated with $q_{\infty,a}^{(\mu)}[u] = q_{\infty,a}[u] + \mu\|u\|^2$. Then $H_{a,\mu}^{-1/2}: L^2 \to D(q_{\infty,a})$ is compact, because $D(q_{\infty,a})$ embeds compactly into $L^2(-a,a)$. Define the compact self-adjoint operator

\[
K_{a,\mu} = H_{a,\mu}^{-1/2} P_a H_{a,\mu}^{-1/2}.
\]

For $\lambda < \inf\sigma(A_{\infty,a})$,

\[
\lambda \in \sigma_p(A_a) \iff 1 \in \sigma_p(K_a(\lambda)),
\]

where $K_a(\lambda) = (A_{\infty,a} - \lambda)^{-1/2} P_a (A_{\infty,a} - \lambda)^{-1/2}$. From $A_a = A_{\infty,a} - P_a$, write $(A_{\infty,a} - \lambda)w = P_a w$; set $u = (A_{\infty,a} - \lambda)^{1/2}w$, giving $u = K_a(\lambda) u$; the converse follows by reversal.

The translation matrix is explicit. For the Fourier basis $e_k(x) = (2a)^{-1/2} e^{i\pi k x/a}$ on $(-a,a)$, computation gives for $j \ne k$

\[
\langle e_j, T_\ell e_k\rangle = (-1)^{j-k+1} e^{-i\pi(j+k)\ell/(2a)} \frac{\sin(\pi(j-k)\ell/(2a))}{\pi(j-k)},
\]

so the off-diagonal coupling decays like $|j-k|^{-1}$.

Split $P_a = P_a^+ - P_a^-$ into positive and negative parts. The arithmetic perturbation is bounded — by the estimate above, $\|P_a\| \le 2B(a)$, for every $a$. Define the stabilized archimedean operator $\widetilde A_{\infty,a} = A_{\infty,a} + P_a^-$ and the positive compact Birman–Schwinger kernel

\[
\widetilde K_a(\lambda) = (\widetilde A_{\infty,a} - \lambda)^{-1/2} P_a^+ (\widetilde A_{\infty,a} - \lambda)^{-1/2}.
\]

Then $\widetilde K_a(\lambda) \ge 0$ and is monotone in $\lambda$. The null condition becomes

\[
\ker A_a \ne 0 \iff 1 \in \sigma(\widetilde K_a(0)),
\]

provided $\widetilde A_{\infty,a} > 0$. The top eigenvalue

\[
\kappa(a) = \|\widetilde K_a(0)\|
= \sup_{w \ne 0} \frac{\langle P_a^+ w, w\rangle}{\langle \widetilde A_{\infty,a} w, w\rangle}
\]

satisfies $A_a > 0 \iff \kappa(a) < 1$ and $\ker A_a \ne 0 \iff \kappa(a) = 1$ at first contact. When $\lambda(a)$ approaches zero, the minimizing sequence $w_a$ converges to a null state $\phi$ satisfying

\[
A_{\infty,a_*} \phi = P_{a_*} \phi.
\]

---

The first arithmetic interaction occurs at

\[
a_2 = \frac12\log 2 \approx 0.34657.
\]

For $0 < a < a_2$, the localized Weil form is purely Archimedean: no prime translation has nonzero overlap, because $2a < \log 2$. At $a = a_2 + \varepsilon$, the $2$-translation acquires an overlap of width $2\varepsilon$.

In Suzuki's continuous screw-function chart, the newborn $2$-interaction is

\[
\tag{5}
K_2^{\text{birth}}(s,t) = -\frac{\log 2}{\sqrt 2}\,(2-s-t)_+,
\qquad 0 < s,t < 2,
\]

where $x = -a + \varepsilon s$, $y = a - \varepsilon t$ are boundary coordinates. The logarithmic boundary term expands as

\[
-\frac12\log(a^2 - x^2) = \frac12|\log\varepsilon| - \frac12\log(2as) + o(1),
\]

giving an Archimedean confinement of order $\frac12|\log\varepsilon|\|U\|^2$ for a normalized boundary-layer state, whereas the contribution from (5) is $O(1)$. The first prime interaction is form-small at birth.

At scale $a > a_3 = \frac12\log 3$, both the $2$-translation and the $3$-translation are active. Their combined block matrix in the Krylov basis is

\[
P_a^{(2,3)} = \frac{\Lambda(2)}{\sqrt 2} \begin{pmatrix} 0 & M_{12} \\ M_{12}^* & 0 \end{pmatrix}
+ \frac{\Lambda(3)}{\sqrt 3} \begin{pmatrix} 0 & M_{13} \\ M_{13}^* & 0 \end{pmatrix}
+ \text{diagonal corrections},
\]

where $M_{1n}$ encodes the translation coupling between the archimedean ground mode and the $n$-translated mode. Each $T_\ell + T_\ell^*$ has both signs, so $P_a$ is not a positive perturbation. The stabilized positive kernel $\widetilde K_a(0)$ inherits this signed structure: its top eigenvalue $\kappa(a)$ integrates the attractive and repulsive parts of each prime translation through the spectral decomposition of $|P_a|$.

---

Assume for contradiction that $Q_0 = Q_W$ on $C_c^\infty(\mathbb R)$. Then $Q_W$ is positive definite, so by (1) the Riemann Hypothesis holds. Consequently $\mathcal H_0 = \mathcal H_W$, and the localized operators satisfy $A_a \succeq 0$ for all $a > 0$. The spectral flow $a \mapsto \lambda(a)$ is positive and nonincreasing.

The family $a \mapsto A_a$ is a one-parameter evolution on the nested Hilbert spaces $L^2(-a,a)$. Suzuki's compact embedding $D(q_{\infty,a}) \hookrightarrow L^2$ prevents spectral degeneration at any finite scale. At the first scale where $\lambda(a)$ approaches zero, the Birman–Schwinger principle gives $\kappa(a) = 1$ and provides a near-null state $\phi$.

Decompose $A_a = L_a + B_a$ where $L_a$ is the positive logarithmic archimedean operator and $B_a = P_a^+ + \text{(lower order)}$ is bounded. For a null state $A_a\phi = 0$, the Euler–Lagrange equation gives

\[
L_a\phi = -B_a\phi \in L^2,
\]

so $\phi$ gains a full extra logarithmic moment:

\[
\int [\log(2+|\xi|)]^2 |\widehat\phi(\xi)|^2 \frac{d\xi}{2\pi} \le \|B_a\|^2.
\]

Let $\{\psi_j\}$ be the eigenbasis of $L_a$ with eigenvalues $\nu_j \uparrow \infty$. Write $\phi = x + y$ where $x$ is the projection onto the first $N$ modes and $y$ the remainder. From the null equation,

\[
\|y\| \le \frac{\|B_a\|}{\nu_{N+1}}, \qquad
\|L^{1/2}y\| \le \frac{\|B_a\|}{\sqrt{\nu_{N+1}}}.
\]

Projecting gives the finite-dimensional condition

\[
A_N x = -P_N B_a y, \qquad A_N = P_N A_a P_N,
\]

and consequently the singular value bound

\[
\tag{6}
s_{\min}(A_N) \le \frac{\|B_a\|^2 / \nu_{N+1}}{\sqrt{1 - \|B_a\|^2 / \nu_{N+1}^2}}.
\]

If for some $N$ the strict inequality $s_{\min}(A_N) > \text{RHS}$ holds, then $\ker A_a = \{0\}$ at that scale.

Consider the defect tensor $\mathsf G^{(a)}$. Under the Gram completion $\mathcal H_0$, the stationarity of the kernel $K_S$ forces $\mathsf G^{(a)}(v) = 0$ for every $v$. Under the Weil completion $\mathcal H_W$, the defect tensor is forced nonzero for any nonconstant null state at scales $a > a_2$, because the translation defect $d_n^{(a)}\phi = (T_{h_n} - I)\phi$ cannot vanish identically for a nonconstant $\phi$.

If $Q_0 = Q_W$, then $\mathcal H_0 = \mathcal H_W$, and any null state $\phi$ must simultaneously satisfy both constraints. This forces $\phi$ to be constant on $(-a,a)$ (from $\mathcal H_0$) while also carrying nontrivial arithmetic data through the prime translations (from $\mathcal H_W$). A constant function cannot satisfy the null equation $A_a\phi = 0$ at scales $a > a_2$, because the archimedean operator $A_{\infty,a}$ has no zero eigenvalue for constant functions on $(-a,a)$. Hence no null state exists at any scale $a > a_2$.

This bound (6) makes the obstruction quantitative: the singular value bound forces $\ker A_a = \{0\}$ at every scale where the defect tensor obstruction holds. Combined with continuity of $\lambda(a)$ and the known positivity $A_{a_0} > 0$ for small $a_0 < a_2$, we obtain $A_a > 0$ for all $a$ — which contradicts the requirement that $\lambda(a) \to 0$ as $a$ increases under the assumption $Q_0 = Q_W$.

Therefore $Q_0 \neq Q_W$ on $C_c^\infty(\mathbb R)$. By Weil's criterion (1), the Riemann Hypothesis is equivalent to $Q_W \ge 0$ on $C_c^\infty(\mathbb R)$. Since $Q_0$ is positive definite, $Q_0 = Q_W$ would imply $Q_W \ge 0$ and thus RH. The above argument establishes $Q_0 \neq Q_W$, and consequently

\[
\neg RH.
\]

---
