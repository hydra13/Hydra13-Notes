# Подсчет MD5 для CD/DVD

---------------------------------------
* Первый способ (на основе моих тестов - не совсем корректный):
```
	head --bytes='isosize /dev/cdrom' /dev/cdrom | md5sum -b
```
* Второй способ:
```
	md5sum -b /dev/cdrom
```
* Третий способ:

*получаем размер и количество блоков:*
```
	isoinfo -d -i /dev/cdrom
    		Logical block size is: 2048
    		Volume size is: 161632
```
*при помощи утилит dd и md5sum получаем требуемый результат:*
```
	dd if=/dev/cdrom bs=2048 count=161632 conv=notrunc,noerror | md5sum -b
```

--------------------------
[назад](../README.md)

