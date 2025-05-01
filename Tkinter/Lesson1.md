### Part 1 - Creating Windows and Labels with Tkinter

**Import the Tkinter module:**

```
import tkinter
```

**Create a window**

```
window = tkinter.Tk
```

**Keep the window on screen** 

```
window.mainloop()
```
Note: keep this line in the very end of the program

**Create a name for the window**
```
window.title("My first GUI Program")
```

**Change the size of the window**
```
window.minsize(width=500, height=300)
```

**Create label**
```
my_label = tkinter.Label(text="I'm a label", font=("Arial", 24, "italic"))
```

But in order to display it, you need to:
```
my_label.pack(side="bottom")
```
Note: side must be top, bottom, left, or right


