# Pedigo's Python development recommendations
Please let me know if anything is confusing or you have difficulty following this guide

---

## Python, environments, and packages
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

--- 

## IDE
"An [Integrated Development Environment (IDE)](https://en.wikipedia.org/wiki/Integrated_development_environment) is a software application that provides comprehensive facilities to computer programmers for software development."

Install [VS Code](https://code.visualstudio.com/docs/setup/setup-overview)
- This is what I recommend for your IDE

Install [VS Code Python Extension](https://code.visualstudio.com/docs/python/python-tutorial)
- Follow the instructions above
- When you get to "Select a Python interpreter" use the name of the virtual environment that you created earlier
   - More details on selecting an environment [here](https://code.visualstudio.com/docs/python/environments)
- Follow the rest of the instructions to go through creating and running a new Python file


There are other libraries that I find very useful while programming in VS Code. 

### Modifying settings in VS Code

- In VS Code, go to ```Preferences``` > ```Settings```
- At the top left you will see that you can modify User settings for all sessions of VS Code,
  Workspace settings, or folder settings.
- Hit the ```{}``` button to bring up your ```settings.json```
- Add whatever settings you would like to change, making sure to keep the file in JSON format

For all of the modifications below, I'll show what to add to your VS Code ```settings.json```.

Formatting code 
- I use [Black](https://black.readthedocs.io/en/stable/) as my code formatter 
- It is very nice to not have to worry about line overhangs, spacing, etc. 
- To set up:
   - Add ```"python.formatting.provider" : "black"``` to ```settings.json```
   - VS Code may prompt you to install ```Black```
   - Otherwise, run ```$ pip install black``` while in the correct virtual/conda environment
   
Linting
- I use [flake8](http://flake8.pycqa.org/en/latest/) to [lint](https://en.wikipedia.org/wiki/Lint_(software)) my Python code
- To set up:
   - Add ```"python.linting.enabled" : true``` to ```settings.json```
   - Add ```"python.linting.flake8Enabled" : true``` to ```settings.json```
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

---

## Git and GitHub
[Git](https://git-scm.com/) is a system for controling verisions and revisions of code. [GitHub](https://github.com/) is a site whete our code is hosted and organized. 
- [This](https://guides.github.com/activities/hello-world/) is an introduction to using a GitHub repository
- [Quick overview](https://rogerdudler.github.io/git-guide/) of git
- [Long tutorial](https://git-scm.com/docs/user-manual.html) on using git. Most important things are "Developing with Git" and "Sharing development with others" sections. 

---

## Other recommentations (Pedigo needs to finish this part)
- VS Code Python data science tools 
   - Running cells 
   - Formatting plots nicely
- Known bugs 
   - Terminal environment activation starting late
   - Backend jupyter notebook not restarting when running code cells
- Testing with Pytest
- Setting up Github

--- 

Other resources 
- [conda vs pip](https://www.anaconda.com/understanding-conda-and-pip/)
- [conda tutorial](https://towardsdatascience.com/a-guide-to-conda-environments-bc6180fc533)
