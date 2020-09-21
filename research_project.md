# How to run a successful Machine Learning / Data Science project

## Important
The most important point is reproducibility. Someone not familiar with the project should be able to get from the raw dataset (which is downloaded automatically) to the trained model without to much intermediate steps. The raw data is considered immutable!

To speed up, intermediate results can be cached and stored somewhere

- use the templated project structure
- jupyter notebooks are not meant for containing large amounts of code -> use python source files instead and import into notebooks
- notebooks are not ideal to work with multiple people


## Tools

- use git and a hosting platform like Gitlab or Github
- use conda to manage your python environment:
    - each project should have its own environment
    - have an environment.yml ready to create the environment
- autoformat your code using `black`

## Results
- experimental results of models should be run with sacred and stored on the server
- figures can be saved in the experiment folder
