# Python Data Science Workshop
![LISA logo](https://raw.githubusercontent.com/wshand/Python-Data-Science-Workshop/master/assets/LISA_logo_medium.jpg)

Notebooks and code for the Spring 2019 Python Data Science Workshop at CU Boulder. Sponsored by the [Laboratory for Interdisciplinary Statistical Analysis (LISA)](https://www.colorado.edu/lab/lisa/).

* [Courses](#courses)
* [Workshop pre-requisites](#prereqs)
* [Required software](#required-software)


## Courses <a id="courses"></a>
**Note**: these workshops are brand-new as of spring 2019. As a result, all of the materials in this repository are still under active development. Currently, the notebook for the scikit-learn workshop is the only one with a complete first draft; the remaining notebooks are still incomplete.

I am developing notebooks for the following short courses:

### Python Data Wrangling
> This course teaches some of the building blocks for handling data in Python. We will show how to parse and manipulate data using Numpy and Pandas, and perform interactive visualization with Plotly. We analyze a real dataset using Scipy, demonstrating how to perform basic statistical tasks in Python.

Notebook: [1. Introduction to Data Science in Python.ipynb](https://github.com/wshand/Python-Data-Science-Workshop/blob/master/1.%20Introduction%20to%20Data%20Science%20in%20Python.ipynb)

-----------------------------------------------------
### Intro to Machine Learning in Python with Scikit-learn
> This course introduces the Scikit-learn library for doing machine learning in Python. Students will start by learning about support vector machines, and gradually explore how Scikit-learn allows you to build a full machine learning pipeline, from feature extraction all the way through to prediction.

Notebook: [2. Intro to Machine Learning in Python with Scikit-learn.ipynb](https://github.com/wshand/Python-Data-Science-Workshop/blob/master/2.%20Intro%20to%20Machine%20Learning%20in%20Python%20with%20Scikit-learn.ipynb)

-----------------------------------------------------
### Building Neural Networks with Keras
> Neural networks are becoming an increasingly important tool in machine learning. In this short course, we demonstrate how to rapidly prototype an artificial neural network (ANN) in Python using the Keras library. We briefly introduce ANNs, including important variations like convolutional networks. Using Keras, students will build their own networks for some basic machine learning problems.

Notebook: [3. Building Neural Networks With Keras.ipynb](https://github.com/wshand/Python-Data-Science-Workshop/blob/master/3.%20Building%20Neural%20Networks%20with%20Keras.ipynb)

## Workshop pre-requisites <a id="prereqs"></a>
For the first workshop, you will need some basic knowledge of Python. It would also help to have at least a little familiarity with Jupyter Notebook (e.g. you should know how to run code cells).

For the second and third workshops you will also need to understand [numpy](https://docs.scipy.org/doc/numpy/reference/) (which is taught in the first workshop). Knowing [matplotlib](https://matplotlib.org/) is a plus but not required.

## Required software <a id="required-software"></a>
In order to participate in this workshop, you have to be able to run a Jupyter Notebook in your web browser. Unless you are using mybinder, you will also need to install some libraries. Below I have provided four methods for running these notebooks and installing the required libriaries:

1. Using [mybinder](https://mybinder.org)
2. Using [Anaconda](https://www.anaconda.com/)
3. By installing Jupyter Notebook through `pip`.
4. Through [CU Boulder's JupyterHub server](https://curc.readthedocs.io/en/latest/gateways/jupyterhub.html)

### mybinder
[mybinder](https://mybinder.org) is an online service that will create an environment for you to run the Jupyter Notebook, and then allow you to run that notebook in your browser. **Note**: mybinder may take a little while to load.

To use mybinder, click the link below that will direct you to the workshop (1, 2, or 3) that you want.

* **Workshop 1:** Python Data Wrangling: https://mybinder.org/v2/gh/wshand/Python-Data-Science-Workshop/master?filepath=1.%20Introduction%20to%20Data%20Science%20in%20Python.ipynb
* **Workshop 2:** Intro to Machine Learning in Python with Scikit-learn: https://mybinder.org/v2/gh/wshand/Python-Data-Science-Workshop/master?filepath=2.%20Intro%20to%20Machine%20Learning%20in%20Python%20with%20Scikit-learn.ipynb
* **Workshop 2:** Building Neural Networks with Keras: https://mybinder.org/v2/gh/wshand/Python-Data-Science-Workshop/master?filepath=3.%20Building%20Neural%20Networks%20with%20Keras.ipynb

-----------------------------------------------------
### Anaconda
First, if you haven't already, install [Anaconda](https://www.anaconda.com/) on your computer. Then, from your terminal, run

```
conda install --yes --file requirements.txt
```

while `cd`'d into this directory. If that command doesn't work, you can also try [this workaround](https://stackoverflow.com/a/38609653) from StackOverflow:

```
while read requirement; do conda install --yes $requirement; done < requirements.txt
```

-----------------------------------------------------
### Using `pip`
Install Jupyter notebook with `pip3 install jupyter` at the terminal, and then run

```
pip3 install -r requirements.txt
```

Alternatively, if you're a fan of [Python virtual environments](https://docs.python.org/3/tutorial/venv.html), you can create a virtual environment for these notebooks and install the requirements from `requirements.txt` there. Then, with the environment activated, you can install the virtual environment as a kernel for Jupyter by running the following snippet (credit: [tschundler on StackOverflow](https://stackoverflow.com/a/37891993)):

```
pip install ipykernel
python -m ipykernel install --user --name workshop-kernel
```

-----------------------------------------------------
### CU Boulder JupyterHub server
Start by setting up a [CU research computing account](https://rcamp.rc.colorado.edu/accounts/account-request/create/organization). Once that's complete, follow the [research computing center's instructions](https://curc.readthedocs.io/en/latest/gateways/jupyterhub.html#start-a-notebook-server) for using JupyterHub to run a Jupyter Notebook on CU's network.
