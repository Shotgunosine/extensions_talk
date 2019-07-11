# Notes for talk about extensions

[This could be a diagram up on the whiteboard]
Talk about jupyter architecture:

kernel       server                 client 
[python,     [server extensions]    [notebook/lab extensions]
R,
julia,
etc.]

We'll start with notebook extensions

conda create -n nbext -c conda-forge python=3 jupyter notebook jupyter_contrib_nbextensions ipywidgets

Demo some neat notebook extensions:
table of contents (2)
Python Markdown
Hide input
conda magic
autopep8
exercise2

ipywidgets

some in-notebook interactive brain viewer
...
autocode formatting (conda install -c conda-forge autopep8)

Now lets look at adding some additional kernels
conda install -c conda-forge r-irkernel # this breaks!

we'll create a separate environment after setting up channel priority
conda config --add channels conda-forge
conda config --set channel_priority strict

conda create -n nbextr -c conda-forge python=3 jupyter notebook jupyter_contrib_nbextensions r-irkernel ipywidgets