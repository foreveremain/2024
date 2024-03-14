---
layout: page
title: Bio+MedVis Challenge
permalink: /biovisChallenges_vis/
---

# Bio+MedVis Challenge @ IEEE VIS 2024

{% include_relative biovis_challenge_news.html %}

## Redesign Challenge: Redesign an Existing Visualization

### Biological Background and Data Description

In biology, structure and function are tightly linked, and the biology
of cells in tissues is no exception. A key challenge for cell biologists
is understanding the spatial patterns characteristic of health and
disease. A cutting-edge area of cell biology is the development and
application of technologies that measure molecular states within cells
while preserving spatial context (historically, many single-cell
profiling techniques have required dissociation of tissues).

A key cellular measurement technique is called transcriptomics, which
provides insight into cell types (e.g., immune cell vs. muscle cell),
cell states (e.g., response to stimuli), and information about proteins
that might be produced downstream (i.e., via translation).
Transcriptomics techniques measure gene expression: the abundance of RNA
transcripts corresponding to each gene in each cell. As the name
implies, _spatial_ transcriptomics methods capture gene expression and
spatial coordinates simultaneously. Resolutions of spatial
transcriptomics methods can vary from subcellular, to single-cell, to
"spots" that represent multiple cells. There is typically a tradeoff
between the spatial resolution and the number of genes that can be
measured by a given technology.

**VISIUM** is a spatial transcriptomics technology developed by 10x
Genomics. It allows researchers to measure gene expression and spatial
organization of tissues simultaneously. For a given tissue slice, VISIUM
can measure transcripts genome-wide (e.g., \~20,000 genes for human
samples) at a resolution of approximately 5-10 cells per spot. This
enables researchers to understand how gene expression patterns vary
across different regions of a tissue sample. This technology has
applications in various fields such as cancer research, developmental
biology, neuroscience, and more, allowing researchers to gain deeper
insights into the molecular mechanisms underlying complex biological
processes within tissues.

Each VISIUM spot represents the gene expression of multiple cells, but
researchers are typically interested in interpreting the data at the
cell type level (e.g., linking expression differences to particular cell
types that are characterized in the biological literature). As a result,
computational methods have been developed to deconvolute each VISIUM
spot into a distribution of (predicted) cell type proportions.
Biologists can then use the deconvolution results to link their findings
to existing cell type knowledge.

These deconvolutional methods thus produce data that, on a per-spot
basis, represents proportional cell-type membership (e.g. 30% Cell Type
1, 50% Cell Type 2, 20% Cell Type 3). Visualizing these data in the
context of the tissue image provides crucial spatial context, enabling
domain experts to explore deconvolution results within the intricate
cellular architecture and tissue morphology. One common technique for
visualizing these data is to superimpose a pie chart on each spot
location representing the cell types represented. Pie charts and their
limitations have been well explored by the visualization community.
Moreover, superimposing them on the image occludes the underlying
tissue.

<figure>
<img src="../images/biovis-challenge/STdeconvolve.png" alt="Example data for Redesign Challenge">

<figcaption>
    <strong>Figure 1:</strong> Example data for Redesign Challenge.
    <strong>(a)</strong> H&E image,
    <strong>(b)</strong> spot cell-type proportion
    pie charts, and
    <strong>(c)</strong> Pie charts superimposed on the image. Plots
    generated w/ STdeconvolve (Miller et al., 2022).
</figcaption>
</figure>

### Data and Documentation

#### Example Dataset

