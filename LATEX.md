# LaTeX Guidelines

To see what our `main.tex` file looks like, you can take a look at our [2025 edition](https://github.com/shsmathmag/2025/blob/main/source/main.tex) source code.

## Document Preamble

We provide many common typesetting and formatting packages (plus several for general settings and formatting the magazine itself). If you use any additional packages, please mention this in your submission.

```tex
\documentclass{article}

% PACKAGES
\usepackage[utf8]{inputenc}
\usepackage{blindtext}
\usepackage{multicol}
\setlength\columnsep{0.35in} % sets space between columns

\usepackage{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{gensymb}
\usepackage{commath}
\usepackage{esdiff} % Differentiation
\usepackage{marvosym, wasysym} % More symbols
\usepackage{mathtools}

\usepackage{graphicx} % images
\usepackage{wrapfig} % text wrapping
\usepackage{scalerel} % Scaling
\usepackage{pdfpages} % import pdf
\usepackage{fancyhdr} % fancy headers and footers
\usepackage{float} % floating tables and figures

\PassOptionsToPackage{usenames, dvipsnames}{color}
\usepackage{color}

\PassOptionsToPackage{hyphens}{url}
\usepackage[hyperfootnotes=false,hidelinks]{hyperref}

\usepackage{comment} % allows using \begin{comment} to do block comments

\usepackage[12pt]{extsizes} % allows larger font sizes (defaulting to 12 pt)
\usepackage[left=0.565in,right=0.565in,top=0.935in,bottom=0.935in]{geometry} % custom margins

\newcommand{\ubar}[1]{\underaccent{\bar}{#1}}
\newcommand\ddfrac[2]{\frac{\displaystyle #1}{\displaystyle #2}} % Allows for "uncramped" fractions
\DeclareMathOperator*{\gint}{\scalerel*{\mathnormal{\pi}}{\big(}} % lowkey idk why this exists

\usepackage{tcolorbox} % colored text boxes
\usepackage{tikz} % diagrams, plots, illustrations, etc using raw LaTeX
\usetikzlibrary{positioning, calc} % additional tikz libraries

\usepackage{accents} % manipulating accent positioning
\usepackage{indentfirst} % indent first paragraph
\usepackage{dirtytalk} % typesetting quotes using \say{...}

\usepackage{lastpage} % allows reference to num of pages (i.e. page X of Y)

\usepackage{tocloft} % table of contents
\renewcommand{\cftsecleader}{\cftdotfill{\cftdotsep}}

\usepackage{setspace} % line spacing control
\setstretch{1.04} % custom line spacing of 1.04
```

## Formatting Your Article

Since your article will be one of many in the magazine, the formatting we ask you to use is slightly different than what you would use for a standalone article.

We encourage you to use standard LaTeX formatting when writing your article. Then, make a copy and make the following changes:

1. Omit the preamble (unless you use additional packages), the `\begin{document}` and `\end{document}` tags, and the `\maketitle`.
2. Increase each section by one level: `\section` to `\subsection`, and so on.
3. Begin your document with:
```tex
\section*{<TITLE>}
\addcontentsline{toc}{section}{<TITLE> by <YOUR NAME> '2X}
\noindent\textbf{<NAME> '2X}
\medbreak
```
4. Remove numberings from equations: `\begin{equation*} ... \end{equation*}` or `\[ ... \]` instead of `\begin{equation}`.
5. Do not use `\cite`. If you wish, you can include sources at the end (`\subsection{Sources}`).
6. For figures, use:
```tex
\begin{center}
  \includegraphics[width=5cm]{<IMAGE>}
\end{center}
```

## Other Issues

We can't possibly cover every edge case that an author might encounter. If you have any questions, please email us (the editors). If we notice any issues, we will also email you, so please keep an eye on your inbox.
