# Urban Morphology with Python: City Structure as a Predictor and a Target

The materials for the SDSS 2025 workshop on Urban Morphology with Python conducted by [**Martin Fleischmann**](https://github.com/martinfleis) and [**James D. Gaboardi**](https://github.com/jGaboardi).

## Setting up to follow the workshop

### Step 1: Download the workshop material

If you are a git user, you can get the workshop materials by cloning this repo:

```sh
git clone https://github.com/martinfleis/sdss2025.git
cd sdss2025
```

Otherwise, to download the repository to your local machine as a zip-file,
click the `download ZIP` on the repository page
<https://github.com/martinfleis/sdss2025>
(green button "Code"). After the download, unzip on the location you prefer
within your user account (e.g. `My Documents`, not `C:\`).

### Step 2: Install the required Python packages

You can set the environment to run the notebook in a few ways - Pixi (recommended) uv (also recommended[^1]), Conda/Mamba, pip.

[^1]: I prefer Pixi as it installs packages from conda-forge which are using same binaries of compiled dependencies. uv installs from PyPI, so each package will bring its own version.

#### Pixi

If you'd like to run the notebook, you can create an environment using [Pixi](https://pixi.sh/latest/). See the Pixi [installation instructions](https://pixi.sh/latest/#__tabbed_1_2).

With Pixi installed, open a command line and start Jupyter Lab from the included Pixi environment. Pixi will automatically install all required dependencies and start the Jupyter Lab IDE with the notebook.

```sh
pixi run jupyter lab workshop.ipynb
```

#### uv

If you'd like to run the notebook, you can create an environment using [`uv`](https://docs.astral.sh/uv/). See the `uv` [installation instructions](https://docs.astral.sh/uv/getting-started/installation/).

With `uv` installed, open a command line, and start Jupyter Lab from the included `uv` environment. `uv` will automatically install all required dependencies and start the Jupyter Lab IDE with the notebook.

```sh
uv run jupyter lab workshop.ipynb
```

#### Conda/Mamba

If you prefer to use conda-based solutions (conda, mamba, anaconda, micromamba), you can create a conda environment using attached environment.yml file.

Using conda, we recommend to create a new environment with all packages using
the following commands (after cloning or downloading this GitHub repo and
navigating to the directory, see above):

```bash
# setting the configuation so all packages come from the conda-forge channel
conda config --add channels conda-forge
conda config --set channel_priority strict
# mamba provides a faster implementation of conda
conda install mamba
# creating the environment
mamba env create --file environment.yml
# activating the environment
conda activate sdss2025
```

Then you can start the notebook.

```sh
jupyter lab workshop.ipynb
```

#### pip / Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/martinfleis/sdss2025/blob/main/workshop.ipynb)

You can also install the necessary dependencies from PyPI using `pip`. The instructions can be used both locally and within Google Colab.

```bash
pip install momepy scikit-learn numba osmnx geopy matplotlib mapclassify folium clustergram bokeh geoplanar neatnet
```

If you are working locally (not using Google Colab), you may want to install Jupyter Lab as well.

```bash
pip install jupyterlab
```

Then you can start the notebook.

```sh
jupyter lab workshop.ipynb
```

## Data

This repository contains a subset of data retrieved from the [CDRC](https://data.cdrc.ac.uk/dataset/index-multiple-deprivation-imd#data-and-resources) under UK Open Government Licence (OGL). Data provided by the Consumer Data Research Centre, an ESRC Data Investment: ES/L011840/1, ES/L011891/1.

## Acknowledgements

* Copyright: This manuscript has been authored in part by UT-Battelle, LLC under Contract No. DE-AC05-00OR22725 with the U.S. Department of Energy. The United States Government retains and the publisher, by accepting the article for publication, acknowledges that the United States Government retains a non-exclusive, paid-up, irrevocable, world-wide license to publish or reproduce the published form of this manuscript, or allow others to do so, for United States Government purposes. The Department of Energy will provide public access to these results of federally sponsored research in accordance with the DOE Public Access Plan (`http://energy.gov/downloads/doe-public-access-plan`).
