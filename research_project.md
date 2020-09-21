# How to run a successful Machine Learning / Data Science project

A fundamental aspect of a project is its reproducibility. A person not familiar with the project should be able to get from the raw dataset to the trained model without any manual intermediate steps. Intermediate results can and should be cached. Those files as well as the immutable raw data are **not** part of version control.

## Guidelines
- use a [templated](https://github.com/j-petit/cookiecutter-data-science) project structure with [cookiecutter](https://cookiecutter.readthedocs.io/en/latest/installation.html) to get started
    - the structure makes it easy and for everyone to navigate around the project
    - see [here for additional explanations](https://drivendata.github.io/cookiecutter-data-science/#contributing)
- jupyter notebooks are not meant for containing large amounts of code: instead use python source files and import modules into notebooks
    - notebooks are not ideal to work with multiple people

## Tools
- use git and a hosting platform like Gitlab or Github
- use conda to manage your python environment
    - each project should have its own environment
    - have an `environment.yml` ready to create the environment
- autoformat your code using [black](https://black.readthedocs.io/en/latest/)

## Results
- save important figures as images in the appropriate folder, a notebook can be exported as html with embedded images
- experiment results should be run with [sacred](https://sacred.readthedocs.io/en/stable/) and the results stored in the MongoDB of the server
    - add files created in the run of the experiment as artefacts
