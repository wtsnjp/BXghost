# The BXghost Package

LaTeX: ghost insertion for proper xkanjiskip

## System requirements

* TeX format: LaTeX
* TeX engine: LuaTeX, XeTeX, pTeX, upTeX, and ApTeX (pTeX-ng)

Since this package is intended to be used for creating documents in Japanese, it assumes appropriate classes and/or packages are loaded in some engines (e.g., LuaTeX-ja for LuaTeX and bxjscls for XeTeX). BXghost does not load any external packages automatically.

## Usage

This package provides following commands:

* `\eghostguarded{<text>}` inserts *Europian ghost* (invisible and zero-width alphabets) before and after the `<text>`. In math mode, it outputs only `<text>` without the ghosts.
* `\jghostguarded{<text>}` inserts *Japanese ghost* (invisible and zero-width Japanese characters) before and after the `<text>`. In math mode, it outputs only `<text>` without the ghosts.

## Acknowledgements

The logic and style of the code in this package is greatly inspired by [Package PXghost](https://gist.github.com/zr-tex8r/4461060) and various packages in [the BX series](http://zrbabbler.sp.land.to/package.html#ssec-bx). I would like to thank the author of the packages, Dr. Takayuki YATO (aka. [ZR](https://github.com/zr-tex8r)).

## License

This package is distributed under [the MIT license](./LICENSE).

## Revision History

* Version 0.2.0  ‹2019/09/17›
  * Add supports for XeTeX and ApTeX (pTeX-ng)
* Version 0.1.0  ‹2019/09/16›
  * The first public version
  * Add supports for LuaTeX to the original [PXghost](https://gist.github.com/zr-tex8r/4461060) package

---

Takuto ASAKURA ([wtsnjp](https://twitter.com/wtsnjp))
