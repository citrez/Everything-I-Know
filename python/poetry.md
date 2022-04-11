# Poetry  

Poetry is a dependancy management tool. In short, within any project there are a host of other external packages that the project relies on. e.g, we might need pandas 1.3.5 which relies on numpy 1.21.1, but scipy 1.6.1 also relies on numpy but needs numpy to be less than 1.0.0, we therefor need to use pandas 1.2.9 which is also compatible with an earlier version of scipu/ Sorting out this headache is the job of a package managment tool. It gives you the most recent version of the packages you need that satisfy your constraints.  

[Realpython - dependency management with poetry](https://realpython.com/dependency-management-python-poetry/) gives a good explaination and  has a useful command reference section.

### Poetry commands

`poetry` - show a list of available commands.

```poetry new new-package```  - Create a poetry directory structure, with the pyproject.toml file etc. 
my-package

`poetry init` - poetry-ify a directory

```poetry add pandas 1.30```  - adds a dependancy to your project. You can use [dependancy specification](https://python-poetry.org/docs/dependency-specification/) to be more specific. Use ```--dev``` to add dev dependancies. This command adds it to the toml file but also installs it in your env. 

`poetry install` - If you have a poetry.lock, this command will just install the exact versions of all relevant packages from there. If no poetry.lock file exists, this takes the dependacies you need from your pyproject file, resolves them (meaning if finds all the latest versions of the packages you need that dont conflict) and then installs them to your virtualenv and creates a virtualenv. If you dont want to development dependacies add `--no-dev`. Also, poetry installs the actual project itself into your environment. `--no-root` disables installing the actual package itself.

`poetry update` - Gives you the **latest** versions of all your dependacies, subject to all of thier constraints. This command, not only updates the dependacy versions, but it writes them to the lock file. You can update particular packages. `poetry update pandas numpy`

On an existing project with a pyproject.toml file and poetry install creates a virtualenv for you and installs all the dependancies

`poetry run` - run a command from poetrys virtualenv. Presumably, the equivalent can be done by activating the virtualenv

Article on why everyone should use [poetry](https://hackersandslackers.com/python-poetry-package-manager/)

`poetry version` - this shows the current version of your poetry project. If you type `poetry version minor`, it bumps up the version.

[poetry commands](https://python-poetry.org/docs/cli/#show) 

### Dependancy specification 

**^ Caret requirement**  
This updates the package as long as it doesnt modify the left-most digit in the 1.3.2 (major.minor.patch) grouping. So a ^0.1.6 specification could update to 0.1.23 but not 0.2.1

|REQUIREMENT|	VERSIONS ALLOWED|
|----|---|
|^1.2.3|	>=1.2.3 <2.0.0|
|^1.2	|>=1.2.0 <2.0.0|
|^1	|>=1.0.0 <2.0.0|
|^0.2.3	|>=0.2.3 <0.3.0|
|^0.0.3	|>=0.0.3 <0.0.4|
|^0.0	|>=0.0.0 <0.1.0|
|^0	|>=0.0.0 <1.0.0|

**Tilde requirements**  
A bit similar to carat. If you speficy 2.1.1, or 2.1 only patch updates are allow. If you specify `pandas ~1` then minor updates are allowed too. 

**Wildcard requirements**  
These allow the latest updates where the wildcard is positioned. 
|REQUIREMENT |	VERSIONS ALLOWED|
|------------|------------------|
|*|	>=0.0.0|
|1.*|	>=1.0.0 <2.0.0|
|1.2.*|	>=1.2.0 <1.3.0|

These seem the most understandable to use. 

**Inequality requirements**
```
>= 1.2.0
> 1
< 2
!= 1.2.3
```

**Exact requirements**
You can specify the exact version of a package. This will tell Poetry to install this version and this version only. If other dependencies require a different version, the solver will ultimately fail and abort any install or update procedures.

**Multiple requirements**
Multiple version requirements can also be separated with a comma, e.g. `>= 1.2, < 1.5`.

Links  
[Youtube video on poetry](https://www.youtube.com/watch?v=G-OAVLBFxbw&ab_channel=PyBites)