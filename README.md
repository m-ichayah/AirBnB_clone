# 0x00. AirBnB clone - The console

## 0x00.Table of contents

* [0x01 Introduction](#0x01-Introduction)
* [0x02 Environment](#0x02-Environment)
* [0x03 Installation](#0x03-Installation)
* [0x04 Testing](#0x04-Testing)
* [0x05 Usage](#0x05-Usage)
* [0x06 Authors](#0x06-Authors)

## 0x01 Introduction

Team project to build a clone of [AirBnB](https://www.airbnb.com/).

The console is a command interpreter to manage objects abstraction between objects and how they are stored.

To see the fundamental background of the project visit the [Wiki](https://github.com/ralexrivero/AirBnB_clone/wiki).

The console will perform the following tasks:

* create a new object
* retrive an object from a file
* do operations on objects
* destroy an object

### Storage

All the classes are handled by the `Storage` engine in the `FileStorage` Class.

## 0x02 Environment

<!-- ubuntu -->
<a href="https://ubuntu.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Ubuntu&color=E95420&logo=Ubuntu&logoColor=E95420&labelColor=2F333A" alt="Suite CRM"></a> <!-- bash --> <a href="https://www.gnu.org/software/bash/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=GNU%20Bash&color=4EAA25&logo=GNU%20Bash&logoColor=4EAA25&labelColor=2F333A" alt="terminal"></a> <!-- python--> <a href="https://www.python.org" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Python&color=FFD43B&logo=python&logoColor=3776AB&labelColor=2F333A" alt="python"></a> </a> <!-- vim --> <a href="https://www.vim.org/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Vim&color=019733&logo=Vim&logoColor=019733&labelColor=2F333A" alt="Suite CRM"></a> <!-- vs code --> <a href="https://code.visualstudio.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Visual%20Studio%20Code&color=5C2D91&logo=Visual%20Studio%20Code&logoColor=5C2D91&labelColor=2F333A" alt="Suite CRM"></a> </a><!-- git --> <a href="https://git-scm.com/" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=Git&color=F05032&logo=Git&logoColor=F05032&labelColor=2F333A" alt="git distributed version control system"></a> <!-- github --> <a href="https://github.com" target="_blank"> <img height="" src="https://img.shields.io/static/v1?label=&message=GitHub&color=181717&logo=GitHub&logoColor=f2f2f2&labelColor=2F333A" alt="Github"></a>
 <!-- Style guidelines -->
* Style guidelines:
  * [pycodestyle (version 2.7.*)](https://pypi.org/project/pycodestyle/)
  * [PEP8](https://pep8.org/)

All the development and testing was runned over an operating system Ubuntu 20.04 LTS using programming language Python 3.8.3. The editors used were VIM 8.1.2269, VSCode 1.6.1 and Atom 1.58.0 . Control version using Git 2.25.1.

## 0x03 Installation

```bash
git clone https://github.com/m-ichayah/AirBnB_clone.git
```

change to the `AirBnb` directory and run the command:

```bash
 ./console.py
```

### Execution

In interactive mode

```bash
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```

in Non-interactive mode

```bash
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

## 0x04 Testing

All the test are defined in the `tests` folder.

### Documentation

* Modules:

```python
python3 -c 'print(__import__("my_module").__doc__)'
```

* Classes:

```python
python3 -c 'print(__import__("my_module").MyClass.__doc__)'
```

* Functions (inside and outside a class):

```python
python3 -c 'print(__import__("my_module").my_function.__doc__)'
```

and

```python
python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'
```

### Python Unit Tests

* unittest module
* File extension ``` .py ```
* Files and folders star with ```test_```
* Organization:for ```models/base.py```, unit tests in: ```tests/test_models/test_base.py```
* Execution command: ```python3 -m unittest discover tests```
* or: ```python3 -m unittest tests/test_models/test_base.py```

### run test in interactive mode

```bash
echo "python3 -m unittest discover tests" | bash
```

### run test in non-interactive mode

To run the tests in non-interactive mode, and discover all the test, you can use the command:

```bash
python3 -m unittest discover tests
```


## 0x05 Usage

* Start the console in interactive mode:

```bash
$ ./console.py
(hbnb)
```

* Use help to see the available commands:

```bash
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb)
```

* Quit the console:

```bash
(hbnb) quit
$
```

### Commands

> The commands are displayed in the following format *Command / usage / example with output*

* Create

> *Creates a new instance of a given class. The class' ID is printed and the instance is saved to the file file.json.*

```bash
create <class>

```

```bash
(hbnb) create BaseModel
4e4728fe-02b6-4302-9c8b-a34f2e042769
(hbnb)
```

* Show

```bash
show <class> <id>
```

```bash
(hbnb) show BaseModel 4e4728fe-02b6-4302-9c8b-a34f2e042769
[BaseModel] (4e4728fe-02b6-4302-9c8b-a34f2e042769) {'id': '4e4728fe-02b6-4302-9c8b-a34f2e042769', 'created_at': datetime.datetime(2023, 2, 15, 0, 29, 26, 145326), 'updated_at': datetime.datetime(2023, 2, 15, 0, 29, 26, 145326)}
(hbnb)
```

* Destroy

> *Deletes an instance of a given class with a given ID.*
> *Update the file.json*

```bash
(hbnb) create User
57971426-3f2f-4f47-8496-c1e6cce29889
(hbnb) destroy User 57971426-3f2f-4f47-8496-c1e6cce29889
(hbnb) show User 57971426-3f2f-4f47-8496-c1e6cce29889
** no instance found **
(hbnb)
```

* all

> *Prints all string representation of all instances of a given class.*
> *If no class is passed, all classes are printed.*

```bash
(hbnb) create BaseModel
1a0f4eca-08e1-49f6-862f-90352bacb5cd
(hbnb) all BaseModel
["[BaseModel] (4e4728fe-02b6-4302-9c8b-a34f2e042769) {'id': '4e4728fe-02b6-4302-9c8b-a34f2e042769', 'created_at': datetime.datetime(2023, 2, 15, 0, 29, 26, 145326), 'updated_at': datetime.datetime(2023, 2, 15, 0, 29, 26, 145326)}", "[BaseModel] (1a0f4eca-08e1-49f6-862f-90352bacb5cd) {'id': '1a0f4eca-08e1-49f6-862f-90352bacb5cd', 'created_at': datetime.datetime(2023, 2, 15, 0, 31, 49, 890652), 'updated_at': datetime.datetime(2023, 2, 15, 0, 31, 49, 890652)}"]
(hbnb)
```

* count

> *Prints the number of instances of a given class.*

```bash
(hbnb) create City
189ce90b-6e3a-438d-81e4-52a5d4cb1074
(hbnb) create City
f59e7e7b-e117-49a2-83b8-1a65fd4e2bae
(hbnb) count City
2
(hbnb)
```

* update

> *Updates an instance based on the class name, id, and kwargs passed.*
> *Update the file.json*

```bash
(hbnb) create User
f5178144-6e27-4525-a3d2-2381f4eb51af
(hbnb) update User f5178144-6e27-4525-a3d2-2381f4eb51af email "ini.michayah@gmail.com"
(hbnb) show User f5178144-6e27-4525-a3d2-2381f4eb51af
[User] (f5178144-6e27-4525-a3d2-2381f4eb51af) {'id': 'f5178144-6e27-4525-a3d2-2381f4eb51af', 'created_at': datetime.datetime(2023, 2, 15, 0, 33, 24, 86694), 'updated_at': datetime.datetime(2023, 2, 15, 0, 33, 24, 86694), 'email': 'ini.michayah@gmail.com'}
(hbnb)

```
## Authors
<details>
    <summary>Iniovosa Michayah O</summary>
    <ul>
    <li><a href="https://www.github.com/m-ichayah">Github</a></li>
    <li><a href="mailto:ini.michayah@gmail.com">e-mail</a></li>
    </ul>
</details>
<details>
    <summary>Favour Okorie</summary>
    <ul>
    <li><a href="https://www.github.com/Memeik">Github</a></li>
    <li><a href="mailto:okorieonyedikachi9@gmail.com">e-mail</a></li>
    </ul>
</details>
