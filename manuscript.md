---
title: The field-dependent nature of PageRank values in citation networks
keywords:
- citation metrics
- pagerank
- science of science
lang: en-US
date-meta: '2022-11-19'
author-meta:
- Benjamin J. Heil
- Casey S. Greene
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="The field-dependent nature of PageRank values in citation networks" />
  <meta name="citation_title" content="The field-dependent nature of PageRank values in citation networks" />
  <meta property="og:title" content="The field-dependent nature of PageRank values in citation networks" />
  <meta property="twitter:title" content="The field-dependent nature of PageRank values in citation networks" />
  <meta name="dc.date" content="2022-11-19" />
  <meta name="citation_publication_date" content="2022-11-19" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Benjamin J. Heil" />
  <meta name="citation_author_institution" content="Genomics and Computational Biology Graduate Group, Perelman School of Medicine, University of Pennsylvania" />
  <meta name="citation_author_orcid" content="0000-0002-2811-1031" />
  <meta name="twitter:creator" content="@autobencoder" />
  <meta name="citation_author" content="Casey S. Greene" />
  <meta name="citation_author_institution" content="Department of Pharmacology, University of Colorado School of Medicine" />
  <meta name="citation_author_institution" content="Department of Biochemistry and Molecular Genetics, University of Colorado School of Medicine" />
  <meta name="citation_author_orcid" content="0000-0001-8713-9213" />
  <meta name="twitter:creator" content="@greenescientist" />
  <link rel="canonical" href="https://greenelab.github.io/indices_manuscript/" />
  <meta property="og:url" content="https://greenelab.github.io/indices_manuscript/" />
  <meta property="twitter:url" content="https://greenelab.github.io/indices_manuscript/" />
  <meta name="citation_fulltext_html_url" content="https://greenelab.github.io/indices_manuscript/" />
  <meta name="citation_pdf_url" content="https://greenelab.github.io/indices_manuscript/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://greenelab.github.io/indices_manuscript/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/indices_manuscript/v/b4b5d0bd8e9d1f726d7721fc844a42e1beacae93/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/b4b5d0bd8e9d1f726d7721fc844a42e1beacae93/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/b4b5d0bd8e9d1f726d7721fc844a42e1beacae93/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://greenelab.github.io/indices_manuscript/v/b4b5d0bd8e9d1f726d7721fc844a42e1beacae93/))
