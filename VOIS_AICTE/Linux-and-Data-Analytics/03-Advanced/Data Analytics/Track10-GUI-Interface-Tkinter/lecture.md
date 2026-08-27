# Getting Started with Tkinter GUI Interface

## Learning Objectives

The learning objective is to gain knowledge on:

* explaining various concepts involved in building GUI applications using Python.
* understanding different options available for GUI programming in Python.
* understanding the purpose and features of **Tkinter**.
* understanding different Tkinter widgets.
* understanding how to handle user interaction with widgets.
* creating GUI applications using Tkinter.
* creating and manage a Tkinter root window.
* instantiating and configure different Tkinter widgets.
* understanding how widgets are positioned inside a GUI.
* understanding the purpose of commonly used Tkinter widgets such as:

  * Button
  * Canvas
  * Checkbutton
  * Entry
  * Frame
  * Label
  * Listbox
  * Menubutton
  * Message
  * Radiobutton
  * Scale
  * Text
  * Spinbox
  * LabelFrame

---

## Prerequisites

The following knowledge is sufficient for understanding this course:

* Basic knowledge of Python.
* Understanding of Python data types.
* Understanding of Python objects.
* Basic familiarity with Python programming.

---

# About the Course

**Tkinter** is the standard GUI library for Python.

Tkinter provides the necessary functionality to create **Graphical User Interfaces (GUIs)** and desktop applications using Python.

This course provides the necessary skills to:

* Create GUI applications.
* Work with Tkinter widgets.
* Handle user interaction.
* Create graphical interfaces.
* Build desktop applications.
* Understand different types of GUI widgets.
* Configure widgets using different parameters.

Tkinter can be used to develop Python GUI applications for practical and commercial purposes.

---

# GUI Programming in Python

Python provides various options for developing **Graphical User Interfaces**, abbreviated as **GUI**.

Some important tools and interfaces supported by Python include:

1. **Tkinter**
2. **wxPython**
3. **Jython**

---

# Tkinter

**Tkinter** is the standard GUI library for Python.

It provides a Python interface to the **Tk GUI toolkit**.

Tkinter allows developers to create graphical user interfaces quickly and easily.

It can be used to create:

* Windows.
* Buttons.
* Labels.
* Text boxes.
* Menus.
* Check buttons.
* Radio buttons.
* Sliders.
* Drawing areas.
* Other graphical components.

Tkinter provides a powerful object-oriented interface to the Tk GUI toolkit.

Using Tkinter, developers can insert, manipulate, and place corresponding GUI widgets in an application.

---

# wxPython

**wxPython** is an open-source Python interface for **wxWidgets**.

It provides functionality for developing graphical user interfaces in Python.

wxPython can be used to create desktop applications with graphical interfaces.

---

# Jython

**Jython** provides Python support for the **Java platform**.

It allows Python programs to access Java class libraries available on the local machine.

Jython provides a way for Python and Java functionality to work together.

---

# Creating a GUI Application Using Tkinter

Creating a GUI application using Tkinter involves a few basic steps.

The general process is:

1. Import the Tkinter library.
2. Instantiate a `Tk` object.
3. Create the required widgets.
4. Place the widgets inside the root window.
5. Start the GUI using the `mainloop()` method.

The basic workflow is:

```text
Import Tkinter
      ↓
Create Root Window
      ↓
Create Widgets
      ↓
Place Widgets
      ↓
Start mainloop()
```

---

# Importing Tkinter

The Tkinter library must first be imported into the Python program.

A common way to import Tkinter is:

```python
import tkinter
```

Tkinter can also be imported using an alias:

```python
import tkinter as tk
```

The alias `tk` provides a shorter way of referencing Tkinter classes and methods.

---

# Root Window

The **root window** is the main window of a Tkinter GUI application.

It can be instantiated using:

```python
root = tk.Tk()
```

The root object represents the main application window.

Other widgets can use the root window as their **master** or parent.

Example:

```python
import tkinter as tk

root = tk.Tk()
```

