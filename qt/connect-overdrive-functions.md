#Коннектим переопределенные функции
```
	connect(ui->comboBox,
			static_cast<void (QComboBox::*)(int)>(&QComboBox::currentIndexChanged), 
			this,
			[=](int value){ /*что-то делаем с value*/ });
```

----------------------
[назад](../README.md)
