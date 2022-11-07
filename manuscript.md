---
title: The field-dependent nature of PageRank values in citation networks
keywords:
- citation metrics
- pagerank
- science of science
lang: en-US
date-meta: '2022-11-07'
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
  <meta name="dc.date" content="2022-11-07" />
  <meta name="citation_publication_date" content="2022-11-07" />
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
  <link rel="alternate" type="text/html" href="https://greenelab.github.io/indices_manuscript/v/ad020b55a10e8e8af2609a0b7bbd9470ffb169ba/" />
  <meta name="manubot_html_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/ad020b55a10e8e8af2609a0b7bbd9470ffb169ba/" />
  <meta name="manubot_pdf_url_versioned" content="https://greenelab.github.io/indices_manuscript/v/ad020b55a10e8e8af2609a0b7bbd9470ffb169ba/manuscript.pdf" />
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
([permalink](https://greenelab.github.io/indices_manuscript/v/ad020b55a10e8e8af2609a0b7bbd9470ffb169ba/))
was automatically generated
from [greenelab/indices_manuscript@ad020b5](https://github.com/greenelab/indices_manuscript/tree/ad020b55a10e8e8af2609a0b7bbd9470ffb169ba)
on November 7, 2022.
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
Determining which papers are important and in doing so solving the resulting prioritization problem is hard.

Part of this difficulty is because "importance" is a subjective measure.
Different metrics attempt to capture it through different approaches.
Citation count assumes the number of citations determines a paper's importance, h-index and Journal Impact Factor focus more on secondary factors like author' or journals' track record, and graph-based methods like PageRank or disruption index use the context of the surrounding papers to evaluate a given article's relevance [@doi:10.1073/pnas.0507655102; @jif; @pagerank; @doi:10.1038/s41586-019-0941-9].
Each of these methods have their own strengths, as well as various permutations that shore up their weaknesses [@doi:10.1371/journal.pbio.1002541; @doi:10.1016/j.joi.2010.01.002; @doi:10.1007/s11192-017-2626-1; @doi:10.1162/qss_a_00068].

In particular, because there are differences between fields' citation practices [@doi:10.1017/S0269889720000022], scientists have developed approaches like normalizing the number of citations based on nearby papers in the citation network, 
studying the relative performance of disruption index variants in a single field,
rescaling fields' citation data to give more consistant PageRank results, and so on [@doi:10.1371/journal.pbio.1002541; @doi:10.1007/s11192-020-03406-8; @doi:10.1016/j.joi.2017.05.014; @doi:10/f48tvt]
Such approaches account for differences between fields, but they tend to focus on normalizing out the effects a field has on a metric.

We argue that this removal of field-specific signal obscures real differences in relevance.
Intuitively, Nobel prize-winning work will stay at the bottom of a cancer biologist's paper pile if the article is about astrophysics.
Trying to apply a universal ranking metric to papers or journals ignores that phenomenon and yields strange results.
For example, Mason and Signh recently pointed out that depending on what field is evaluating it, the journal *Christian Higher Education* is either ranked as a Q1 (top quartile) journal or a Q4 (bottom quartile) journal [@doi:10.1007/s11192-022-04402-w].

The purpose of this paper is not to create a new metric that attempts to measure articles' importance.
Instead, we aim to shed light on a less-studied aspect of prioritizing papers: differences between fields.
To that end we show differences between PageRanks for the same paper in different field citation networks.
We then demonstrate that some of the differences are field-specific by estimating the distribution of possible citation networks with a degree-preserving graph shuffling method.
We also demonstrate that while it is possible to rank journals using standard metrics [@eigenfactor], their rank changes depending on field.
Finally, we make our results more easily available by creating a web app that visualizes pairs of fields with overlapping papers.

Ultimately we show that there is great potential in analyzing articles while keeping field in mind.
Going forward, we hope more field-aware methods of assessing article importance will be developed.


## Results

### Workflow

We built citation networks from pairs of MeSH headings corresponding to fields.
We then created 100 shuffled versions of each combined network using a degree-preserving shuffling approach (see Methods).
We split both the original and shuffled networks into papers of each constituent field, then calculated the PageRank for all networks.
Finally, we created percentile scores by comparing the PageRanks for the original and shuffled networks, and made our results available at (TODO web server URL).

![ 
Schematic of the network analysis workflow. 
We construct networks of citations from pairs of MeSH headings, create shuffled versions of the graphs, split the networks into their component fields, and calculate the PageRank for each article in the networks.
](./images/schematic.png "Workflow schematic"){#fig:workflow width="100%"}

### The same paper will have different PageRanks in different fields

To demonstrate different relationships between fields' PageRanks, we visualized networks from four different field pairs.
The first, nanotechnology/microscopy is a fairly average network in terms of inter-field PageRank correlation (Fig. @fig:heatmaps A).
The second, immunochemistry/anatomy has a high correlation but still has outlier points (Fig. @fig:heatmaps B).
The third and fourth, proteomics/metabolomics and computational biology/human genetics show two fields with a larger degree of difference between PageRanks in each field (Fig. @fig:heatmaps C,D).

![
Heatmap of shared papers across fields
](./images/combined_heatmap.png "Heatmaps"){#fig:heatmaps width="100%"}

### This variance is not entirely field independent
It's hard to say that a paper with a large difference between field-specific PageRanks is more important in one field than the other.
It's possible that the scores are skewed by different field sizes, or caused by randomness in MeSH tagging.

To disentangle the random chance from the actual differences in network structure, we needed something to compare against.
We decided on shuffling citation networks in a way that preserved their citation counts while randomizing which papers they cite.
By doing so, we created 100 shuffled networks for each pair of fields where the degree distribution of the network is maintained but the global structure is removed from the networks.
We then calculated a percentile score based on how many of the random networks had lower PageRank for a given paper than its true PageRank. 
That is to say that a paper with a PageRank higher than all the random networks would have a score of one, a paper with a PageRank less than all the random networks would have a zero, and the rest would fall somewhere in between. 
We used the difference in these scores between fields to determine the field-specific affinity for a given paper. 

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

### Journals aren't a great proxy for field, as they often have papers present from multiple fields.
In addition to article metrics, papers are often prioritized by selecting prestigious journals.
In an attempt to quantify the relative importance of journals, scientists have created rankings using metrics like Eigenfactor [@doi:10.5860/crln.68.5.7804]. 
While such metrics return intuitively reasonable results, we discovered that the inherent aggregation that they apply masks differences between fields.

When considering the fields nanotechnology or microscopy, the journal *Science* is far and away the most influential journal based on median PageRank (Fig. @fig:journals A).
*Science*'s dominance isn't universal though — it ranks fifth behind journals like *Nature* and *Cell* when looking at immunochemistry and anatomy (Fig. @fig:journals B).
Further, while journals are sometimes used as a proxy measure for field [@doi:10.1007/s11192-020-03406-8], we find they often play host to interdisciplinary papers that may be more accurately assigned to a different field.
For example, "The metabonomic signature of celiac disease" is a paper with an extremely high PageRank in the field of metabolomics, but it was actually published in the *Journal of Proteome Research* [@doi:10.1021/pr800548z].

![
Differences between journal ranks across fields. Each point in the figure represents the median pagerank of all papers in the journal for the given fields.
](./images/combined_journals.png "Differences between journals ranks"){#fig:journals width="100%"}

### Here's a web app 

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

We analyzed hundreds of pairwise citation networks in order to determine the effects of field on citation metrics.
In doing so we found that there are, in fact, differences in PageRanks between fields that warrant some form of normalization when making comparisons.
However, we also showed that these effects aren't solely driven by differences in citation practices that should be regressed out.
Instead, there appear to be meaningful differences between fields for individual papers that exist in both fields.
Normalizing out this variation or creating a single global ranking obscures meaningful signal about how papers are perceived in different communities.

That is not to say that our analysis is perfect, however.
For one thing, there are inherent issues with the concept of ranking papers.
While we point out that not using field information when prioritizing papers can lose some of the nuance of the data, we're still just discussing different ways of measuring proxy variables.
One's goal is often to read the papers most relevant to them, or the most influential papers in their field.
However, since the ground truth of relevance or influence is difficult or impossible to quanitfy we end up using PageRank, citation count, Journal Impact Factor, or some other metric.
While these proxy variables are hopefully correlated with the characteristics we care about, its important to acknowledge that they're not the same thing.

Our percentile score is also an area for potential improvement.
We decide to make three times as many swaps as our network has edges, but it is unclear what the ideal number of swaps is to ensure a network is drawn uniformly at random from the distribution of possible networks with the same degree distribution.
Additionally, sampling graphs at random from degree-preserving network swaps isn't perfectly representative of what a potential alternate universe's citation network would look like.
For that we'd need a way to avoid edge swaps that caused "back-in-time" citations, a method to swap citations to a paper based on what similar papers had cited, and the ability to add or subtract citations to and from a given paper, as the number of citations for a given paper is partly due to random chance.
While outside of the scope of this paper, implementing these features into a citation graph randomization method would be an interesting avenue of future research.

A third limitation of our paper comes from the way we selected MeSH terms.
Our threshold number of papers required to include a field was chosen so that we could investigate a diverse set of fields while still keeping a reasonable amount of papers in each combination of fields.
However, it is possible that a more (or less) granular field selection approach would give clearer results.

Similar approaches to ours may be helpful for an expert in one field learning a new one.
For example, a expert in computational biology might get a better idea of the difference in perspective across fields by reading articles that have a high percentile score in genetics and a low score in computational biology.
While such papers are important in genetics, the computational biologist would be unlikely to be familiar with them due to the field difference.

Ultimately we hope to see more analyses going forward use field information for evaluating the influence of scientific articles.
We believe this to be particularly important in the case of interdisciplinary papers that exist between fields by their very nature.
A paper largely ignored in one field may be groundbreaking in another, and that dynamic should be accounted for when attempting to make sense of citation networks.


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
