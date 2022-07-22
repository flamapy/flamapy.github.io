---
title: "BDD metamodel"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
---

The BDD model plugin provides the metaclases required to work with 
SAT models and to transform feature models into BDD.

## Description
This plugin supports Binary Decision Diagrams (BDDs) representations for feature models.

This is the architecture followed by this plugin:

![Architecture](https://raw.githubusercontent.com/flamapy/bdd_metamodel/master/doc/bdd_plugin.png)

The BDD plugin relies on the [dd](https://github.com/tulip-control/dd) library to manipulate BDDs.
The complete documentation of such library is available [here](https://github.com/tulip-control/dd/blob/main/doc.md).

The following is an example of feature model and its BDD using complemented arcs.

![FM Example](https://raw.githubusercontent.com/flamapy/bdd_metamodel/master/doc/fm_example.png)

![BDD Example](https://raw.githubusercontent.com/flamapy/bdd_metamodel/master/doc/bdd_example.svg)


# Objectives

The core plugin provides the following functionallity

1. Storage and manipulation of BDD
2. Read and store of BDD models
3. Implement operations that require a complex analysis
4. Transform feature models into BDD models

# Operations
Currently, this plugin enables the following operations. 

* Sampling
* Feature Inclusion Probability
* Product distribution
* List products
* Products number
* Uniform sampling

# Transformations supported
Currently this plugins enables a set of transformations for CNF and feaute models. Concretely we support:

|    Format/model   |  Model2Model | Model2Text  | Text2Model  |
| -----------       | ------------ | ----------- | ----------- |
| Feature model     | [x]          |             |             |
| BDD               |              |             |  [x]        |


## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/bdd_metamodel)