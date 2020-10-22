## Temp repo to reproduce [jupyterlab/jupyterlab#9203](https://github.com/jupyterlab/jupyterlab/issues/9203)

Steps to reproduce:

- Check out this repo

    `git clone https://github.com/ajbozarth/libexpl.git`
    
    `cd libexpl`

- Install Jupyterlab 3.0
    
    `pip install --pre jupyterlab`

- Install lib package

    `cd mylibrary`
    
    `jlpm`
    
    `jlpm build`
    
    `jupyter labextension link --no-build .`

- Install extension

    `cd ../myextension`
    
    `jlpm`
    
    `jlpm build`
    
    `jupyter labextension install .`

- Note the error on the final step

If you install jupyterlab 2.x and update the package.json files to use 2.X in the dependacies and follow these steps there is no error
