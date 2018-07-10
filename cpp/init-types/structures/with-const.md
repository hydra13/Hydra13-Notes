# Инициализация структур с конструктором

---------------------------------------

```
	Size size(10, 10);
    Point point(5, 5);
    Rectangle rect(size, point); 

    struct Size {
        int width, height;

        Size () {}
        Size (int width, int height) {
            this->width = width;
            this->height = height;
        }
    };

    struct Point {
        int top, left;

        Point () {}
        Point (int top, int left) {
            this->top = top;
            this->left = left;
        }
    };

    struct Rectangle {
        Size size;
        Point point;

        Rectangle (Size size1, Point point) {
            this->size = size1;
            this->point = point;
        }
    };
```

--------------------------
[назад](../../../README.md)