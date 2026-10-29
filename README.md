# OpenSeesPy Learning Series

A self-directed series I worked through to learn **nonlinear structural analysis in OpenSeesPy**. It runs from a simple elastic truss to a nonlinear reinforced concrete (RC) portal frame. Each step adds one new concept: elements, then sections, then materials, then static, cyclic and dynamic analysis. Each folder also includes **my own verification check** against a hand calculation or ETABS.

> **Author:** Rajesh Bhandari, B.E. Civil Engineering, IOE Pulchowk Campus (2026); Structural Engineer, Miyamoto International Nepal
> **Interests:** Performance-based seismic design, seismic assessment and retrofit of RC and steel structures, earthquake engineering


(<img width="250" height="150" alt="output" src="https://github.com/user-attachments/assets/774f9c5d-a69c-4a7b-a519-8313818da0cb" />
)(<img width="250" height="150" alt="output" src="https://github.com/user-attachments/assets/5e7a410f-045f-4233-8f28-fa4417fd5b10" />
)(<img width="250" height="150" alt="output" src="https://github.com/user-attachments/assets/e26e8381-2621-490a-9852-afa1e91062f9" />
)

----

## Contents

| # | Topic | Analysis type | Key OpenSees features |
|---|-------|---------------|-----------------------|
| 01 | [Basic Elastic Truss Analysis](01.Basic%20Elastic%20Truss%20Analysis/) | Linear static | `truss`, `Elastic` material |
| 02 | [Elastic Portal Frame Analysis](02.Elastic%20Portal%20Frame%20Analysis/) | Gravity + eigenvalue | `elasticBeamColumn`, `eigen` |
| 03 | [Fiber Section of RCC](03.Fiber%20Section%20of%20RCC/) | Section definition | `section Fiber`, `Concrete01/02`, `Steel02` |
| 04 | [Nonlinear Cantilever Column Pushover Analysis](04.Nonlinear%20Cantilever%20Column%20Pushover%20Analysis/) | Nonlinear static | `forceBeamColumn`, P-Delta, `DisplacementControl` |
| 05 | [Nonlinear Cantilever Column Reverse Cyclic Pushover Analysis](05.Nonlinear%20Cantilever%20Column%20Reverse%20Cyclic%20Pushover%20Analysis/) | Reversed cyclic | Cyclic displacement protocol |
| 06 | [Nonlinear Cantilever Column Time History Analysis](06.Nonlinear%20Cantilever%20Column%20Time%20History%20Analysis/) | Nonlinear dynamic | `UniformExcitation`, Rayleigh damping, `Newmark` |

## What I learned

<!-- Write 3–5 honest, specific points in your own words. Examples: -->
- How fiber discretisation and confinement change the moment–curvature response of an RC section.
- Why convergence fails in nonlinear analysis, and how algorithm switching, step size and test tolerance fix it.
- How P-Delta effects reduce post-yield stiffness in a cantilever column.
- How Rayleigh damping assumptions affect peak drift in time-history analysis.


---

## Repository structure

```
openseespy-learning-series/
├── README.md
├── requirements.txt
├── figures/                    
├── 01-elastic-truss/
│   ├── truss.py               # what, key result, verification
│   └── results/
├── 02-elastic-portal-frame/     # gravity + eigenvalue analysis
├── 03-rc-fiber-section/
├── 04-moment-curvature/
├── 05-cantilever-pushover/
├── 06-cantilever-cyclic-pushover/
├── 07-cantilever-time-history/
│   └── ground_motions/          # record source cited in folder README
└── 08-nonlinear-rc-portal-frame/
```

Each folder contains a script, its output plots, and a short README covering:
1. **What is modeled:** geometry, materials and loads.
2. **Key result:** one figure plus one sentence.


---

## How to run


**requirements.txt**
```
openseespy
numpy
matplotlib
pandas
```

**Units:** kN, m, s throughout, unless stated otherwise in a script header.

---

## Next step

This series is the foundation for a full-scale study I am now working on:
**Seismic performance and retrofit assessment of a non-ductile RC frame.** It covers incremental dynamic analysis (IDA), fragility curves, and a comparison of the frame before and after retrofit.

<!-- Add the link once that repo exists -->

---

## References

- McKenna, F., Scott, M. H., & Fenves, G. L. (2010). Nonlinear finite-element analysis software architecture using object composition. *Journal of Computing in Civil Engineering*, 24(1), 95–107.
- Zhu, M., McKenna, F., & Scott, M. H. (2018). OpenSeesPy: Python library for the OpenSees finite element framework. *SoftwareX*, 7, 6–11.
- Mander, J. B., Priestley, M. J. N., & Park, R. (1988). Theoretical stress-strain model for confined concrete. *Journal of Structural Engineering*, 114(8), 1804–1826.
- OpenSeesPy documentation: https://openseespydoc.readthedocs.io

---


*Open to graduate research opportunities in structural and earthquake engineering (Fall 2027).*
