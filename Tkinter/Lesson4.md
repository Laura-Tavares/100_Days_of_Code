## Lesson 4 - Layout Managers: pack(), place() and grid()

**Pack**

Possible parameters:

- **expand** − When set to true, widget expands to fill any space not otherwise used in widget's parent.

- **fill** − Determines whether widget fills any extra space allocated to it by the packer, or keeps its own minimal dimensions: NONE (default), X (fill only horizontally), Y (fill only vertically), or BOTH (fill both horizontally and vertically).

- **side** − Determines which side of the parent widget packs against: TOP (default), BOTTOM, LEFT, or RIGHT.


**Place**

Used for precise positioning (you can set specific values for x and y to each widget).

Place allows you explicitly set the position and size of a window, either in absolute terms, or relative to another window. 

**Grid**

Grid puts the widgets in a 2-dimensional table. The master widget is split into a number of rows and columns, and each “cell” in the resulting table can hold a widget.


*Note: It starts with row 0 column 0* 


Example: You want to set the label, buttom and entry to be on a diagonal. For that you'll:

```
my_label.grid(column = 0, row = 0)
button.grid(column = 1, row = 1)
input.grid(column = 2, row = 2)
```

*Note: grid and place are not compatiple*


