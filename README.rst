itkwidgets
==========

.. image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
    :target: https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/LICENSE
    :alt: License

.. image:: https://img.shields.io/pypi/v/itkwidgets.svg
    :target: https://pypi.python.org/pypi/itkwidgets
    :alt: PyPI

.. image:: https://circleci.com/gh/InsightSoftwareConsortium/itkwidgets.svg?style=shield
    :target: https://circleci.com/gh/InsightSoftwareConsortium/itkwidgets
    :alt: Build status

.. image:: https://mybinder.org/badge.svg
    :target: https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples%2F3DImage.ipynb

Interactive `Jupyter <https://jupyter.org/>`_ widgets to visualize images,
point sets, and meshes.

.. image:: https://i.imgur.com/d8aXycW.png
    :width: 800px
    :alt: itkwidgets chest CT in JupyterLab

**Key Features**:

- Visualize 2D and 3D images, point sets, and geometry, e.g. meshes, in Jupyter
- Support for

  - NumPy array images
  - itk.Image
  - Dask array images
  - vtk.vtkImageData
  - pyvista.UniformGrid
  - vtkplotter.Volume
  - ImageJ / Fiji / ImageJ2 images
  - Additional NumPy array-like objects

  - NumPy array point sets
  - itk.PointSet
  - vtk.vtkPolyData point sets
  - pyvista.PolyData point sets

  - itk.Mesh
  - vtk.vtkPolyData
  - vtk.vtkStructuredGrid
  - vtk.vtkUnstructuredGrid
  - vtk.vtkActor
  - vtk.vtkVolume
  - vtk.vtkAssembly
  - pyvista.PolyData
  - pyvista.StructuredGrid
  - pyvista.UnstructuredGrid
  - vtkplotter.Actor
  - vtkplotter.Assembly

- Exquisite volume rendering
- Tri-plane volume slicing
- Innovative, powerful opacity transfer function / window / level widget
- Anisotropic voxel spacing supported
- Image line profile widget
- Widgets to select solid colors for geometry or colormaps when point data or
  cell data is availble
- Visualize point sets as points or spheres and interactively adjust the point
  size
- Combine with other *ipywidgets* to quickly create graphical interfaces
  that interactively provide insights into data algorithms

.. image:: https://thumbs.gfycat.com/ShyFelineBeetle-size_restricted.gif
    :width: 640px
    :alt: itkwidgets demo
    :align: center

These widgets are designed to support spatial analysis with the `Insight Toolkit
(ITK) <https://itk.org/>`_, but they work equally well with other spatial analysis tools
in the scientific Python ecosystem.

These widgets are built on
`itk.js <https://github.com/InsightSoftwareConsortium/itk-js>`_ and
`vtk.js <https://github.com/Kitware/vtk-js>`_.

Examples on Binder
------------------

Data types:

- `Binder: 2D ITK Images <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples%2F2DImage.ipynb>`_
- `Binder: 3D ITK Images <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples%2F3DImage.ipynb>`_
- `Binder: Dask Array images <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/DaskArray.ipynb>`_
- `Binder: Large volumes <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/LargeVolumes.ipynb>`_
- `Binder: NumPy array images (processed with SciPy) <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/NumPyArrayImage.ipynb>`_
- `Binder: NumPy array images (processed with scikit-image) <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/scikit-image.ipynb>`_
- `Binder: NumPy array for image with anisotropic spacing <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/ImageWithAnisotropicPixelSpacing.ipynb>`_
- `Binder: NumPy array point sets <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/NumPyArrayPointSet.ipynb>`_
- `Binder: ITK Mesh <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/Mesh.ipynb>`_

Tasks:

- `Binder: Compare images with a checkerboard pattern <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/Checkerboard.ipynb>`_
- `Binder: Examine a line profile <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/LineProfile.ipynb>`_
- `Binder: Interactively explore algorithm parameters <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/InteractiveParameterExploration.ipynb>`_
- `Binder: Record a video <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/RecordAVideo.ipynb>`_
- `Binder: Select a region of interest <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/SelectRegionOfInterest.ipynb>`_
- `Binder: Specify camera parameters <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/SpecifyCameraParameters.ipynb>`_
- `Binder: Specify a colormap <https://mybinder.org/v2/gh/InsightSoftwareConsortium/itkwidgets/master?filepath=examples/SpecifyAColormap.ipynb>`_

Installation
------------

To install the widgets for the Jupyter Notebook with pip::

  pip install itkwidgets

or with conda::

  conda install -c conda-forge itkwidgets

For Jupyter Lab, additionally run::

  jupyter labextension install @jupyter-widgets/jupyterlab-manager itkwidgets

Usage
-----

In Jupyter, import the ``view`` function::

  from itkwidgets import view

Then, call the ``view`` function at the end of a cell, passing in the image to
examine::

  view(image)

For information on additional options, see the ``view`` function docstring::

  view?

Other available widgets:

- ``itkwidgets.line_profile``: Plot an intensity line profile.
- ``itkwidgets.checkerboard``: Compare two images in a checkerboard pattern.

Advanced Usage
^^^^^^^^^^^^^^

