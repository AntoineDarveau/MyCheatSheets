## Add environment variables to a specific conda environment
Taken from https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html
```shell
conda activate test-env  # Need to activate your environment first
conda env config vars list  # To list any variables you may have
conda env config vars set MY_VAR=value  # To set environment variables
conda deactivate  # you have to reactivate your environment
conda activate test-env  # reactivate 
```
## Stop conda to look into packages outside of the environement
This is useful to stop conda from looking into `.local/`, where packages are installed when using `pip install --user`. To do so, simply set the variable `PYTHONNOUSERSITE = False` by following the previous example. It would look like:
```shell
conda activate test-env  # Need to activate your environment first
conda env config vars set PYTHONNOUSERSITE=False # To set environment variables
conda deactivate  # you have to reactivate your environment
conda activate test-env  # reactivate 
```

## add path to your environment
Usefull when developing new codes. Access annywhere on your computer.
```shell
conda develop path/to/the/code
```
Some versions of miniconda do not have the `develop` command, so manually add the path in the file
`<path-to-miniconda>/envs/<your_env>/lib/pythonX.X/site-packages/conda.pth`. Create it if it does not exist.
