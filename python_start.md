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
   - ```$ conda create -n myenv python=3.7 scipy=0.15.0```
- See the linked tutorial above for more details

Install [VS Code](https://code.visualstudio.com/docs/setup/setup-overview)
- This is what I recommend for your IDE

Install [VS Code Python Extension](https://code.visualstudio.com/docs/python/python-tutorial)
- Follow the instructions above
- When you get to "Select a Python interpreter" use the name of the virtual environment that you created earlier
   - More details on selecting an environment [here](https://code.visualstudio.com/docs/python/environments)
- Follow the rest of the instructions to go through creating and running a new Python file

Other recommentations (Pedigo needs to finish this part)
- VS Code Python data science tools 
   - Running cells 
   - Formatting plots nicely
- Known bugs 
   - Terminal environment activation starting late
   - Backend jupyter notebook not restarting when running code cells
- Testing with Pytest
- Formatting code with Black
- Linting with Flake8
- Refactoring with Rope
- Setting up Github
