---
layout: page
title: "Setup"
permalink: /setup/
---

## Installing Python Using Anaconda

[Python][python] is a popular language for scientific computing, and a frequent choice
for machine learning as well. Installing all of its scientific packages
individually can be a bit difficult, however, so we recommend the installer [Anaconda][anaconda]
which includes most (but not all) of the software you will need.

Regardless of how you choose to install it, please make sure you install Python
version 3.x (e.g., 3.4 is fine). Also, please set up your python environment at
least a day in advance of the workshop.  If you encounter problems with the
installation procedure, ask your workshop organizers via e-mail for assistance so
you are ready to go as soon as the workshop begins.

### Windows - [Video tutorial][video-windows]

1. Open [http://continuum.io/downloads][continuum-windows]
   with your web browser.

2. Download the Python 3 installer for Windows.

3. Double-click the executable and install Python 3 using _MOST_ of the
   default settings. The only exception is to check the
   **Make Anaconda the default Python** option.

### Mac OS X - [Video tutorial][video-mac]

1. Open [http://continuum.io/downloads][continuum-mac]
   with your web browser.

2. Download the Python 3 installer for OS X.

3. Install Python 3 using all of the defaults for installation.

### Linux

Note that the following installation steps require you to work from the shell.
If you run into any difficulties, please request help before the workshop begins.

1.  Open [http://continuum.io/downloads][continuum-linux] with your web browser.

2.  Download the Python 3 installer for Linux.

3.  Install Python 3 using all of the defaults for installation.

    a.  Open a terminal window.

    b.  Navigate to the folder where you downloaded the installer

    c.  Type

    ~~~
    $ bash Anaconda3-
    ~~~
    {: .language-bash}

    and press tab.  The name of the file you just downloaded should appear.

    d.  Press enter.

    e.  Follow the text-only prompts.  When the license agreement appears (a colon
        will be present at the bottom of the screen) hold the down arrow until the
        bottom of the text. Type `yes` and press enter to approve the license. Press
        enter again to approve the default location for the files. Type `yes` and
        press enter to prepend Anaconda to your `PATH` (this makes the Anaconda
        distribution the default Python).

> ## conda version
>
> If you already have anaconda installed at your computer, make sure you have an up-to-date version of conda running.
> See [these instructions](https://docs.anaconda.com/anaconda/install/update-version/) for updating conda.
>
{: .callout}

## Installing the required packages

Open a terminal and type the command (note that installing tensorflow causes keras to
be installed too):
~~~
$ conda install "tensorflow>=2.5" seaborn "scikit-learn>=0.22" pandas
~~~
{: .language-bash}


## Starting a Jupyter Notebook

We will teach using Python in a [Jupyter notebook][jupyter], a
programming environment that runs in a web browser. Jupyter requires a reasonably
up-to-date browser, preferably a current version of Chrome, Safari, or Firefox
(note that Internet Explorer version 9 and below are *not* supported). If you
installed Python using Anaconda, Jupyter should already be on your system. If
you did not use Anaconda, use the Python package manager pip
(see the [Jupyter website][jupyter-install] for details.)

To start the notebook, open a terminal or git bash and type the command:

~~~
$ jupyter notebook
~~~
{: .language-bash}

To start the Python interpreter without the notebook, open a terminal
or git bash and type the command:

~~~
$ python
~~~
{: .language-bash}

## Check your setup
To check whether all packages installed correctly, start a jupyter notebook as
explained above. Run the following lines of code:
~~~
import sklearn
print('sklearn version: ', sklearn.__version__)

import seaborn
print('seaborn version: ', seaborn.__version__)

import pandas
print('pandas version: ', pandas.__version__)

from tensorflow import keras
print('Keras version: ', keras.__version__)
~~~
{:.language-python}

This should output the versions of all required packages without giving errors.
Most versions will work fine with this lesson, but for Keras, the minimum version is 2.2.4, and for sklearn the minimum version is 0.22.

## Fallback option: cloud environment
If a local installation does not work for you, it is also possible to run this lesson in [Google colab](https://colab.research.google.com/). If you open a notebook here, the required packages are already pre-installed.

## Downloading the required datasets

Download the [weather dataset prediction csv][weatherdata] and [BBQ labels][weatherbbqdata].

[anaconda]: https://www.continuum.io/anaconda
[continuum-mac]: http://continuum.io/downloads#_macosx
[continuum-linux]: http://continuum.io/downloads#_unix
[continuum-windows]: http://continuum.io/downloads#_windows
[jupyter]: http://jupyter.org/
[jupyter-install]: http://jupyter.readthedocs.io/en/latest/install.html#optional-for-experienced-python-developers-installing-jupyter-with-pip
[python]: https://python.org
[video-mac]: https://www.youtube.com/watch?v=TcSAln46u9U
[video-windows]: https://www.youtube.com/watch?v=xxQ0mzZ8UvA
[penguindata]: https://zenodo.org/record/3960218/files/allisonhorst/palmerpenguins-v0.1.0.zip?download=1
[weatherdata]: https://zenodo.org/record/4980359/files/weather_prediction_dataset.csv?download=1
[weatherbbqdata]: https://zenodo.org/record/4980359/files/weather_prediction_bbq_labels.csv?download=1
