# Support Vector Machine Lab

An interactive study guide for §17.3–17.3.4 of Kevin P. Murphy, *Probabilistic Machine Learning: An Introduction*
(large margin classifiers, the dual problem, soft margin classifiers, and the kernel trick).

**Live:** https://isaackrallison.github.io/support-vector-machines/

Every section has an **Explain it** box at four levels (Kid, High school, Undergrad, Grad / MLE), switchable globally from the top bar.

- **17.3.1 Large margin classifiers:** turn and slide your own line, see its margin band, and compare against the max-margin solution. Click a point for the geometry of Fig. 17.13(a): x⊥, r = f(x)/‖w‖ and the normal w. A scale slider shows why ‖w‖ can be fixed so the closest point has ỹf = 1 (Eqs. 17.63–17.68). A feature-scaling panel reproduces Fig. 17.14.
- **17.3.2 The dual problem:** step through SMO one pair of multipliers at a time. Bars for every αₙ, the dual objective climbing to the primal optimum, ŵ = Σ αₙỹₙxₙ written out, ŵ₀ averaged over support vectors, and a live KKT table (Eqs. 17.69–17.82).
- **17.3.3 Soft margin classifiers:** a log-scale C slider with slack segments, solid rings for on-margin points (0 < α < C) and dashed rings for α = C, Σξ vs. misclassified count, the ν-SVM bracket, and street width and #SV along the regularization path (Eqs. 17.83–17.92).
- **17.3.4 The kernel trick** (the deepest section):
  - A playground with linear, polynomial and RBF kernels on rings, moons, XOR and blobs. Click to add points, drag them, and hover for Eq. 17.93 term by term.
  - A slice view that splits f(x) into one bump αₙỹₙK(xₙ, x) per support vector, plus ŵ₀.
  - A 3 × 4 grid of RBF SVMs over length scale ℓ and C, with SV counts. Click a tile to load it.
  - A lift from x to (x, x²) that shows where curved boundaries come from, with φ(a)ᵀφ(b) = K(a, b) checked on picked points.
  - An explicit-features vs. kernel panel: a numeric check of the 6 features of (xᵀx′ + 1)², and C(D+d, d) feature counts against the O(D) cost of the kernel.
  - A string-kernel SVM that classifies typed words as English or Spanish from shared bigrams (the book's "structured objects").
  - An aside previewing Fig. 17.15 (SVM score vs. true log-odds).
  - Math: a table of every place a dot product becomes K, why a PSD kernel keeps the dual convex, and the polynomial kernel expanded.
- Step-by-step math for Eqs. 17.63–17.94, a 32-question quiz tagged by level, and a cheat sheet.

Single self-contained `index.html`, no build step. Loads Google Fonts and MathJax from cdnjs. All data are synthetic and generated in the page from fixed seeds. The SVMs are trained live in the browser with SMO.
