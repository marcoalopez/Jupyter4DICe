
![](https://raw.githubusercontent.com/marcoalopez/Jupyter4DICe/main/imgs/header.webp)_This project is maintained by [Marco A. Lopez-Sanchez](https://marcoalopez.github.io/)_ - Last update: 2023/06/12

> 🚨 This project is under continuous development and the examples of Jupyter notebooks may not be finished. In any event, the examples they contain are fully usable.

## What is this?

[Jupyter4DICe](https://github.com/marcoalopez/Jupyter4DICe) is a series of [Jupyter notebooks](https://jupyter.org/) written in Python for post-processing digital image correlation (DIC) data obtained with the open-source digital image correlation [DICe tool](https://github.com/dicengine/dice). Although the DICe tool already produces a file that can be viewed directly with an application called Paraview, the use of Jupyter notebooks has two main advantages:

- it is more versatile
- it allows you to record and detail all post-processing steps, which is advantageous for reproducibility. For example, this allows you to create a complete step-by-step report that you can use as supplementary material in your scientific publications.

These notebooks assume that the user is familiar with basic Python concepts (data types, loops, conditionals, functions, modules), and the Numpy and Matplotlib libraries. The goal of these notebooks is to keep dependencies to a minimum to avoid future compatibility problems, using only well-manteined Python libraries. All _ad hoc_ methods used for the DIC data treatment are contained within the notebooks.

### The notebooks

To visualize the content of the notebooks as a website just click on the topic you are interested in (the list may increase or decrease without notice over time)

- [Loading data from DICe output](https://nbviewer.jupyter.org/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/LoadingDICe_data.ipynb) (Done) / [View on Deepnote](https://deepnote.com/viewer/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/LoadingDICe_data.ipynb)
- [Visualizing and assessing strain](https://github.com/marcoalopez/Jupyter4DICe/blob/4107e0e8483b9d72ae1e5693b360097c099540b7/notebooks/Strain_analysis.ipynb) (working on it!) / [View on Deepnote](https://deepnote.com/viewer/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/Strain_analysis.ipynb)
- [Visualizing and assessing displacements](https://nbviewer.jupyter.org/github/marcoalopez/Jupyter4DICe/blob/24dc818212c3b12139f421712aa60f1572298ad2/notebooks/Displacement_analysis.ipynb) (working on it!) / [View on Deepnote](https://deepnote.com/viewer/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/Displacement_analysis.ipynb)
- [How to assess and visualise the quality of the DIC solution and clean the dataset](https://nbviewer.jupyter.org/github/marcoalopez/Jupyter4DICe/blob/main/notebooks/assesing_quality.ipynb?flush_cache=true) (TODO!)

If you have utilized the provided examples in these Jupyter notebooks as a foundation for processing your DIC data and intend to publish, we kindly ask to consider citing the following paper,  which outlines the complete protocol:

> Lopez-Sanchez, M.A., Chauve, T., Montagnat, M., Tommasi, A., 2023. Decoupling between strain localisation and the microstructural record revealed by in-situ strain measurements in polycrystalline ice. Earth and Planetary Science Letters 611, 118149. https://doi.org/10.1016/j.epsl.2023.118149

By acknowledging this paper, you provide proper credit to the authors and acknowledge their work as the basis for the methodology used in processing your DIC data.

## FAQs

### What is digital image correlation?

Digital image correlation is an image-based method that uses digital image recording and tracking techniques to make accurate 2D (or 3D) full-field measurements during the deformation of a sample. Tracking coordinate fields allows the user to estimate different parameters of interest such as [displacement](https://en.wikipedia.org/wiki/Displacement_field_(mechanics)) (motion), [strains](https://en.wikipedia.org/wiki/Strain_(materials_science)), strain rates, particle velocities, etc. The technique is non-contact, usually inexpensive, and can be applied at virtually any scale (from [nano](https://doi.org/10.1016/j.actamat.2020.05.029) to [kilometric](https://doi.org/10.1007/s11340-014-9893-z) scales), becoming increasingly common in many areas of science and engineering. In mechanical tests, the amount of information collected compared to [strain gauges](https://en.wikipedia.org/wiki/Strain_gage) such as extensometers is increased due to the ability to provide both local (full field) and average (mean field) information. More useful information at https://www.idics.org/

### What is a Jupyter notebook and how to use it?

A Jupyter notebook is a document that supports mixing executable code ( **Ju**lia, **Pyt**hon, **R**, etc.), equations, visualizations, and narrative text, known as [literate computing](https://osf.io/h9gsd/). There are two main options to interact with a Jupyter notebook:

- Open the notebook locally on your computer, i.e. the notebook is stored on your hard disk. This is the fastest way to open and interact with a notebook and always have access to it. This requires, however, installing a Python distribution that includes Jupyter and several Python scientific libraries (see _Requirements & Python installation_ below) and download the notebooks. _A link to download all the notebooks will be available soon!_
- Open the notebook on remote servers as a web application (e.g. in [mybinder.org](https://mybinder.org/) or [Google Colab](https://colab.research.google.com/)). The process of loading the notebook in this way can be quite slow, depending on its size, but it has the advantage of requiring nothing more than a browser and an internet connection. _More details on this modality coming soon!_

Lastly, there are exceptional Jupyter notebook video tutorials on the web (others not so much). For example, this one here https://www.youtube.com/watch?v=HW29067qVWk

### Requirements & Python installation

A popular software distribution that includes the Jupyter notebook is the [Anaconda distribution (individual edition)](https://www.anaconda.com/products/individual), which is free, includes all the necessary scientific packages (> 5 GB disk space), and is ready to install on Windows, Mac, and Linux. Pick the installer with the newest version of Python and voila! Another option is to install [Miniconda](https://docs.conda.io/en/latest/miniconda.html), which is a free minimal Python & Conda installation. If you are not sure whether you should install it, read [this](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html#anaconda-or-miniconda). If you installed Miniconda, open the _Anaconda prompt_ and use the following command to install the minimum necessary dependencies to interact locally with the notebooks.

```shell
>>> conda install numpy pandas matplotlib scipy jupyter ipython jupyterlab astropy 
```

Jupyter notebooks can be launched from the terminal (_Anaconda prompt_) typing ``jupyter lab`` or  ``jupyter notebook``. Also, by open the Anaconda navigator (if you installed Anaconda) and launching the _Jupyter lab_ or the _Jupyter notebook_. Then, you'll see the application opening in your browser. If you prefer a standalone application to interact with the notebooks you can install https://code.visualstudio.com/, which is completely free, and add the *Python* and *Jupyter* plug-ins.

### How to contribute to this project?

The GitHub website hosting the project provides several options (you will need a GitHub account, it’s free!):

- Open a [discussion](https://github.com/marcoalopez/Jupyter4DICe/discussions): This is a place to:
  - Ask questions you are wondering about.
  - Share ideas.
  - Engage with the developers (still just me).
- Open and [issue](https://github.com/marcoalopez/Jupyter4DICe/issues): This is a place to track bugs or requests for specific features on the notebooks.
- Create a [pull request](https://github.com/marcoalopez/Jupyter4DICe/pulls): You modified, corrected or added a feature to one of the notebooks and send it for one of the developers to review it and add it to the main page.

For a quick explanation see https://www.youtube.com/watch?v=R8OAwrcMlRw. Besides, if you want to contribute to the project, you might want to glimpse at the [code of conduct](https://github.com/marcoalopez/Jupyter4DICe/blob/main/CODE_OF_CONDUCT.md) (TLDR: be nice to others 😉).

### Is the DICe tool required to use the notebooks?

Not necessarily. We encourage the use of this software because it is free and open-source and allows the whole process to be traceable and reproducible, but the data processing shown in the notebooks is generally applicable. You would only need to import the data from the output files of your DIC software of choice.

---

*Copyright © 2023 Marco A. Lopez-Sanchez*  

*Information presented on this website and the notebooks is provided without any express or implied warranty and may include technical inaccuracies or typing errors; the author reserve the right to modify or enhance the content of this website as well as the notebooks at any time without previous notice. This webpage and the notebooks are not liable for the content of external links. Notebook contents under [Creative Commons Attribution license CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) and codes under [Mozilla Public License 2.0](https://www.mozilla.org/en-US/MPL/2.0/).*

*Hosted on GitHub Pages — This website was created with [Typora](https://typora.io/)*

