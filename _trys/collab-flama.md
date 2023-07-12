---
title: "Use Flama in Google Colab"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
layout: try

---
## Execute and test Flama in Google colab
[Go to Google Colab](https://colab.research.google.com/drive/1ktuEn2KAqv7dbzeHQc-G_kUxUEW-n_av?usp=sharing)
[![Goto Google Colab](/images/illustrations/colab.png)](https://colab.research.google.com/drive/1ktuEn2KAqv7dbzeHQc-G_kUxUEW-n_av?usp=sharing)

Google Colab, short for Google Colaboratory, is a cloud-based development environment provided by Google. It offers a Jupyter notebook interface that allows users to write and execute Python code directly in a web browser, eliminating the need for local installations or setups.

This tutorial explores the different steps and actions to use Flama. This involves preparing the execution environment, installation of plugins, using the framework as an end user, using it as a developer, and creating a new plugin.

Preparing the execution environment: This section focuses on installing Python 3.9 and its dependencies, including Python 3.9 dev, build essential package, pip, and venv. It also sets the default Python version to 3.9.

Installation: Here, a set of plugins for flamapy and the flamapy core component are installed. The plugins include flamapy, flamapy-fm, flamapy-sat, and flamapy-bdd.

Use as an end user: This section demonstrates the usage of the framework's command-line interface (CLI). The flamapy-admin command is introduced, and various commands are executed, such as getting installed plugins and their operations. The operations are performed on downloaded models, including executing the Valid and Products operations on a Pizzas feature model.

Use as a developer: This section covers two approaches for developers to use the framework. First, it shows how to use Flama within a Python script, where an example script named products_automatic.py is executed. Then, it demonstrates how to expose an API using ngrok and Hug. An API file named diverso_lab.py is downloaded, and the server is launched.

Create your own plugin: In this section, the process of creating a new plugin is explained. The flamapy core repository is cloned, a new plugin named ovm_metamodel is created using the flamapy-admin command, and the structure of the plugin is explored. Additionally, the bdd repository is cloned and installed as a new plugin. The get_plugins command is used to verify the installation, and the Products operation is executed to observe the different results obtained from the new plugin.


