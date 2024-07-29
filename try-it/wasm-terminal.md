---
layout: default
title: WASM terminal
parent: Try it
permalink: /try-it/wasm-terminal
nav_order: 1
---

# WASM terminal
{: .no_toc }

As stated, {% include flamapy.html %} provides a version of all its components and the SAT solver, which can rely on Pyodide. With this in mind, we have created a simple website to execute some operations directly in your browser. Note that the analysis, in this case, is covered by you when loading this website. 

![Web assembly](/assets/images/web_assembly.png){: .quarter-size .center}

This iframe is loading an entire Python terminal being run in your browser, with all the dependencies required to launch {% include flamapy.html %} already installed. This also downloads and unzips the contents of [Flamapy tutorial](https://github.com/flamapy/tutorial) so we have some models available in the wasm environment.

When loaded, try to execute the following code:

```
from flamapy.interfaces.python.flamapy_feature_model import FLAMAFeatureModel
fm = FLAMAFeatureModel("./valid_model.uvl")
result=fm.satisfiable()
print(result)
```

Now play and modify it.
<iframe id="inlineFrameExample"
    title="Inline Frame Example"
    width="100%"
    height="400"
    src="/assets/web_assembly/console.html">
</iframe>