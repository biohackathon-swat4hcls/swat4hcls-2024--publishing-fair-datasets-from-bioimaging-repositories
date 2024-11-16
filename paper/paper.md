---
title: 'SWAT4HCLS 2024 report: Publishing FAIR datasets from Bioimaging repositories'
title_short: 'SWAT4HCLS #7: FAIR Bioimaging repositories publishing'
tags:
  - Bioimaging
  - publishing
  - FAIR
authors:
  - name: Stefan Dvoretskii
    affiliation: 1
  - name: Philipp Schader
    orcid: 0000-0002-6075-0757
    affiliation: 1, 2
  - name: Marco Nolden
    orcid: 0000-0001-9629-0564
    affiliation: 1, 2, 3
  - name: Josh Moore
    orcid: 0000-0003-4028-811X
    affiliation: 4, 5, 6
affiliations:
  - name: DKFZ Division of Medical Computing
    index: 1
  - name: Helmholtz Metadata Collaboration (HMC) Hub Health, DKFZ, Heidelberg, Germany
    index: 2
  - name: Pattern Analysis and Learning Group, Heidelberg University Hospital
    index: 3
  - name: German BioImaging e.V., University of Konstanz, Germany
    index: 4
  - name: National Research Data Infrastructure for Microscopy and BioImage Analysis (NFDI4BIOIMAGE)
    index: 5
  - name: Open Microscopy Environment (OME)
    index: 6
date: 9 October 2024
cito-bibliography: paper.bib
event: SWAT4HCLS24
biohackathon_name: "SWAT4HCLS"
biohackathon_url:   "[https://biohackathon-europe.org/](https://www.swat4ls.org/workshops/leiden2024/hackathon/)"
biohackathon_location: "Leiden, The Netherlands, 2024"
group: Group 7
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-swat4hcls/swat4hcls-2024--publishing-fair-datasets-from-bioimaging-repositories.git
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: S. Dvoretskii, P. Schader, M. Nolden, J. Moore
---


# **Introduction**

During the SWAT4HCLS 2024 hackathon, a group of participants from various
research initiatives and consortia in bioimaging and medical imaging, including
German BioImaging e.V, the Helmholtz Metadata Collaboration (HMC) Hub Health,
the Division of Medical Image Computing at the German Cancer Research Center
(DKFZ) and the EU Horizon project CCE\_DART (Data Rich Clinical Trials), came
together.

With 2024 being the 10-year anniversary of FAIR data, our discussion quickly
came to revolve around the state of FAIR access to bioimaging data, and ideas
how to improve it. Within the research bioimaging community, the Open
Microscopy Environment (OME) Consortium has been working to standardize access
to large-scale imaging data. The OME consortium is a long-term effort which has
produced rich software and standards (\>=2000). Imaging Data Resource (IDR) has
appeared as an annotation rich imaging portal in 2016\. As of today, it
provides access to 130 Studies with more than 400TB data in more that 14
million images, continuously growing. ([@usesMethodIn:Williams2017]). 

Similarly, to facilitate multi-centric research on medical imaging data the
Kaapana framework ([@usesMethodIn:scherer2020joint]) was created. It provides
an open-source framework based on cloud native technologies enabling the
large-scale analysis of medical imaging data as well as sharing analysis
methods across installations. Primary data as well as analysis results can be
stored in the platform and metadata for example from DICOM images is extracted
to support cross-center definition and curation of imaging patient cohorts.
Multi center data discovery, like in the DART project of Cancer Core Europe
(CCE) also requires approaches for managing and sharing catalogs of metadata. .

Though much data is available, to optimize re-use the FAIRness of data in
research repositories like the IDR could be further improved. A common,
harmonized representation of the metadata is needed, both for discovery as well
as linking to other resources outside the imaging domain. We propose RDF is the
best mechanism for that connection
([@citesAsPotentialSolution:moore_2024_10687659]), but a catalog is needed to
make the produced RDF triples discoverable.


# **Goals**

During the hackathon, we assessed the implementation of the FAIR principles in
the current bioimaging and clinical imaging data repositories. Additionally, to
make the RDF export triples from the IDR discoverable, we also explored the
Fair Data Point interface ([@citesAsAuthority:da2023fair]), as a mechanism to
facilitate the exposure of machine-actionable metadata and how it could be
added to the Imaging Data Resource (IDR) portal. 


# **Results**

To classify the real-world problems with imaging datasets, we formulated a new
“tier” system for publicly available datasets. This tier system grades datasets
on a scale of their compliance with best data practices. It complements
existing assessments like the FAIR principles or the 5-star Open Data system
([@discusses:Berners-Lee_2009]). While existing tools assess the principal
readiness of the data to be FAIR and interlinked, mainly from a technical
perspective, the proposed tier system focuses on tangible amount of manual
labor that is required to obtain necessary metadata and download public imaging
datasets, e.g. finding the right contact person, filling out forms, machine
access to metadata or the actual data etc.

We will continue to work on a more precise tier system formulation to indicate
typical real-world access problems with public imaging datasets, and propose
ways to improve accessibility. On the technical side, we were successful to
gain a working knowledge and fix multiple bugs in the FDP implementation for
the IDR. We plan to carry on this work at upcoming hackathons, e.g. the
[3rd BioHackathon Germany (denbi.de)](https://www.denbi.de/de-nbi-events/1678-biohackathon-germany-3).


### **Cultural change, community building and tool development**

We agreed the road to a FAIR data space in the bioimaging community poses
challenges on very different levels. Some are community or domain specific,
others are more general. Within the Helmholtz Association, the Helmholtz
Metadata Collaboration is a platform of the Incubator for Information and Data
Science aims at supporting infrastructures and researchers on their way to
implementing a FAIR data space by providing guidance and tools,

Furthermore, the hackathon working group was composed of individuals both from
the Open Microscopy Environment (OME) and Digital Imaging and Communications in
Medicine (DICOM) domains. This meeting of cross research and medical
communities proved fruitful in addressing cross-sectional problems, and the
continuation of this collaboration could lead to a cultural change.


# **Funding**

**CCE\_DART** has received funding from the European Union’s Horizon 2020
research and innovation programme under grant agreement No 965397.
**NFDI4BIOIMAGE** is funded by DFG grant number NFDI 46/1, project number
501864659.

# **References**
