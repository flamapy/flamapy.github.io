---
title: Distributions
layout: distributions
description: Distributions
intro_image: "images/illustrations/simplified_aafm.png"
intro_image_absolute: false
intro_image_hide_on_mobile: true
---

# Easier ussage for feature model users

1. Swagger UI API: Currently, Flama-FM provides a Swagger UI-based documentation that provides easy integration for those tools that do not rely on the Python framework. This API can be accessed (with restrictions on [URL](URL)), also it can be deployed on any server using Docker.
2. Command-line interface: While the Flama framework already provides a command line interface, flama-fm emphatises this by enabling a more complete and useful CMD based on Fire.
3. Simplistic Python programming interface: Finally, for the sake of easy of use when using a new framework such Flama, we are providing an easy interface to execute the feature model operations. This is, a class that you instantiate passing as a single argument the path for the model in any of the supported formas and then we can call queries by simple methods of that class. This pattern was sucesfull for examample in Familiar. Below you can find a simple snipet of how you can use this class. 