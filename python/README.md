# Python

## Links

[Using black in vscode](https://dev.to/adamlombard/how-to-use-the-black-python-code-formatter-in-vscode-3lo0)

* [PEP-8 Style guide for python](https://www.python.org/dev/peps/pep-0008/#a-foolish-consistency-is-the-hobgoblin-of-little-minds) is the definative style guide in python and should be used like the bible. 

* [Advanced Python](https://www.pythontutorial.net/advanced-python/)
    * [Closure](https://www.pythontutorial.net/advanced-python/python-closures/) These are a nested functions that references one or more variables from its enclosing scope. - In python you can define a function within a functon (a nested function) and use a variable that is definied in the outer function.
    * [Decorators](https://www.pythontutorial.net/advanced-python/python-decorators/) are functions that return functions that have been been modified with new functionality. 

* [Object Oriented Programming](https://www.pythontutorial.net/python-oop/)
Everything in python is an object. An object has a state/data (attributes) and behaviors (methods). To create an object you need to define the class it belongs to and from there you can create/instantiate 1 or more objects. The objects are an instance of the class.

* [Learn X in Y minutes](https://learnxinyminutes.com/docs/python/) - this site can be used for learning other languages too!

* [Creating modules in Python](https://docs.python.org/3/tutorial/modules.html)

* [Book for creating packages in Python](https://py-pkgs.org/01-introduction)

* [Decorators](https://www.youtube.com/watch?v=tfCz563ebsU\&ab\_channel=TechWithTim)

* [zip](https://careerkarma.com/blog/python-zip/)

* [unpacking](https://stackabuse.com/unpacking-in-python-beyond-parallel-assignment/)

* [Excpetion Hierarchy](https://docs.python.org/2/library/exceptions.html#exception-hierarchy)

## Abstract base classes ABC
I see these as like the blue print of classes. They set out methods that are needed in classes so that there is some type of consistency between classes that share similar structure. Classes inherit from the abstract base cless. The instances of a class that inherits from abstract base classes must contain all the methods defined in the abstract base class. 

## Python Packages
> NOTE: Can think about turning these bullets into subpages if the bullets become too large.

* [**BeautfulSoup**](https://www.crummy.com/software/BeautifulSoup/bs4/doc/) is a package for parsing html doucments. Extracting from them the bits you want. 
[Beautfulsoup walkthrough](https://www.digitalocean.com/community/tutorials/how-to-work-with-web-data-using-requests-and-beautiful-soup-with-python-3)

* **Pandas** implements the pandas dataframe, a staple in any data anaylitics in python.
  * [Method chaining](https://towardsdatascience.com/the-unreasonable-effectiveness-of-method-chaining-in-pandas-15c2109e3c69) can be used in python much like the pipe in R.
  * [Link](https://towardsdatascience.com/how-to-show-all-columns-rows-of-a-pandas-dataframe-c49d4507fcf). Show more rows and columns when displaying a dataframe in a notebook. 

* Flask
[Flask Tutorial](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)


* Selenium
[Waiting](https://selenium-python.readthedocs.io/waits.html)

## pyenv
Use pyenvs for using different python versions both globally and locally in directories/projects. What if you are working on a project that supports lots of versions of python, and you want to test out how it will work with a different version. pyenv lets you quickly and easily switch between different instances of python. 

Why use pyenv?
It is a great tool for managing many versions of python, meaning you can easily try out new language features. 

Why not use 'system python'?
'System python' is just the python that comes installed on your operating system. If you use mac or linux, by default when you type python in your terminal you get a nice pyhon [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop). After all, this python belongs to the operating system, and when you run `which python` that is what is used. But this python version is 2.7.12 (just run `python -V`)

Probelms of installing multiple version of the same package to your system python tend to bite you when you least excpect it. You may find you have installed the wrong version of a dependancy of another pacakge and its causing lots of errors. 

So we want 4 things from pyenv:
1. Install Python in your user space
2. Install multiple versions of Python
3. Specify the exact Python version you want
4. Switch between the installed versions

### Using pyenv to install python

`pyenv install --list | grep " 3\.[678]"` This shows all the Python versions that pyenv knows about that match the regular expression.

Once you find the version you want, you can install it with the command `pyenv install -v 3.7.1`

pyenv works by building Python from source. Each version that you have installed is located nicely in your pyenv root directory
`ls ~/.pyenv/versions/` will show you all the version, and deleting one is as easy as 
`rm -rf ~/.pyenv/versions/2.7.15`
Of course pyenv also provides a command to uninstall a particular Python version `pyenv uninstall 2.7.15`

Lets checks the versions of python we have available with ```pyenv versions```. The * indicates which python version is currently active.

`python -V` shows you the version of python youre using.

If you try to confirm using `which python` you get /home/realpython/.pyenv/shims/python, which isnt helpful.

This might be surprising, but this is how pyenv works. pyenv inserts itself into your PATH and from your OS’s perspective is the executable that is getting called. If you want to see the actual path, you can run the following
`pyenv which python`

If you wanted to switch to using 2.7.15, it is as simple as running the global command
`pyenv global 2.7.15`
then use 
`pyenv versions` to check it has been changed. 
`pyenv global system` will take you back to your system default


[understanding shims](https://github.com/pyenv/pyenv#understanding-shims). Shims are just appending pyenvs desired python or pip to the begining of your $PATH enviroment variable, so that it redicts you to where it wants. 



[virtualenv in jupyter ](https://janakiev.com/blog/jupyter-virtual-envs/)

```
pip install --user ipykernel

python -m ipykernel install --user --name=myenv
 ```

 * RISE
 Turn your jupyter notebook into presentations, with a button. 

 * Panel
 Like shiny for jupyter, make your notebooks interactive.

* hvplot
Interactive plots

* [Papermill](https://papermill.readthedocs.io/en/latest/)
Papermill is a tool for parameterizing and executing Jupyter Notebooks.

## Dataclasses

Data class are really what they say on the tin. If you want to build a class that is mainly used to store data, dataclass is the way to go - since they reduce the boilerplate code you need to get things up and running. See [ariancodes](https://www.youtube.com/watch?v=vRVVyl9uaZc) explaination.

Classes are a combination of behavior, in the form of methods and data in the form of attributes. They are the blueprint for objects and form the basis of object orientated programming. They can be used in amillion way. Some are containers for behavior, think of a class for drawing things on screen. Others aere more a container for data, think of a vehcle registration class. (question, why wouldnt uou use a database for the storing of the data?)

Inheritence may be used a lot when uou are mainlu changing behavior and there will also likely not be that many instances of the class. A class that contains data instances mau behave very differently, you will likely want to order, compare and inspect them very easily.

Some languages have a more data oriented version of a class, for example c sharp has a 'structype'. As of version 3.7 python has a dataclasses module. It can allow you to initialiser quicker. 

see [9 good reasons to use dataclasses](https://towardsdatascience.com/9-reasons-why-you-should-start-using-python-dataclasses-98271adadc66)

[dataclasses](https://realpython.com/python-data-classes/#alternatives-to-data-classes)

## pydantic

Pydantic can be seen as an extension to the built in dataclass module. 
Usually in python you need to give type hints and then instantialise the object, with pydantic the type hints are sufficient.
Adding validator decorators is where pydantic really shines.
[8 reasons to start using pydantic](https://towardsdatascience.com/8-reasons-to-start-using-pydantic-to-improve-data-parsing-and-validation-4f437eae7678)



## pytest
pytest is a framework to help you write small tests for your python code. pytest is a package for python that can be installed using pip. But gives you access to a cmd line executable 'pytest' which basically does the same thing. You can group many tests in a class to help organise yourself.

```pytest test_example.py``` will run all tests in that file. Testing functions (or methods) need to start with an underscore test, i.e test_this_is_test().

test a directory using
`tests/model/`

pytest test a file using 
```pytest tests/model/test_expenses.py```

test a particular function using
```pytest -k "test_apply_adjustment"```

More generally, check out the pytest [conventions for test discovery](https://docs.pytest.org/en/6.2.x/goodpractices.html#test-discovery)

Use [fixtures](https://docs.pytest.org/en/6.2.x/fixture.html#fixtures) if you need to prepare data for a test.

## Notes

A **module** is a bunch of related code saved in a file with the extension .py. Python modules help you focus on one small portion of a task rather than an entire problem. . With Python modules, you can define separate namespaces to avoid collisions between identifiers in different parts of your application.

**Packages** are a directory of a collection of modules. Packages allow the hierarchical structure of the module namespace. Just like we organize our files on a hard drive into folders and sub-folders, we can organize our modules into packages and subpackages.

A **library** is an umbrella term referring to a reusable chunk of code. Usually, a Python library contains a collection of related modules and packages. Actually, this term is often used interchangeably with “Python package” because packages can also contain modules and other packages (subpackages). However, it is often assumed that while a package is a collection of modules, a library is a collection of packages.

[info from here](https://learnpython.com/blog/python-modules-packages-libraries-frameworks/)

When a python module is imported, everything in it is run. Thats why the 
```
if __name__ == __main__:
    do_something()

```
paradigm works. This is also why we can import things at the begining of modules. 

## Creating Packages

distutils is the inbuilt package that helps you build packages but it has really been superceded by setuptoolsl. The distutils package may be destined for depreciation. 

There are a few standard files and folders that it is stndard to have in a pachage at setup. There are cookie cutter blue prints for making packages but it is informative to DIY at least once.

CHANGES.txt: log of changes with each release
LICENSE.txt: text of the license you choose (do choose one!)
MANIFEST.in: description of what non-code files to include
README.txt: description of the package – should be written in ReST or Markdown (for PyPi):
setup.py: the script for building/installing package.
bin/: This is where you put top-level scripts( some folks use scripts )
docs/: the documentation
package_name/: The main package – this is where the code goes.
test/: your unit tests. 

The setup.py file is what describes your pachage and tells setuptools how to package, build and install it.

[overview of making a package](https://betterscientificsoftware.github.io/python-for-hpc/tutorials/python-pypi-packaging/)

[official python paclaging user guide](https://packaging.python.org/en/latest/)

[makin a minimal package](https://python-packaging.readthedocs.io/en/latest/minimal.html)

[Exercise to create a small example package](https://python-packaging-tutorial.readthedocs.io/en/latest/setup_py.html#exercise-a-small-example-package)

[how to package a python](https://py-pkgs.org/03-how-to-package-a-python)

