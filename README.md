#mchemJS
This project is an simple adaptation of [mhchem/MathJax-mhchem](https://github.com/mhchem/MathJax-mhchem) to be used with [Khan/KaTeX](https://github.com/Khan/KaTeX/).

##Usage
```javascript
var latex = mchem.parse("C6H12O + O2 -> CO2 + H2O");

console.log(latex);// "\text{C}_{6}\text{H}_{12}\text{O}+\text{O}_{2}\longrightarrow \text{CO}_{2}+\text{H}_{2}\text{O}"
```

You can also user as filter:
```javascript
var latex = "\\text{Outside ce function} \\ce{H2O <=> H+ + O^2-}";

function mchemFilter(element){
	return element.replace(/\\ce\{[\s\S]*?\}/g,function(block){
		return mchem.parse(block.substr(3));
	});
}

console.log(katex.renderToString(mchemFilter(latex)));
```
