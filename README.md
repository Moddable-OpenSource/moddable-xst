# Moddable XS Test Engine

**XS** is the JavaScript engine at the center of the [Moddable SDK](https://github.com/Moddable-OpenSource/moddable).

Please visit [Moddable](http://www.moddable.com) to get the source code, documentation and licence of **XS**

This repository only releases **xst**, a JavaScript engine to test **XS** on Linux, macOS and Windows and **xsbug**, the **XS** debugger.

You can use the [jsvu CLI](https://github.com/GoogleChromeLabs/jsvu) to install or update  **xst** from this repostiory.  

## Usage

	xst [-h] [-e] [-m] [-s] [-v] strings...

- `-h`: print this help message
- `-e`: eval `strings`
- `-m`: `strings` are paths to modules
- `-s`: `strings` are paths to scripts
- `-v`: print XS version

Without the `-e`, `-m` or `-s` options, `strings` are paths to **test262** cases or directories. 

<!--### eshost

To test XS with **eshost**, install the [eshost CLI](https://github.com/bterlson/eshost-cli). Then add XS to the hosts:

	eshost --add 'XS' xs ~/.jsvu/xst

**eshost** uses the `-s` option of **xst**.
-->
### test262

To test XS with **test262**, clone [test262](https://github.com/tc39/test262) and change the directory to the `test` directory inside the `test262` directory. For instance:
	
	cd ~/test262/test
	xst language/block-scope
	xst built-ins/TypedArrays/buffer-arg-*

See [XS Conformance](https://github.com/Moddable-OpenSource/moddable/blob/public/documentation/xs/XS%20Conformance.md) for details about how **XS** currently passes **test262** cases.

Running **xsbug** while passing a bunch of **test262** cases can be cumbersome. Just quit **xsbug** or at least uncheck Break - On Exceptions in the preferences.

## xsbug

See the [xsbug documentation](https://github.com/Moddable-OpenSource/moddable/blob/public/documentation/xs/xsbug.md) in the **Moddable SDK**. 
