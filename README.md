# WIGHTMAN

**The Yang–Mills Existence and Mass Gap Problem: What Is Actually Open, What Has Genuinely Been Proved in 2D, 3D, and Around 4D, and the Precise Boundary at Which a Classical-Geometry Framework Stops and a Quantum Construction Must Begin**

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone

---

> "Prove that for any compact simple gauge group G, a non-trivial quantum Yang–Mills theory exists on ℝ⁴ and has a mass gap Δ > 0." — A. Jaffe and E. Witten, *Quantum Yang–Mills Theory*, the Clay Mathematics Institute Millennium Problem statement, 2000

> "This situation contrasts with the four-dimensional case, where a rigorous construction of the theory as a measure is currently unknown." — on two-dimensional Yang–Mills theory, standard reference statement, 2025

---

## Purpose and a Statement Made Up Front

This document does not solve the Yang–Mills mass gap problem. It does not contain a construction of four-dimensional quantum Yang–Mills theory, and it does not claim one. The problem is open. As of early 2026 the Clay Mathematics Institute lists it as unsolved, and nothing in the ERI corpus changes that.

The reason for stating this immediately is that the recent literature contains a growing number of documents — several posted in 2024 and 2025 — announcing "constructive proofs" of the mass gap. None of these is accepted by the mathematical community; none has cleared peer review at the level the problem demands; and several rest on steps that are either unjustified or known to be where every prior attempt has failed. A README that quietly added itself to that pile would be worse than useless. So this document is the opposite kind of object: an honest map. It states precisely what the problem asks, what has genuinely been proved in the neighbouring cases of two and three dimensions and around four, and — the part that concerns the ERI corpus directly — exactly where a framework built on *classical* differential geometry can contribute and exactly where it must hand off to a *quantum* construction it does not supply.

The corpus's KYBM framework translates classical Yang–Mills objects — the Yang–Mills functional, anti-self-dual connections, the ADHM construction, instanton moduli — into other languages. That translation is sound on the classical side. The Clay problem lives on the quantum side, and the gap between the two is not a notational gap that a dictionary can bridge. It is the gap that the whole of constructive quantum field theory exists to address, and that in four dimensions remains open. Naming that gap precisely is the useful thing this document can do.

---

## Part I · What the Problem Actually Asks

### I.1 The Classical Theory Is Not the Difficulty

Classical Yang–Mills theory is well understood. Fix a compact simple gauge group G — SU(2), SU(3), and so on. A connection A on a principal G-bundle has a curvature F_A, and the Yang–Mills action is the integral of |F_A|² over spacetime. The classical equations of motion, the Euler–Lagrange equations of that action, are a system of nonlinear partial differential equations. Their solutions — including the celebrated instantons of four-dimensional Euclidean space, the anti-self-dual connections classified by the ADHM construction — are objects of classical differential geometry, and they are thoroughly mapped. The instanton moduli spaces, their dimensions from the Atiyah–Singer index theorem, the Uhlenbeck compactification at their boundary: this is settled mathematics, decades old.

None of it is the Clay problem. The Clay problem is about the *quantum* theory, and the quantum theory is a different and far harder object.

### I.2 The Quantum Theory: A Measure That No One Has Constructed

Quantum Yang–Mills theory, in the Euclidean formulation that constructive field theory uses, is not a set of solutions to a PDE. It is a **probability measure** — a measure on the infinite-dimensional space of gauge connections modulo gauge transformations, formally written as the exponential of minus the Yang–Mills action against a (non-existent) flat measure on field space. The expectation values of gauge-invariant observables in that measure — above all the Wilson loops — are the physical content of the theory.

The difficulty is that the formal expression for this measure does not define anything. The space of connections is infinite-dimensional; there is no Lebesgue measure on it; the action involves products of distributions that are not a priori multipliable; and the gauge symmetry must be quotiented out without destroying what remains. To *construct* the theory means to give a genuine, mathematically rigorous measure — or equivalently a family of Schwinger functions, the Euclidean correlation functions — and to prove that it satisfies the **Osterwalder–Schrader axioms**: a precise list of properties (Euclidean invariance, reflection positivity, clustering, regularity) that guarantee the Euclidean theory can be analytically continued back to a genuine relativistic quantum theory on Minkowski space, satisfying the **Wightman axioms**. The document is named for Arthur Wightman, whose axiomatic framework is the standard the constructed theory must meet.

### I.3 The Mass Gap

