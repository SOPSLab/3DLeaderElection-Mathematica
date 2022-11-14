# 3DLeaderElection-Mathematica

This repository contains all Mathematica code used to generate the figures and verify the proofs in "Asynchronous Deterministic Leader Election in Three-Dimensional Programmable Matter" by Joseph L. Briones, Tishya Chhabra, Joshua J. Daymude, and Andréa W. Richa.
This paper will be published at ICDCN 2023 and is available on [arXiv](https://arxiv.org/abs/2205.15412).

All code for figure generation can be found in `figures.nb`.
The proofs of the safety and progress lemmas can be found in `safety.nb` and `progress.nb`, respectively.

The key invariant to be checked computationally for the safety lemma is that no configuration of an amoebot's at most five neighbors has a corresponding closed union of rhombic dodecahedrons containing a topological hole.
In `safety.nb`, we verify this by exhaustively enumerating all subsets of at most five neighbors, creating their corresponding unions of rhombic dodecahedrons, and verifying that the genus of the structure is always zero.
This enumeration is visualized in [this video](https://www.youtube-nocookie.com/embed/HlLYpJ79n8M).

The key invariant to be checked computationally for the progress lemma is that, for certain classes of polyhedra, any vertex of the polyhedron with a strictly positive external angle corresponds to a node in our amoebot system with at most five neighbors.
In `progress.nb`, we verify this statement by showing that any node in an amoebot system with at least six neighbors corresponds to a vertex in the associated polyhedron with a nonpositive external angle.
This enumeration is visualized in [this video](https://www.youtube-nocookie.com/embed/Tjj3X8Y_zPQ).
