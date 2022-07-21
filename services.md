---
title: Plugins
layout: services
description: Plugins
intro_image: "images/illustrations/simplified_aafm.png"
intro_image_absolute: false
intro_image_hide_on_mobile: true
---

# Plugins to provide extensive support on analysis opeations

This framework considers plugins as a first order element on its designs. A plugin consists on three main modules:

* Metamodel classes: This module encapsulates all the needed classes to support the plugin’s functionality. For example, in an OVM-metamodel, it would store the information about the VPs and variants. Also, in a CSP plugin, it will host the classes required to execute the CSP solver.

* Operations: This module is where the operations using the elements in the metamodel are implemented. Each operation returns a set of metrics or information after being called. For example, a CSP plugin could provide an operation to check whether an attributed feature model is valid or not.

* Transformations: This is where the transformations between models are defined. This module supports three model transformations flavors.