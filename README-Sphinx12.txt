python3.5 -m venv .py35env
source .py35env/bin/activate
pip install --upgrade pip
pip install 'Sphinx>=1.2.0,<=1.2.9999'

sphinx-build -W -v -b latex -d build/doctrees docs build/latex
cat build/latex/Python.tex

	...
	...
	...
	Generic Admonition example from Docutils

	\begin{notice}{note}
	You can make up your own admonition too.
	\end{notice}

	A little bit changed to use a literal string inside

	\begin{notice}{note}{And, by the way...}

	\code{You can make up your own admonition too.}
	\end{notice}


rst2latex.py docs/contents.rst build/contents.tex
cat build/contents.tex

	...
	...
	...
	Generic Admonition example from Docutils

	\DUadmonition[admonition-and-by-the-way]{
	\DUtitle[admonition-and-by-the-way]{And, by the way...}

	You can make up your own admonition too.
	}

	A little bit changed to use a literal string inside

	\DUadmonition[admonition-and-by-the-way]{
	\DUtitle[admonition-and-by-the-way]{And, by the way...}

	\texttt{You can make up your own admonition too.}
	}
