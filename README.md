# Tuto module usage

## What is a module ?

A module is something that allows you to bundle some python scripts

## How to create a module ?

To create a module, one have to make a directory and add a `__init__.py`

## How to handle paths ?

If one launches an ipython console and try to import the module he would
have the following message :
``ModuleNotFoundError: No module named 'module_one'``

This is because the path of the directory that contains the
module is not known by python
``ModuleNotFoundError: No module named 'module_one'``

To update the paths list one need to use the following lines in the
ipython console :
```python
import sys

sys.path.append('##PATH##')
```

## Best practice to declare classes

The best practice to declare Fooa in module\_one is to add
the following line in the `__init__.py` file :

```python
from .Fooa import Fooa
```

This line allow you to import Fooa the following way `from module_one import Fooa` instead
of this way `from module_one.Fooa import Fooa`.
