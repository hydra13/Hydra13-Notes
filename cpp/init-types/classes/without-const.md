# Инициализация классов без конструкторов

---------------------------------------

```
	#include <iostream>
	using namespace std;

	Phone nokiaPhone {"Nokia 6610"};

	Phone iPhone5 {"iPhone 5"};

	Employee kim {"Victorya", "Kim", iPhone5};

	class Phone {
	    public:
	    string model;
	};

	class Employee {
	    public:
	    string firstName;
	    string lastName;
	    Phone personalPhone;
	};
```

--------------------------
[назад](../../../README.md)

