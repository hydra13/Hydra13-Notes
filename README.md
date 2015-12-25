# Zorin OS 9 сборка ванильного ядра версии 4.3.3

Это небольшая заметка по обновлению ядра в дистрибутиве линукс Zorin OS 9.
Последовательность действий основана на моем личном опыте :)
Так что эту информацию вы используете на свой страх и риск. 
> Автор не несет никакой ответственности за ваши действия/бездействия!

Zorin OS 9 - Compile Linux Core v 4.3.3
---------------------------------------
* в самом начале требуется установить дополнительные пакеты:
```
	sudo apt-get update
	sudo apt-get build-dep linux
	sudo apt-get install kernel-package
```
* для конфигурирования при помощи menuconfig:
```
	sudo apt-get install libncurses5-dev
```
* для версии 4.3.3 требуется openssl:
```
	sudo apt-get install libssl-dev
```
* скачиваем с kernel.org ядро требуемой версии (в моем случае 4.3.3)

* распаковываем в /usr/src

* заходим в linux-4.3.3

* копируем старую конфигурацию: 
```
	sudo cp /boot/config-$(uname -r) .config
```
* конфигурируем ядро на основе старой конфигурации: 
```
	sudo make oldconfig 
```
* рекомендую просмотреть настройки ядра после конфигурации: 
```
	make menuconfig
```
* компилируем: 
```
	fakeroot make-kpkg -j 9 --initrd --append-to-version=-custom kernel_image kernel_headers #-j <количество ядер>+1
```
* выходим на уровень выше 
* устанавливаем 1: 
```
	sudo dpkg -i linux-image-4.3.3-custom_..._.deb
```
* устанавливаем 2: 
```
	sudo dpkg -i linux-headers-4.3.3-custom_..._.deb
```
* генерируем начальный RAM-диск: 
```
	sudo update-initramfs -c -k 4.3.3-custom
```
* обновляем grub: 
```
	sudo update-grub
```
* ну и: 
	sudo reboot

Всем добра! :)
______________