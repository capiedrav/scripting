# Scripting - Automation with Bash, PowerShell and Python

## Chapter 3 - Bash and Zsh

### 3.3.1 Operating the Terminal

#### Keyboard Shortcuts

![](./images/table3.1.png)
![](./images/table3.1b.png)

### 3.3.2 Online Help

```man <command>``` displays a longer info text for many commands. Thus, ```man ls``` explains
how to use the ```ls``` command and what options are available. You can navigate through
the multi-page text using the cursor keys. The space bar scrolls down an entire page.
Using **/** you can search for an expression in the help text. **N** jumps to the next
search result if necessary, and **Q** closes the help interface.

### 3.5.1 Hash Bang (Shebang)

The first line of a script to be executed on Linux or macOS must start with the characters, **#** (“hash” or “sharp”)
and **!** (“bang”) as well as the path of the interpreter. “Shebang”
is a linguistic shortening of “sharp bang.”

On Linux, the Bash program is predominantly installed in the /bin directory. Thus, a
Bash script starts with the following line:

```#!/bin/bash```

If you want your script to work regardless of whether Bash or Zsh is available, the following hash bang will get 
you there:

```#!/bin/sh```

### 3.7.1 Redirecting Input and Output

#### Operators for Redirecting Input and Output

![](./images/table3.2.png)

### 3.8 Globbing, Brace Extension, and Handling File and Directory Names

#### Globbing Characters

![](./images/table3.3.png)

### 3.8.3 Brace Extension

In Bash, you can formulate enumerations separated by commas or ranges created via
```..``` in curly brackets. Before the command gets executed, all possible combinations are
created, so the expression specified in parentheses is “expanded.” Unlike globbing, however, the brace extension does not consider whether corresponding files already
exist or not. The easiest way to understand the mechanism is by looking at some examples:

![](./images/brace-extension-examples.png)

### 3.9.3 Performing Calculations in Bash

Bash “thinks” in terms of character strings. Calculations or the analysis of mathematical expressions are only possible in a special context using ```let``` 
or within double parentheses (see Table). All mathematical calculations use only integers as a matter of principle.

![](./images/table3.5.png)
![](./images/note1.png)

The following lines contain some examples of mathematical expressions in Bash. In the process, some otherwise common rules have been softened. For example, within
```((...))```, assignments also work with spaces before and after ```=```. (But not with ```let```!) In
addition, you are permitted to omit the preceding ```$``` character when reading variables.

![](./images/examples-of-math-in-bash.png)

### 3.9.4 Arrays

Besides simple variables, Bash also can deal with arrays. Ordinary arrays use integers as
index. Note the ```${field(n)}``` syntax for accessing the *nth* element, which differs from
many other programming languages.

![](./images/examples-of-arrays-in-bash.png)

### 3.9.5 Predefined Variables

Bash scripts can access predefined variables (see Table). These variables can only be
read, but not changed. The abbreviation *PID* stands for process ID (i.e., the internal process number).

![](./images/table3.6.png)
