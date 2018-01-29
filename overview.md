# Overviews

## <a id="3torsion">3-torsion and conductor of genus 2 curves</a> ([arXiv](https://arxiv.org/abs/1706.06162))

Given a curve defined over the rational numbers (or a number field), its (global) conductor is an integer measuring its "arithmetic complexity". It is a local quantity, meaning that its p-part (the "local conductor exponent") is a function of the curve over the field of p-adic numbers. For odd p, the p-part of the conductor is well-understood and computable. The 2-part however is more difficult: the previous best algorithm for computing this relies on the conjectural functional equation of the L-function of the curve, and as such it does not yield proven results. Furthermore, it uses global arithmetic, and so its run time is quadratic in the conductor, and so is only practical for small conductor.

We give an algorithm to compute the conductor for curves of genus 2. It is based on the analysis of 3-torsion of the Jacobian for genus 2 curves over 2-adic fields. In particular, the algorithm yields proven results. Furthermore, it mainly works 2-adically and so its run-time does not depend strongly on the global conductor.

An implementation is available [here](https://cjdoris.github.io/Genus2Conductor). It has been used to verify the conductors of most genus 2 curves in the [LMFDB](http://www.lmfdb.org/Genus2Curve/Q).
