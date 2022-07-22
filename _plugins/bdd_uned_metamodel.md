---
title: "BDD metamodel - Colosal FM's"
date: 2019-05-18T12:33:46+10:00
weight: 5
---

The BDD model plugin provides the metaclases required to work with 
colosal feature models and transform them to BDD.

However, this implementation is relying on the optimizations performed in the paper Ruben Heradio, David Fernández-Amorós, José A. Galindo, David Benavides, Don S. Batory: Uniform and scalable sampling of highly configurable systems. Empir. Softw. Eng. 27(2): 44 (2022) which enables a better scalability of the analysis. 

## Description
This plugin supports Binary Decision Diagrams (BDDs) representations for feature models.

# Objectives

The core plugin provides the following functionallity

1. Increase scalability for colosal feature models

# Operations
Currently, this plugin enables the following operations. 

* Sampling
* Feature Inclusion Probability
* Product distribution


# Transformations supported
Currently this plugins enables a set of transformations for CNF and feaute models. Concretely we support:

|    Format/model   |  Model2Model | Model2Text  | Text2Model  |
| -----------       | ------------ | ----------- | ----------- |
| Feature model     | [x]          |             |             |
| DDDMP               |              |     [x]        |  [x]        |
| SPLX | | | [x]|

## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/bdd_metamodel)