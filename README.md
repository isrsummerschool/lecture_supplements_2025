# lecture_supplements_2025
A collection of codes and notebooks to supplement the 2025 ISR summer school lectures.

___

## Using in the Cloud
You can interact with the Jupyter notebooks in this repository using the free server, Binder. [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/isrsummerschool/lecture_supplements_2025/main)
___

## Using Locally

If you want to use this locally, here are the basics steps:
1. clone this repository
2. set up a python environment
3. run a Jupyter Lab server

Below, we have some basic guiding instructions for installing and using this repository on the Windows 10, macOS, and Linux operating systems.

___

### Windows
#### Recommended Python and Git Installation
We recommend using a package manager to obtain several common developer tools, including git and miniconda. We'll use git to clone git repositories and miniconda to provide a Python installation. Miniconda is a free minimal installation of conda. Many Python packages depend on other system libraries and conda provides both the Python packages and the system libraries in a platform independent way. Basically this helps make using Python on Windows and macOS much easier.
1.    Download and install chocolatey. It’s a package manager for helping you install and manage other things: https://chocolatey.org/
2.    In a powershell terminal with administrative privledges, install git, bash, miniconda, and the mingw32 compiler:
    1. choco install git
    2. choco install miniconda3 --params="'/AddToPath:1'" --params="'/RegisterPython:1'"

For more information, see the documentation on chocolatey for [git](https://community.chocolatey.org/packages/git), [miniconda3](https://community.chocolatey.org/packages/miniconda3), and [anaconda3](https://community.chocolatey.org/packages/anaconda3)

##### Using Anaconda instead of miniconda
If you would prefer to install the full Anaconda instead of miniconda, replace step 2.ii. with:
```
choco install anaconda3 --params="'/AddToPath:1'"
```
#### Installing Python and Git Without Chocolatey
If you would prefer to install git and miniconda without using chocolatey, you can do so by following these instructions:
1. Download and install git-bash from [here](https://gitforwindows.org/)
2. Download and install [miniconda](https://docs.conda.io/en/latest/miniconda.html) or [anaconda](https://www.anaconda.com/products/individual-b)

#### Environment Setup and Usage
All of the following commands should be run either from the "Anaconda Powershell" or "Git Bash":

**1)** Set up a Python environment:

    $ conda create -n isrschool anaconda   #(or use a different name than isrschool)
    $ conda activate isrschool

**2)** Clone this repository:

    $ git clone https://github.com/isrsummerschool/lecture_supplements_2025.git

**3)** Install the python packages that the lecture supplement notebooks need:

    $ cd lecture_supplements_2025
    $ pip install -r requirements.txt

**4)** Now you can start up a Jupyter Lab server and work with the notebooks:

    $ jupyter lab

___

### macOS (with Xcode Command Line Tools, no conda)

**1)** Be sure to have Xcode Command Line Tools. A couple of choices:
1. Install the full Xcode package from App Store
2. Install Xcode Command Line Tools from a terminal:
    - Examples of commands that will trigger a prompt to install Xcode Command Line Tools: *clang*, *gcc*, *git*
    - Or enter the command:

            $ xcode-select --install

Verify that you've successfully install Xcode Command Line Tools:

        $ xcode-select -p

**2)** Install latest with Python 3 from https://www.python.org  (e.g. Download Python 3.13.3)

**3)** Set up a Python environment with the existing or newly installed python3:

Open a terminal, in case you just installed Python3.13 you create a virtual environment using:

    $ python3.13 -m venv isrschool

This will create a virtual environment named isrschool based on Python3.13.
**3.1)** Activate the virtual environment and update pip

    $ source isrschool/bin/activate
Now update pip

    (isrschool) $ pip install --upgrade pip

**3.2** Update the Certificate Authority (CA) certificates For Python 3.13 the path to the exceutable would be:

    $ /Applications/Python 3.13/Install Certificates.command

**4)** Clone this repository:

    (isrschool) $ git clone https://github.com/isrsummerschool/lecture_supplements_2025.git
    
**5)** Inside the virtual environment install the python packages that the lecture supplement notebooks need:

    (isrschool) $ cd lecture_supplements_2025
    (isrschool) $ pip install -r requirements.txt

**6)** Now you can start up a Jupyter Lab server and work with the notebooks:

    (isrschool) $ jupyter lab


### macOS (with conda)

**1)** Install Anaconda for mac from https://www.anaconda.com/products/individual

**2)** Set up a Python environment

Open a terminal, then:

    $ conda create -n isrschool anaconda   #(or use a different name than isrschool)
    $ conda activate isrschool
    
**3)** Install git

    $ conda install git 
    
**4)** Clone this repository:

    $ git clone https://github.com/isrsummerschool/lecture_supplements_2025.git
    
**5)** Install the python packages that the lecture supplement notebooks need:

    $ cd lecture_supplements_2025
    $ pip install -r requirements.txt


**6)** Now you can start up a Jupyter Lab server and work with the notebooks:

    $ jupyter lab

___

### Linux

Here we provide example commands for Ubuntu. The process is identical in other Linux distributions, but the package names and package manager may be different.

**1)** Install ``git`` with your package manager and clone the repository:

    $ sudo apt-get install git-all

**2)** Clone this repository:

    $ git clone https://github.com/isrsummerschool/lecture_supplements_2025.git
    
**3)** Set up a python environment (for more details read this: https://virtualenv.pypa.io/en/latest/user_guide.html)

Install the Python ``pip`` and ``virtualenv`` packages:

    $ sudo apt-get install python3-pip
    $ pip install virtualenv
    
and then create a virtual environment:

    $ virtualenv isrschool
    $ source isrschool/bin/activate
    
and finally, install the python packages that the lecture supplement notebooks need:

    $ cd lecture_supplements_2025
    $ pip install -r requirements.txt

**4)** Now you can start up a Jupyter Lab server and work with the notebooks:

    $ jupyter lab
