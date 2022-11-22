---
title: The field-dependent nature of PageRank values in citation networks
keywords:
- citation metrics
- pagerank
- science of science
lang: en-US
date-meta: '2022-11-22'
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
  <meta name="dc.date" content="2022-11-22" />
  <meta name="citation_publication_date" content="2022-11-22" />
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
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/indices_manuscript/v/bd37d51a50213e884d44ad1a63822eb3a7a28216/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/bd37d51a50213e884d44ad1a63822eb3a7a28216/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/bd37d51a50213e884d44ad1a63822eb3a7a28216/manuscript.pdf" />
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
([permalink](https://greenelab.github.io/indices_manuscript/v/bd37d51a50213e884d44ad1a63822eb3a7a28216/))
was automatically generated
from [greenelab/indices_manuscript@bd37d51](https://github.com/greenelab/indices_manuscript/tree/bd37d51a50213e884d44ad1a63822eb3a7a28216)
on November 22, 2022.
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
DORA further argues in favor of evaluating the content of scientific content of articles and notes that any metrics used should be article-level ones (https://sfdora.org/read/).
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
](./images/updated_schematic.png "Workflow schematic"){#fig:workflow width="100%"}

### Journal Rankings Differ Between Fields

In an attempt to quantify the relative importance of journals, scientists have created rankings using metrics the Journal Impact Factor, which is essentially based on citations per article, and those that rely on more complex representations like Eigenfactor [@doi:10.5860/crln.68.5.7804]. 
It has previously been reported that journal rankings differ substantially between fields using metrics based on citation numbers [@doi:10.1007/s11192-022-04402-w].
We calculated a PageRank-based score for the journal as the median PageRank of manuscripts published in that journal for that field.
We first sought to understand the extent to which journal ranking differences replicated using PageRank.

To do so, we ranked the journals in each of the 45 fields in our dataset to determine whether the top ranking journal would be consistent across fields or different (Fig. @fig:jrank).
We found that the most common top-ranked journal was *Science*.
This was unsurprising, given that it tends to rank highly among global journal level metrics such as eigenfactor.
However, the ranking was very field-dependent, with only 20% of fields having *Science* as their top ranked journal.

One could argue that while general journals may have differing influence by field, specialty journals correspond to a single field so field-aware metrics are irrelevant.
That turns out to be untrue.
Of the 5,178 journals with at least 50 articles present in our dataset, only 56 (1.1%) have more than 90 percent of their articles within a single field.
One driver of the rarity in truly field-specific journals is the overlap between fields.
For example, proteomics and metabolomics are different fields with different focuses, but their techniques are often applied in conjunction with each other.
This overlap leads to papers like "The metabonomic signature of celiac disease," a paper with an extremely high PageRank in the field of metabolomics, that was published in the *Journal of Proteome Research* [@doi:10.1021/pr800548z].

![
The number of times each journal had the highest median PageRank for a field.
](./images/journal_hist.png "Differences between journals ranks"){#fig:jrank width="100%"}

### Manuscript PageRanks Differ Between Fields

We examined the univariate distributions of PageRank across fields (Fig. @fig:fieldhist).
To control for differences in the papers present, we also performed the analyses for field pairs using only the intersecting papers (Fig. @fig:pairhist).
We found that fields differed in their PageRank distributions.
We also examined the correspondence of individual papers within the field-pair intersections.
We selected field pairs with varying degrees of correlation between their PageRanks (Fig. @fig:heatmaps).
We found that many papers exhibited some correspondence between fields.
However, given the differences in univariate distributions, it remained difficult to determine which differences might be meaningful.

![
The distribution of article PageRanks in various fields
](./images/per-field.png "Article PageRanks"){#fig:fieldhist width="100%"}

![
The distribution of PageRanks for articles shared between fields.
](./images/combined_histogram.png "Article Pair PageRanks"){#fig:pairhist width="100%"}

![
Heatmap of shared papers across fields
](./images/combined_heatmap.png "Heatmaps"){#fig:heatmaps width="100%"}

We devised a strategy to generate an empirical null for a field pair under the assumption that the field pair represented a single, homogenous field.
For each field-pair intersection, we performed a degree-distribution preserving permutation.
We created 100 permuted networks for each field pair.
We then calculated a percentile using the number of permuted networks with a lower PageRank for a manuscript than the true PageRank.
A manuscript with a PageRank higher than all networks has a percentile of 100, and one lower than all permuted networks has a percentile of zero. 
<!--at this point I am very confused about how what you are describing here is different than the first subsection-->
We used the difference in the percentile in each field as the field-specific affinity for a given paper.

By examining the fields' PageRank percentiles, we found that many articles had large differences in their perception between fields.
In nanotechnology and microscopy, papers with high nanotechnology percentiles and low microscopy percentiles tended towards applications of nanotechnology, while their counterparts with high microscopy percentiles and low nanotechnology percentiles were often papers about technological developments in microscopy (Fig. @fig:percentiles A, Table 1).
Immunochemistry-favored papers are largely applications of immunochemical methods, while anatomy-favored articles tend to focus experiments on a single anatomical region (Fig. @fig:percentiles B, Table 2).
Proteomics and metabolomics tend to use similar methods, so the fields on either end are largely (though not entirely) field-specific applications of those methods (Fig. @fig:percentiles C, Table 3).
Computational biology is similarly applications-focused, though human genetics tends towards policy papers due to its MeSH heading (H01.158.273.343.385) excluding fields like genomics, population genetics, and microbial genetics (Fig. @fig:percentiles D, Table 4).
In addition to papers with large differences between fields, each field also has papers with high PageRanks and similar percentiles in both fields.
Overall it is clear that while some papers may be influential in multiple fields, others have more field-specific import.

| Nanotechnology Percentile | Microscopy Percentile | Title | Reference |
|----------|----------|----------|----------|
| 100 | 4  | A robust DNA mechanical device controlled by hybridization topology | [@doi:10.1038/415062a] |
| 100 | 5  | Bioadhesive poly(methyl methacrylate) microdevices for controlled drug delivery | [@doi:10/c7fpg4] |
| 99  | 2  | DNA-templated self-assembly of protein arrays and highly conductive nanowrires | [@doi:10.1126/science.1089389] |
| 0   | 100| Photostable luminescent nanoparticles as biological label for cell recognition of system lupus erythematosus patients | [@doi:10.1166/jnn.2002.105] |
| 5   | 90 | WSXM: a software for scanning probe microscopy and a tool for nanotechnology | [@horcas2007wsxm] |
| 0   | 77 | Measuring Distances in Supported Bilayers by Fluorescence Interference-Contrast Microscopy: Polymer Supports and SNARE Proteins | [@doi:10/dqsg2c] |
| 100 | 99 | Toward fluorescence nanoscopy | [@doi:10.1038/nbt895] |
| 100 | 86 | In vivo imaging of quantum dots encapsulated in phospholipid micelles | [@doi:10.1126/science.1077194]|
| 100 | 99 | Water-Soluble Quantum Dots for Multiphoton Fluorescence Imaging in Vivo | [@doi:10.1126/science.1083780]|

Table 1: Nanotechnology/microscopy papers of interest 

| Immunochemistry Percentile| Anatomy Percentile | Title | Reference |
|----------|----------|----------|----------|
| 100 | 45 | Immunoelectron microscopic exploration of the Golgi complex | [@doi:10.1177/31.8.6863900] |
| 100 | 14 | Immunocytochemical and electrophoretic analyses of changes in myosin gene expression in cat posterior temporalis muscle during postnatal development | [@doi:10.1007/bf01682147] |
| 98 | 5 | Electron microscopic demonstration of calcitonin in human medullary carcinoma of thyroid by the immuno gold staining method | [@doi:10.1007/bf00514331] |
| 12 | 100 | Grafting genetically modified cells into the rat brain: characteristics of E. coli β-galactosidase as a reporter gene | [@doi:10/dptnbm] |
| 12 | 100 | Vitamin-D-dependent calcium-binding-protein and parvalbumin occur in bones and teeth | [@doi:10.1007/bf02405306] |
| 3 | 100 | Mapping of brain areas containing RNA homologous to cDNAs encoding the alpha and beta subunits of the rat GABAA gamma-aminobutyrate receptor | [@doi:10.1073/pnas.85.20.7815] |
| 100 | 100 | Studies of the HER-2/neu Proto-Oncogene in Human Breast and Ovarian Cancer| [@doi:10.1126/science.2470152] |
| 100 | 100 | Expression of c-fos Protein in Brain: Metabolic Mapping at the Cellular Level| [@doi:10.1126/science.3131879] |
| 100 | 100 | Proliferating cell nuclear antigen (PCNA) immunolocalization in paraffin sections: An index of cell proliferation with evidence of deregulated expression in some neoplasms| [@doi:10.1126/science.3131879] |

Table 2: Immunochemistry/anatomy papers of interest 

| Proteomics Percentile | Metabolomics Percentile | Title | Reference |
|----------|----------|----------|----------|
| 67 | 2 | Proteomics Standards Initiative: Fifteen Years of Progress and Future Work | [@doi:10.1021/acs.jproteome.7b00370] |
| 99 | 0 | Limited Environmental Serine and Glycine Confer Brain Metastasis Sensitivity to PHGDH Inhibition | [@doi:10.1158/2159-8290.cd-19-1228] |
| 100 | 0 | A high-throughput processing service for retention time alignment of complex proteomics and metabolomics LC-MS data| [@doi:10.1093/bioinformatics/btr094 ] |
| 0 | 100 | MeltDB: a software platform for the analysis and integration of metabolomics experiment data| [@doi:10.1093/bioinformatics/btn452] |
| 0 | 98 | In silico fragmentation for computer assisted identification of metabolite mass spectra| [@doi:10.1186/1471-2105-11-148] |
| 0 | 100 | The Metabonomic Signature of Celiac Disease| [@doi:10.1021/pr800548z] |
| 91 | 70 | Visualization of omics data for systems biology| [@doi:10.1186/1471-2105-11-148] |
| 0 | 16 | FunRich: An open access standalone functional enrichment and interaction network analysis tool| [@doi:10.1002/pmic.201400515] |
| 0 | 5 | Proteomic and Metabolomic Characterization of COVID-19 Patient Sera| [@doi:10.1016/j.cell.2020.05.032] |

Table 3: Proteomics/metabolomics papers of interest 

| Computational Biology Percentile | Human Genetics Percentile | Title | Reference |
|----------|----------|----------|----------|
| 99 | 0 | Development of Human Protein Reference Database as an Initial Platform for Approaching Systems Biology in Humans| [@doi:10.1101/gr.1680803] |
| 100 | 1 | A database for post-genome analysis| [@doi:10/cfgb98] |
| 100 | 1 | Use of mass spectrometry-derived data to annotate nucleotide and protein sequence databases| [@doi:10/ch565r] |
| 12 | 100| Genetic Discrimination: Perspectives of Consumers | [@doi:10.1126/science.274.5287.621] |
| 0 | 81 | Committee Opinion No. 690: Carrier Screening in the Age of Genomic Medicine | [@doi:10.1097/aog.0000000000001951 ] |
| 23 | 100 | Public health genomics: The end of the beginning| [@doi:10.1097/gim.0b013e31821024ca] |
| 100 | 99 | Initial sequencing and analysis of the human genome| [@doi:10.1038/35057062] |
| 100 | 100 | An STS-Based Map of the Human Genome| [@doi:10.1126/science.270.5244.1945] |
| 100 | 100 | A New Five-Year Plan for the U.S. Human Genome Project| [@doi:10.1126/science.8211127] |

Table 4: Computational biology/human genetics papers of interest 

![
The difference between percentile scores for four field pairs. 
](./images/combined_difference.png "Differences between fields' percentile scores"){#fig:percentiles width="100%"}

It is not possible to describe all the field-pairs and relevant differences between fields within the space of a journal article.
Instead, we have developed a web server that displays the percentiles for all pairs of fields in our dataset with at least 1000 shared articles.
The web server can be found at TODO.


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
As previously reported, we find systematic differences in PageRanks between fields [@doi:10.1007/s11192-017-2626-1; @doi:10.1007/s11192-014-1308-5] that would warrant some form of normalization when making cross-field comparisons with global statistics.
However, we also find that field-specific differences are not driven solely by differences in citation practices.
Instead, the importances of individual papers appear to differ meaningfully between fields.
Global rankings or efforts to normalize out field-specific effects obscure meaningful differences in manuscript importance between communities.

As with any study, this research has certain limitations.
One example is our selection of MeSH terms to represent fields.
We used MeSH because it is a widely-annotated set of subjects in biomedicine and thresholded MeSH term sizes to balance having enough observations to calculate appropriate statistics with having sufficient granularity to capture fields.
This resulted in fields at the granularity of "biophysics" and "ecology."
We also have to select a number of swaps to generate a background distribution of PageRanks for each field pair.
We selected three times as many swaps as edges, where each swap modifies three edges, but certain network structures may require a different number.

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


#### Acknowledgements
- Add funding
- Add cluster 
- Thank Greenelab 


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
