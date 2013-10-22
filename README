kotex-utf
=========

Introduction
------------

kotex-utf is a macro package for typesetting Hangul, the native 
alphabet of the Korean language. The Korean text should be a UTF-8
encoded Unicode text.  kotex-utf belongs to ko.TeX, 
a comprehensive Korean typesetting system together with packages kotex-oblivoir, 
kotex-plain, cjk-ko, xetex-ko, luaxex-ko, and kotex-utils.

Usage
-----

Call kotex.sty with package options as follows:

    \usepackage[<options>]{kotex}

Certain package options are inter-related to the TeX engines
that are used for compilation.
For pdfLaTeX and LaTeX, you can use *utf* option:

    \usepackage[utf]{kotex}

This will activate the default behavior of kotex-utf. The option 
*utf* does not need to be specified since it is a default option. 
You can use other common options such as *hangul*, *hanja*, 
and *nojosa*.

Calling kotex.sty in the following way

    \usepackage[cjk]{kotex}

will typeset Hangul using the cjk-ko package. Options *usedotemph* 
and *usecjkt1font* can be specified in addition to the common options. 

For XeLaTeX and LuaLaTeX, you can just load kotex.sty without 
any package options. kotex-utf will call XeTeX-ko or LuaTeX-ko accordingly.

Sample document
---------------

The following document is a sample document utilizing the iftex 
package for coping with multiple engines:

    \documentclass{article}
    \usepackage{amsmath,amssymb}
    \usepackage{hyperref}
    \usepackage[hangul]{kotex}
    \usepackage{kotex-logo}
    \usepackage{iftex}
    \ifPDFTeX
      \usepackage{dhucs-nanumfont}
      \hypersetup{pdftex,unicode,bookmarks}
      \input glyphtounicode
      \pdfgentounicode=1
    \else\ifXeTeX
      \setmainhangulfont[Ligatures=TeX]{HCR Batang LVT}
      \setsanshangulfont[Ligatures=TeX]{HCR Dotum LVT}
    \else\ifLuaTeX
      \hypersetup{unicode,bookmarks}
      \setmainhangulfont[Ligatures=TeX]{HCR Batang LVT}
      \setsanshangulfont[Ligatures=TeX]{HCR Dotum LVT}
    \fi\fi\fi
    \begin{document}
    \title{\koTeX-article 템플릿}
    \author{저자}
    \date{}
    \maketitle
    \section{절 제목}
    \subsection{소절 제목}
    이 문서는 \koTeX\ 문서입니다.
    \end{document}

For more information, please refer to the included documentation (written in Korean).

License
-------

kotex-utf is licensed under the LaTeX Project Public
License (LPPL).

Contacts
--------

Please report any errors or suggestions to the package maintainer,
Kihwang Lee <leekh at ktug org>.

