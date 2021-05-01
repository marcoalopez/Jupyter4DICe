# Jupyter4DICe
_This project is maintained by [Marco A. Lopez-Sanchez](https://marcoalopez.github.io/)_ - Last update: 2021/05/2

## What is this?

[Jupyter4DICe](https://github.com/marcoalopez/Jupyter4DICe) is a series of [Jupyter notebooks](https://jupyter.org/) written in Python for post-processing digital image correlation (DIC) data, in particular for DIC processing data obtained with the open source digital image correlation tool [DICe](https://github.com/dicengine/dice). Although the DICe tool already produces a file that can be viewed directly with a visualisation application called Paraview, the use of Jupyter notebooks has two main advantages over this approach:

- it is more versatile
- it allows you to record and detail all post-processing steps, which is advantageous for the reproducibility of the results. For example, this allows you to create a complete step-by-step report that you can use as supplementary material in your publications.

These Jupyter notebooks assume that the user is familiar with basic Python concepts (data types, loops, functions, modules), and the Numpy (particularly multidimensional array indexing) and Matplotlib libraries.

### The notebooks

To visualize the content of the notebooks as a website just click on the topic you are interested in (the list may increase or decrease without notice over time)

- [Loading data from DICe output](https://github.com/marcoalopez/Jupyter4DICe/blob/main/notebooks/LoadingDICe_data.ipynb)
- [Visualizing strain and strain analysis]([Jupyter4DICe/Strain_analysis.ipynb at main · marcoalopez/Jupyter4DICe (github.com)](https://github.com/marcoalopez/Jupyter4DICe/blob/main/notebooks/Strain_analysis.ipynb))
- [Visualizing displacements](https://nbviewer.jupyter.org/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/displacements.ipynb?flush_cache=true)
- [Assessing and visualizing the quality of the solution](https://nbviewer.jupyter.org/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/assesing_quality.ipynb?flush_cache=true)

## FAQs

### What is digital image correlation?

Digital image correlation is an image-based method that uses image tracking and recording techniques to make accurate full-field 2D or 3D measurements during deformation. Tracking coordinate fields allows the user to estimate different parameters of interest such as [displacement](https://en.wikipedia.org/wiki/Displacement_field_(mechanics)) (motion), [strains](https://en.wikipedia.org/wiki/Strain_(materials_science)), strain rates, particle velocities, etc. The technique is non-contact, usually inexpensive, and can be applied at virtually any scale (from microscales to plate tectonic scales), becoming increasingly common in many areas of science and engineering. In mechanical tests and compared to [strain gauges](https://en.wikipedia.org/wiki/Strain_gage) such as extensometers, the amount of information collected is increased due to the ability to provide both local and average data. See more information at https://www.idics.org/

### What is a Jupyter notebook and how to use it?

A Jupyter notebook is a document that supports mixing executable code ( **Ju**lia, **Pyt**hon, **R**, etc.), equations, visualizations, and narrative text, known as [literate computing](https://osf.io/h9gsd/). There are two main options to interact with a Jupyter notebook:

- Open the notebook locally on your computer, i.e. the notebook is stored on your hard disk. This is the fastest way to open and interact with a notebook and always have access to it. This requires, however, installing a Python distribution that includes Jupyter and several Python scientific libraries (see _Requirements & Python installation_ below) and download the notebooks. _A link to download all the notebooks available soon!_
- Open the notebook on remote servers as a web application (e.g. in [mybinder.org](https://mybinder.org/) or [Google Colab](https://colab.research.google.com/)). The process of loading the notebook in this way can be quite slow, depending on its size, but it has the advantage of requiring nothing more than a browser and an internet connection. _More details on this modality coming soon!_

Lastly, there are exceptional Jupyter notebook video tutorials on the web (others not so much). For example, this one here https://www.youtube.com/watch?v=HW29067qVWk

### Requirements & Python installation

A popular software distribution that includes the Jupyter notebook is the [Anaconda distribution (individual edition)](https://www.anaconda.com/products/individual), which is free, includes all the necessary scientific packages (> 5 GB disk space), and is ready to install on Windows, Mac, and Linux. Pick the installer with the newest version of Python and voila! Another option is to install [Miniconda](https://docs.conda.io/en/latest/miniconda.html), which is a free minimal Python & Conda installation. If you are not sure whether you should install it, read [this](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html#anaconda-or-miniconda). If you installed Miniconda, open the _Anaconda prompt_ and use the following command to install the minimum necessary dependencies to interact locally with the notebooks.

```shell
>>> conda install numpy pandas matplotlib jupyter ipython jupyterlab astropy 
```

Jupyter notebooks can be launched by open the Anaconda navigator (if you installed Anaconda) and launching the _Jupyter lab_ (preferred option) or the _Jupyter notebook_ or, more quickly, from the terminal (_Anaconda prompt_) typing ``jupyter notebook`` or ``jupyter lab``. Then, you'll see the application opening in one of your browser tabs. If you prefer a standalone application to interact with the notebooks you can install https://code.visualstudio.com/ and add the *Python* and *Jupyter* plug-ins.

### How to contribute to this project?

The GitHub website hosting the project provides several options (you will need a GitHub account, it’s free!):

- Open a [discussion](https://github.com/marcoalopez/Jupyter4DICe/discussions): This is a place to:
  - Ask questions you are wondering about.
  - Share ideas.
  - Engage with the developers (still just me).
- Open and [issue](https://github.com/marcoalopez/Jupyter4DICe/issues): This is a place to track bugs or requests for specific features on the notebooks.
- Create a [pull request](https://github.com/marcoalopez/Jupyter4DICe/pulls): You modified, corrected or added a feature to one of the notebooks and send it for one of the developers to review it and add it to the main page.

Besides, if you want to contribute to the project, you might want to glimpse at the [code of conduct](https://github.com/marcoalopez/Jupyter4DICe/blob/main/CODE_OF_CONDUCT.md) (TLDR: be nice to others 😉).  