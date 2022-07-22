---
title: "SAT metamodel"
date: 2019-01-28T15:15:26+10:00
weight: 3
promoted: true
---

The pysat model plugin provides the metaclases required to work with 
SAT models and to transform feature models into SAT.

# Description
This plugin implements the classes to perform AAFM using the [PySAT](https://pysathq.github.io/) metasolver. This is, it encompases the set of variables and constraints objects to execute the analysis operations using PySAT as the backend. This allows us to rely on more than ten SAT solvers. This plugin offers the following functionality: i) the metaclases required run the sat instance representing our feature models; ii) a set of operations to extract information from the models; iii) a set of model to text transformations to save the CNF representation of the current SAT instance.

# Objectives

The core plugin provides the following functionallity

1. Storage and manipulation of SAT
2. Read and store of SAT models
3. Implement operations that require a complex analysis
4. Transform feature models into SAT models

# Operations
Currently, this plugin enables the following operations. 

* Commonality
* Core Features
* Dead features detection
* Error detection
* False optional detection
* Filter
* List products
* Products number
* Valid
* Valid product (full configuration)
* Valid configuration (partial configuration)


# Transformations supported
Currently this plugins enables a set of transformations for CNF and feaute models. Concretely we support:

|    Format/model   |  Model2Model | Model2Text  | Text2Model  |
| -----------       | ------------ | ----------- | ----------- |
| Feature model     | [x]          |             |             |
| CNF               |              |             |  [x]        |


## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/pysat_metamodel)