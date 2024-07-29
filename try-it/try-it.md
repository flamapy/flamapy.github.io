---
layout: default
title: Try it
nav_order: 3
has_children: true
description: "Try it - flamapy official site"
permalink: /try-it
---


# Try it online
{: .fs-9 }

The {% include flamapy.html %} library can be easily installed on any local Python environment starting from version 3.9. It is also fully compatible with WebAssembly (WASM) and Google Colab. Below, you will find examples showcasing the capabilities and applications of this compatibility.

## WASM terminal

As stated, {% include flamapy.html %} provides a version of all its components and the SAT solver, which can rely on Pyodide. With this in mind, we have created a simple website to execute some operations directly in your browser.

[Try it online]({{site.baseurl}}/try-it/wasm-terminal){: .btn  .btn-light  .fs-4 .mb-4 .mb-md-0 }

## WASM UVL Analysis

We have designed a section where you can test the different analysis operations on an example UVL. All this from your browser.

[Try it online]({{site.baseurl}}/try-it/wasm-uvl-analysis){: .btn  .btn-light  .fs-4 .mb-4 .mb-md-0 }

## Consume a rest API
We have deployed a backend solver api, documented useing swagger in the onRender free tier.

[Try it online](https://flamapy-rest.onrender.com){: .btn  .btn-light  .fs-4 .mb-4 .mb-md-0 }

## Google Colab

Google Colab, short for Google Colaboratory, is a cloud-based development environment provided by Google. It offers a Jupyter notebook interface that allows users to write and execute Python code directly in a web browser, eliminating the need for local installations or setups.

**Coming soon**