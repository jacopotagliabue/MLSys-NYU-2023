# Fundamentals 

This file contains introductory documentation to the [Command Line](#command-line-basics) and [Python and Rye](#python-and-rye). While I encourage you to work through each section on your own computer, you should also no limit yourself to only learning what is in this document. The command line is a powerful tool, and there are many commands, tricks, and skills to learn that will make you more productive. Do not be afraid to search online and learn beyond this file!

## Command Line Basics

Move to your "home" directory
```
cd ~
```

Create a `basics` directory
```
mkdir basics
```

Move into the `basics` directory
```
cd basics
```

Move "up" a directory back into the home directory

```
cd ..
```

From the home directory, create a `sub` directory within `basics`

```
mkdir basics/sub
```

Move into the `sub` directory

```
cd basics/sub
```

Move back into the home directory

```
cd ../..
```

Move into the `basics` directory and delete the `sub` directory

```
cd basics
rmdir sub
```

Create an empty file named `hello.txt`

```
# On Mac or Git Bash
touch hello.txt
# On Powershell
ni hello.txt
```

Rename `hello.txt` to `hello_world.txt`

```
mv hello.txt hello_world.txt
```

Copy `hello_world.txt` to a new file named `hello.txt`

```
cp hello_world.txt hello.txt
```

Delete `hello.txt` and `hello_world.txt`

```
rm hello.txt
rm hello_world.txt
```

## Python and Rye

Create a new [Rye](https://rye-up.com/) project

```
rye init my-project
```

Move into the newly created directory

```
cd my-project
```

Set the version of Python used in the project
```
rye pin 3.11
```

Open up a `python` shell

```
python
```

Open up Visual Studio Code and create a file named `hello.py`

```
code hello.py
```

Paste the following text into Visual Studio Code and save the file:

```python
print("hello world")
```

Run `hello.py` from the command line as a script

```
python hello.py
```

Add [ipython](https://ipython.org/) and [numpy](https://numpy.org/) to the list of dependencies for this project

```
rye add ipython numpy
```

Install all dependencies

```
rye sync
```

Note: without `Rye`, you would typically install a Python dependency with `pip`, like 

```
pip install numpy
```

If you ever see documentation online to use `pip` to install something, you should instead use `rye add`.

Open up an `ipython` shell (this is like the regular python shell but with more features). Note: when you install a _Python_ dependency like `ipython` that is started via its own special command, you must run that command with `rye run`. 

```
rye run ipython
```

Exit out of `ipython`

```
exit
```
