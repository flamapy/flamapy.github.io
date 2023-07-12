---
title: "Flama Feature Model Distribution"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
layout: distribution
---
## Flama as a feature model analysis tool

As we have shown, the Flama framework could be adapted to support other kinds of variability descriptions by creating new plugins that represent the meta-classes to define it and the transformation to any existing reasoning technique. This is, for example, the case of a plugin to analyze software dependencies with security concerns information. However, its main purpose is the analysis of feature models. Because of that, Flama provides a single Python package that installs all the required plugins and provides a more straightforward usage of the tooling.

Concretely, this pip package provides the following operations implementations:

1. Average Branching factor: This refers to the average number of child features that a parent feature has in a feature model. It's calculated by dividing the total number of child features by the total number of parent features. A high average branching factor indicates a complex feature model with many options, while a low average branching factor indicates a simpler model.
2. Leaf count: This operation counts the number of leaf features in a feature model. Leaf features are those that do not have any child features. They represent the most specific options in a product line.
3. Estimated number of products: These are the features that are directly or indirectly the parent of a given feature in a feature model. Ancestors of a feature are found by traversing up the feature hierarchy. This information can be useful to understand the context and dependencies of a feature.
4. Feature ancestors: These are the features that are directly or indirectly the parent of a given feature in a feature model. Ancestors of a feature are found by traversing up the feature hierarchy. This information can be useful to understand the context and dependencies of a feature.
5. Leaf features: This operation returns the leaf features if they are found in the model. If the model does not follow the UVL specification, an exception is raised, and the operation returns False.
6. Max depth: This operation returns the max depth of the tree. If the model does not follow the UVL specification, an exception is raised, and the operation returns False.
7. Commonality: This is a measure of how often a feature appears in the products of a product line. It's usually expressed as a percentage. A feature with 100% commonality is a core feature, as it appears in all products.
8. Core features: These are the features that are present in all products of a product line. In a feature model, they are the features that are mandatory and not optional. Core features define the commonality among all products in a product line. This call requires sat to be called; however, there is an implementation within Flama that does not require sat. Please use the framework in case of needing it.
9. Valid configuration: This is a combination of features that satisfies all the constraints and dependencies in the feature model. A valid configuration can be turned into a product.
10. Valid product: This is a product that is produced from a valid configuration of features. A valid product satisfies all the constraints and dependencies in the feature model.
11. Valid model: In the context of feature models, this usually refers to whether the feature model itself satisfies all the constraints and dependencies. A valid feature model is one that does encode at least a single valid product.

Moreover, it also provides the following interfaces:

1. Swagger UI API: Currently, Flama-FM provides a Swagger UI-based documentation that provides easy integration for those tools that do not rely on the Python framework. This API can be accessed (with restrictions on [URL](URL)), also it can be deployed on any server using Docker.
2. Command-line interface: While the Flama framework already provides a command line interface, flama-fm emphatises this by enabling a more complete and useful CMD based on Fire.
3. Simplistic Python programming interface: Finally, for the sake of easy of use when using a new framework such Flama, we are providing an easy interface to execute the feature model operations. This is, a class that you instantiate passing as a single argument the path for the model in any of the supported formas and then we can call queries by simple methods of that class. This pattern was sucesfull for examample in Familiar. Below you can find a simple snipet of how you can use this class. 

## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/flama-fm-dist)