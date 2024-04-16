---
title: 'BioHackEU23 report: Template for the very long title'
title_short: 'BioHackEU23 #26: unknown chemical substances'
tags:
  - cheminformatics
  - PubChem
  - unknown chemical substances
authors:
  - name: First Author
    affiliation: 1
  - name: Last Author
    orcid: 0000-0000-0000-0000
    affiliation: 2
affiliations:
  - name: First Affiliation
    index: 1
  - name: Second Affiliation
    index: 2
date: 8 November 2023
cito-bibliography: paper.bib
event: BH23EU
biohackathon_name: "BioHackathon Europe 2023"
biohackathon_url:   "https://biohackathon-europe.org/"
biohackathon_location: "Barcelona, Spain, 2023"
group: Project 26
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackrxiv/publication-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---


# Introduction

As part of the BioHackathon Europe 2023, we here report...



# Bioimaging dataset aggregation projects

Automated processing workflows and Machine Learning make it instructable to combine different datasets from across the different research institutions and consortia. In the ideal world, it would then be possible to make automatic queries across the various research data repositories to pull the required images and the adjacent metadata automatically in one place with minimal manual involvence / correction. Unfortunately, that is not the case because of the variety of reasons.

## Problems with FAIRness of bioimaging datasets

### Tiers of the problems

In SWAT4HCLS this year, there were a lot of posters about FAIR Data Points (FDP). However, in the reality of "scraping web" for imaging data the FDPs are simply not provided in most of the cases. Some imaging datasets in life sciences (e.g. BABRI `[@citesAsDataSource:yang2021early]` ) have not even a clear way to access the data **manually**, i.e. the data is accessible on paper but in reality the website has been taken down, the corresponding author does not respond or similar.

Maybe, the issues can be roughly classified as following tier structure:
Tier 0: the corresponding author is not reachable and/or the dataset is not exposed on the web 
Tier 1: the author is reachable, but there are not even a proper metadata file **internally** that describes the dataset well
Tier 2: there is an exposed metadata which is not/poorly structured and helps not to understand the dataset **manually**
Tier 3: metadata is machine readable, but the dataset is not accessible in an automatic way (arguably re3data published datasets `[@citesAsDataSource:pampel2013making]`)
Tier 4: metadata is machine readable, dataset is accessible automatically but not in a really FAIR way
Tier 5: metadata is machine readable and dataset is FAIRly accessible

In following, I extend on the proposed main pitfalls of some tiers.

### Tier 0: dataset is not published

That's it. We might know there are some big amounts of data which could help to save lives, improve diagnosis and provide other helpful function to the imaging / clinical community, but they are just not accessible, and the data about them is false or inaccessible.

### Tier 1: FAIR metadata is not supplied

Apparently, the topics like data provenance, data quality and data interpretability are not important enough on that tier that at least a human-readable description of the dataset in one place is added. Metadata is scattered across the publication, the website, the supplementary publication information and takes a really hard effort to find. For example, an analysed dataset (`[@citesAsDataSource:nymberg2013analytical]`) took around a 5 human-hours effort to scrape manually the documentation, the original paper and the website for the _number of unique 3D volumes of MRI images_ in the study. The next part was contacting the dataset owners directly. They were helpful, but only provided the _estimate_ of the number of images in the dataset.
This approach clearly does not scale well and is nothing for Big Data analysis.

### Tier 3-4: Endless manual request and licensing issues

The data is there, but in order to access it we have to face gigantic bureaucratic hurdles. Nowadays it means filling 3-4 page paper documents for access and license agreements (`[@citesAsAuthority:DataUsag94-online]`), facing days-long e-mail conversations with responsible digitization officers about analysis specifics (especially if it is in a protected research environment), all of which is severely affecting working hours spent to fetch the datasets as well as push the deadlines of the potential data project back significantly.

### Tier 3-4: Access points are not FAIR

It's great if sometimes with significant manual effort one gains the access to the dataset. Next step? Copy-paste the login credentials. Find out how to install the NBIA data retriever (`[@citesAsAuthority:NBIAData67-online]`). Fetch the metadata in the table with differences in structure for each of the TCIA published datasets! There are so many wonderful concepts in Semantic Web like triple stores, FDPs et cetera, but let's face the reality: even "big players" like TCIA do not employ these services as of now. 

## Who to blame and what to do






-

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables and figures

Tables can be added in the following way, though alternatives are possible:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

A figure is added with:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
