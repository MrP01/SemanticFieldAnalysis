# Semantic Field Analysis

A Special Topic in Networks on how to use Graph Clustering algorithms to perform semantic field tagging.

The report is available [here](https://raw.githubusercontent.com/MrP01/SemanticFieldAnalysis/master/report/report.pdf)!

In this report, we have introduced a few basic notions of network theory, discussed in
detail two graph clustering approaches, the Louvain method (cf. Section 2.1), where
we rederived the gain in modularity upon clustering of an isolated vertex, and Chinese
Whispers (cf. Section 2.2). These methods make significant progress in a problem
that is usually NP-hard. Using a neighbourhood-based approach with parameter r, we
constructed large networks G4, G8 and G12 from an original classicist Latin literature
corpus and applied the abovementioned methods to cluster them. The constructed
graphs’ vertices only represent principal words, so the text corpus was analyzed up to
grammatical equivalences in the Latin language which is entirely original.

We then analyzed three clustering methods from a computational perspective with
results presented in Table 2, Table 4 and visualised in Figure 5. The Louvain method
was by far the fastest algorithm for our application. The eigengap of the spectrum of
the Laplacian then yielded a good estimate for the expected number of clusters.

As the author describes in Biemann 2006, Chinese Whispers generally produces a fairly
high number of clusters as compared to other methods, which one may circumvent
by adjusting either the convergence condition or introduce a minimum cluster size
through minor adjustments of the algorithm. Similar measures may be taken for
the other algorithms. In our case however, the clusters produced make a reasonable
impression when looking at the words contained therein.

Even better results for the semantic fields could be achieved by incorporating an even
larger text corpus to prevent clustering of words which are only used once or twice, so
only in the context given by the literature.
17 / 19
