# The BXghost Package

LaTeX: ghost insertion for proper xkanjiskip

## Requirements

* TeX format: LaTeX
* TeX engine: LuaTeX, XeTeX, pTeX, upTeX, and ApTeX (pTeX-ng)
* LuaTeX-ja is required in LuaTeX

Since this package is intended to be used for creating documents in Japanese, it assumes appropriate classes and/or packages are loaded in some engines (e.g., LuaTeX-ja for LuaTeX and bxjscls for XeTeX).

## Usage

This package provides following commands:

* `\eghostguarded{<text>}` inserts *European ghost* (invisible and zero-width alphabets) before and after the `<text>`. In math mode, it outputs only `<text>` without the ghosts.
* `\jghostguarded{<text>}` inserts *Japanese ghost* (invisible and zero-width Japanese characters) before and after the `<text>`. In math mode, it outputs only `<text>` without the ghosts.

In addition, the following package options are available:

* `verb` patches the `\verb` command of LaTeX to be guarded by European ghost.
* `noverb` disables the `verb` feature. (default)

### For package authors

To use the function of this package in your package, a library version is available:

```tex
\RequirePackage{bxghost-lib}
```

This provides all the commands defined in the package but does not have any package option to prevent the problem of option clashes.

## Acknowledgements

The logic and style of the code in this package is greatly inspired by [Package PXghost](https://gist.github.com/zr-tex8r/4461060) and various packages in [the BX series](http://zrbabbler.sp.land.to/package.html#ssec-bx). I would like to thank the author of the packages, Dr. Takayuki Yato (aka. [ZR](https://github.com/zr-tex8r)).

## License

This package is distributed under [the MIT license](./LICENSE).

## Revision History

* Version 0.5.1  ‹2023/02/26›
  * Add support for e-upTeX based pLaTeX
* Version 0.5.0  ‹2022/05/20›
  * Provide `bxghost-lib` for internal use from other packages
* Version 0.4.0  ‹2022/02/12›
  * More general implementation for `\jghostguarded`
  * Add the `noverb` option
* Version 0.3.0  ‹2020/01/31›
  * Add the `verb` option
* Version 0.2.0  ‹2019/09/17›
  * Add supports for XeTeX and ApTeX (pTeX-ng)
* Version 0.1.0  ‹2019/09/16›
  * The first public version
  * Add supports for LuaTeX to the original [PXghost](https://gist.github.com/zr-tex8r/4461060) package

---

Takuto Asakura ([wtsnjp](https://twitter.com/wtsnjp))
