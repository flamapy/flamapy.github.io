---
layout: default
title: WASM UVL Analysis
parent: Try it
permalink: /try-it/wasm-uvl-analysis
nav_order: 3
---

# WASM UVL Analysis

![Web assembly](/assets/images/web_assembly.png){: .quarter-size .center}

WebAssembly (often abbreviated as WASM) is a binary instruction format designed for web browsers. It is a low-level, compact, and portable format that allows developers to run code written in programming languages other than JavaScript in web browsers. WebAssembly is supported by all major web browsers, including Chrome, Firefox, Safari, and Edge. It acts as a virtual machine or container runtime. {% include flamapy.html %} provides a version of all its components and the SAT solver, who can rely on provide. With this in mind, we have created a simple website to execute some operations directly in your browser. Note that the analysis, in this case, is covered by you when loading this website. 

## Custom UVL

The textarea below is intented to write a UVL file than can be later analyzed:

{: .important }
> Currenlty this website does not support linter in the text area. Take a look con dev console if there is any parsing error of your text (tabs are difficult to be writen in a browser)

<div>


<textarea id="uvlfile" style="width: 100%;" rows="20">
features
    eCommerce { abstract }
        mandatory
            Server { abstract }
                mandatory
                    PHP
                        mandatory
                            v74
                    Storage
                        alternative
                            LOW
                            ENOUGH
            Web { abstract }
                mandatory
                    Catalog
                    Search
                        alternative
                            BASIC
                            ADVANCED
                    Shopping 
                        mandatory
                            Cart
                            Payment
                                or
                                    PayPal
                                    CreditCard
                                    Mobile
                    Security
                        alternative
                            HIGH
                            STANDARD
                optional
                    Backup
                    Marketing
                        optional
                            SEO
                            Socials
                                or
                                    Twitter
                                    Facebook
                                    YouTube
constraints
    CreditCard => HIGH
    Mobile => HIGH
    LOW => !Backup</textarea>

<div>
	<button class="operation" onclick="flamapy('configurations')" disabled>Get configurations</button>
	<button class="operation" onclick="flamapy('satisfiable')" disabled>Is satisfiable?</button>
	<button class="operation" onclick="flamapy('configurations_number')" disabled>How many products there are?</button>
	<button class="operation" onclick="flamapy('atomic_sets')" disabled>atomic_sets</button>
	<button class="operation" onclick="flamapy('average_branching_factor')" disabled>average_branching_factor</button>
	<button class="operation" onclick="flamapy('count_leafs')" disabled>count_leafs</button>
	<button class="operation" onclick="flamapy('estimated_number_of_configurations')" disabled>estimated_number_of_configurations</button>
	<button class="operation" onclick="flamapy('leaf_features')" disabled>leaf_features</button>
	<button class="operation" onclick="flamapy('max_depth')" disabled>max_depth</button>
	<button class="operation" onclick="flamapy('core_features')" disabled>core_features</button>
	<button class="operation" onclick="flamapy('dead_features')" disabled>dead_features</button>
	<button class="operation" onclick="flamapy('false_optional_features')" disabled>false_optional_features</button>
</div>

<div>
	<h2>The output is:</h2>
	<div id="loading" style="display:none;"><img src="loading.gif" width="100px" /> Loading, more details in the javascript console </div> 
	<div id="result"><div id="loading" style="display:none;"></div></div>
</div>

</div>

<script type="text/javascript" src="https://cdn.jsdelivr.net/pyodide/v0.23.4/full/pyodide.js"></script>
<script src="wasm_uvl.js" defer></script>
<script>
    document.addEventListener('DOMContentLoaded', (event) => {
        preparare_WASM()
        
    });
</script>
