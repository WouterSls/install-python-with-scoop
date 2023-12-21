# Python scoop installation
In order to run python scripts you will need python on your pc.
We can install python using scoop package manager

**Table of content:**
- [Installing scoop](#item-one)
- [Installing python](#item-two)
- [Running the script](#item-three)

<a id="item-one"></a>
### Installing scoop package manager 

scoop is a microsoft package manager which can easly be used to install all kinds of software.
To install scoop you need to run two commands in a powershell terminal

Set the needed exexcution policy
```ps1
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Install scoop
```ps1
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```

You can check if scoop installed correctly with following command
```ps1
scoop -v
```

this should return an output like this

```
Current Scoop version:
v0.3.1 - Released at 2022-11-15

'extras' bucket:
567baafbd (HEAD -> master, origin/master, origin/HEAD) kate: Update to version 23.08.4-2251

'main' bucket:
34d7e77d6 (HEAD -> master, origin/master, origin/HEAD) protolint: Update to version 0.47.0

'versions' bucket:
f309c30d5 (HEAD -> master, origin/master, origin/HEAD) vscode-insiders: Update to version 1.86.0-insider+1702875943397
```

You should now have scoop succesfully installed and are now ready to start installing software with it!

<a id="item-two"></a>
### Installing python with scoop

To add python to your pc with scoop use following commands

```ps1
scoop bucket add main
```
this will add the main bucket (which contains python) to your scoop installation


you can now install python on your system using scoop with following command

```ps1
scoop install main/python
```

After you have installed scoop make sure to run 

**install-pep-514.reg** 

in 
> *C:\Users\YourUser\scoop\apps\python\current*

this will allow other applications to make use of python

If you did everything as follows you should now be able to run following command to get your python version
```ps1
py --version
```

<a id="item-three"></a>
### Running the python script from the terminal 

After you have succesfully installed python on your pc, you can now use it to run python scripts!

python scripts have the .py extension

Example script:

**test.py**

located in : **c:\dev\test.py**
```py
print("hello world")
```


----------


In order to run a script. You first have to navigate to the script in a terminal environment.

after you have located your script *and are situated in the correct directory**,
launch it by typing :
```ps1
py test.py
```

> Output: Hello world


