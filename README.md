# Semantic Field Analysis

A Special Topic in Networks on how to use Graph Clustering algorithms to perform semantic field tagging.  
The report is available [here](https://raw.githubusercontent.com/MrP01/SemanticFieldAnalysis/master/report/report.pdf)!

Here are some of the resulting semantic fields:

- conterritus (frightened), minitabundus (threatening), infensus (hostile), properus (quick)
- hibernus (wintry), tardus (slow), upilio (shepherd), formosus (beautiful), hibernum (winter camp (pl.)), subulcus (swineherd)
- fraus (deceit), fraus (fraud), infitiatio (denial), furtum (theft)
- fraxinus (ash-tree), laurea (laurel/bay tree), fraxinus (of ash), corylus (hazel-tree), edurus (very hard), abies (fir tree/wood)
- vicina (neighbor), vicinus (nearby), vicinus (neighbor), vicinum (neighborhood)
- repens (sudden), susurro (whisperer), nutrix (nurse), susurrus (whispering), immanitas (brutality), susurrus (whisper), diritas (frightfulness)
- Aegyptius (Egyptian), Aethiopia (Ethiopia), siccitas (dryness), Aegyptus (Egypt), desertum (desert), Aegyptius (Egyptian), aspis (asp), Arabia (Arabia)
- Marius (Marius), Maria (Mary), caelia (kind of beer), citrum (wood of citron tree), alternatus (alternate), citrus (African citrus tree), series (row), citrus (lemon tree)
- inexspectatus (invincible), armum (arms (pl.)), tribunicius (of/belonging to tribune), intutus (defenseless), Arma (Arms), arma (weapons)
- globosus (round), rotundus (round)

In this report, we have introduced a few basic notions of network theory, discussed in
detail two graph clustering approaches, the Louvain method (cf. Section 2.1), where
we rederived the gain in modularity upon clustering of an isolated vertex, and Chinese
Whispers (cf. Section 2.2). These methods make significant progress in a problem
that is usually NP-hard. Using a neighbourhood-based approach with parameter r, we
constructed large networks G4, G8 and G12 from an original classicist Latin literature
corpus and applied the abovementioned methods to cluster them. The constructed
graphs’ vertices only represent principal words, so the text corpus was analyzed up to
grammatical equivalences in the Latin language which is entirely original.

![Clusters](https://i.imgur.com/1bj0gDz.png)

We then analyzed three clustering methods from a computational perspective with
results presented in Table 2, Table 4 and visualised in Figure 5. The Louvain method
was by far the fastest algorithm for our application. The eigengap of the spectrum of
the Laplacian then yielded a good estimate for the expected number of clusters.

![Eigengap](https://i.imgur.com/jjbo26x.png)

As the author describes in Biemann 2006, Chinese Whispers generally produces a fairly
high number of clusters as compared to other methods, which one may circumvent
by adjusting either the convergence condition or introduce a minimum cluster size
through minor adjustments of the algorithm. Similar measures may be taken for
the other algorithms. In our case however, the clusters produced make a reasonable
impression when looking at the words contained therein.

Even better results for the semantic fields could be achieved by incorporating an even
larger text corpus to prevent clustering of words which are only used once or twice, so
only in the context given by the literature.