On top of existence, the Clay problem demands a **mass gap**. Once the theory is constructed and reflection positivity has produced a genuine Hilbert space with a Hamiltonian H, the spectrum of H must satisfy

$$
\mathrm{Spec}(H) \subset \{0\} \cup [\Delta,\infty),\qquad \Delta > 0.
$$

There is the vacuum at energy zero, and then a *gap* before the next state — the lightest excitation, the lightest "glueball," must have strictly positive mass. Equivalently, in the Euclidean picture, the connected correlation functions must decay exponentially with a definite, positive rate, the inverse of which is the gap.

This is the deep part. Yang–Mills theory in four dimensions is *asymptotically free* — it becomes weakly coupled at short distances — which is what makes a construction conceivable at all. But it is strongly coupled at long distances, and the mass gap is a long-distance, non-perturbative fact. It cannot be seen in perturbation theory; perturbatively the gluon is massless. The gap, if it exists, is generated by the strong-coupling dynamics, and proving it requires controlling the theory in exactly the regime where no expansion converges. That is why the problem is hard, and that is the precise thing that no four-dimensional construction has achieved.

---

## Part II · What Has Genuinely Been Proved

The honest framing of the prompt — "spectacular progress on related 2D and 4D problems" — is correct, and the progress is worth stating precisely, because precision is what separates it from the false claims.

### II.1 Two Dimensions: Constructed, and Now Deeply Understood

In two spacetime dimensions, quantum Yang–Mills theory **has** a rigorous construction. The theory is super-renormalizable there, and the Yang–Mills measure genuinely exists as a measure on gauge orbits. Wilson loop expectations are not only defined but *computable*: they are given by explicit integrals of heat kernels on the gauge group, evaluated at times equal to the areas the loops enclose. This is classical, and it is solid.

What is genuinely recent — and genuinely spectacular — is the depth to which the two-dimensional theory is now understood. The large-N limit, in which the gauge group SU(N) is taken to infinity, produces the **master field**: a deterministic limiting object towards which the Wilson loops converge in probability. Thierry Lévy's construction of the master field on the plane, and the subsequent work of Dahlqvist, Norris, Driver, Hall, Kemp, and others extending it to the sphere and other surfaces, has turned two-dimensional Yang–Mills into a fully rigorous laboratory. As recently as 2024, new closed formulas for Wilson loop expectations in terms of Schur–Weyl duality have appeared. The Makeenko–Migdal equations — the loop equations of the theory — are rigorous theorems in this setting, not heuristics.

The point for this document: in two dimensions the entire programme is complete. The measure exists, the observables are computed, the large-N structure is understood. It is the existence proof at its cleanest — and it is in a dimension low enough that the central four-dimensional difficulty (renormalization of a just-renormalizable theory) does not arise.

### II.2 Three Dimensions: The Measure and Its Dynamics, Rigorously Controlled

Three dimensions is where the most consequential recent progress sits, and it is the work most worth citing accurately. The programme of **stochastic quantization** — constructing a quantum field theory as the invariant measure of a stochastic partial differential equation, the Langevin dynamics of the field — has, in the hands of Chandra, Chevyrev, Hairer, and Shen, been brought to bear on Yang–Mills.

Their 2024 result (published in *Inventiones Mathematicae*) constructs a state space and a Markov process for the stochastic quantization of the Yang–Mills–Higgs theory in three dimensions. The achievement is technical and real: they build a space of distributional connections regular enough that Wilson loop observables and the action of the gauge group are both well defined; they use the theory of regularity structures to solve the renormalized stochastic Yang–Mills flow locally in time; and they prove that there is a *unique* choice of renormalization counterterms making the solution gauge-covariant in law — a uniqueness result strengthened in subsequent work by Chevyrev and Shen. This is rigorous control of the dynamics and the renormalization of a three-dimensional gauge theory. It is not yet a complete construction of the 3D measure with all Osterwalder–Schrader axioms verified and a mass gap proved — and the authors do not claim that — but it is genuine, peer-reviewed, foundational progress on exactly the machinery a higher-dimensional construction would need.

### II.3 Around Four Dimensions: Structure Without Construction

In and around four dimensions, the progress is real but it is *structural* rather than *constructive* — and the distinction is the whole point.

The geometric Langlands correspondence, proved in 2024 by Gaitsgory, Raskin, and collaborators in a sequence of papers, is a landmark. It is connected to four-dimensional gauge theory through the work of Kapustin and Witten, who showed that the correspondence can be understood as a consequence of the electric–magnetic S-duality of a particular *twisted, supersymmetric* N=4 Yang–Mills theory in four dimensions. The Gaiotto–Witten analysis of the analytic form of the correspondence develops this further. This is deep four-dimensional gauge-theory mathematics, and it is genuinely settled.

