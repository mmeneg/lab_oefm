# Optics and Modern Physics Labs
This repo contains the labs reports (written in LaTex) for the lab activities
of the academic second year of the Physics' Bachelor degree at Università degli Studi di Milano

## Organization
The repository is organized by experience, each folder represent an experience. 
Whithin each folder there are a bounch of LaTex files (extension .tex), one file is the main one
which point to all the child files (that represent the sections in the main document),
you have to work on your assigned child file.
This is the list of main files:
- e/m ratio:
	-- directory: e_m
	-- main: e_m.tex

## How to contribute

### Git usage

#### Repo initial download
`git clone https://github.com/mmeneg/corda_vibrante.git`
this command create a new directory named after the project, used once to download the initial content 
**Note:** all the command must be executed in the root directory created by Git

#### Work routine
`git pull origin`
pull and merge all the changes occured since your last commit 
**Remember:** use this command before each and every time you start working on files

`git add .`
once you have modified the file you intend to modify add it (or add them) to stage

`git commit -m "meaningful comment"`
commit changes locally, please add a meaningful comment such as "Linear regression chart added"

`git push origin main`
push your changes to the remote central repository

#### Git ignore
In the root directory there's a file called .gitignore, this file include all the files and directory 
that fill be ignored by Git.
This included all working file for Visual Studio and Sublime Text IDEs, all working files and pdf output
from LaTex compilations.
**Note:** please do not modify this file (unless you know what you are doing)

### Latex usage
#### Build/Compile
`pdflatex [filename].tex`
this command will compile [filename].tex and output [filename].pdf.
You can also use the Build command of your IDE on the file (that usually run such command for you in the background)
**Remember:** you have to build/compile only the main document (e.g. e_m.tex)

#### Structure
Your section file will be inserted into a `\section{Title}` of the main document.
You can use `\subsection{SubSectionTitle}` in your section file to further organize the content.

#### Inline formulas
Inline formulas are enclosed by `$`.
For example `$\sqrt{3x-1}+(1+x)^2$` will render as $\sqrt{3x-1}+(1+x)^2$

#### Block single line formulas
Block formulas are render centrally aligned, the delimiter `\[` start the block while `\]` will end it
For example
```
\[
    L_{0}=(78.8 \pm 0.1) \ \text{cm}
\]
```
will render as 
```math
L_{0}=(78.8 \pm 0.1) \ \text{cm}
```

#### Block multi line formulas
The delimiter `\begin{align*}` start the block while `\end{align*}` will end it.
Use `&` to align the beginning character of a new line, use `\\` to end the line.
For example
```
\begin{align*}
    &2A_{0}=(11.0 \pm 0.1) \ \text{cm} \\
    &L_{0,max}=(79.6 \pm 0.1) \ \text{cm} \\
    &cos{\alpha} = (0.990 \pm 0.002)
\end{align*}
```
will render as 
```math
\begin{align*} &2A_{0}=(11.0 \pm 0.1) \ \text{cm} \\ &L_{0,max}=(79.6 \pm 0.1) \ \text{cm} \\ &cos{\alpha} = (0.990 \pm 0.002) \end{align*}
```

