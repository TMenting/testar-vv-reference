This application is based on the [Qt application example](https://doc.qt.io/qt-5/qtwidgets-mainwindows-application-example.html) and used as a controlled environment for testing the visual validation module of [TESTAR](https://github.com/TESTARtool/TESTAR).

We have extended the application by adding multi language support and injected presentation failures.
Currently English and Dutch are supported. 


## Building the application
We have used Qt 5.12.2 in combination with Visual studio 2015 x64 on a Windows machine.
Other operating systems haven't been tested.

The project can be opened and compiled with Qt creator.
For the translations we have used the embedded translation tool to regenerate the TS files.
```
Tools -> External -> Linguist -> Update translations 
```
The translations can be provided by using the linguist.exe which can be found in the installation folder of Qt.
NOTE: Once the translations are completed don't forget to run the relase translations, this will generate the QM files.
```
Tools -> External -> Linguist -> Release translations 
```
To use the application outside Qt creator, run the windeployqt.exe. This executable can also be found in the installation directory of Qt.


## Running the application
Running the application with a preselected language is possible by using the -l argument, e.g.:
```
application.exe -l English
```
Also starting the application with a preloaded text file is possible by using the -f argument followed by the absolute path of the text file.