# Инициализация словарей

---------------------------------------

```
	#include <iostream>
	#include <map>
	using namespace std;

	//Dictionary<String, String>
	map<string, string> languages = {
	    {"ru", "russian"},
	    {"en", "english"}
	};

	//Dictionary<Int, String>
	map<int, string>  numbers {
	    {1, "one"}, {2, "two"}, {3, "three"}
	};

	//Dictionary<Int, Employee>
	map<int, Employee> employees {
	    {1, Employee("Anton", "Pavlov")},
	    {2, Employee("Elena", "Kirienko")}
	};
```

--------------------------
[назад](../../../README.md)