---

# Main Loop

After creating the root window and adding widgets, the Tkinter application must start its event loop.

This is done using:

```python
root.mainloop()
```

The `mainloop()` method keeps the GUI application running and allows it to respond to user interaction.

A basic Tkinter application can therefore be written as:

```python
import tkinter as tk

root = tk.Tk()

root.mainloop()
```

---

# Tkinter Widgets

Tkinter provides a number of widgets for creating graphical user interfaces.

The major widgets discussed in this course are:

| Widget      | Purpose                                     |
| ----------- | ------------------------------------------- |
| Button      | Displays a clickable button                 |
| Canvas      | Provides an area for drawing                |
| Checkbutton | Allows multiple selections                  |
| Entry       | Accepts single-line text input              |
| Frame       | Groups and organizes widgets                |
| Label       | Displays text or images                     |
| Listbox     | Displays a list of selectable items         |
| Menubutton  | Provides a dropdown menu                    |
| Message     | Displays multiline text                     |
| Radiobutton | Allows one selection from a group           |
| Scale       | Provides a graphical slider                 |
| Text        | Allows multiline editable text              |
| Spinbox     | Allows selection from a fixed set of values |
| LabelFrame  | Provides a labelled container               |

---

# Button Widget

The **Button** widget is used when you want to display a button containing text or an image.

Buttons are commonly used to allow the user to perform an action.

The basic syntax involves creating a Button object and passing the required arguments.

Example:

```python
button = tk.Button(root, text="Click Me")
```

Here:

```text
root → master
text → text displayed on the button
```

---

## Button Widget Parameters

The first argument is the:

```text
master
```

The `master` represents the parent window or root window on which the widget is placed.

Other options are generally specified as **key-value pairs**.

Example:

```python
button = tk.Button(
    root,
    text="Click Me",
    width=20
)
```

Common options can be used to control properties such as:

* Text.
* Width.
* Height.
* Color.
* Command.
* Displayed image.

---

# Canvas Widget

The **Canvas** widget provides a rectangular area intended for drawing pictures or creating complex layouts.

Canvas can be used to:

* Draw graphics.
* Draw lines.
* Draw arcs.
* Draw circles.
* Draw ellipses.
* Display images.
* Create graphical structures.

The Canvas widget is available as part of the Tkinter toolkit.

Example:

```python
canvas = tk.Canvas(
    root,
    width=400,
    height=300
)
```

---

## Canvas Parameters

The first parameter is the:

```text
master
```

The master represents the parent window on which the Canvas widget is placed.

Other options are generally supplied as key-value pairs.

Example:

```python
canvas = tk.Canvas(
    root,
    width=400,
    height=300
)
```

---

# Canvas Drawing Functions

Tkinter Canvas provides several functions for drawing graphical objects.

Important Canvas functions include:

* `create_arc()`
* `create_image()`
* `create_line()`
* `create_oval()`

---

# Canvas Arc

The `create_arc()` function is used to create an arc on the Canvas.

Example structure:

```python
canvas.create_arc(
    x1,
    y1,
    x2,
    y2,
    start=0,
    extent=90,
    fill="blue"
)
```

The coordinates define the area in which the arc is created.

Important parameters include:

* Starting coordinates.
* Extent.
* Fill color.

---

# Canvas Image

The `create_image()` function is used to create an image item on the Canvas.

It can be used to place an image on the blank Canvas area.

The function requires the appropriate coordinates and image object.

Conceptually:

```python
canvas.create_image(
    x,
    y,
    image=image_object
)
```

---

# Canvas Line

The `create_line()` function is used to draw a line on a Canvas.

Coordinates are provided to specify the points through which the line passes.

Example:

```python
canvas.create_line(
    x1,
    y1,
    x2,
    y2
)
```

Multiple coordinates can be provided to create more complex lines.

---

# Canvas Oval

The `create_oval()` function is used to create a circle or ellipse on the Canvas.

The coordinates define the bounding area of the oval.

