## Lesson 2 - Buttons, Entry and Setting Components Options

**Creating a button**

Using Tkinter module and button class

```
button = tkinter.button(text = "Click me", command = name_of_the_command)
button.pack()
```

Example of usage:

```
my_label = tkinter.label(text = "Button waiting to be clicked")

def button_clicked():
  my_label.config(text = "Button got clicked")

button = tkinter.button(text = "Click me", command = button_clicked)
button.pack()
```

**Creating an Entry**

```
entry = tkinter.entry()
entry.pack()
```

Note that for an entry it has standard options and widget specific options
(Read doccumentation for more)


Example of usage:
```
my_label = tkinter.label(text = "Waiting Entry")

def button_clicked():
  new_text = input.get()
  my_label.config(text = new_text)

button = tkinter.button(text = "Click me", command = button_clicked)
button.pack()

input = tkinter.entry(width = 10)
input.pack()
print(input.get())
```
