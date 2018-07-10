

# Инициализация структур без конструкторов

---------------------------------------

```
	Rectangle rect = {{10, 10}, {5, 5}};   

    struct Size {
        int width, height;
    };

    struct Point {
        int top, left;
    };

    struct Rectangle {
        Size size;
        Point point;
    };
```

--------------------------
[назад](../../../README.md)