Example:

```python
canvas.create_oval(
    x1,
    y1,
    x2,
    y2
)
```

Depending on the dimensions of the bounding box, the result can appear as:

* Circle.
* Ellipse.

---

# Practical Example — Canvas

A basic Canvas application follows these steps:

1. Import Tkinter.
2. Import required message-box functionality if required.
3. Instantiate the root window.
4. Create the Canvas.
5. Specify the Canvas width and height.
6. Specify the fill/background properties.
7. Create the required graphical object.
8. Pack the Canvas.
9. Start the main loop.

Example:

```python
import tkinter as tk

root = tk.Tk()

canvas = tk.Canvas(
    root,
    width=400,
    height=300
)

canvas.create_arc(
    50,
    50,
    200,
    200,
    start=0,
    extent=90,
    fill="blue"
)

canvas.pack()

root.mainloop()
```

---

# Checkbutton Widget

The **Checkbutton** widget is used to display a number of options that the user can select.

Checkbuttons generally appear as selectable boxes.

The user can:

* Select an option.
* Deselect an option.
* Select multiple options.

Unlike radio buttons, multiple checkbuttons can be selected simultaneously.

Images can also be associated with checkbuttons.

---

# Checkbutton Syntax

The basic syntax involves calling the `Checkbutton` method.

The first argument is:

```text
master
```

The master represents the parent window or root window.

Other options are supplied as key-value pairs.

Example:

```python
check = tk.Checkbutton(
    root,
    text="Option 1"
)
```

---

# Checkbutton Variables

Variables can be associated with checkbuttons to determine whether they are selected or deselected.

Tkinter provides variable types such as:

```python
tk.IntVar()
```

Example:

```python
var1 = tk.IntVar()
var2 = tk.IntVar()
```

The variables can then be associated with checkbuttons.

Example:

```python
check1 = tk.Checkbutton(
    root,
    text="Option 1",
    variable=var1
)
```

The checkbutton can use values representing its selected and unselected states.

---

# Practical Example — Checkbutton

A basic Checkbutton application can follow these steps:

1. Import Tkinter.
2. Import message-box functionality if required.
3. Create the root window.
4. Create variables for the checkbuttons.
5. Create the Checkbutton widgets.
6. Specify the text.
7. Associate the variables.
8. Configure the on/off values.
9. Pack the widgets.
10. Start the main loop.

---

# Entry Widget

The **Entry** widget is primarily used to accept **single-line text input** from the user.

It is useful when a user needs to enter information such as:

* Name.
* Username.
* Email.
* Search text.
* Other single-line values.

Example:

```python
entry = tk.Entry(root)
```

---

# Entry vs Text vs Label

Different Tkinter widgets are suitable for different types of content.

| Widget | Purpose                         |
| ------ | ------------------------------- |
| Entry  | Single-line user input          |
| Text   | Multiple lines of editable text |
| Label  | Displaying text or images       |

If multiple lines of text need to be entered or edited, the **Text** widget is more appropriate.

If text only needs to be displayed, the **Label** widget can be used.

---

# Entry Widget Example

A practical Entry application can contain a Label and an Entry widget.

Example:

```python
import tkinter as tk

root = tk.Tk()

label = tk.Label(root, text="Name:")
label.pack()

entry = tk.Entry(root)
entry.pack()

root.mainloop()
```

The Entry widget can be configured using different options for:

* Width.
* Allowed characters.
* Appearance.
* Position.

---

# Frame Widget

The **Frame** widget is important for grouping and organizing other widgets.

A Frame acts as a **container**.

It provides a rectangular area in which other widgets can be arranged.

Frames are useful when:

* Several widgets need to be grouped.
* The layout needs to be organized.
* Different sections of a GUI need to be separated.
* Complex GUI structures need to be created.

---

# Frame as a Container

A Frame can contain other widgets.

The general structure can be represented as:

```text
Root Window
│
├── Frame
│   ├── Button
│   ├── Button
│   ├── Button
│   └── Button
│
└── Other Widgets
```

