# cpp-gui-programming-qt4

To buil each example go to its folder and run the following command:

```
qmake -project
``` 

This will generate a `*.pro` file with the name corresponding to the current folder.

Note: The created `*.pro` file probably will need to be edited. 
For example add the `QT` variable to specify what modules are required.
Especially for Qt5 you will most likely need to add the following line to the `*.pro` file:

```
QT += widgets
```

Then execute the following command to generate a `Makefile`.

```
qmake <folder_name>.pro
```

Wit the generated `Makefile` it is possible to execute `make` to build the target.
