#mchemJS
This project is an simple adaptation of [mhchem/MathJax-mhchem](https://github.com/mhchem/MathJax-mhchem) to be used with [Khan/KaTeX](https://github.com/Khan/KaTeX/).

##Usage
```javascript
var latex = mchem.parse("C6H12O + O2 -> CO2 + H2O");

console.log(latex);// "\text{C}_{6}\text{H}_{12}\text{O}+\text{O}_{2}\longrightarrow \text{CO}_{2}+\text{H}_{2}\text{O}"
```
