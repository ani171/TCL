# Tool Command Language

* Tcl (Tool Command Language) is a dynamic scripting language designed for rapid prototyping, scripted applications, and creating embedded command languages.

### Installation (Ubuntu)
Use the following command to install Tcl
`sudo apt-get install tcl`
![image](https://github.com/ani171/TCL/assets/97838595/c1116b37-d55e-450a-b4e1-db6988b31d7c)

### Verification
After installation, verify Tcl is installed correctly by running <br>
`tclsh` <br>
![image](https://github.com/ani171/TCL/assets/97838595/4620e1f5-c9aa-4ad0-99dd-5e2fd324b195)
You should see the Tcl shell prompt (%), indicating Tcl is ready to use. <br>

### Tcl Man pages
* Man pages provide essential documentation for commands and software packages directly accessible from the terminal. While Tcl's core man pages might be included with its installation, ensuring you have comprehensive documentation available locally can be beneficial for understanding commands, syntax, and Tcl features.
* Before installing or updating Tcl man pages, check if they are already available:
`man tclsh`
![image](https://github.com/ani171/TCL/assets/97838595/6f6a193d-6c86-43d4-8e2a-2f65329feee4)
* If the man pages are not installed or you want to ensure full documentation, follow these steps:
    * The Tcl documentation package may not always be installed by default. To install it <br>
     `sudo apt-get install tcl-doc` <br>
      This package includes man pages and other documentation files. <br>
      ![image](https://github.com/ani171/TCL/assets/97838595/953cda1a-98b1-45fb-b571-712536fe6461)

### Variables in Tcl

* The set command is used for creating and modifying variables in Tcl. It assigns a value to a variable
   * Syntax `set variableName value`
* The puts command outputs data to the standard output, typically the terminal or console. <br>

`set money 1900` <br>
* Tcl creates a variable named money and assigns it the value 1900. If money already exists, it updates its value to 1900
`puts money is = $money` <br>
* Tcl outputs the string money is = followed by the value of money (which is 1900)
![image](https://github.com/ani171/TCL/assets/97838595/da40758b-5629-4a3e-9e10-70653947a193)

```
set a 10;\
set b [expr $a +5];\
puts "a=$a and b=$b"
```
* square brackets [ ] are used for command substitution. This means the command inside the brackets is executed first, and its result is used in place of the bracketed expression.

```
unset a
puts "a=$a and b=$b
```
* Now value of a is completely undefined
![image](https://github.com/ani171/TCL/assets/97838595/1ad9b824-9995-4c0e-9271-94818d5f3d1b)

```
if {![info exists a]}{
set a 50
}
```
* `info exists` checks if a variable exists
* `!condition` used to check if the condition is not true
![image](https://github.com/ani171/TCL/assets/97838595/e8221f1b-d7bf-448c-b28c-df9cec9f1c33)

### If-else 

```
set num -5
if {$num > 0} {
    puts "$num is positive."
} elseif {$num < 0} {
    puts "$num is negative."
} else {
    puts "$num is zero."
}
```
