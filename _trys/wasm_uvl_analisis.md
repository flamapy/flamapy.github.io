---
title: "Webassembly UVL analysis"
date: 2019-05-18T12:33:46+10:00
weight: 4
promoted: true
layout: try

---
## Webassembly Flama version enables UVL analysis.

![Web assembly](/images/illustrations/web_assembly.png)

WebAssembly (often abbreviated as wasm) is a binary instruction format designed for web browsers. It is a low-level, compact, and portable format that allows developers to run code written in programming languages other than JavaScript in web browsers. WebAssembly is supported by all major web browsers, including Chrome, Firefox, Safari, and Edge. It basically acts as a virtual machine or container runtime. Flama, provides a version of all its components and the SAT solver which can rely on pyodide.  With this in mind, we have created a simmple website to execute some operations diectly in your browser. Note that the analysis in this case is cover by you when loading this website. 

Note that the code of this website is not intended to be elegant but to provide insigts on how to use the tool in a webassembly enviroment. 
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
	CheesyCrust => Big"
</textarea>
</div>
<div>
<button onclick="products()">Get products</button>
<button onclick="valid()">Is a valid model?</button>
<button onclick="numberofproducts()">What's the number of products?</button>

</div>
<div>
<h2>The output is:</h2>
<div id="loading" style="display:none;"><img SRC="/images/illustrations/loading.gif" width=100px> Loading, more details in the javascript console </div> 
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
      await micropip.install("uvlparser");
      await micropip.install("flamapy-fm");
      await micropip.install("flamapy-sat");
			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
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

div.innerHTML = result
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
      await micropip.install("uvlparser");
      await micropip.install("flamapy-fm");
      await micropip.install("flamapy-sat");
			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
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

div.innerHTML = result
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
      await micropip.install("uvlparser");
      await micropip.install("flamapy-fm");
      await micropip.install("flamapy-sat");
			await pyodide.runPythonAsync(`
import micropip
await micropip.install("flamapy-fm-dist", deps=False)#this is to avoid problems with deps later on
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

div.innerHTML = result
js.document.getElementById('result').append(div)
		  `);
        } catch (err) {
          console.log(err);
        }
			

      }
</script>