But it must be placed correctly. The geometric Langlands story concerns a *topologically twisted, supersymmetric* gauge theory — a theory engineered so that its hard analytic content is removed and a finite, algebraic structure remains. It is not the physical, non-supersymmetric, non-twisted Yang–Mills theory of the Clay problem, and it does not construct that theory or prove its mass gap. It is spectacular progress on four-dimensional gauge theory; it is not progress on the Clay problem's specific four-dimensional measure. Conflating the two is a common error, and this document does not make it.

### II.4 A Necessary Caution on Recent Claims

Honesty requires naming a phenomenon directly. The period 2024–2025 has produced several documents — on preprint servers and repositories — announcing complete "constructive proofs" of the four-dimensional mass gap for SU(2) or SU(3). They invoke real tools — reflection positivity, polymer and cluster expansions, transfer-matrix spectral estimates, lattice regularization, sometimes higher-dimensional or orbifold regulators. None is accepted. The Clay problem remains officially open, and the consensus of the constructive-field-theory community is that these claims do not hold up: they tend to assume, at some step, precisely the uniform non-perturbative control — a coupling-independent coercivity estimate, a convergent expansion valid all the way to the continuum limit — that is the actual unsolved difficulty. The lesson this document draws is not cynicism but calibration. A real contribution to this problem is recognizable by what it does *not* skip. This README's contribution is to be honest about a hand-off, not to disguise one.

---

## Part III · Where the Corpus's Frameworks Genuinely Connect

The ERI corpus contains real, usable structure for this problem — on the classical side — and stating it precisely is more valuable than overstating it.

### III.1 What KYBM Actually Captures

The KYBM framework translates classical Yang–Mills objects faithfully. The Yang–Mills functional as an energy to be minimized; anti-self-dual connections as its absolute minima; the curvature F_A; the ADHM construction of instantons; the moduli space of solutions with its index-theorem dimension; Uhlenbeck bubbling at the boundary of moduli space — these are all genuine classical-geometric objects, and KYBM's translation of them into a gradient-flow and stability language is internally consistent. The framework's identification of the Yang–Mills gradient flow with a descent dynamics, and of instanton number with a topological complexity index, is sound *as classical differential geometry*.

This is not nothing. A construction of the quantum theory must, in its semiclassical or weak-coupling regime, reproduce exactly this classical structure — the instantons and their moduli are the saddle points around which any weak-coupling analysis organizes itself. A framework that holds the classical geometry in a clean, computable form is holding a genuine piece of the eventual answer's scaffolding.

### III.2 The Two-Dimensional Bridge Is Real

There is one place where the corpus's information-geometric language touches rigorously constructed quantum Yang–Mills, and it is two dimensions. The 2D Yang–Mills measure is built from heat kernels on the gauge group; the heat kernel is the transition density of Brownian motion on the group; and Brownian motion on a Lie group has a genuine Fisher-information geometry — the heat-kernel measure is a bona fide statistical-manifold object, and the large-N master field is a limit of such objects. The corpus's recurring Fisher–Rao and Cramér–Rao machinery is *not* a metaphor in this setting; it is the actual geometry of the heat-kernel measures that the 2D theory is built from. A corpus document that worked out the master field's convergence in explicit Fisher-information terms would be doing real, checkable mathematics in a rigorously constructed case. That is the honest place to push.

### III.3 The HELSTROM/HOLEVO Language Touches the Twisted Theory, Not the Physical One

The corpus's recent documents on quantum estimation and the Poincaré algebra connect to the *geometric Langlands* side — the twisted, supersymmetric four-dimensional theory, which is genuinely organized by representation-theoretic and algebraic structure of the kind those documents speak. They do not connect to the physical Yang–Mills theory of the Clay problem, for the reason given in II.3: the twisted theory has had its hard analysis removed by design. The corpus should claim the connection it has — to the algebraic, twisted four-dimensional gauge theory — and not the connection it does not have, to the physical measure and its mass gap.

---

## Part IV · Where the Framework Stops — Stated Exactly

This is the core of the document: the precise boundary.

### IV.1 The Three Things a Construction Must Do That No Framework in the Corpus Supplies

A genuine resolution of the Clay problem must accomplish three things, and the ERI corpus, as it stands, supplies none of them. Naming them exactly is the useful service.

