# Installation Instructions

Install the [Anaconda distribution](https://www.anaconda.com/products/individual), then open *Anaconda prompt*.

## Using environment.yaml

1. Download the [environment.yaml](https://github.com/jamescalam/transformers/blob/main/environment.yaml) for the course.

2. In *Anaconda prompt*, navigate to the directory containing the *environment.yaml* and write `conda env create -f environment.yaml`.

3. Activate the new environment with `conda activate ml`.

4. Move onto the **Installation of PyTorch** section.

## Using requirements.txt

[See here](https://towardsdatascience.com/how-to-setup-python-for-machine-learning-173cb25f0206?sk=8e25eb341c8910209ff683071650c180) for more detailed guide of steps 1-2, 5-7.

1. Create a new Python environment with `conda create -n ml python=3.8.5 anaconda`.

2. Activate the new environment with `conda activate ml`.

3. Navigate to directory containing the *requirements.txt* of this repository ([here](https://github.com/jamescalam/transformers/blob/main/requirements.txt)).

4. Write `pip install -r requirements.txt`.

5. Move onto the **Installation of PyTorch** section.

## Installation of PyTorch

1. Open the [PyTorch installation page](https://pytorch.org/get-started/locally/).

2. Select your specifications. If using GPU, follow instructions in **Enable GPU** section below first. Otherwise, under *CUDA*, select *None*.

3. Copy the given command and run it in Anaconda prompt.

## Enable GPU

If you have a CUDA enabled GPU, you can take advantage of GPU acceleration. If you already have CUDA installed, skip steps 1-3.

1. Install a NVIDIA GPU driver from [here](https://www.nvidia.com/download/index.aspx?lang=en-us).

2. Install [CUDA toolkit](https://developer.nvidia.com/cuda-toolkit-archive), this course originally used version 11.1 but feel free to use a more recent version that is displayed [here](https://pytorch.org/get-started/locally/) under *CUDA*.

3. Install [cuDNN](https://developer.nvidia.com/cudnn).

4. Confirm installation by writing `nvcc --version` in *Anaconda prompt*, the CUDA version should appear (such as *cuda_11.1*).

5. Once complete, install PyTorch using instructions in **Installation of PyTorch** section above.

## Adding to Jupyter

Once your environment is setup, it can be added as a kernel to Jupyter lab/notebook by:

1. In *Anaconda prompt* write `conda active ml`.

2. Then write `python -m ipykernel install --user --name ml --display-name "ML"`

3. The kernel has been installed, switch back to *base* with `conda activate base` then open Jupyter with `jupyter lab`/`jupyter notebook`.