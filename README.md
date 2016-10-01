#mchemJS
This project is an simple adaptation of [mhchem/MathJax-mhchem](https://github.com/mhchem/MathJax-mhchem) to be used with [Khan/KaTeX](https://github.com/Khan/KaTeX/).

##Usage
```javascript
var latex = mchem.parse("C6H12O + O2 -> CO2 + H2O");
console.log(katex.renderToString(latex));
```

adaptations:

remove spaces
"\\vphantom","\\hphantom","\\mathrel" -> ""
"\\mkern*","\\mskip*" -> "\\ "

remove long from arrows
"\\long*" -> "\\*" 

replacing xrightarrow and alike with arrays

##Warning
This is not intended to be an official Mchem support to KaTeX.