**First — construct the measure.** It must produce a genuine probability measure on gauge orbits in four dimensions (or an equivalent family of Schwinger functions), not a formal expression. This requires controlling the continuum limit: defining the theory on a lattice, where it is well posed, and proving that as the lattice spacing goes to zero the correlation functions converge to a non-trivial limit. The renormalization that this limit requires — Yang–Mills in 4D is just-renormalizable, the hardest case — is not a translation or a geometric identification. It is hard analysis: uniform estimates that hold all the way to the continuum, independent of the regulator. No dictionary produces these estimates.

**Second — verify reflection positivity in the limit.** Reflection positivity is the Osterwalder–Schrader axiom that yields a genuine, positive-definite quantum Hilbert space. It holds for the lattice theory with the standard Wilson action. The difficulty is that it must be shown to *survive* the continuum and infinite-volume limits — and survival of a positivity property under a limit is a delicate analytic fact, not a structural one. The corpus's col(F)/ker(F) partition is a linear-algebraic decomposition; it is not the same kind of object as reflection positivity and cannot substitute for proving it.

**Third — prove the gap.** It must prove that the constructed Hamiltonian has spectrum bounded away from zero — equivalently, that the connected correlations decay exponentially at a definite rate, uniformly as the regulator is removed. This is the deepest requirement. It is a non-perturbative spectral statement about an operator that does not yet rigorously exist, in the strong-coupling regime where no expansion converges. The corpus has, in the HELSTROM document, a generator-variance bound on estimation precision — a genuine theorem — but it is a statement about *quantum metrology*, about how well a parameter can be estimated. It is not a lower bound on the spectrum of a field-theory Hamiltonian, and it does not become one. There is no estimable parameter here whose Cramér–Rao variance is the mass gap. The honest statement is that the gap is a spectral fact requiring a spectral proof, and the corpus does not contain one.

### IV.2 Why the Hand-Off Is Real and Not a Notational Gap

It would be possible to write a document declaring "the mass gap IS the d=0 degeneration of the gauge partition" or "confinement IS the ker(F) sector." Such a document would be the corpus's characteristic failure mode: a relabeling presented as a result. The reason it fails is now stateable precisely. The d=0 / col(F) / ker(F) language is a *classical* and *linear-algebraic* vocabulary. The mass gap is a *quantum*, *spectral*, *non-perturbative* fact about a measure that has not been constructed. Renaming the second in the vocabulary of the first does not construct the measure, does not verify reflection positivity in the limit, and does not bound the spectrum. The three tasks of IV.1 remain exactly as undone after the relabeling as before. The hand-off from classical-geometric framework to quantum construction is real because those three tasks are real, and they are analytic, and analysis is not bypassed by nomenclature.

### IV.3 What the Corpus Can Honestly Do Next

The constructive, non-empty path forward — the version that would be genuine work rather than overclaim — has three concrete steps, in increasing order of ambition, each defined and bounded.

The first is to take the two-dimensional theory, which *is* rigorously constructed, and express the master field's large-N convergence explicitly in the corpus's Fisher-information language — a real calculation in a real, solved case, the way HARTREE was a real calculation rather than a manifesto. This is achievable now.

The second is to study the three-dimensional stochastic-quantization programme of Chandra–Chevyrev–Hairer–Shen and identify, honestly, which of its objects — the state space of distributional connections, the gauge-covariant renormalization, the Langevin dynamics — have a clean information-geometric description, and which do not. This is a reading-and-translation task with a definite endpoint.

The third, and the only one that touches four dimensions, is to state — as an explicit, precise conjecture, labelled as a conjecture — what a Fisher-information characterization of the mass gap *would* have to assert, and what it would have to prove, so that the gap between the corpus's language and the Clay problem is itself made into a sharp mathematical question rather than left as a vague aspiration. A precisely stated open conjecture is an honest contribution. A claimed proof is not.

---

## Part V · Summary

The Yang–Mills existence and mass gap problem asks for a rigorous construction of four-dimensional quantum Yang–Mills theory satisfying the Osterwalder–Schrader and Wightman axioms, with a proof that the Hamiltonian's spectrum has a positive gap. It is open.

