# Quick introduction to Python
## History 
In 1989, Guido Van Rossum (a fan of the *Monthy Python's Flying Circus* TV show) created the first version of Python during one week of holidays. Until 1999 he kept developpinig it in his free time and with his colleagues. The Python language is an open-source programming language, to which anyone can contribute. The evolution of the language is supervised by a nonprofit organisation, the [Python Software Foundation](https://www.python.org/psf/), launched in 2001.
Van Rossum was still considered as the leader of the Python Project and titled [*Benevolent Dictator for Life*](https://www.urbandictionary.com/define.php?term=BDFL) until his departure in permanent vacation in 2018 following a [conflict](https://hub.packtpub.com/why-guido-van-rossum-quit/) regarding a new Python feature. 


## Python in the lab
One of the greatest advantage of Python for laboratory scientists is that it can replace you for repetitive tasks. 
A few examples: 

- Imagine you have 30 Excel sheets of similar data. You can write a code to overlap the graphs of all 30 sheets on a single graph in less time then it would take to do it manually. And next time you acquire similar data, you will have your plot in a single click.
- Imagine you want to monitor a chemical reaction by video. Annotating the 1000 frames manually would take hours. You can write a Python code to analyse the images one by one, and compute the desired results automatically. 
  
But you can go even further. It is possible to controle your instruments with Python (camera, LEDs, temperature controllers...) and that way you can launch and control your experiments remotely, even from home or from your cellphone.

To sum up, the time you invest in learning Python will be saved in all the repetitive tasks you will avoid. 

# Installing Anaconda

Installing Anaconda will install a working Python environment. Follow the instructions according to your Operating System (Windows, Mac, Linux OS): https://docs.anaconda.com/anaconda/install/. Don't forget to [verify your installation](https://docs.anaconda.com/anaconda/install/verify-install/) especially if you have never used the command line before.  

# Python packaging

You will soon become familiar with Python packages. A package is a set of features that you install and import in your code so you can use it. For example you can import a package for: 
- array computations (numpy)
- plotting (matplotlib)
- image analysis (scikit-image)
- statistics and regression (scipy, scikit-learn)
- data tables (pandas, equivalent of Excel)

Most of the time, someone has already written the code or function that you want to use. It is often much quicker to search the package online and install it then to code it. 

Another interesting point: the instruments you will use in the lab require repetitive tasks of analysis, graph plotting etc. Someone has probably already written it and posted it online, so check it out first.

# Virtual environments
## Why are they necessary ?
 As Python is an open-source programming language, these packages have been developped voluntarily by different teams. As the language is in constant evolution, one has to be careful with **version mismatches**. 
 Imagine this situation: you wrote a simulation code in 2020 at the begining of your PhD. Now it's 2023 and you need to run the simulation to make a figure for your manuscript. But in the meantime you've updated Python and some pakages and your [simulation](https://pbs.twimg.com/media/Dxqe0QDXcAEBeth?format=jpg&name=small) doesn't work anymore. 

 If want to be able to:
 - work on two different projects which don't use the same python and packages version 
 - share your code with other users
 - be able to run your code years after you wrote it
  
You will need to get familiar with **Virtual Environments**. 
Good news, it is very simple !
The idea is to isolate the Python environment on which your project relies. Everytime you create a new project, you create a new environment. You can fully describe this environment and transfer it to a new computer or share it with other users. 


## Creating a virtual environment

To create the said environment, open the application Anaconda Prompt:
![anaconda prompt](Figures/anaconda_prompt.jpg)

Then type: 

`conda create --name myenv`

you will be asked: 

`proceed ([y]/n)?`

press *y* and it will create the environment called myenv.

Now to switch to your Python environment, type: 

`conda activate myenv`

Your environment name should appear in parenthesis.

![venv](Figures/venv.png)

To exit the environment type:

`conda deactivate` 

Note: 
You will most probably be using Python 3. However if you find out that a code you want to run was written with Python 2, then you must specify the version when you create the environment (called Py2env here):

`conda create --name Py2env python=2.7`

## Anaconda packages

To install a package with Anaconda you should search it in [Anaconda Cloud](https://anaconda.org/) (no need to subscribe). Else type "anaconda install *packagename*" in Google.
The usual syntax is:

`conda install -c conda-forge packagename`

Run it in the Anaconda prompt once your environment is activated.


# Refreshing your memories

## Writing a script
To write a script you need a Python editor. Sypder is a good option, you can also use more advanced editors like [Visual Studio Code](https://code.visualstudio.com/) which also integrates LaTeX, Markdown and much more. 

If you want to use Spyder, install it in your virtual environment: 

`conda install -c anaconda spyder`

Then you can launch it from Anaconda prompt by simply typing:

`spyder`

or from your apps (select the one corresponding to your current environment).

![spyder](Figures/spyder.jpg)









## Pip install

If you can't find the package on Anaconda Cloud, check if it can be installed with pip (Python package installer). Type "pip install *packagename*" in Google and type in the command line:  

`pip install packagename`



## Github packages

Github is a plateform that hosts codes online. Anyone can publish its work on Github