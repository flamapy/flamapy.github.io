---
layout: default
title: Community
nav_order: 3
has_children: true
description: "flamapy friends"
permalink: /community
---

# flamapy friends and associated projects

As mentioned in the documentation, the aim of flamapy is to reuse analysis in different circumstances. This section presents a set of projects and papers that either use flamapy or are linked to its development. 

## UVL grammar
Feature modeling is a cornerstone of software product line engineering, providing a means to represent software variability through features and their relationships. Since its inception in 1990, feature modeling has evolved through various extensions, and after three decades of development, there is a growing consensus on the need for a standardized feature modeling language. Despite multiple endeavors to standardize variability modeling and the creation of various textual languages, researchers and practitioners continue to use their own approaches, impeding effective model sharing. 

In 2018, a collaborative initiative was launched by a group of researchers to develop a novel textual language for representing feature models. This effort resulted in the Universal Variability Language (UVL), a human-readable language that serves as a pivot language for diverse software engineering tools. The development of UVL drew upon community feedback and leveraged established literature in the field of variability modeling. The language is structured into three levels – Boolean, Arithmetic, and Type – and allows for language extensions to introduce additional constructs enhancing its expressiveness. 

UVL is integrated into various existing software tools, such as FeatureIDE and flamapy, and is maintained by a consortium of institutions. All tools that support the language are released in an open-source format, complemented by dedicated parser implementations for Python and Java. Beyond academia, UVL has found adoption within a range of institutions and companies. It is envisaged that UVL will become the language of choice in the future for a multitude of purposes, including knowledge sharing, educational instruction, and tool integration and interoperability. UVL aims to address the limitations of prior attempts and foster collaboration and innovation in the domain of software product line engineering.

* [TOOL](https://universal-variability-language.github.io/)
* [Paper]()


## flamapy.ide
Feature modeling is widely used to represent variability in software systems, but as feature models grow in size and complexity, manual analysis becomes infeasible. Automated Analysis of Feature Models (AAFM) is a set of tools and algorithms that enable the computer-aided analysis of such models. Recently, the AAFM community has made an effort to enable the interoperability of tools by means of the UVL language. However, most of the supporting tools need to execute the operations on a server. This has two main drawbacks: first, it requires users to upload the model to remote servers, raising security concerns; and second, it limits the complexity of the operations that an online tool can offer. 

flamapy.ide is an integrated development environment (IDE) based on the flamapy framework, designed to perform AAFM directly within the browser by relying on WASM technologies. flamapy.ide provides SAT and BDD solvers for efficient feature model analysis and offers support for handling UVL files. Additionally, it enables the configuration and visualization of such models, relying on a fully client-side approach. This tool brings AAFM capabilities to web-based platforms, eliminating the need for server-side computation while ensuring ease of use and accessibility.

* [TOOL](http://ide.flamapy.org)
* [Paper]()

## UVLHub
Feature models are the de facto standard for modeling variabilities and commonalities in features and relationships in software product lines. They are the base artifacts in many engineering activities, such as product configuration, derivation, or testing. Concrete models in different domains exist; however, many are in private or sparse repositories or belong to discontinued projects. The dispersion of knowledge of feature models hinders the study and reuse of these artifacts in different studies. 

The Universal Variability Language (UVL) is a community effort textual feature model language that promotes a common way of serializing feature models independently of concrete tools. Open science principles promote transparency, accessibility, and collaboration in scientific research. Although some attempts exist to promote feature model sharing, the existing solutions lack open science principles by design. In addition, existing and public feature models are described using formats not always supported by current tools. 

UVLHub is introduced as a repository of feature models in UVL format. This tool provides a front end that facilitates the search, upload, storage, and management of feature model datasets, improving the capabilities of discontinued proposals. Furthermore, UVLHub communicates with Zenodo – one of the most well-known open science repositories – providing a permanent save of datasets and following open science principles. It includes existing datasets and is readily available to include new data and functionalities in the future. UVLHub is maintained by three active universities in variability modeling.

* [TOOL](https://www.uvlhub.io/)
* [Paper](https://doi.org/10.1016/j.jss.2024.112029)

## FM FactLabel
FM Fact Label is a tool for visualizing the characterizations of feature models based on their metadata, structural measures, and analytical metrics. Although there are various metrics available to characterize feature models, there is no standard method to visualize and identify unique properties of feature models. Unlike existing tools, FM Fact Label provides a standalone web-based platform for configurable and interactive visualization, enabling export to various formats. This contribution is significant because it supports the Universal Variability Language (UVL) and enhances the UVL ecosystem by offering a common representation of the results of existing analysis tools.

* [TOOL](https://fmfactlabel.adabyron.uma.es/?v=1.7.0)
* [Paper](https://doi.org/10.1016/j.scico.2024.103214)

