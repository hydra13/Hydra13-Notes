# Установка дополнений гостевой ОС в VirtualBox

---------------------------------------
* сначала обновляемся:
```
	sudo apt-get update
```
* устанавливаем необходимые зависимости:
```
	sudo apt-get install linux-headers-$(uname -r) dkms build-essential
```
* запускаем установку дополнений:
```
	sudo ./VBoxLinuxAdditions.run
```
* проверяем:
```
	sudo reboot
```

--------------------
[назад](../README.md)
