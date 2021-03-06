# beamerthementnu
A LaTeX beamer theme for NTNU presentation templates

## Overview

This beamer theme implements the [NTNU PowerPoint templates]
(https://innsida.ntnu.no/wiki/-/wiki/Norsk/Lage+presentasjon) for LaTeX
beamer. See usage example below.

The single theme can produce almost all the different templates, and
both in 4:3 and 16:9 format. Notably, the campus dependent version and
16:10 format are *not* implemented.

If you have technical questions, please contact [Martin Strand]
(https://www.ntnu.edu/employees/martin.strand). Do not send such 
questions to the NTNU Communications Division.


## Usage

The basic usage is the command

```latex
\usetheme[style=ntnu|simple|vertical|horizontal, language=bm|nn|en]{ntnu2015}
```

along with the special title page command

```latex
\ntnutitlepage
```

A minimal working example

```latex
\documentclass[screen, aspectratio=43]{beamer}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}

% Use the NTNU-temaet for beamer 
% \usetheme[style=ntnu|simple|vertical|horizontal, language=bm|nn|en]{ntnu2015}
\usetheme[style=ntnu,language=en]{ntnu2015}
 
\title[Short title]{The full and long title of the presentation}
\subtitle{Subtitle if you want}
\author[O. Nordmann]{Ola Nordmann}
\institute[NTNU]{Department of LaTeX-ical sciences, NTNU}
\date{1 January 1970}
%\date{} % To have an empty date


\begin{document}

% Special title page command to get a different background
\ntnutitlepage

\begin{frame}
  \frametitle{Main theorem}
  \begin{theorem}
    LaTeX makes things easier.
  \end{theorem}
\end{frame}

\end{document}
```


## Installation

Simply copy the folder `beamerntnu2015` into your `texmf/tex/latex` folder. 
The precise location varies on different operating systems. 


## Known issues

 - The **simple** template is not localised


## Contributions and license

The code is based on [Håvard Berland's original work in 2005]
(http://www.pvv.ntnu.no/~berland/ntnubeamer/). In private conversation
in December 2015, Berland licensed his code under a [Creative Commons 
Attribution-ShareAlike 4.0 International License]
(http://creativecommons.org/licenses/by-sa/4.0/), and so naturally goes 
for all code in this repository.

However, the design is owned by NTNU, and should not be altered 
substantially without checking it with the [Communication Division]
(https://www.ntnu.no/adm/komm).

So far, this is built using duct tape and chewing gum, so any 
contribution to improve the code is very welcome.

This theme also includes code from the following sources:
 - [Detect aspect ration](http://tex.stackexchange.com/questions/123106/detect-aspect-ratio-in-beamer), by StackExchange user egreg
