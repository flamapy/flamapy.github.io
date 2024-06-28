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

{: .important-title }
> Note
> 
> The code of this website is not intended to be elegant but to provide insights on how to use the tool in a WebAssembly environment

<div>
The textarea below is intented to write a UVL file than can be later analyzed

<textarea id="uvlfile" style="width: 100%;" rows="20">
namespace Pizza

features
	Pizza {abstract}	
		mandatory
			Topping	
				or
					Salami
					Ham
					Mozzarella
			Size	
				alternative
					Normal
					Big
			Dough	
				alternative
					Neapolitan
					Sicilian

		optional
			CheesyCrust

constraints
	CheesyCrust => Big
</textarea>
</div>
<div>
<button type="button" name="button" class="btn" onclick="products()" style="margin-right: 10px">Get products</button>
<button type="button" name="button" class="btn" onclick="valid()" style="margin-right: 10px">Is a valid model?</button>
<button type="button" name="button" class="btn" onclick="numberofproducts()">What's the number of products?</button>

</div>
<div>
<h2>The output is:</h2>
<div id="loading" style="display:none;"><img SRC="/assets/images/loading.gif" width=100px> Loading, more details in the javascript console </div> 
<div id="result"><div id="loading" style="display:none;">  

</div>
</div>
</div>

<script type="text/javascript" src="https://cdn.jsdelivr.net/pyodide/v0.23.4/full/pyodide.js"></script>

<script type="text/javascript">
	  const uvlfile = document.getElementById("uvlfile");

		function showLoading(){
			document.getElementById("loading").style.display = "initial";
		}
		function hideLoading(){
			document.getElementById("loading").style.display = "none";

		}
		
	  async function valid() {
			showLoading()
      let pyodide = await loadPyodide();
      await pyodide.loadPackage("micropip");
      const micropip = pyodide.pyimport("micropip");
		  await micropip.install("/assets/web_assembly/antlr4_python3_runtime-4.7.2-py3-none-any.whl");
			await micropip.install("uvlparser==1.0.2");
			await micropip.install("afmparser==1.0.0");

			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
await micropip.install("flamapy==1.1.3", deps=False);
await micropip.install("flamapy-fm==1.1.3", deps=False);
await micropip.install("flamapy-sat");
`)
		hideLoading()

		try {
          let output = pyodide.runPython(
		  `
import js

file_content = js.document.getElementById('uvlfile').value
div = js.document.createElement("result")

with open("uvlfile.uvl", "w") as text_file:
    print(file_content, file=text_file)

from flamapy.interfaces.python.FLAMAFeatureModel import FLAMAFeatureModel

fm = FLAMAFeatureModel("uvlfile.uvl")
result=fm.valid()

div.innerHTML = "<div id='deleteme'>"+str(result)+"</div>"
exists=js.document.getElementById('deleteme')
if(exists):
	exists.remove()

js.document.getElementById('result').append(div)
		  `);
        } catch (err) {
          console.log(err);
        }
			

      }

 async function products() {
			showLoading()
      let pyodide = await loadPyodide();
      await pyodide.loadPackage("micropip");
      const micropip = pyodide.pyimport("micropip");
		  await micropip.install("/assets/web_assembly/antlr4_python3_runtime-4.7.2-py3-none-any.whl");
			await micropip.install("uvlparser==1.0.2");
			await micropip.install("afmparser==1.0.0");

			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
await micropip.install("flamapy==1.1.3", deps=False);
await micropip.install("flamapy-fm==1.1.3", deps=False);
await micropip.install("flamapy-sat");
`)
		hideLoading()

		try {
          let output = pyodide.runPython(
		  `
import js

file_content = js.document.getElementById('uvlfile').value
div = js.document.createElement("result")

with open("uvlfile.uvl", "w") as text_file:
    print(file_content, file=text_file)

from flamapy.interfaces.python.FLAMAFeatureModel import FLAMAFeatureModel

fm = FLAMAFeatureModel("uvlfile.uvl")
result=fm.products()
result = "<br>".join([f'P({i}): {p}' for i, p in enumerate(result, 1)])
div.innerHTML = "<div id='deleteme'>"+str(result)+"</div>"
exists=js.document.getElementById('deleteme')
if(exists):
	exists.remove()

js.document.getElementById('result').append(div)
		  `);
        } catch (err) {
          console.log(err);
        }
			

      }


	  async function numberofproducts() {
						showLoading()
      let pyodide = await loadPyodide();
      await pyodide.loadPackage("micropip");
      const micropip = pyodide.pyimport("micropip");
		  await micropip.install("/assets/web_assembly/antlr4_python3_runtime-4.7.2-py3-none-any.whl");
			await micropip.install("uvlparser==1.0.2");
			await micropip.install("afmparser==1.0.0");

			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
await micropip.install("flamapy==1.1.3", deps=False);
await micropip.install("flamapy-fm==1.1.3", deps=False);
await micropip.install("flamapy-sat");
`)
		hideLoading()

		try {
          let output = pyodide.runPython(
		  `
import js

file_content = js.document.getElementById('uvlfile').value
div = js.document.createElement("result")

with open("uvlfile.uvl", "w") as text_file:
    print(file_content, file=text_file)

from flamapy.interfaces.python.FLAMAFeatureModel import FLAMAFeatureModel

fm = FLAMAFeatureModel("uvlfile.uvl")
result=fm.products_number()

div.innerHTML = "<div id='deleteme'>"+str(result)+"</div>"
exists=js.document.getElementById('deleteme')
if(exists):
	exists.remove()
js.document.getElementById('result').append(div)
		  `);
        } catch (err) {
          console.log(err);
        }
			

      }
</script>