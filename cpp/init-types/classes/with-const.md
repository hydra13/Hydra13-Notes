# Инициализация классов с конструктором

---------------------------------------

```
	#include <iostream>
	using namespace std;

	Phone nokiaPhone("Nokia 6610");
	Employee kim("Victorya", "Kim",
	    Phone("iPhone 5"));

	class Phone {
	    public:
	    string model;
	    
	    Phone(string model) {
	        this->model = model;
	    }
	    
	    Phone(){}
	};

	class Employee {
	    public:
	    string firstName;
	    string lastName;
	    Phone personalPhone;
	    
	    Employee(string firstName, string lastName, Phone phone) {
	        this->firstName = firstName;
	        this->lastName = lastName;
	        personalPhone = phone;
	    }
	};
```

--------------------------
[назад](../../../README.md)

