---
title: Data Science workflow recommendation
toc: true
comments: true
layout: post
image: images/explore-refactor_loop.png
description: A workflow recommended for data science.
categories: [tutorial]
---
Repository of this workflow is stored [here](https://github.com/phucnsp/production_data_science_template)   

# Production data science template

The template of this repository follows [production-data-science workflow](https://github.com/Satalia/production-data-science/tree/master/tutorial/a-setup), 
 which focuses on productionizing data scientist's work, make the analysis or research to be reusable, applicable to
production.  
The workflow is separated into 2 phases: 
- `exploration phase` is where data scientist explores the project, mainly work with jupyter notebook. All the work in
this phase will be stored in `exploration` folder.
- `production phase` is where data scientists' works are refactored into packages so it can be reuse, imported. All the 
work in this phase will be stored in `your_package` folder.

## How to setup a new repository - for maintainer

```bash
git clone https://gitlab.com/Phuc_Su/production_data_science_template.git
git clone <your_project_repository>
cd <your_project_name>
git checkout -b product-initial-setup
# open Finder, copy all content of production_data_science_template into your project repository, except .git and .idea folder 
conda create --name <environment_name> python=3.6
source activate <environment_name>
pip install git-lfs
# in case you want to add some large file extension other than .jpg, .pdf, .csv, .xlsx
git lfs track <add large file path>
# rename <your package> folder and modify setup.py, most importance is require_packages. See example below
# write something about your project in README.md
pip install -e .
pip freeze | grep -v <package_name> > requirements.txt
git add .
git commit -m "First commit"
git push -u origin HEAD
```

Example of `setup.py`

```python
setup(
    name='your_project',
    version='v0.1',
    description='',
    long_description=readme(),
    classifiers=[
        'Programming Language :: Python :: 3',
    ],
    url='https://github.com/phucnsp/production_data_science_template',
    author='Phuc_Su',
    author_email='',
    license='',
    packages=['your_package'],
    install_requires=[
        'pypandoc>=1.4',
        'watermark>=1.5.0',
        'pandas>=0.20.3',
        'scikit-learn>=0.19.0',
        'scipy>=0.19.1',
        'matplotlib>=2.1.0',
        'pytest>=3.2.3',
        'pytest-runner>=2.12.1',
        'click>=6.7'
    ],
    setup_requires=['pytest-runner'],
    tests_require=['pytest'],
)
```


and you are ready~! 🎉

Note: if you want to setup notification on slack for merge request from gitlab, reference
 [here](https://docs.gitlab.com/ee/user/project/integrations/slack.html) 
 
## How to contribute - for developers
#### Setup first time  
    ```bash
    conda create --name <environment_name> python=3.6
    source activate <environment_name>
    git clone  <repository url>
    cd to/the/project/directory
    pip install -r requirements.txt
    pip install -e .
    ```

> For a private repository accessible only through an SSH authentication, substitute `https://github.com/` with `git@github.com:`.

#### Returning to work  

- Some rules: 
    - `1 branch/1 exploration/1 folder`
    - branch-name convention: `explore-* for exploration, refactor-* for refactor`
    
```bash
git checkout master
git pull --all 
# if you continue to work on old branch
git checkout <branch>
# if you want to start a new exploration
git checkout -b <new_branch>
# if your branch is far behind master and you want to merge 
git merge master
#####################
    Start working
#####################
git add <path_to_work_files/folder>
git commit -m "some message"
git push -u origin HEAD
```

## Notes

- `requirements.txt` helps to setup your virtual environment, to make sure all contributors working on the same environments.  
So whenever you have a new libraries need to install, after installing you need to add it into `requirements.txt` by  `pip freeze | grep -v <package_name> > requirements.txt`
- `setup.py` allows you to create packages that you can redistribute. This script is meant to install your package on the end user's system, not to prepare the development environment.
    - `packages` - in-house development packages.
    - `install_requires` - packages that our development packages dependence on.
    - `py_modules=['new_module']` - in-house development modules need to install (placed in root directory)
- `pip install -e . ` - to install packages/modules from `setup.py`, in the editable mode.
- If you want to add large file into working repository:
    ```bash
    pip install git-lfs
    git lfs install
    # Tell LFS to track files with given path
        git lfs track "path_to_large_file"
    # Tell LFS to track files with format "*.jpg"
        git lfs track "*.jpg"
    # Tell LFS to track content of the whole directory
        git lfs track "data/*"
    ```

## How to use the package - for users

Install the library
```bash
conda create --name <environment_name> python=3.6
source activate <environment_name>
pip install -e 'git+https://github.com/phucnsp/production_data_science_template.git'
```
> For a private repository accessible only through an SSH authentication, substitute `git+https://github.com` with `git+ssh://git@github.com`.  
Note that `-e` argument above to make the installation editable.
        
        
## Leisure read
- [Production Data Science tutorial](https://github.com/Satalia/production-data-science)
- [Writing a setup script](https://docs.python.org/3/distutils/setupscript.html)
- [Minimum structure](https://python-packaging.readthedocs.io/en/latest/minimal.html)
- [gitlab slack notification service](https://docs.gitlab.com/ee/user/project/integrations/slack.html)
- [git strategy](https://gitlab.com/Phuc_Su/production_data_science_template/blob/master/GIT_STRATEGY.md)
        
        
        
        
        
        
        
        
        
        