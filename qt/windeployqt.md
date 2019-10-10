# Утилита Qt для сборки библиотек, необходимых для работы приложения
- открываем cmd.exe
- переходим в каталог Qt
```
cd C:\Qt\Qt5.6.0\5.6\msvc2015\bin
```
- запускаем утилиту windeployqt с указанием полного пути до нужного файла
```
windeployqt C:\pathToYourProgram\programName.exe
```
- радуемся :)
----------------------
- P.S.: для QML требуется использовать дополнительные параметры:
```
windeployqt --release --qmldir c:\Qt\Qt5.5.1_EXT\5.11.1\msvc2017_64\qml d:\QuickJomSwitching\QuickJomSwitching.exe
```

### источники:
[Документация Qt5](http://doc.qt.io/qt-5/windows-deployment.html)
[Форум Qt(QML)](https://forum.qt.io/topic/73340/windeployqt-and-qml/2)

----------------------
[назад](../README.md)
