# Mixing Times of Markov Chains

**Candidato / Author:** Giordano Sorrentino
**Relatore / Advisor:** Prof. Alessandra Caraceni
**Università di Pisa** — Dipartimento di Matematica, Laurea Triennale in Matematica, A.A. 2025/2026

📄 **[Read the full thesis (PDF, in Italian)](thesis/tesi.pdf)**

---

## Abstract

This thesis studies the mixing time of finite-state Markov chains — how long it takes for a chain's distribution to become close to its stationary distribution. After introducing Markov chains, stationary distributions, and total variation distance, it presents three central tools for estimating mixing times: **coupling**, **strong stationary times**, and **spectral methods**. It then covers the **cutoff phenomenon**, a sharp transition from far-from-equilibrium to near-equilibrium behavior that many natural chains exhibit.

These tools are applied to two classical shuffles on the symmetric group:

- **Random transpositions** (swap two uniformly random cards each step): a strong stationary time built from a card-coloring procedure gives an upper bound of order `n log n` on the mixing time.
- **Adjacent transpositions** (swap only neighboring cards): following Wilson's approach, spectral methods combined with a lattice-path coupling give a mixing time of order `n³ log n`.

---

## Key results

| Chain | Mixing time | Method | Reference result |
|---|---|---|---|
| Lazy random walk on the cycle `Z_n` | `Θ(n²)` | Coupling + spectral (ℓ² bound) | — |
| Lazy random walk on the hypercube `{0,1}ⁿ` | Cutoff at `½ n log n` | Strong stationary time | — |
| Random transpositions | Cutoff at `½ n log n` | This thesis: strong stationary time, upper bound `5/4 n log n` | Diaconis–Shahshahani (1981) |
| Adjacent transpositions | Cutoff at `1/π² · n³ log n` | This thesis: Wilson's eigenfunction method (lower bound `1/π² n³ log n`) + lattice-path coupling (upper bound `8/π² n³ log n`) | Lacoin (2016) |

### A highlight: finding the gap in Matthews' 1988 proof

Chapter 5 doesn't just apply known techniques — it works through **Broder's** (1985) and **Matthews'** (1988) strong-stationary-time constructions for the random transposition shuffle, and shows explicitly, with a worked example on `S₄`, why Matthews' argument for achieving the optimal `½ n log n` bound is flawed (following a subtlety first identified in Graham White's 2017 PhD thesis). The thesis then salvages what can be kept from the construction, obtaining a corrected upper bound of `5/4 n log n`.

---

## Table of contents

1. **Preliminaries** — Markov chains, random walks on groups, conditional expectation, ℓᵖ norms
2. **Introduction to mixing** — total variation distance, mixing time, coupling, the `d̄` distance and submultiplicativity
3. **Techniques** — coupling, strong stationary times, spectral methods, Wilson's method for lower bounds
4. **The cutoff phenomenon**
5. **Random transpositions** — Broder's and Matthews' constructions, the error in Matthews' proof, limit profile
6. **Adjacent transpositions** — lattice paths and Wilson's method

## Main techniques

- **Coupling** — building two copies of a chain from different starting points and bounding the time until they meet.
- **Strong stationary times** — random stopping times at which the chain is exactly stationary, independent of the stopping time itself.
- **Spectral methods** — relating the mixing time to the eigenvalues/eigenfunctions of the transition matrix (relaxation time, ℓ² bounds).
- **Wilson's method** — using an eigenfunction to get matching lower bounds, and reducing adjacent-transposition mixing to coalescence of extremal lattice paths.

## Selected references

- Diaconis, P. & Shahshahani, M. (1981). *Generating a random permutation with random transpositions.*
- Aldous, D. (1983). *Random walks on finite groups and rapidly mixing Markov chains.*
- Wilson, D. B. (2004). *Mixing times of lozenge tiling and card shuffling Markov chains.*
- Lacoin, H. (2016). *Mixing time and cutoff for the adjacent transposition shuffle and the simple exclusion.*
- Levin, D. A. & Peres, Y. (2017). *Markov Chains and Mixing Times*, 2nd ed. (main textbook reference)

Full bibliography in the thesis.

## Repository structure

```
.
├── thesis/
│   └── tesi.pdf        # full thesis (Italian)
└── README.md
```

## License

Thesis text: © Giordano Sorrentino. Shared for portfolio/review purposes.
