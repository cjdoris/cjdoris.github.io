# Overviews

<h2 id="exactpadics">ExactpAdics: An exact representation of p-adic numbers (<a href="https://arxiv.org/abs/1805.09794">arXiv</a>)</h2>

To date, the only highly-featured implementations of p-adic numbers are in Sage and Magma, and in both cases they are represented inexactly as a residue class, like `1 + O(2^10)`, which is the p-adic analogue of a real number being represented in floating-point arithmetic as `1.0000000000`. Since they work to a fixed finite precision, which must be decided in advance by the user, precision errors can occur. When this happens, the user must manually increase the initial precision and try again. This is also inefficient because some computations do not require a high precision. In Magma at least, it is not always clear whether `1 + O(2^10)` is really representing a p-adic number or the residue class itself, the distinction being important because some operations, such as polynomial factorization, depend on the interpretation.

We describe two new packages `ExactpAdics` and `ExactpAdics2` for the Magma computer algebra system for working with p-adic numbers exactly, in the sense that numbers are represented lazily to infinite p-adic precision. This has the benefits of increasing user-friendliness and speeding up some computations, as well as forcibly producing provable results. The two packages use different methods for lazy evaluation, which we describe and compare in detail. The intention is that this article will be of benefit to anyone wanting to implement similar functionality in other languages.

We currently recomment the typical user to use `ExactpAdics2`, which is available [here](https://cjdoris.github.io/ExactpAdics2). The original `ExactpAdics`, which is typically slower but could be faster in some applications, is available [here](https://cjdoris.github.io/ExactpAdics).

<h2 id="extensions">On enumerating extensions of p-adic fields with given invariants (<a href="https://arxiv.org/abs/1803.08023">arXiv</a>)</h2>

A well-known invariant of a Galois extension of p-adic fields is its Galois group, and the ramification filtration of the Galois group. For non-Galois extensions, replacing the Galois group by the *Galois set* of embeddings into a normal closure, this Galois set still has a filtration which obeys the "Galois correspondence".

Some information about the ramification filtration is encoded in the *ramification polygon* of the extension, defined to be the Newton polygon of a certain *ramification polynomial*. More information is encoded in the leading p-adic digits of the coefficients of the ramification polynomial, and these also form an invariant, up to some equivalence relation.

This theory was recently used by Pauli and Sinclair in order to efficiently generate sets of defining polynomials for all extensions of a p-adic field of a given degree. This article is a re-exposition of the same results, containing little new content but with shorter and possibly more enlightening proofs. We supplement this with an algorithm to produce all ramification polygons of a given degree, and hence we can produce all totally ramified extensions of a given degree.

An implementation of these invariants is available [here](https://cjdoris.github.io/pAdicExtensions).

<h2 id="3torsion">3-torsion and conductor of genus 2 curves (<a href="https://arxiv.org/abs/1706.06162">arXiv</a>)</h2>

Given a curve defined over the rational numbers (or a number field), its (global) conductor is an integer measuring its "arithmetic complexity". It is a local quantity, meaning that its p-part (the "local conductor exponent") is a function of the curve over the field of p-adic numbers. For odd p, the p-part of the conductor is well-understood and computable. The 2-part however is more difficult: the previous best algorithm for computing this relies on the conjectural functional equation of the L-function of the curve, and as such it does not yield proven results. Furthermore, it uses global arithmetic, and so its run time is quadratic in the conductor, and so is only practical for small conductor.

We give an algorithm to compute the conductor for curves of genus 2. It is based on the analysis of 3-torsion of the Jacobian for genus 2 curves over 2-adic fields. In particular, the algorithm yields proven results. Furthermore, it mainly works 2-adically and so its run-time does not depend strongly on the global conductor.

An implementation is available [here](https://cjdoris.github.io/Genus2Conductor). It has been used to verify the conductors of most genus 2 curves in the [LMFDB](http://www.lmfdb.org/Genus2Curve/Q).

<div style="margin-top:30px; text-align:right;"><a style="color: grey; font-size: small;" href="https://github.com/cjdoris/cjdoris.github.io/edit/master/overview.md">edit me</a></div>