[https://drive.google.com/drive/folders/1t6aeMDh2l067_6DEMFyovtRO5swZieBF?usp=sharing](https://drive.google.com/drive/folders/1t6aeMDh2l067_6DEMFyovtRO5swZieBF?usp=sharing)

#### Data Description

-   `Genes.csv` - List of genes in the feature matrix
-   `FeatureMatrix.mtx` - Feature matrix, stored as a sparse matrix
-   `ClusterGeneExpression.csv` - Gene expression per cell-type cluster
-   `SpotClusterMembership.csv` - Cell type proportions per spot
-   `SpotPositions.csv` - Spot positions and radiuses
-   `Images/scalefactors_json.json` - Scale factors between spot positions
-   `Images/tissue_hires_image.png` - H&E image

#### Additional Data and Resources

-   Visium data from Kleshchevnikov et al., 2022:
    [https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-11114](https://www.ebi.ac.uk/biostudies/arrayexpress/studies/E-MTAB-11114),
    filter by sample ST8059049
-   Summary:
    [https://ftp.ebi.ac.uk/biostudies/fire/E-MTAB-/114/E-MTAB-11114/Files/ST8059049_web_summary.html](https://ftp.ebi.ac.uk/biostudies/fire/E-MTAB-/114/E-MTAB-11114/Files/ST8059049_web_summary.html)
-   Vitessce demo of this data:
    [http://vitessce.io/#?dataset=spatialdata-visium](http://vitessce.io/#?dataset=spatialdata-visium)
-   Vitessce documentation & information:
    [http://vitessce.io/docs/](http://vitessce.io/docs/)

### Redesign Challenge Task

For this challenge, we ask participants to propose an alternative
visualization approach that links the spot cell-type proportion to the
H&E image. Submissions should consider visualization theory and
principles.

Sketching and prototyping as well as fully interactive solutions will be
accepted. Creativity and novelty will be considered in the evaluation.

### References

Kleshchevnikov, V., Shmatko, A., Dann, E. et al. Cell2location maps
fine-grained cell types in spatial transcriptomics. Nat Biotechnol 40,
661--671 (2022).
[https://doi.org/10.1038/s41587-021-01139-4](https://doi.org/10.1038/s41587-021-01139-4)

Miller, B.F., Huang, F., Atta, L. et al. Reference-free cell type
deconvolution of multi-cellular pixel-resolution spatially resolved
transcriptomics data. Nat Commun 13, 2339 (2022).
[https://doi.org/10.1038/s41467-022-30033-z](https://doi.org/10.1038/s41467-022-30033-z)

## Submission

Submissions will be considered for talk or poster presentations. Please
send a two-page PDF abstract with up to 5 additional figures and a draft
of your proposed poster (max 10MB) to the PCS
[new.precisionconference.com/submissions](http://new.precisionconference.com/submissions).
The abstract should include:

-   aspects of the figure identified as needing improvement or
    clarification,
-   justification of encoding and design choices,
-   at least one or more images of your design
-   optional: a video or screencast to explain the visual encoding

Selected submissions will be invited for talk presentations during the
Bio+MedVis session at the [IEEE VIS 2024](https://ieeevis.org/year/2024/welcome)
conference.

## Evaluation of Submissions

All submissions will be thoroughly reviewed by at least two reviewers,
coming from the challenge chairs and selected domain experts. All
accepted submissions will be published in the conference proceedings.
Winning designs may be invited to become a plugin or extension to
Vitessce.

## Important dates

-   Submission: {{ site.IEEE_deadline_submission }}
-   Notification: {{ site.IEEE_deadline_notification }}
-   Camera-ready version: {{ site.IEEE_deadline_camera }}

## Questions?

Please feel free to ask questions at: biovis_challenge@ieeevis.org.

The chairs of the Bio+MedVis Challenge @ IEEE VIS 2024:

-   [Barbora Kozlikova](https://www.fi.muni.cz/~xkozlik/), Masaryk University, Czech Republic
-   [Nils Gehlenborg](https://dbmi.hms.harvard.edu/people/nils-gehlenborg), Harvard Medical School, USA
-   [Laura Garrison](https://www.laura-garrison.com/), University of Bergen, Norway
-   [Eric Mörth](https://dbmi.hms.harvard.edu/people/eric-moerth), Harvard Medical School, USA
-   [Simon Warchol](https://simonwarchol.com/), Harvard University, USA
-   [Morgan Turner](https://morganlturner.com/), Harvard Medical School, USA