The *itkwidgets* are based on `ipywidgets
<https://ipywidgets.readthedocs.io/en/latest/examples/Widget%20Basics.html>`_.
As a consequence, widgets traits can be queried, assigned, or observed with
the `viewer` object returned by the `view` function. *itkwidgets* can
be combined with other *ipywidgets* to quickly explore algorithm parameters,
create graphical interfaces, or create data visualization dashboards.

Mouse Controls
^^^^^^^^^^^^^^

**Left click + drag**
  Rotate

**Right click + drag** or **shift + left click + drag**
  Pan

**Mouse wheel** or **control + left click + drag** or **pinch**
  Zoom

**Alt + left click + drag left-right**
  Change color transfer function window

**Shift + left click + drag top-bottom**
  Change color transfer function level

**Shift + alt + left click + drag top-bottom**
  Change primary Gaussian volume opacity transfer function magnitude

Keyboard Shortcuts
^^^^^^^^^^^^^^^^^^

Keyboard shortcuts take effect when the mouse is positioned inside the viewer.
All shortcuts are prefixed with **Alt+**. Corresponding keys for the Dvorak
keyboard layout have the same effect.

**Alt + 1**
  X-plane mode

**Alt + 2**
  Y-plane mode

**Alt + 3**
  Z-plane mode

**Alt + 4**
  Volume rendering mode

**Alt + q**
  Toggle user interface

**Alt + w**
  Toggle region of interest (ROI) selection widget

**Alt + e**
  Reset ROI

**Alt + r**
  Reset camera

**Alt + s**
  Toggle slicing planes in volume rendering mode

**Alt + f**
  Toggle fullscreen


Examples
--------

After installation, try the following examples that demonstrate how to visualize:

- `2D ITK Images <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/2DImage.ipynb>`_
- `3D ITK Images <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/3DImage.ipynb>`_
- `Dask Array images <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/DaskArray.ipynb>`_
- `Large volumes <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/LargeVolumes.ipynb>`_
- `ImageJ ImgLib2 images <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/ImageJImgLib2.ipynb>`_ (requires `conda <https://conda.io/>`_ and a local `Fiji <https://fiji.sc/>`_ installation)
- `NumPy array images (processed with SciPy) <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/NumPyArrayImage.ipynb>`_
- `NumPy array images (processed with scikit-image) <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/scikit-image.ipynb>`_
- `NumPy array for image with anisotropic spacing <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/ImageWithAnisotropicPixelSpacing.ipynb>`_
- `VTK vtkImageData <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/vtkImageData.ipynb>`_
- `pyvista UniformGrid <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/pyvista.UniformGrid.ipynb>`_
- `NumPy array point sets <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/NumPyArrayPointSet.ipynb>`_
- `ITK Mesh <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/Mesh.ipynb>`_
- `VTK vtkPolyData <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/vtkPolyData.ipynb>`_
- `VTK vtkUnstructuredGrid <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/vtkUnstructuredGrid.ipynb>`_
- `pyvista PolyData <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/pyvista.PolyData.ipynb>`_
- `pyvista StructuredGrid <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/pyvista.StructuredGrid.ipynb>`_
- `pyvista UnstructuredGrid <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/pyvista.UnstructuredGrid.ipynb>`_
- `pyvista LiDAR <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/pyvistaLiDAR.ipynb>`_
- `vtkplotter actors and volumes <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/vtkplotter.ipynb>`_

or how to:

- `Compares images with a checkerboard pattern <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/Checkerboard.ipynb>`_
- `Examine a line profile <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/LineProfile.ipynb>`_
- `Interatively explore algorithm parameters <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/InteractiveParameterExploration.ipynb>`_
- `Record a video <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/RecordAVideo.ipynb>`_
- `Select a region of interest <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/SelectRegionOfInterest.ipynb>`_
- `Specify camera parameters <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/SpecifyCameraParameters.ipynb>`_
- `Specify a colormap <https://github.com/InsightSoftwareConsortium/itkwidgets/blob/master/examples/SpecifyAColormap.ipynb>`_


Troubleshooting
---------------

If you experience the notebook warning::

  IOPub data rate exceeded.
  The notebook server will temporarily stop sending output
  to the client in order to avoid crashing it.
  To change this limit, set the config variable
  `--NotebookApp.iopub_data_rate_limit`.

Set the notebook configuration value::

  jupyter notebook --NotebookApp.iopub_data_rate_limit=1e12

Hacking
-------

Participation is welcome! For a development installation (requires `Node.js <https://nodejs.org/en/download/>`_)::

  git clone https://github.com/InsightSoftwareConsortium/itkwidgets.git
  cd itkwidgets
  python -m pip install -r requirements-dev.txt -r requirements.txt
  python -m pip install -e .
  jupyter nbextension install --py --symlink --sys-prefix itkwidgets
  jupyter nbextension enable --py --sys-prefix itkwidgets
  jupyter nbextension enable --py --sys-prefix widgetsnbextension
  python -m pytest

The above commands will setup your system for development with the Jupyter
Notebook. To develop for Jupyter Lab, additionally run::

  jupyter labextension install @jupyter-widgets/jupyterlab-manager
  jupyter labextension install ./js

.. note::

  Historical note: this project was previously named *itk-jupyter-widgets*, but it was renamed to *itkwidgets* to be consistent with the package name.

.. warning::

  This project is under active development. Its API and behavior may change at
  any time. We mean it.