Example:

```python
frame = tk.Frame(root)
frame.pack()
```

Widgets can then use the Frame as their master.

---

# Practical Example — Frame

A GUI can contain different buttons inside a Frame.

For example:

```python
import tkinter as tk

root = tk.Tk()

frame = tk.Frame(root)
frame.pack()

red_button = tk.Button(frame, text="Red")
green_button = tk.Button(frame, text="Green")
blue_button = tk.Button(frame, text="Blue")
black_button = tk.Button(frame, text="Black")

red_button.pack()
green_button.pack()
blue_button.pack()
black_button.pack()

root.mainloop()
```

The buttons use the Frame as their parent rather than directly using the root window.

---

# Label Widget

The **Label** widget is used to implement a display area where text or images can be placed.

A Label can display:

* Text.
* Images.

The text displayed by a Label can be updated during program execution.

A Label can also provide formatting options such as:

* Font.
* Underlining.
* Text color.
* Alignment.

---

# Label Syntax

The basic syntax involves calling the `Label` method.

Example:

```python
label = tk.Label(
    root,
    text="Hello Students"
)
```

The first argument is the:

```text
master
```

The master represents the parent or root window.

---

# Label Example

A basic Label application can be written as:

```python
import tkinter as tk

root = tk.Tk()

label = tk.Label(
    root,
    text="Hello Students"
)

label.pack()

root.mainloop()
```

The Label can also be associated with a variable.

The displayed text can then be changed during program execution.

---

# Listbox Widget

The **Listbox** widget is used to display a list of items from which a user can select one or more items.

A Listbox can be used when the application needs to provide a list of available choices.

Example:

```python
listbox = tk.Listbox(root)
```

---

# Adding Items to a Listbox

Items can be inserted into a Listbox using the `insert()` method.

The method requires:

1. The sequence/index position.
2. The text to be displayed.

Example:

```python
listbox.insert(1, "Python")
listbox.insert(2, "Java")
listbox.insert(3, "C++")
```

The Listbox can then be packed into the root window.

---

# Practical Example — Listbox

```python
import tkinter as tk

root = tk.Tk()

listbox = tk.Listbox(root)

listbox.insert(1, "Python")
listbox.insert(2, "Java")
listbox.insert(3, "C++")
listbox.insert(4, "JavaScript")

listbox.pack()

root.mainloop()
```

The user can select items from the displayed list.

---

# Menubutton Widget

The **Menubutton** widget is part of a dropdown menu system.

It can be used to create a menu option that displays additional choices when clicked.

A Menubutton is associated with a **Menu** widget.

When the user clicks the Menubutton, a dropdown list can appear.

---

# Menubutton Structure

The general structure is:

```text
Menubutton
     ↓
   Menu
     ↓
Dropdown Options
```

The user can select an individual option from the dropdown menu.

---

# Creating a Menubutton

The basic process is:

1. Create the root window.
2. Create a Menubutton.
3. Specify the displayed text.
4. Create the associated Menu.
5. Add menu elements.
6. Add checkbuttons or labels if required.
7. Pack the Menubutton.
8. Start the main loop.

Example:

```python
import tkinter as tk

root = tk.Tk()

menubutton = tk.Menubutton(
    root,
    text="Options"
)

menu = tk.Menu(
    menubutton,
    tearoff=0
)

menu.add_checkbutton(label="Option 1")
menu.add_checkbutton(label="Option 2")

menubutton["menu"] = menu

menubutton.pack()

root.mainloop()
```

---

# Message Widget

The **Message** widget is used to display multiline text.

It provides functionality similar to the Label widget but is particularly useful for longer text.

One important feature of the Message widget is that it can automatically **wrap text** according to the available width.

It also supports:

* Multiline text.
* Automatic line breaking.
* Content justification.
* Width-based text wrapping.

---

# Message vs Label

The Message widget is similar to a Label but provides additional functionality for handling multiline text.

