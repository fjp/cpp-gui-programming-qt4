# Book: C++ GUI Programming with Qt4, examples in Qt5

The book is from 2008 with the examples shown working in Qt4.
Because of the new Qt5 version the examples in this repository are adapted to use Qt5, not Qt4 as the name suggests.


## Build instructions

Each example folder usually contains a `<folder_name>.pro` file which can be used to create a platform specific `Makefile`
using the following command:

```
qmake <folder_name>.pro
```

With the generated `Makefile` it is possible to execute `make` to build the target.

## Build intstructions if example folder contains no .pro file

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

With the generated `Makefile` it is possible to execute `make` to build the target.
After the target was created (windows: `target_name.exe`, mac: `target_name.app`, linux: `target_name`) 
without errors it is possible to run it (windows: `target_name.exe`, mac: `open target_name.app`, linux: `./target_name`).

## Migration from Qt4 to Qt5

In Qt5 most of the previously known as QtGui functionality now is being called QtWidgets.

Use `#include <QtWidgets>` instead of `#include <QtGui>`.
