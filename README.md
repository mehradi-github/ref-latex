# LaTeX – A document preparation system

[LaTeX](https://www.latex-project.org/) is a high-quality typesetting system; it includes features designed for the production of technical and  scientific documentation. LaTeX is the de facto standard for the communication and publication of scientific documents. LaTeX is available as free software.


## How to build Latex

|You want to build with...|Use this `latexmk` command|
|---|---|
|**`pdflatex`**|`latexmk -pdf your-document.tex`|
|**`xelatex`**|`latexmk -xelatex your-document.tex`|

```sh
# Build
pdflatex hello.tex
xelatex file.tex                    # Basic build
xelatex --help


latexmk -xelatex file.tex           # Smart build
latexmk -pvc -xelatex file.tex      # Auto-rebuild on save

# Clean
latexmk -c                          # Remove aux files
latexmk -C                          # Remove everything including PDF
rm -f *.{aux,log,out,toc}          # Manual clean

# View PDF
xdg-open file.pdf                   # Linux
open file.pdf                       # macOS
start file.pdf                      # Windows

# Check system
which xelatex                       # Find XeLaTeX location
xelatex --version                   # Check version
fc-list :lang=fa                   # List Persian fonts

# Continuous mode (auto-rebuild when files change)
latexmk -pvc -xelatex mydocument.tex

```