| Widget  | Main Use                                       |
| ------- | ---------------------------------------------- |
| Label   | Display text or images                         |
| Message | Display multiline text with automatic wrapping |

---

# Message Example

Example:

```python
import tkinter as tk

root = tk.Tk()

message = tk.Message(
    root,
    text="This is a multiline message displayed using Tkinter."
)

message.pack()

root.mainloop()
```

The Message widget automatically handles line wrapping based on its configured width.

---

# Radiobutton Widget

The **Radiobutton** widget is used to implement a multiple-choice selection mechanism where the user can choose **only one option** from a group.

Each group of radio buttons must be associated with the **same variable**.

Each radio button represents a different value.

For example:

```text
○ Option 1
○ Option 2
○ Option 3
```

Only one option can be selected at a time.

---

# Radiobutton Variables

A variable is associated with the group of radio buttons.

Example:

```python
choice = tk.IntVar()
```

Each radio button can then specify a different value.

Example:

```python
r1 = tk.Radiobutton(
    root,
    text="Option 1",
    variable=choice,
    value=1
)

r2 = tk.Radiobutton(
    root,
    text="Option 2",
    variable=choice,
    value=2
)

r3 = tk.Radiobutton(
    root,
    text="Option 3",
    variable=choice,
    value=3
)
```

Because all three buttons use the same variable, only one can be selected at a time.

---

# Handling Radiobutton Selection

A user-defined function can be used to determine which option the user selected.

The selected value can then be displayed using another widget such as a Label.

Example:

```python
def selected():
    label.config(text=str(choice.get()))
```

A button can be used to call the function.

---

# Practical Example — Radiobutton

```python
import tkinter as tk

root = tk.Tk()

choice = tk.IntVar()

r1 = tk.Radiobutton(
    root,
    text="Option 1",
    variable=choice,
    value=1
)

r2 = tk.Radiobutton(
    root,
    text="Option 2",
    variable=choice,
    value=2
)

r3 = tk.Radiobutton(
    root,
    text="Option 3",
    variable=choice,
    value=3
)

label = tk.Label(root, text="Select an option")

r1.pack()
r2.pack()
r3.pack()
label.pack()

root.mainloop()
```

The user can use the keyboard `Tab` key to move between radio buttons.

---

# Scale Widget

The **Scale** widget provides a graphical slider that allows the user to select a value from a specific range.

A Scale can be used when the user needs to select a value by moving a slider.

Conceptually:

```text
0 -----------●----------- 100
             ↑
           Slider
```

---

# Scale Widget Parameters

The first parameter is the:

```text
master
```

The master represents the parent or root window.

A variable can be associated with the Scale to store the selected value.

A `DoubleVar` can be used when decimal values are required.

Example:

```python
value = tk.DoubleVar()

scale = tk.Scale(
    root,
    variable=value
)
```

---

# Scale Example

The Scale can be positioned using options such as `anchor`.

Example:

```python
scale.pack(anchor="center")
```

A button can be used to retrieve the current Scale value.

Example:

```python
def select():
    print(value.get())
```

A Button can then call the `select()` function.

---

# Text Widget

The **Text** widget provides advanced functionality for editing multiline text.

It can be used to:

* Edit multiline text.
* Format text.
* Change text colors.
* Change font settings.
* Add tags.
* Insert images.
* Embed windows.
* Work with plain text.
* Work with formatted text.

The Text widget is designed to handle both plain and formatted text.

---

# Text Widget vs Entry Widget

| Widget | Purpose                 |
| ------ | ----------------------- |
| Entry  | Single-line text        |
| Text   | Multiline editable text |

The Entry widget is appropriate for short single-line input.

The Text widget is appropriate when multiple lines of editable text are required.

---

# Text Widget Example

Example:

```python
import tkinter as tk

root = tk.Tk()

text = tk.Text(root)

text.insert(
    "1.0",
    "Hello Students"
)

text.pack()

root.mainloop()
```

The Text widget can be modified and formatted during program execution.

