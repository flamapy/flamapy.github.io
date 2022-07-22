---
title: "Feature model metamodel"
date: 2018-12-28T15:14:39+10:00
weight: 2
promoted: true
---

The feature model plugin provides the metaclases required to work with feature models

# Description
One of the main parts of this framework is the feature model metamodel. This plugin provides i) the metaclasses required to store and manipulate cardinality based feature models; ii) a transformation into the PySAT metamodel; iii) a set of models to text, and, text to model transformations to read and save feature model serializations.

This is enabling the reading and saving of feature models into XML and Json files [22]; and, iv) a set of operations to extract information from the structural properties of the model. This is, counting the number of features, the number of cross-tree constraints, the branching factor, etc


# Objectives

The core plugin provides the following functionallity

1. Storage and manipulation of feature models
2. Read and store of feature models
3. Implement operations that do not rely on solvers backend

# Operations
Currently, this plugin enables the following operations. Note that these operations are executed without a backend solver which makes them scalable and fast while having some limitations:

* Atomic sets
* Average Branching factor
* Core Features
* Count leafs
* Estimated product number
* Feature ancestors
* Leaf features
* Max depth tree
* Average Branching factor


# Transformations supported
Currently this plugins enables a set of TextToModel transformations (a.k.a Parsers) and ModelToText transformations (a.k.a serializations) for the most common variability serializations found in the literatures. Concretely we support:

|    Format   |  Model2Text  |    Text2Model   |
| ----------- | ------------ | --------------- |
| AFM (Fama format)   | [x]  |        [x]      |
| Feature IDE |              |        [x]      |
| Glencoe     |     [x]      |        [x]      |
| Splot       |     [x]      |                 |
| UVL         |     [x]      |        [x]      |
| Fama XML    |              |        [x]      |
| Json        |     [x]      |                 |


## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/fm_metamodel)