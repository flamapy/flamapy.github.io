---
title: "Core"
date: 2018-11-18T12:33:46+10:00
weight: 1
promoted: true
proyect_url: "https://www.github.com/flamapy/core"
---

The core component is the main entry point of Flama

# Description
The core component of this framework has three primary purposes. First, to provide a set of interfaces that serve as communicating components between the different plugins and the core. Second, to orchestrate the different plugins available in a Python installation. Finally, to help developers to create new plugins. To fulfill the first purpose, it provides interfaces for the different transformations we can define. Those are model to text (M2T), text to model (T2M), and model to model (M2M). Those transformations
allow the reading and saving of model serializations as well as implement the translation between variability models and solvers, which are both threated as metamodels in this architecture. Also, it does provide a set of common interfaces for the operations over feature models


![Architecture](/images/illustrations/architecture.png)

# Objectives

The core plugin provides the following functionallity

1. Orchestrating the execution by providing a common interface with the end user. Currently three interfaces are offered:
  * As a command line utility
  * As a Python library to be embeded in your proyect
  * As a REST API to be consumed. 
2. Help with the creating of skeletons for future plugins. In order to increment the number of plugins and ease the creation the core plugin offers commands to generate empty plugins to be implemented
3. Offers a set of interfaces (yes interfaces in Python) for automated analysis operations to be implemented.  

## Repository

You can find the repository of this plugin in [HERE](https://www.github.com/flamapy/core)