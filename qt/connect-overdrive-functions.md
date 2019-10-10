# Коннектим переопределенные функции

----------------------
- Для сигналов с разными наборами аргументов требуется явное указание типов аргументов
```
	connect(ui->comboBox,
			static_cast<void (QComboBox::*)(int)>(&QComboBox::currentIndexChanged), 
			this,
			[=](int value){ /*что-то делаем с value*/ });
```

----------------------
[назад](../README.md)