---

# Text Tags

Tkinter Text widgets support **tags**.

Tags can be used to apply formatting to specific portions of text.

For example, a tag can specify:

* Background color.
* Foreground color.
* Font.
* Other formatting properties.

Example:

```python
text.tag_config(
    "highlight",
    background="yellow"
)
```

A tag can then be applied to a selected range of text.

This makes it possible to format different portions of the Text widget differently.

---

# Spinbox Widget

The **Spinbox** widget is a variation of the standard Entry widget.

It is primarily used to select a value from a **fixed number of values**.

The user can manually spin through the available values and select one.

Example:

```text
0
1
2
3
4
5
...
10
```

---

# Spinbox Example

A Spinbox can be created as follows:

```python
import tkinter as tk

root = tk.Tk()

spinbox = tk.Spinbox(
    root,
    from_=0,
    to=10
)

spinbox.pack()

root.mainloop()
```

This creates a Spinbox containing values from `0` to `10`.

---

# LabelFrame Widget

The **LabelFrame** widget is a container used for organizing complex GUI layouts.

It provides the functionality of a Frame while also allowing a **label** to be displayed around the container.

A LabelFrame can therefore be considered as:

```text
Frame
+
Label
```

It can act as a spacer or container for complex window layouts.

---

# LabelFrame Example

A LabelFrame can be created using:

```python
import tkinter as tk

root = tk.Tk()

labelframe = tk.LabelFrame(
    root,
    text="This is a Label Frame"
)

labelframe.pack()

root.mainloop()
```

Other widgets can be placed inside the LabelFrame.

Example:

```python
label = tk.Label(
    labelframe,
    text="Hello Students"
)

label.pack()
```

Here, the LabelFrame acts as the master of the Label widget.

---

# Tkinter Widget Hierarchy

Tkinter applications can contain widgets inside other widgets.

A typical structure can be represented as:

```text
Root Window
│
├── Frame
│   ├── Button
│   ├── Label
│   └── Entry
│
├── Canvas
│
├── Listbox
│
├── Scale
│
└── LabelFrame
    └── Label
```

This hierarchical structure makes it possible to organize complex graphical interfaces.

---

# Master Parameter

Most Tkinter widgets require a **master** parameter.

The master identifies the parent widget or window.

For example:

```python
button = tk.Button(root)
```

Here:

```text
root → master
button → child widget
```

A widget can also use another container as its master.

Example:

```python
frame = tk.Frame(root)

button = tk.Button(frame)
```

Here:

```text
root
 ↓
frame
 ↓
button
```

---

# Widget Options

Tkinter widgets can be configured using options.

These options are generally supplied as:

```text
key=value
```

Example:

```python
tk.Button(
    root,
    text="Click",
    width=20
)
```

The exact options depend on the widget.

Common types of options include:

* Text.
* Width.
* Height.
* Background.
* Foreground.
* Font.
* Variable.
* Command.
* Value.
* Image.
* Alignment.

---

# The Pack Method

The course examples use the `pack()` method to place widgets inside their parent.

Example:

```python
button.pack()
```

The `pack()` method adds the widget to the GUI layout.

Additional parameters can be used to control placement.

Example:

```python
scale.pack(anchor="center")
```

---

# Handling User Interaction

Tkinter widgets can respond to user actions.

For example:

* A Button can execute a function.
* A Checkbutton can store a selected/unselected state.
* A Radiobutton can store a selected value.
* A Scale can provide a selected numerical value.
* An Entry can receive user input.
* A Listbox can provide selected items.
* A Menubutton can display menu choices.

Tkinter therefore provides the functionality required to create interactive GUI applications.

---

# Tkinter Application Workflow

The overall workflow for creating a Tkinter GUI application is:

```text
Import Tkinter
       ↓
Create Root Window
       ↓
Create Variables if Required
       ↓
Create Widgets
       ↓
Configure Widget Parameters
       ↓
Place Widgets
       ↓
Define User Interaction Functions
       ↓
Start mainloop()
```

