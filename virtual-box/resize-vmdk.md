

# Изменение размера HDD (VMDK) виртуальной машины (VirtualBox)

---------------------------------------
* В коммандной строке при помощи следующих комманд (размер в Мб):
```
	VBoxManage clonehd "source.vmdk" "cloned.vdi" --format vdi
	VBoxManage modifyhd "cloned.vdi" --resize 163840
	VBoxManage clonehd "cloned.vdi" "resized.vmdk" --format vmdk
```
* Далее требуется применить изменения в самой виртуальной системе. Для этого загружаемся с live-dvd и при помощи GParted изменяем размер используемого раздела.

--------------------------
[назад](../README.md)