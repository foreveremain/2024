---
layout: page
title: Bio+MedVis Challenge
permalink: /biovisChallenges_vis/
---

# Bio+MedVis Challenge @ IEEE VIS 2023

{% include_relative biovis_challenge_news.html %}

## Summary

This year’s challenge will be based on a study recently published in Cancer Cell
by the ProCan® team ([Gonçalves et al.,
2022](<https://www.cell.com/cancer-cell/fulltext/S1535-6108(22)00274-4>)). The
study generated a comprehensive pan-cancer proteomic map of 949 human cancer
cell lines to aid in the discovery of cancer biomarkers and targets for the
development of new cancer treatments. The primary goals of this challenge can be
found in the "Challenge tasks" section. This year, in addition to the
description below and the slack channel, we will also hold an online Q&A session
where you can directly ask questions to the ProCan team. The date/time of this
session will be announced here, as well as our slack
([https://biovis2016.slack.com/](https://biovis2016.slack.com/)) and twitter
([@biovis_net](https://twitter.com/biovis_net)) channels.

## Biological Background and Data Description

The ProCan team used mass spectrometry-based proteomics to identify and quantify
proteins in 949 human cell lines that represented 28 different tissue types and
over 40 genetically and histologically diverse cancer types. These cell lines
were treated with 625 anti-cancer compounds and for many of them over 17,000
gene essentialities had been tested via CRISPR-Cas9 knockout screens. The
analysis resulted in a dataset of approximately 8,500 proteins that were
quantified across the cell lines, capturing cell type features and evidence of
post-transcriptional control of protein levels. This dataset was then further
analyzed using a deep learning-based pipeline that integrated multi-omics, drug
response, and CRISPR-Cas9 gene edits; this analysis revealed thousands of
statistically significant protein biomarkers of cancer vulnerabilities that were
not significant at the transcript level. Overall, the ProCan team found that the
power of the proteome to predict drug response was very similar to that of the
transcriptome. Interestingly, the team also found that random downsampling to
only 1,500 proteins had limited impact on the ability to predict drug responses,
consistent with protein networks being highly connected and co-regulated. This
proteomic dataset is a high-quality resource for mechanistic investigation of
network organisation and regulatory principles of the proteome, as well as for
translational discoveries.

## Data Sets

The data are provided by domain experts from ProCan, Children’s Medical Research
Institute, The University of Sydney.

1. A peptide data matrix of 949 cell lines with 79,621 quantified peptides.
2. A protein data matrix of 949 cell lines with 8,498 quantified proteins.
3. An annotation file of tissue and cancer types.
4. Drug response data.

The intensity values of peptides and proteins have been averaged over six
replicates. The drug response data record 578,238 half-maximal inhibitory
concentrations (IC50) of the 625 anti-cancer drugs. The data are available
under the following link:
[Dropbox](https://www.dropbox.com/sh/0nemsahltwwstjp/AADb9f6b99K4z2XUPwsJf96Qa?dl=0)

## Challenge tasks

The figure ([Gonçalves et al.,
2022](<https://www.cell.com/cancer-cell/fulltext/S1535-6108(22)00274-4>)) below
provides an overview of the study, which displays a comprehensive pan-cancer
proteomic map. This map quantifies proteomes of 949 human cancer cell lines
originating from 28 distinct tissues and over 40 diverse cancer types, analysed
using six mass spectrometers.

<figure>
    <img src="../images/biovis-challenge/goncalves-graphical-abstract.jpg" alt="Graphical Abstract">
</figure>

The following tasks provide guidelines for your submission. We also welcome
submissions that do not solve all of these tasks and only focus on a subset
thereof:

1. The first task is to create an easy-to-understand visualization of peptide
   and protein intensities by including phenotypic information about tissue and
   cancer types. This challenge requires a user-friendly and interactive solution
   that helps researchers explore the complex data in an engaging way and reveal
   hidden patterns. Here, the participants can define subcategories for protein
   groups, such as house-keeping proteins, tissue-specific and cancer-specific
   proteins.
2. Extracting meaningful insights from the existing peptide and protein data
   matrices and annotation files, as the relevant information is not easily
   accessible or comprehensible in a tabular format. This challenge calls for
   participants to create an intuitive visualization that seamlessly connects drug
   responses to their respective proteins and cell lines.
3. Create an interactive tool to visualise drug response data across cell lines
   in relation to their proteomic data. The tool should allow users to select a
   protein and analyse drugs that target them. Similarly, it should also allow
   users to select a specific drug and visualise proteins that are strongly
   associated with the drug response. The drug response data can be retrieved from
   [https://www.cancerrxgene.org/downloads/bulk_download](https://www.cancerrxgene.org/downloads/bulk_download)
   and protein-drug association information can be found in Supplementary Table 5
   of the paper ([Gonçalves et al.,
   2022](<https://www.cell.com/cancer-cell/fulltext/S1535-6108(22)00274-4>)).

### Design challenge: Re-design an existing visualization

In addition to the main challenge, we also host a complementary design
challenge. Teams that submitted entries to the main challenges are allowed to
also submit to the design challenge track and vice versa.

For this challenge, submitters are asked to improve the current protein network
plot in Fig. 7F ([Gonçalves et al.,
2022](<https://www.cell.com/cancer-cell/fulltext/S1535-6108(22)00274-4>)) by
creating an interactive and responsive visualization of the protein network.
This solution should allow users to zoom in and out, focus on specific proteins,
and explore the relationships between them more easily. Suggestions for features
that can be developed: pop-up annotations when a user hovers over a protein
node; and a search function that enables users to quickly locate proteins of
interest. Color-coding and distinct symbols can be used to represent different
types of proteins or protein functions.

## Program

The Bio+MedVis Challenge, jointly organized by the [BioVis](../) and
[VCBM](https://conferences.eg.org/vcbm2023/) communities, will be organized as a
half-day event within the [IEEE VIS 2023](https://ieeevis.org/year/2023/welcome)
conference. The program will consist of invited talks (we are happy to announce
that [Drew Berry](https://www.wehi.edu.au/people/drew-berry) already confirmed
our invitation), presentations of accepted submissions, and other supplementary
sessions. Details will follow soon.

## Important dates

-   Submission: <time>{{ site.IEEE_deadline_submission }}</time>
-   Notification: <time>{{ site.IEEE_deadline_notification }}</time>
-   Camera-ready version: <time>{{ site.IEEE_deadline_camera }}</time>

## Submission

Submissions will be considered for talk and/or poster presentations. You will be
requested to submit a two-page PDF abstract with unlimited additional figures
and a draft of your proposed poster (max 10MB) to the PCS. The deadlines will be
announced soon. Last year, the acceptance rate for presentations was 89%; such
an acceptance rate is not guaranteed. Selected submissions will be invited for
talk presentations during the Bio+MedVis Challenge session within the [IEEE VIS
2023](https://ieeevis.org/year/2023/welcome) conference.

## Questions?

Please feel free to ask questions on our Slack channel if you need more
information and details about the data or tasks:  
[biovis2016.slack.com](https://biovis2016.slack.com/) » #biovis-challenge2023

Otherwise, feel free to contact us at: biovis_challenge@ieeevis.org

## The chairs of the Bio+MedVis Challenge @ IEEE VIS 2023

[Barbora Kozlikova](https://www.fi.muni.cz/~xkozlik/), Masaryk University, Czech Republic  
[Daniel Jönsson](https://liu.se/en/employee/danjo37), Linköping University, Sweden  
[Renata Raidou](https://renataraidou.com/), TU Wien, Austria  
[Sean O'Donoghue](https://www.garvan.org.au/about-us/people/seaodo), Garvan Institute of Medical Research, Sydney

## References

E. Gonçalves, et al., Pan-cancer proteomic map of 949 human cell lines, Cancer
Cell. 40 (2022) 835–849.
