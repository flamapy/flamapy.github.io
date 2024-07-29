---
layout: default
title: Welcome to Flamapy Official Site
nav_order: 1
description: "A Python-based AAFM framework that takes into consideration previous AAFM tool designs and enables multi-solver and multi-metamodel support for the integration of AAFM tooling on the Python ecosystem."
permalink: /
---

![Texto alternativo](/assets/images/flamapy_horizontal_logo_white.svg){: .center }

The cutting-edge Python-based tool for Automated Analysis of Feature Models (AAFM) using UVL and more with advanced multi-solver and multi-metamodel capabilities
{: .fs-6 .fw-500 .center-text} 

<div class="center-buttons">
    <a href="https://docs.flamapy.org/getting-started/" class="btn btn-primary fs-5 mb-4 mb-md-0 mr-2">Getting started</a>
    <a href="{{site.baseurl}}/try-it" class="btn btn-green fs-5 fs-5 mb-4 mb-md-0 mr-2">Try it online</a>
    <a href="https://github.com/flamapy/flamapy" class="btn fs-5 mb-4 mb-md-0">View it on GitHub</a>
</div>

---

# <i class="fa-solid fa-puzzle-piece"></i> Easily extensible

### Plugin generator
Simplifies the process of creating new plugins with a semi-automatic generator, making customization and expansion straightforward.

### Variability modelling in the wild
Initially supports cardinality-based feature models, with the flexibility to easily incorporate other types like attributed feature models.

# <i class="fa-solid fa-life-ring"></i> Robust solver support

### PySAT integration
Utilizes the PySAT metasolver, offering access to more than ten distinct solvers. This diversity allows for optimal solution finding across various complex scenarios.

### BDD integration
Utilizes the CU-BDD metasolver, offering efficient variability model analysis for some operations. 


# <i class="fa-solid fa-laptop-code"></i> Easy to use, easy to integrate

### Easy-to-use python facade
Designed with capabilities to analyse modes in Python with just a line of code.

### Command line direct use
Easy to integrate in any ecosystem.

### WASM support
Run analysis in your browser. Currently, both {% include flamapy.html %} and PySAT are WASM compatible. Enable analysis with 0 configuration process.

### REST / SWAGGER available
Integrate the tool in yours by means of a robust backend Rest API.

# <i class="fa-solid fa-calculator"></i> Large set of operations

Examples of operations include:

#### **Dead features**
Identify features that are no longer in use.

#### **Void features**
Determine if a feature model is void. A feature model is considered void if it represents no products, often due to incorrect usage of cross-tree constraints.

#### **Valid product**
Validate whether a product (i.e., a set of features) belongs to the set of products represented by a feature model. This involves checking if the product conforms to the constraints and structure of the feature model.

#### **All products**
Generate a complete list of all products.

#### **Filter**
This operation takes as input a feature model and a configuration (potentially partial) and returns the set of products including the input configuration that can be derived from the model. Note that this operation does not modify the feature model itself.

{: .fs-6 .fw-300 }

## Entities involved

<div class="entities-container">
  <a href="https://www.us.es/" target="_blank" class="entity">
    <img src="/assets/images/university_of_seville.svg" alt="University of Seville">
  </a>
  <a href="https://www.uma.es/" target="_blank" class="entity">
    <img src="/assets/images/university_of_malaga.svg" alt="University of Malaga">
  </a>
  <a href="https://www.uni-graz.at/en/" target="_blank" class="entity">
    <img src="/assets/images/university_of_graz.svg" alt="University of Graz">
  </a>
  <a href="https://www.uned.es/" target="_blank" class="entity">
    <img src="/assets/images/uned.jpg" alt="UNED">
  </a>
</div>



---

### Changelog

Detailed changes for each release are documented in the [release notes].

### Contributing

When contributing to this repository, please first read [contributing].

[^1]: The [source file for this page] uses all three markup languages.

[^2]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Jekyll]: https://jekyllrb.com
[Markdown]: https://daringfireball.net/projects/markdown/
[Liquid]: https://github.com/Shopify/liquid/wiki
[Front matter]: https://jekyllrb.com/docs/front-matter/
[Jekyll configuration]: https://jekyllrb.com/docs/configuration/
[source file for this page]: https://github.com/just-the-docs/just-the-docs/blob/main/index.md
[Just the Docs Template]: https://just-the-docs.github.io/just-the-docs-template/
[Just the Docs]: https://just-the-docs.com
[flamapy repo]: https://github.com/flamapy/
[Just the Docs README]: https://github.com/just-the-docs/just-the-docs/blob/main/README.md
[GitHub Pages]: https://pages.github.com/
[Template README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/

[use the template]: https://github.com/just-the-docs/just-the-docs-template/generate

[release notes]: https://github.com/flamapy/flamapy_fw/releases

[contributing]: https://docs.flamapy.org/developing/contributing/