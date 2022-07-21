---
title: Plugins
layout: services
description: Plugins
intro_image: "images/illustrations/simplified_aafm.png"
intro_image_absolute: true
intro_image_hide_on_mobile: true
---

# Plugins to provide extensive support on analysis opeations

This framework considers plugins as a first order element on its designs. A plugin consists on three main modules:
* metamodel classes: This module encapsulates all the needed classes to support the plugin’s functionality. For example, in an OVM-metamodel, it would store the information about the VPs and variants. Also, in a CSP plugin, it will host the classes required to execute the CSP solver.
* operations: This module is where the operations using the elements in the metamodel are implemented. Each operation returns a set of metrics or information after being called. For example, a CSP plugin could provide an operation to check whether an attributed feature model is valid or not. Usually,
this module offers the implementations for the operations defined in the core. However, it is also possible to provide a new operation implementation without the need to have it previously defined in the core.
* transformations: This is where the transformations between models are defined. This module supports three model transformations flavors.
    * Text to model (T2M): This set of plugins is responsible for reading metamodels instances out of text files.
    * Model to text (M2T): This set of plugins generates the serializations of the models supported by the framework.
    * Model to model (M2M): This set of plugins are implementing model to model transformation. This is, these plugins are responsible for translating the models to a reasoning logic or to other variability model.
