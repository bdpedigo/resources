# Pedigo's Python development recommendations
Please let me know if anything is confusing or could be explained better

-------
Get [miniconda](https://docs.conda.io/en/latest/miniconda.html)
- Miniconda includes a Python distribution as well as the [Conda package manager](https://en.wikipedia.org/wiki/Conda_(package_manager))

Create a [conda environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) from the terminal
- A virtual environment is a way to manage a set of dependencies and requirements for a particular project
- This may seem like more work than installing things without a virtual environment, but it will save you a lot of stress later
- From the command line, run 
   - ```$ conda create -n {my_environment_name} python=3.7```
- You can also install packages and specify versions at creation
   - ```$ conda create -n {my_environment_name} python=3.7 scipy=0.15.0```
- See the linked tutorial above for more details

Install [VS Code](https://code.visualstudio.com/docs/setup/setup-overview)
- This is what I recommend for your IDE

Install [VS Code Python Extension](https://code.visualstudio.com/docs/python/python-tutorial)
- Follow the instructions above
- When you get to "Select a Python interpreter" use the name of the virtual environment that you created earlier
   - More details on selecting an environment [here](https://code.visualstudio.com/docs/python/environments)
- Follow the rest of the instructions to go through creating and running a new Python file

---
There are other libraries that I find very useful while programming in VS Code. 

Modifying settings in VS Code
In all of the below, I am showing the ```settings.json``` argument to change
in order to activate these libraries.


Formatting code 
- I use [Black](https://black.readthedocs.io/en/stable/) as my code formatter 
- It is very nice to not have to worry about line overhangs, spacing, etc. 
- To set up:
   - ```"python.formatting.provider" : "black"```
   - VS Code may prompt you to install ```Black```
   - Otherwise, run ```$ pip install black``` while in the correct virtual/conda environment
   
Linting
- I use [flake8]() to [lint](https://en.wikipedia.org/wiki/Lint_(software)) my Python code
- To set up:
   - ```"python.linting.enabled" : true```
   - ```"python.linting.flake8Enabled" : true```
   - VS Code may prompt you to install ```flake8```
   - Otherwise, run ```$ pip install flake8``` while in the correct virtual/conda environment
   
Rope
- I use [rope](https://github.com/python-rope/rope/blob/master/docs/rope.rst) to refactor my Python code
- Refactoring allows you to right-click the name of something in your code and change its name. It can 
  also refactor functions or variables for you. 
- To set up: 
   - Right-click on a variable and attempt to do "Rename symbol"
   - VS Code should prompt you to install ```rope```
   - Otherwise, run ```pip install rope```
  
Sort Imports 
- VS Code uses [isort](https://isort.readthedocs.io/en/latest/) to sort imports 
- This should be enabled by default
- To use, right-click anywhere in your file and select sort imports



Other recommentations (Pedigo needs to finish this part)
- VS Code Python data science tools 
   - Running cells 
   - Formatting plots nicely
- Known bugs 
   - Terminal environment activation starting late
   - Backend jupyter notebook not restarting when running code cells
- Testing with Pytest
- Setting up Github
