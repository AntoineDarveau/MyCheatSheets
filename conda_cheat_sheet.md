## Add environment variables to a specific conda environment
```shell
conda activate test-env  # Need to activate your environment first
conda env config vars list  # To list any variables you may have
conda env config vars set MY_VAR=value  # To set environment variables
conda deactivate  # you have to reactivate your environment
conda activate test-env  # reactivate
