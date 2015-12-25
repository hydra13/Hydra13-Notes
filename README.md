# Zorin OS 9 сборка ванильного ядра версии 4.3.3

Это небольшая заметка по обновлению ядра в дистрибутиве линукс Zorin OS 9.
Последовательность действий основана на моем личном опыте, который не очень хорош :)
Так что эту информацию вы используете на свой страх и риск. Автор не несет никакой
ответственности за ваши действия/бездействия!

Zorin OS 9 - Compile Linux Core v 4.3.3:

0) в самом начале требуется установить дополнительные пакеты:
	sudo apt-get update
	sudo apt-get build-dep linux
	sudo apt-get install kernel-package
	+- sudo apt-get install libncurses5-dev
	для версии 4.3.3 требуется openssl:
	sudo apt-get install libssl-dev

1) скачиваем с kernel.org ядро требуемой версии (в моем случае 4.3.3)

2) распаковываем в /usr/src

3) заходим в linux-4.3.3

4) копируем старую конфигурацию: sudo cp /boot/config-$(uname -r) .config

5) конфигурируем ядро на основе старой конфигурации: sudo make oldconfig (рекомендую просмотреть настройки ядра после конфигурации: make menuconfig)

6) компилируем: fakeroot make-kpkg -j 9 --initrd --append-to-version=-custom kernel_image kernel_headers #-j <количество ядер>+1

7) выходим на уровень выше 

8) устанавливаем 1: sudo dpkg -i linux-image-4.3.3-custom_..._.deb

9) устанавливаем 2: sudo dpkg -i linux-headers-4.3.3-custom_..._.deb

10) генерируем начальный RAM-диск: sudo update-initramfs -c -k 4.3.3-custom

11) обновляем grub: sudo update-grub

ну и sudo reboot

Всем добра! :)