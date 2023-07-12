---
title: "Flama WASM terminal"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
layout: try

---
## Flama python terminal in your browser

![Web assembly](/images/illustrations/web_assembly.png)

As stated, Flama provides a version of all its components and the SAT solver, which can rely on Pyodide. With this in mind, we have created a simple website to execute some operations directly in your browser. Note that the analysis, in this case, is covered by you when loading this website. 

This iframe is loading an entire Python terminal being run in your browser, with all the dependencies required to launch Flama already installed. This also downloads and unzips the contents of https://github.com/flamapy/tutorial, so we have some models available in the wasm environment.

When loaded, try to execute the following code:
 <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/10.0.3/styles/default.min.css">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/10.0.3/highlight.min.js"></script>
  <script>hljs.initHighlightingOnLoad();</script>
  <pre><code class="python">
from flamapy.interfaces.python.FLAMAFeatureModel import FLAMAFeatureModel
fm = FLAMAFeatureModel("./tutorial-main/models/pizzas/pizzas.uvl")
result=fm.products() 
print(result)
</code></pre>
Now play and modify it.
<iframe id="inlineFrameExample"
    title="Inline Frame Example"
    width="100%"
    height="400"
    src="/assets/web_assembly/console.html">
</iframe>