# Notes for talk about extensions

## preparation
This uses two conda environments, both relying on conda-forge
I added conda-forge as a higher priority channel and set strict channel priority to get this to work, ymmv:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

Then these are the two environments used:
```
conda create -n nbext -c conda-forge python=3 jupyter notebook jupyter_contrib_nbextensions ipywidgets

conda create -n nbextr -c conda-forge python=3 jupyter notebook jupyter_contrib_nbextensions r-irkernel ipywidgets r-ggplot2
```

[This could be a diagram up on the whiteboard]. 
Talk about jupyter architecture:  

|kernel    |   server             |    client 
-----------|----------------------|-----------------------------
|Python    |  server extensions   | notebook/lab extensions
|R
|Julia
|etc.

We'll start with notebook extensions

conda create -n nbext -c conda-forge python=3 jupyter notebook jupyter_contrib_nbextensions ipywidgets

Demo some neat notebook extensions:
table of contents (2)
Python Markdown
Hide input
conda magic
autopep8
exercise2

[todo]ipywidgets

[todo] some in-notebook interactive brain viewer
[todo] others?
autocode formatting (conda install -c conda-forge autopep8)


switch over to the nbextr environment
then you can show a notebook with an R kernel and some ggplotting

