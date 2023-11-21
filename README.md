# 42_get_next_line
## What is get_next_line?
This is a project that is part of the 42 common core curriculum.  
The purpose is to develop a program that reads a line from a file descriptor and returns it.  
In the bonus part, we essentially need to be able to do this with more than one file descriptor without losing the value of the last one.
For more details, read the subject.

## Files within the project
Please note, while reading the subject, that we have some limitations.
For this project, the subject asks for 3 files:
- get_next_line.c -> Contains the main function and some auxiliaries.
- get_next_line_utils.c -> Contains more auxiliaries.
- get_next_line.h -> Header of the functions.
For the bonus part is basically the same, only changing the name of the files with a _bonut at the end.

## How does the algorithm work?
Below, I have a simple diagram that illustrates the workflow and explains the functioning of the algorithm.
![Workflow](workflow.jpg)

## Bonus part
For the bonus part, the solution remains essentially the same. However, a crucial enhancement involves defining the static variable as an array. This ensures that the last value from a specific file descriptor (fd) is preserved when calling the function for another. This modification to the static variable within the code guarantees consistent behavior.
