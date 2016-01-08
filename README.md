# Fast Closure Translater

*NOTE: this project is new and has not been tested against multiple Closure Templates versions -
it could be buggy. Use at your own risk.*

This project consists of a Node module for translating goog.getMsg() calls in Closure Template JS.

It is possible to run the Closure Templates compiler for compiling *.soy to *.js in two modes:

 1. The compiler translates all message strings to the appropriate translations, producing a different
		set of JS files for each locale
 2. The compiler generates one set of JS files, with `goog.getMsg()` calls in place of each translated
		message (`shouldGenerateGoogMsgDefs` option). Traditionally after this point, <a href="https://developers.google.com/closure/templates/docs/translation#closurecompiler">Closure Compiler is used</a> to perform the actual translation.

This project addresses the second case above, seeking to provide a fast alternative to using Closure Compiler to
translate, suitable for projects that use another JavaScript build tool besides Closure Compiler.

See <a href="./test/index.js">the test suite</a> for example usage.