---

# Common Tkinter Widgets — Quick Reference

| Widget          | Main Purpose                                     |
| --------------- | ------------------------------------------------ |
| **Button**      | Display text or image and allow user interaction |
| **Canvas**      | Draw graphical objects                           |
| **Checkbutton** | Select or deselect multiple options              |
| **Entry**       | Accept single-line text input                    |
| **Frame**       | Group and organize widgets                       |
| **Label**       | Display text or images                           |
| **Listbox**     | Display selectable list items                    |
| **Menubutton**  | Display a dropdown menu                          |
| **Message**     | Display multiline wrapped text                   |
| **Radiobutton** | Select one option from a group                   |
| **Scale**       | Select a value using a slider                    |
| **Text**        | Edit multiline text                              |
| **Spinbox**     | Select values from a fixed set                   |
| **LabelFrame**  | Provide a labelled container                     |

---

# Important Widget Differences

## Checkbutton vs Radiobutton

### Checkbutton

Allows multiple options to be selected.

Example:

```text
☑ Python
☑ Java
☐ C++
```

### Radiobutton

Allows only one option from a group to be selected.

Example:

```text
○ Python
● Java
○ C++
```

---

## Entry vs Text

### Entry

Used for:

```text
Single-line text
```

### Text

Used for:

```text
Multiline editable text
```

---

## Label vs Message

### Label

Used to display text or images.

### Message

Used to display multiline text with automatic wrapping.

---

## Frame vs LabelFrame

### Frame

A general-purpose container used to group widgets.

### LabelFrame

A container that also displays a label.

---

## Canvas vs Other Widgets

Canvas is specifically intended for graphical content.

It can be used to draw:

* Lines.
* Arcs.
* Ovals.
* Images.
* Other graphical objects.

---

# Important Tkinter Methods and Functions

| Method / Function | Purpose                                           |
| ----------------- | ------------------------------------------------- |
| `Tk()`            | Creates the root window                           |
| `mainloop()`      | Starts the Tkinter event loop                     |
| `pack()`          | Places a widget in its parent                     |
| `create_arc()`    | Creates an arc on Canvas                          |
| `create_image()`  | Creates an image item on Canvas                   |
| `create_line()`   | Creates a line on Canvas                          |
| `create_oval()`   | Creates an oval or circle on Canvas               |
| `insert()`        | Inserts content into widgets such as Listbox/Text |
| `get()`           | Retrieves a variable or widget value              |
| `tag_config()`    | Configures formatting for Text tags               |

---

# Example — Basic Complete Tkinter Application

The following example demonstrates the fundamental structure of a Tkinter GUI application:

```python
import tkinter as tk

root = tk.Tk()

label = tk.Label(
    root,
    text="Hello Students"
)

entry = tk.Entry(root)

button = tk.Button(
    root,
    text="Submit"
)

label.pack()
entry.pack()
button.pack()

root.mainloop()
```

The application follows the basic Tkinter workflow:

```text
Import library
      ↓
Create root window
      ↓
Create widgets
      ↓
Place widgets
      ↓
Start main loop
```

---

# Example — Combining Multiple Widgets

Tkinter allows different widgets to be combined in the same application.

Example:

```python
import tkinter as tk

root = tk.Tk()

frame = tk.Frame(root)
frame.pack()

label = tk.Label(
    frame,
    text="Enter your name:"
)

entry = tk.Entry(frame)

button = tk.Button(
    frame,
    text="Submit"
)

label.pack()
entry.pack()
button.pack()

root.mainloop()
```

Here:

```text
Root Window
     ↓
   Frame
     ↓
 ┌───────────────┐
 │ Label         │
 │ Entry         │
 │ Button        │
 └───────────────┘
```

---

# Key Concepts to Remember

## Tkinter

Tkinter is the **standard GUI library for Python**.

---

## GUI

GUI stands for:

```text
Graphical User Interface
```

It allows users to interact with applications through graphical components.

---

## Root Window

