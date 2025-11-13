# RaspiCar

RaspiCar is a project designed for operating a Raspberry Pi-powered car. This repository contains all the necessary code, documentation, and resources to get started controlling the car.

## Documentation

For detailed setup and usage instructions, please refer to the [Reference Manual](./doc/Reference_Manual_RaspiCar.pdf).


## Repository Structure

- **Notebooks/**
  - Contains Jupyter notebookdata analysis of custom recorded datasets.

- **data/**
  - Stores datasets used for training neural network models such as PilotNet

- **doc/**
  - Documentation and user manuals, including `Reference_Manual_RaspiCar.pdf`.

- **src_pi/**
  - Source code for running on the Raspberry Pi.

- **src_pico/**
  - Source code for the Raspberry Pi Pico microcontroller.

- **training/**
  - Script and training logs related to training machine learning models.

- **LICENCE**
  - Licensing information for the project.

- **Makefile**
  - Makefile for automating tasks such as code upload to the Raspberry Pi 3.

- **requirements_pc.txt**
  - Python dependencies for running on a PC.

- **requirements_raspberry.txt**
  - Python dependencies for running on a Raspberry Pi.

## Getting Started

This guide assumes you are setting up the project on a Raspberry Pi.
Please also refer to [User Manual PDF](doc/Reference_Manual_RaspiCar.pdf)

### 1. Prerequisites

1.  Ensure you are using **Python 3.11**.
2.  Install the GDAL library. This is required to build the `fiona` package, which is one of the dependencies:
    ```bash
    sudo apt install libgdal-dev
    ```

### 2. Installation (using uv)

We recommend using `uv` for fast dependency management.

1.  Install `uv`:
    ```bash
    curl -LsSf https://astral.sh/uv/install.sh | sh
    ```

2.  Install the requirements:
    *(After installing uv, you may need to source your shell profile or open a new terminal)*
    ```bash
    uv venv --python 3.11
    source .venv/bin/activate
    uv pip install -r requirements_raspberry.txt
    ```

### 3. Running the Application

To start the program:

```bash
python main.py --log DEBUG
```



