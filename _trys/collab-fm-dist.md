---
title: "Use the FM distribution in Google Colab"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
layout: try

---
## Flama Fm distribution in Google Colab
[Go to Google Colab](https://colab.research.google.com/drive/1moSXdK3thM44UIV6NVF3RfjtMxhJLzfs?usp=sharing)
[![Goto Google Colab](/images/illustrations/colab.png)](https://colab.research.google.com/drive/1moSXdK3thM44UIV6NVF3RfjtMxhJLzfs?usp=sharing)

This tutorial also executes in Google Colab. In this case, what we are using is the Feature Model oriented distribution. This tutorial offers a Jupyter notebook interface eliminating the need for local installations or setups. Concretely the tutorial demonstrates the usage of the Flamapy Feature Model distribution. The notebook includes installation commands, some UVL file downloads, and examples of using the distribution through different interfaces.

Here are the main steps covered in the notebook:

1. Installation: The Flamapy Feature Model distribution is installed using the `pip` command. Additionally, two files required for testing are downloaded using the `wget` command. Those files are UVL models and configurations.

2. Command-line Usage: The notebook demonstrates the usage of the Flamapy Feature Model distribution through the command line. Three commands are executed using `flamapy-fm-cli`: `valid`, `products`, and `valid_configuration`. These commands take different arguments and provide different outputs.

3. Programming Interface: The notebook shows how to use the Flamapy Feature Model distribution through a simple programming interface. Two examples are provided using the `FLAMAFeatureModel` class. In the first example, the feature model is loaded, and the `valid()` method is called to check the validity of the model. In the second example, the `valid_configuration()` method is used to validate a configuration specified in a CSV file.

4. REST API Programming Interface: The notebook briefly mentions using the Flamapy Feature Model distribution through a REST API programming interface. It mentions downloading the code, installing ngrok, and accessing it within Google Colab. However, it suggests referring to the Flamapy GitHub repository for detailed instructions on using Docker or a local installation for this interface.

The notebook provides an overview of how to install and use the Flamapy Feature Model distribution through different interfaces, including the command line, programming interface, and REST API.