The root window is the main window of a Tkinter application.

It is created using:

```python
root = tk.Tk()
```

---

## Main Loop

The Tkinter event loop is started using:

```python
root.mainloop()
```

---

## Master

The master represents the parent window or parent container of a widget.

Example:

```python
button = tk.Button(root)
```

Here `root` is the master.

---

## Button

Used to display text or images and provide an interactive button.

---

## Canvas

Used for drawing:

```text
Lines
Arcs
Ovals
Images
Graphics
```

---

## Checkbutton

Used when multiple options can be selected.

---

## Entry

Used for single-line text input.

---

## Frame

Used as a container for grouping and organizing widgets.

---

## Label

Used to display text or images.

---

## Listbox

Used to display a list from which users can select items.

---

## Menubutton

Used to create a dropdown menu selection mechanism.

---

## Message

Used to display multiline text with automatic wrapping.

---

## Radiobutton

Used when the user must choose only one option from a group.

---

## Scale

Used to select a value using a graphical slider.

---

## Text

Used for multiline editable and formatted text.

---

## Spinbox

Used to select a value from a fixed set of values.

---

## LabelFrame

Used as a container that combines the features of a Frame with a displayed label.

---

# Quick Reference

```text
Python GUI library
        ↓
     Tkinter

Main application window
        ↓
      Tk()

Keep GUI running
        ↓
   mainloop()

Single-line input
        ↓
     Entry

Multiline text
        ↓
      Text

Display text/image
        ↓
      Label

Clickable control
        ↓
     Button

Multiple selections
        ↓
   Checkbutton

Single selection
        ↓
   Radiobutton

Selectable list
        ↓
     Listbox

Graphical drawing
        ↓
     Canvas

Graphical slider
        ↓
      Scale

Fixed values
        ↓
    Spinbox

Widget container
        ↓
      Frame

Labelled container
        ↓
   LabelFrame

Dropdown menu
        ↓
   Menubutton

Multiline wrapped display
        ↓
     Message
```

---

# Course Summary

This course introduced **GUI programming in Python using Tkinter**.

The major topics covered were:

* Python GUI programming.
* Tkinter as the standard GUI library for Python.
* wxPython as an alternative Python GUI interface.
* Jython for Python support on the Java platform.
* Creating a Tkinter root window.
* Creating and configuring widgets.
* Using the `mainloop()` method.
* Understanding the `master` parameter.
* Using the `pack()` method.
* **Button** widgets for interactive buttons.
* **Canvas** widgets for graphical drawing.
* Canvas functions such as:

  * `create_arc()`
  * `create_image()`
  * `create_line()`
  * `create_oval()`
* **Checkbutton** widgets for multiple selections.
* **Entry** widgets for single-line text input.
* **Frame** widgets for grouping and organizing widgets.
* **Label** widgets for displaying text or images.
* **Listbox** widgets for displaying selectable lists.
* **Menubutton** widgets for dropdown menus.
* **Message** widgets for multiline wrapped text.
* **Radiobutton** widgets for single-choice selections.
* **Scale** widgets for graphical sliders.
* **Text** widgets for multiline editable and formatted text.
* **Spinbox** widgets for fixed-value selection.
* **LabelFrame** widgets for labelled containers.
* Handling user interaction with widgets.
* Organizing widgets into a hierarchical GUI structure.

The overall Tkinter workflow can be summarized as:

```text
Import Tkinter
       ↓
Create Root Window
       ↓
Create Variables
       ↓
Create Widgets
       ↓
Configure Widgets
       ↓
Place Widgets
       ↓
Handle User Interaction
       ↓
Start mainloop()
```

After completing the course, you should be able to understand how to use Tkinter in Python programming, create a root window, instantiate different Tkinter widgets, configure widget parameters, organize widgets, and build interactive GUI applications.

---

# Course Files

```text
10-Getting-Started-with-Tkinter-GUI-Interface/
├── lecture.md
├── assessment.md
└── certificate.pdf
```