was automatically generated
from [greenelab/indices_manuscript@b4b5d0b](https://github.com/greenelab/indices_manuscript/tree/b4b5d0bd8e9d1f726d7721fc844a42e1beacae93)
on November 19, 2022.
</em></small>

## Authors



+ **Benjamin J. Heil**
  <br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0002-2811-1031](https://orcid.org/0000-0002-2811-1031)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [ben-heil](https://github.com/ben-heil)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [autobencoder](https://twitter.com/autobencoder)<br>
  <small>
     Genomics and Computational Biology Graduate Group, Perelman School of Medicine, University of Pennsylvania
     · Funded by The Gordon and Betty Moore Foundation (GBMF4552)
  </small>

+ **Casey S. Greene**
  ^[✉](#correspondence)^<br>
    ![ORCID icon](images/orcid.svg){.inline_icon width=16 height=16}
    [0000-0001-8713-9213](https://orcid.org/0000-0001-8713-9213)
    · ![GitHub icon](images/github.svg){.inline_icon width=16 height=16}
    [cgreene](https://github.com/cgreene)
    · ![Twitter icon](images/twitter.svg){.inline_icon width=16 height=16}
    [greenescientist](https://twitter.com/greenescientist)<br>
  <small>
     Department of Pharmacology, University of Colorado School of Medicine; Department of Biochemistry and Molecular Genetics, University of Colorado School of Medicine
     · Funded by The Gordon and Betty Moore Foundation (GBMF4552); The National Human Genome Research Institute (R01 HG10067)
  </small>


::: {#correspondence}
✉ — Correspondence possible via [GitHub Issues](https://github.com/greenelab/indices_manuscript/issues)
or email to
Casey S. Greene \<casey.s.greene@cuanschutz.edu\>.


:::


## Abstract {.page_break_before}




## Introduction

There are more academic papers than any human can read in a lifetime.
Attention has been given to ranking papers, journals, or researchers by their "importance," assessed via various metrics.
Citation count assumes the number of citations determines a paper's importance.
The h-index and Journal Impact Factor focus on secondary factors like author or journal track records.
Graph-based methods like PageRank or disruption index use the context of the citing papers to evaluate an article's relevance [@doi:10.1073/pnas.0507655102; @jif; @pagerank; @doi:10.1038/s41586-019-0941-9].
Each of these methods has its strengths, and permutations exist that attempt to shore up specific weaknesses [@doi:10.1371/journal.pbio.1002541; @doi:10.1016/j.joi.2010.01.002; @doi:10.1007/s11192-017-2626-1; @doi:10.1162/qss_a_00068].

One objection to such practices is that "importance" is subjective.
The San Francisco Declaration on Research Assessment (DORA) argues against using Journal Impact Factor, or any journal-based metric, to assess individual manuscripts or scientists [@doi:10.1126/science.1240319].
DORA further argues in favor of evaluating the content of scientific content of articles and notes that any metrics used should be article-level ones [@https://sfdora.org/read/].
However, even article-level importance ignores that the importance of a specific scientific output will fundamentally differ across fields.
Nobel prize-winning work will often be less important in cancer biology if the prize-winning article is an astrophysics one.

Because there are differences between fields' citation practices [@doi:10.1017/S0269889720000022], scientists have developed strategies including normalizing the number of citations based on nearby papers in a citation network, rescaling fields' citation data to give more consistent PageRank results, and so on [@doi:10.1371/journal.pbio.1002541; @doi:10.1007/s11192-020-03406-8; @doi:10.1016/j.joi.2017.05.014; @doi:10/f48tvt].
Such approaches normalize away field-specific effects, which might help to compare one researcher with another in a very different field but do not address the difference in the relevance of a topic between fields.
This phenomenon of field-specific importance has been observed at the level of journal metrics.
Mason and Singh recently noted that depending on the field, the journal *Christian Higher Education* is either ranked as a Q1 (top quartile) journal or a Q4 (bottom quartile) journal [@doi:10.1007/s11192-022-04402-w].

It is possible that, while global journal-level metrics fail to capture field-specific importance, article-level metrics are sufficiently granular that the importance of a manuscript remains constant across fields.
We sought to examine the extent to which article-level metrics generalize between fields.
We examine this using MeSH terms to define fields and use field-specific citation graphs to assess their importance within the field.
While it is trivially apparent that journals or articles that do not have cross-field citations will have variable importance, we ignore these cases and include only those including citations in both fields, where we expect possible consistency.
We first replicate previous findings that journal-level metrics can differ substantially among fields.
We also find field-specific variability in importance at the article level.
We make our results explorable through a web app that shows metrics for overlapping papers between pairs of fields.

Our results show that even article-level metrics can differ substantially among fields.
We recommend that metrics used for assessing research outputs include field-specific, in addition to global, ones.
While qualitative assessment of the content of manuscripts remains time-consuming, our results suggest that within-field and across-field assessment remains key to assessing the importance of research outputs.


## Results

### Field-specific Citation Networks and Importances

We built citation networks using MeSH headings to denote fields.
We created a combined network and 100 shuffled versions for each pair of fields using a degree-preserving shuffling approach (see Methods).
We then split the original and shuffled networks to maintain the same set of papers within each constituent field, calculating the PageRank for all networks.
This process allows us to compare the manuscript's observed PageRank in each field with that constructed from a null that assumes no meaningful differences in citation patterns between fields.
Finally, we calculated percentile scores by comparing the PageRanks for the original and shuffled networks and made our results available at (TODO web server URL).

![ 
Schematic of the network analysis workflow. 
We construct networks of citations from pairs of MeSH headings, create shuffled versions of the graphs, split the networks into their component fields, and calculate the PageRank for each article in the networks.
](./images/schematic.png "Workflow schematic"){#fig:workflow width="100%"}

### Journal Importances Differ Between Fields

In an attempt to quantify the relative importance of journals, scientists have created rankings using metrics the Journal Impact Factor, which is essentially based on citations per article, and those that rely on more complex representations like Eigenfactor [@doi:10.5860/crln.68.5.7804]. 
It has previously been reported that journal rankings differ substantially between fields using metrics based on citation numbers [@doi:10.1007/s11192-022-04402-w].
We calculated a PageRank-based score for the journal as the median PageRank of manuscripts published in that journal for that field.
We first sought to understand the extent to which journal importance differences replicated using PageRank.

The journal *Science* provides an example of field-specific PageRank scores.
In the fields of nanotechnology or microscopy, the journal *Science* is the most influential journal based on median PageRank (Fig. @fig:journals A). <!--just to be clear, is this in each of these fields individually or in the field pair? if the field pair, how should that be interpreted?-->
However, for immunochemistry and anatomy, *Science* ranks fifth behind journals including *Nature* and *Cell* (Fig. @fig:journals B).
<!--are there other examples of journals with big differences?-->

<!--I'm not sure what to do with the below - is your argument that even specialty journals are often multi-disciplinary and consequently difficult to use as a proxy for importance? if so, what fraction of journals have 90% percent of their papers in only one "field" (MeSH heading here) vs what fraction have >1 MeSH heading with reasonable representation? It feels like something is missing in these sentences.-->
Further, while journals are sometimes used as a proxy measure for field [@doi:10.1007/s11192-020-03406-8], we find they often play host to interdisciplinary papers that may be more accurately assigned to a different field.
For example, "The metabonomic signature of celiac disease" is a paper with an extremely high PageRank in the field of metabolomics, but it was actually published in the *Journal of Proteome Research* [@doi:10.1021/pr800548z].

![
Differences between journal ranks across fields. Each point in the figure represents the median pagerank of all papers in the journal for the given fields.
](./images/combined_journals.png "Differences between journals ranks"){#fig:journals width="100%"}

### Manuscript PageRanks Differ Between Fields

We examined the univariate distributions of PageRank across fields (Fig. TODO).
To control for differences in the papers present, we also performed the analyses for field pairs using only the intersecting papers (Fig. TODO).
We found that fields differed in their PageRank distributions.
We also examined the correspondence of individual papers within the field-pair intersections.
We selected a representative field pair (Fig. @fig:heatmaps A), a field pair above the median (Fig. @fig:heatmaps B), and two high correlation field pairs (Fig. @fig:heatmaps C,D).
We found that many papers exhibited some correspondence between fields.
However, given the differences in univariate distributions, it remained difficult to determine which differences might be meaningful.

![
Heatmap of shared papers across fields
](./images/combined_heatmap.png "Heatmaps"){#fig:heatmaps width="100%"}

We devised a strategy to generate an empirical null for a field pair under the assumption that the field pair represented a single, homogenous field.
For each field-pair intersection, we performed a degree-distribution preserving permutation.
We created 100 permuted networks for each field pair.
We then calculated a percentile using the number of permuted networks with a lower PageRank for a manuscript than the true PageRank.
A manuscript with a PageRank higher than all networks has a percentile of 100, and one lower than all permuted networks has a percentile of zero. <!--Can we use percentiles here? Since you are generating 100 permutations it may be more natural. Will require multiplication by 100 for all the places you present it.-->
<!--at this point I am very confused about how what you are describing here is different than the first subsection-->
We used the difference in the percentile in each field as the field-specific affinity for a given paper.

<!--I feel like from here through the end of this section it just becomes a verbal description of the figures. Can you revise this to make it more clear how this relates to the premise of your paper (field-specific importances don't just apply to journals, they apply to manuscripts too?). It'd probably be good to have a lot less description of the figures. You may need to add some global comparisons/tables/etc - perhaps for the most extreme differences across the dataset and/or which fields have overlapping papers but the most differences vs. many overlapping papers and high similarities?-->
The nanotechnology/microscopy plot has a normal amount of variance, and clearly demonstrates the differences between fields (Fig. @fig:percentiles A).
In the center of the plot are papers that have similar percentile scores in both fields.
Towards the right side most papers have a large positive nanotech-microscopy score, indicating that they are more highly valued in the field of nanotechnology than in microscopy.
Such papers include "A robust DNA mechanical device controlled by hybridization topology" and "Bioadhesive poly(methyl methacrylate) microdevices for controlled drug delivery", while other papers such as "Turning the spotlight on cellular imaging" appropriately have a large negative nanotechnology-microscopy score despite falling far to the nanotech side of the distribution [@doi:10.1038/415062a; @doi:10/c7fpg4; @doi:10.1038/nbt1101-1013].
Meanwhile, the left side holds papers with strong negative scores, indicating the field of microscopy values the papers more.
The left side has papers like "Photostable luminescent nanoparticles as biological label for cell recognition of system lupus erythematosus patients" and "WSXM: a software for scanning probe microscopy and a tool for nanotechnology" [@doi:10.1166/jnn.2002.105; @horcas2007wsxm].
The papers with a high PageRank and similar percentile scores between fields are likely to be influential in both fields. 
In nanotechnology/microscopy these papers are frequently nanoscopic imaging papers like "Imaging intracellular fluorescent proteins at nanometer resolution", "In vivo imaging of quantum dots encapsulated in phospholipid micelles", and "Water-Soluble Quantum Dots for Multiphoton Fluorescence Imaging in Vivo" [@doi:10.1126/science.1127344; @doi:10.1126/science.1077194; @doi:10.1126/science.1083780].

The immunochemistry/anatomy fields have much higher correlation in their shared papers, but still have some outliers (Fig. @fig:percentiles B).
Examples of papers preferred in the immunochemistry field are "Immunoelectron microscopic exploration of the Golgi complex", "Immunocytochemical and electrophoretic analyses of changes in myosin gene expression in cat posterior temporalis muscle during postnatal development", and "Electron microscopic demonstration of calcitonin in human medullary carcinoma of thyroid by the immuno gold staining method" [@doi:10.1177/31.8.6863900; @doi:10.1007/bf01682147; @doi:10.1007/bf00514331].
Papers preferred in anatomy include "Grafting genetically modified cells into the rat brain: characteristics of E. coli β-galactosidase as a reporter gene", "Vitamin-D-dependent calcium-binding-protein and parvalbumin occur in bones and teeth", and "Mapping of brain areas containing RNA homologous to cDNAs encoding the alpha and beta subunits of the rat GABAA gamma-aminobutyrate receptor" [@doi:10/dptnbm; @doi:10.1007/bf02405306; @doi:10.1073/pnas.85.20.7815]
Papers with high PageRank in both domains and a similar importance are "Studies of the HER-2/neu Proto-Oncogene in Human Breast and Ovarian Cancer", "Expression of c-fos Protein in Brain: Metabolic Mapping at the Cellular Level", and "Proliferating cell nuclear antigen (PCNA) immunolocalization in paraffin sections: An index of cell proliferation with evidence of deregulated expression in some, neoplasms" [@doi:10.1126/science.2470152; @doi:10.1126/science.3131879; @doi:10.1002/path.1711620403].

Where immunochemistry/anatomy served as an example of a highly correlated pair of fields, papers in proteomics/metabolomics have very different PageRanks between fields (Fig. @fig:percentiles C). 
These fields illustrate one of the reasons why the difference in percentile scores is a useful metric: there is so much dispersion that it's hard to tell where a trend line should be.
When coloring by the difference in scores, however, it is easy to see which papers are valued more in each field.
The proteomics-heavy papers include "Proteomics Standards Initiative: Fifteen Years of Progress and Future Work", "Limited Environmental Serine and Glycine Confer Brain Metastasis Sensitivity to PHGDH Inhibition", and "A high-throughput processing service for retention time alignment of complex proteomics and metabolomics LC-MS data", [@doi:10.1021/acs.jproteome.7b00370;@doi:10/ghf85j;@doi:10.1093/bioinformatics/btr094] while the metabolomics papers have titles such as "MeltDB: a software platform for the analysis and integration of metabolomics experiment data", "In silico fragmentation for computer assisted identification of metabolite mass spectra", and "The Metabonomic Signature of Celiac Disease" [@doi:10.1093/bioinformatics/btn452;@doi:10/d7gpf5;@doi:10.1021/pr800548z].
The articles with high PageRank and importance in both fields include "Visualization of omics data for systems biology", "FunRich: An open access standalone functional enrichment and interaction network analysis tool", and "Proteomic and Metabolomic Characterization of COVID-19 Patient Sera" [@doi:10.1038/nmeth.1436;@doi:10.1002/pmic.201400515;@doi:10.1016/j.cell.2020.05.032].

The final pair, computational biology/human genetics, is interesting because while there is a good degree of variance in the PageRank values across fields, the highest rated papers in both fields had very similar percentile scores (Fig. @fig:percentiles D).
The high percentile difference papers in computational biology include several database papers [@doi:10.1101/gr.1680803; @doi:10/cfgb98; @doi:10/ch565r].
Their counterparts in human genetics were more on the policy paper side, likely because the human genetics MeSH subheading is distinct from the several other genetics subheadings including genetic research, population genetics, genomics, etc. [@doi:10.1126/science.274.5287.621; @doi:10.1097/aog.0000000000001951; @doi:10.1097/gim.0b013e31821024ca].
Meanwhile, the papers with high PageRanks in both fields tend to have similar percentile scores and be related to the genome sequencing and mapping [@doi:10.1038/35057062; @doi:10.1126/science.270.5244.1945; @doi:10/fwkrnb].

![
The difference between percentile scores for four field pairs. 
](./images/combined_difference.png "Differences between fields' percentile scores"){#fig:percentiles width="100%"}

### Here's a web app 

<!-- if this is going to be a section, something needs to be revised above - at the moment it's way short and just restates what's up there.-->
To demonstrate our findings, we have also set up a web server with all pairs of networks instead of solely the ones shown in this paper.
The web server can be found at X


## Methods

#### COCI
We used the March 2022 version of the COCI citation index [@doi:10.1007/s11192-019-03217-6] as the source of our citation data.
This dataset contains around 1.3 billion citations from ~73 million bibliographic resources.

#### Selecting fields
To differentiate between scientific fields, we needed a way to map papers to fields.
Fortunately, all the papers in Pubmed Central (https://www.ncbi.nlm.nih.gov/pmc/) have corresponding Medical Subject Headings (MeSH) terms.
While MeSH terms are varied and numerous, the subheadings of the Natural Science Disciplines (H01) category fit our needs.
However, MeSH terms are hierarchical, and vary greatly in their size and specificity.
To extract a balanced set of terms we recursively traversed the tree and selected headings that have least 10000 DOIs and don't have multiple children that also meet the cutoff.
Our resulting set of headings contained 45 terms, from "Acoustics" to "Water Microbiology".

#### Building single heading citation networks
The COCI dataset consists of pairs of Digital Object Identifiers (DOIs).
To change these pairs into a form we could run calculations on, we needed to convert them into networks.
To do so, we created 45 empty networks, one for each MeSH term we selected previously.
We then iterated over each pair of DOIs in COCI, and added them to a network if the DOIs corresponded to two journal articles written in english, both of which were tagged with the corresponding MeSH heading.

#### Building combined networks
Because we were interested in the differences between fields, we also needed to build networks from pairs of MeSH headings.
These networks were built via the same process, except that instead of keeping articles corresponding to a single DOI we added a citation to the network if both articles were in the pair of fields, even if the citation occurred across fields.
Running this network-building process yielded 990 two-heading networks.

#### Shuffling networks
Sampling a graph from the degree distribution while preserving the distribution of degrees in the network turned out to be challenging.
Because citation graphs are directed, it's not possible to simply swap pairs of edges and end up with a graph that is uniformly sampled from the space.
Instead, a more sophisticated three-edge swap method must be used [@arxiv:0905.4913].
Because this algorithm had not been implemented yet in NetworkX [@networkx], we wrote the code to perform shuffles and submitted our change to the library.
With the shuffling code implemented, we created 100 shuffled versions of each of our combined networks to act as a background distribution to compare metrics against.

#### Splitting networks 
Once we had a collection of shuffled networks, we needed to split them into their constituent fields.
To do so, we reduced the network to solely the nodes that were present in the single heading citation network, and kept only citations between these nodes.

#### Running PageRank
We used the NetworkX implementation of PageRank with default parameters to evaluate paper importance within fields.

#### Percentile score
To determine the degree to which the papers' PageRank values were higher or lower than expected, we compared the PageRank values calculated for the true citation networks to the values in the shuffled networks for each paper.
We then recorded the fraction of shuffled networks where the paper had a lower PageRank than in the true network to derive a single number that described these values.
For example, if a paper had a higher PageRank in the true network than in all the shuffled networks it received a score of 1.
Likewise, if it had a lower PageRank in the true network than in all the shuffled networks it received a score of 0.
Papers in between the two extremes had fractional values, like .5 (a paper that fell in the middle of the pack) and so on.

#### Differences in percentiles
A convenient feature of the percentile scores is that they're directly comparable between fields.
If a paper is present in two fields, the difference in scores between the two fields can be used to estimate its relative importance.
For example, if a paper has a score of 1 in field A (indicating a higher PageRank in the field than expected given its number of citations and the network structure) and a score of 0 in field B (indicating a lower than expected PageRank), then the large difference in scores indicates the paper is more highly valued in field A than field B.
If the paper has similar scores in both fields, it indicates that the paper is similarly valued in the two fields.

#### Hardware/runtime
The analysis pipeline was run on the RMACC Summit cluster.
The full pipeline, from downloading the data to analyzing it to vizualizing it took about a week to run.
However, that number is heavily dependent on details such as the number of CPU nodes available and the network speed.

#### Server details
Our webserver is built by visualizing our data in Plotly (https://plotly.com/python/plotly-express/) on the Streamlit platform (https://streamlit.io/).
The field pairs made available by the frontend are those with at least 1000 shared papers after filtering out papers with more than a 5% missingness level of their PageRanks after shuffling.
The journals available for visualization are those with at least 25 papers for the given field pair.


## Discussion/Conclusion

We analyze hundreds of field-pair citation networks to examine the extent to which article-level importance metrics vary between fields.
As previously reported (TODO: ADD REFS), we find systematic differences in PageRanks between fields that would warrant some form of normalization when making cross-field comparisons with global statistics.
However, we also find that field-specific differences are not driven solely by differences in citation practices.
Instead, the importances of individual papers appear to differ meaningfully between fields.
Global rankings or efforts to normalize out field-specific effects obscure meaningful differences in manuscript importance between communities.

As with any study, this research has certain limitations.
We generate a background distribution of PageRanks for each field pair by performing a defined number of swaps.
Our empirical results suggest that three times as many swaps as edges reach a point of stability <!--TODO: need to present at least some results on this-->, but certain network structures may require a different number.
Another limitation is our selection of MeSH terms to represent fields.
We used MeSH because it is a widely-annotated set of subjects in biomedicine and thresholded MeSH term sizes to balance having enough observations to calculate appropriate statistics with having sufficient granularity to capture fields.
This resulted in fields at the granularity of "X" and "Y."

We also note that there are inherent issues with the premise of ranking manuscript importances.
We sought to understand the extent to which such rankings were stable between fields after correcting for field-specific citation practices.
We found limited stability between fields, mostly between closely-related fields, suggesting that the concept of a universal ranking of importances is difficult to justify.
In the way that reducing a distribution to a Journal Impact Factor distorts assessment, attempting to use a single universal score to represent importance across fields poses similar challenges at the level of individual manucripts.
Furthermore, this work's natural progression would extend to estimating the importance of individual manuscripts to individual researchers.
Thus, a holistic measure of importance would need to include a distribution of scores not only across fields but across researchers.
It may ultimately be impossible to calculate a meaningful importance score.
The lack of ground truth for importance is an inherent feature, not a bug, of science's step-wide progression.

Shifting from the perspective of evaluation to discovery can reveal more appropriate uses for these types of statistics.
Field-pair calculations for such metrics may help with self-directed learning of new fields.
An expert in one field, e.g., computational biology, who aims to learn more about genetics may find manuscripts with high importance in genetics and low importance in computational biology to be important reads.
These represent manuscripts not currently widely cited in one's field but highly influential in a target field.
Our application can reveal these manuscripts for MeSH field pairs, and our source code allows others to perform our analysis with different granularity.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
