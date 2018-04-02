# Резервные копии списка пакетов dpkg

---------------------------------------
* создание резервной копии списка пакетов:
```
	dpkg --get-selections > pkgs.list
```
* дублирование на другой системе:
```
	dpkg --set-selections pkgs.list
	apt-get dselect-upgrade
```

--------------------
[назад](../README.md)