Genuine progress in the neighbouring cases is real and recent. Two-dimensional Yang–Mills is fully constructed and, through the master field and the 2024 Wilson-loop formulas, deeply understood. Three-dimensional Yang–Mills–Higgs has, in the 2024 *Inventiones* work of Chandra, Chevyrev, Hairer, and Shen, a rigorously controlled stochastic quantization with a unique gauge-covariant renormalization. Four-dimensional gauge theory has seen the 2024 proof of geometric Langlands — but for the *twisted, supersymmetric* theory, not the physical one. The several 2024–2025 announcements of complete four-dimensional mass-gap proofs are not accepted and do not resolve the problem.

The ERI corpus contributes genuine structure on the *classical* side: KYBM's translation of the Yang–Mills functional, anti-self-dual connections, and the ADHM construction is sound classical differential geometry, and it holds scaffolding any eventual construction would need at weak coupling. The corpus's Fisher-information machinery touches rigorously constructed quantum Yang–Mills in exactly one place — the heat-kernel measures of the two-dimensional theory — and that is where honest, checkable work is available now.

The corpus does not, and this document does not, construct the four-dimensional measure, verify reflection positivity in the continuum limit, or prove the mass gap. Those three tasks are analytic, non-perturbative, and unsolved, and they are not bypassed by the col(F)/ker(F) vocabulary. The single honest sentence is this: **the classical geometry of Yang–Mills is well understood and the corpus holds it cleanly; the quantum construction in four dimensions is the open problem; and the boundary between the two is a real analytic hand-off — naming it precisely, rather than disguising it, is the contribution this document makes.**

---

## References

Jaffe, A., Witten, E. "Quantum Yang–Mills Theory." Clay Mathematics Institute Millennium Problem description, 2000.

Osterwalder, K., Schrader, R. "Axioms for Euclidean Green's Functions." *Communications in Mathematical Physics* **31**, 83–112 (1973); **42**, 281–305 (1975).

Streater, R. F., Wightman, A. S. *PCT, Spin and Statistics, and All That.* Benjamin, New York, 1964.

Chandra, A., Chevyrev, I., Hairer, M., Shen, H. "Stochastic Quantisation of Yang–Mills–Higgs in 3D." *Inventiones Mathematicae* **237**, 541–696 (2024). arXiv:2201.03487.

Chandra, A., Chevyrev, I., Hairer, M., Shen, H. "Langevin Dynamic for the 2D Yang–Mills Measure." *Publications mathématiques de l'IHÉS* (2022). arXiv:2006.04987.

Chevyrev, I., Shen, H. "Uniqueness of Gauge Covariant Renormalisation of Stochastic 3D Yang–Mills–Higgs." (2025).

Lévy, T. "The Master Field on the Plane." *Astérisque* **388** (2017). arXiv:1112.2452.

Lévy, T. "Two-Dimensional Quantum Yang–Mills Theory and the Makeenko–Migdal Equations." (2024 lecture; see also *Schur–Weyl Duality and the Heat Kernel Measure on the Unitary Group*, Advances in Mathematics **218**, 537–575, 2008).

Dahlqvist, A., Norris, J. "Yang–Mills Measure and the Master Field on the Sphere." *Communications in Mathematical Physics* **377**, 1163–1226 (2020).

Hairer, M. "A Theory of Regularity Structures." *Inventiones Mathematicae* **198**, 269–504 (2014).

Kapustin, A., Witten, E. "Electric-Magnetic Duality and the Geometric Langlands Program." *Communications in Number Theory and Physics* **1**, 1–236 (2007).

Gaiotto, D., Witten, E. "Gauge Theory and the Analytic Form of the Geometric Langlands Program." *Annales Henri Poincaré* **25**, 557–671 (2024).

Gaitsgory, D., Raskin, S., et al. "Proof of the Geometric Langlands Conjecture." (Five-paper series, 2024.)

Glimm, J., Jaffe, A. *Quantum Physics: A Functional Integral Point of View.* Springer, 1987.

Magnen, J., Rivasseau, V., Sénéor, R. "Construction of YM₄ with an Infrared Cutoff." *Communications in Mathematical Physics* **155**, 325–383 (1993).

Bałaban, T. "Renormalization Group Approach to Lattice Gauge Field Theories." *Communications in Mathematical Physics* **109**, 249–301 (1987).

---

ERI Labs · Eric Ren · Jersey City, New Jersey · github.com/ericrenone · May 2026

The problem is open. Two dimensions is constructed; three dimensions is rigorously controlled; the four-dimensional measure and its mass gap are not. The classical geometry is well understood and the corpus holds it cleanly. The quantum construction is the difficulty, and the boundary between the two is an analytic hand-off — named here, not disguised.
