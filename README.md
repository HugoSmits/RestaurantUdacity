# My Restaurant tutorial

## Description

#### The task is understand the rudimentary built up of a web service in python and then to showcase the usage of a web framework , for instance FLASK. Outside library used to communicate with the database and to set it up is sqlalchemy.

#### Webserver.py shows the rudimentary built.
#### project.py shows the framework FLASK in junction with sqlAlchemy.

## Index
1. [Bio and File info](#bio-and-file-info)
2. [Version](#version)
3. [Keywords](#keywords)
4. [Setting up for this project](#setting-up-for-this-project)
5. [Aditional setup for this project](#aditional-setup-for-this-project)
6. [Usage](#usage)
7. [Populate the database](#populate-the-database)
8. [Solutions to "common" problems](#solutions-to-"common"-problems)
9. [Contribuition](#contribuition)
10. [Licensing info](#licensing-info)
11. [WebBio](#webbio)

## Bio and File info

- ##### Author: Hugo Smits
- ##### Date of creation : 25/11/2018
- ##### Last modified : 25/11/2018

## Version

##### Current version of the repository is version 1.0 .

## Keywords
- ##### sqlAlchemy (Open Source orm)
- ##### ORM(Object-Relational Mapping)

## Setting up for this project
##### To do the exercises in this project, you will need access to a Linux machine you can log into with SSH. One option is to install a Linux-based virtual machine on your own computer.

### Your Linux machine (Local VM option)
##### If you prefer to work on your own computer instead of a commercial service, you can run a Linux virtual machine (VM) on top of your regular operating system.

### You will need to install two pieces of software:

- ##### VirtualBox, which you can get from this [download page](https://www.virtualbox.org/wiki/Downloads).
- ##### Vagrant, which you can get from this [download page](https://www.vagrantup.com/downloads.html).

##### You will also need a Unix-style terminal program. On Mac or Linux systems, you can use the built-in Terminal. On Windows, I recommend Git Bash, which is installed with the Git version control software.

- ##### Git, which you can get from this [download page](git-scm.com).

##### Once you have VirtualBox and Vagrant installed, open a terminal and run the following commands:
```
mkdir networking
cd fullstack/vagrant
vagrant init ubuntu/trusty64
vagrant up
```
##### This will create a new directory for this project and begin downloading a Linux image into this directory. It may take a long time to download, depending on your Internet connection.

##### When it is complete, you can log into the Linux instance with ```vagrant ssh```. You are now ready to continue with the project.

#####To turn the virtual machine off (without deleting anything), type ```vagrant halt```.

##### If you log out of the Linux instance or close the terminal, the next time you want to use it you only need to run ```cd networking``` and ```vagrant ssh```.

## Download the data

##### Next, download the data [here](https://github.com/HugoSmits/RestaurantUdacity). You can fork the repository and clone it to your local git repository. The files needed are called database_setup.py and lotsofmenus.py . The rest are personal answers to the project. Put these files into the vagrant directory, which is shared with your virtual machine.

##### Within the repository you can find the file called Vagrantfile which will help you set up your vagrant environment with the right configurations. BEWARE: config.vm.box_download_insecure is set to TRUE. Doesn't verify ssl certificates. Line can be removed or altered at said file. Setup can't be guaranteed if done so.

## Aditional setup for this project

##### Installements to run in the command line.
```
pip install autopep8 --user
```

```
pip install reindent --user
```

## Usage

##### The following source code is written according to [PEP8 guidelines](https://www.python.org/dev/peps/pep-0008/).
```
autopep8 --in-place -a --max-line-length 79 project.py
```

##### Reindent is used to eliminate any tabs and spaces mix ups. 
##### Caution: Flag or option n will modify the file.
```
reindent -n project.py
```

## Setup the database
```
python database_setup.py
```
##### Which gives an output file with the name: 
- ##### restaurantmenu.db

## Populate the database
```
python lotsofmenus.py
```

## Solutions to "common" problems
##### Add the following argument to the create_engine in sqlAlchemy to solve multiple threads issues
eliminate commas as seen fit.

```
,connect_args={'check_same_thread':False},
```

## Contribuition

##### To contribuite to this project the person must follow the guidelines mentioned in **Usage** and send a written email to the moderator of the source code hugo.smits1995@gmail.com 

## Licensing info

##### The following project uses the [MIT license](https://opensource.org/licenses/MIT)

## WebBio
- ##### http://simeonfranklin.com/blog/2012/jul/1/python-decorators-in-12-steps/
- ##### http://www.blog.pythonlibrary.org/2017/12/14/flask-101-adding-editing-and-displaying-data/
- ##### http://flask.pocoo.org/docs/0.12/quickstart/
- ##### http://flask.pocoo.org/docs/1.0/patterns/flashing/
- ##### https://docs.sqlalchemy.org/en/latest/core/engines.html
- ##### https://docs.sqlalchemy.org/en/latest/core/engines.html#custom-dbapi-args
- ##### https://stackoverflow.com/questions/11233128/how-to-clean-the-database-dropping-all-records-using-sqlalchemy
- ##### https://docs.sqlalchemy.org/en/rel_0_9/orm/query.html