# Dev10-Plate-Stacking
Prework submission to Dev10 for talent selection. 

## Instructions 
> Goal

Stack plates, one on top of another. A larger plate cannot be stacked on top of a smaller plate. Plates are ordered from the largest at the bottom, to the smallest at the top.

The plate "stack" is represented as a Python list. The bottom plate is the first index. The stack can grow to any size. A plate is represented by a positive integer, which is also the plate's size.

> High Level Requirements

    Add a plate: add a plate to the top of the stack.
    Print plates: display the stack of plates in the terminal.
    Remove plates: remove 1-to-n plates from the top of the stack.

> Sample UI

Use the following as inspiration. Your UI is not required to be identical.
Main Menu

Menu
================
0. [Exit]       
1. Add a plate  
2. Print plates 
3. Remove plates
Select [0-3]:

Add a Plate
Success

Add a plate
===========
Enter a plate size: 10
Success!

Error

Add a plate
===========
Enter a plate size: 12
Cannot place a plate of size 12 on top of another plate of size 10.

Print Plates
Standard

Print plates
============
5
7
10
10

Fancier

Print plates
============
  #####
 #######
##########
##########

No plates.

Print plates
============
There are no stacked plates.

Remove Plates
Success

Remove plates
=============
How many plates to remove?: 2
Success!

Error

Remove plates
=============
How many plates to remove?: 4
Cannot remove more than 2 plates. You chose 4.

Exit

Menu
====
0. [Exit]
1. Add a plate
2. Print plates
3. Remove plates
Select [1-3]: 0
Goodbye!

> Requirements
Add a Plate

Add a plate to the top of the stack. Plates are represented by a positive integer. If the plate is less than or equal to zero, issue a warning and don't add the plate.

If there are no plates on the stack, add it.

The plate "below" must be greater than or equal to the current plate size. If the current plate is too big, issue a warning and don't add the plate. If not, add it to the top of the stack.

Example

This list (plate stack) is valid: [9, 9, 8, 5, 1]. The size of the bottom plate is always greater than or equal to the plate on top of it.

This list (plate stack) is invalid: [9, 5, 8, 9, 1]. We never allow a larger plate to be placed on top of a smaller plate.
Print Plates

Prints plates to the terminal.

Plates should stack vertically, with the largest plate on the bottom and the smallest plate on the top.

If there are no plates, display a message.
Remove Plates

Remove a given number of plates from the top of the stack. The value should be a positive integer. If the value is less than or equal to zero, reject the operation and issue a warning.

If there are too many plates selected, reject the operation and issue a warning. Otherwise, remove plates from the stack and print a message.
Technical Requirements

    Use a Python list to track plates. Don't define the list inside a function. Keep it at file scope.
    Each menu item should be a function. You can add additional utility functions as well. (This isn't a hard requirement. You can solve the problem any way you see fit.)
    To collect positive integers from the user, convert the string value from the input function to an integer using the int function.

Approach

Plan before you write code.

Your plan can be a list of steps for each UI scenario and how they relate to the main menu. It can be some sort of pseudocode describing each scenario. If you prefer a more spatial plan, consider flowcharts. The important thing is that you start with a solid plan before you write your first line of code.

Answer these questions:

    What are the steps?
    What is the step sequence?
    Which decisions need to be made?
    What repeats (loops)?
    What data is needed?
    Which data types are appropriate?
    Does creating a function simplify the problem?

Struggles

If you struggle with this project, it might help to go back and complete any of the optional exercises that you skipped.

If you completed the optional exercises, watch the wrap-up video. The wrap-up video has parallels:

    dogs = [] -> plates = []
    add_dog function -> add_plate
    display_dogs function -> display_plates
    remove_dog function -> remove_plates
    run function with menu -> run function with menu

# Planning 
High-level plan (this is what you’d write before coding)

## Main loop

Print menu

Ask user for choice

Call the appropriate function

Repeat until exit

## Add plate

Ask for plate size

Convert input to int

If <= 0 → error

If stack empty → append

Else:

Compare with top plate

If larger → reject

Else → append

## Print plates

If stack empty → message

Else:

Print from top to bottom

Optionally render visually

## Remove plates

Ask how many to remove

Convert to int

If <= 0 → error

If greater than stack length → error

Else → remove using loop or slicing
