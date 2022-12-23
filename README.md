This project is about creating simple shell. It is written and documented by Yvonne Manuni and Wilfred Lagat.
Write a simple UNIX command interpreter.







^ “The Gates of Shell”, by Spencer Cheng, featuring Julien Barbier

Output

Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.

The only difference is when you print an error, the name of the program must be equivalen

	Example of error with sh:



	$ echo "qwerty" | /bin/sh

	/bin/sh: 1: qwerty: not found

	$ echo "qwerty" | /bin/../bin/sh

	/bin/../bin/sh: 1: qwerty: not found

	$

	Same error with your program hsh:



	$ echo "qwerty" | ./hsh

	./hsh: 1: qwerty: not found

	$ echo "qwerty" | ./././hsh

	./././hsh: 1: qwerty: not found

	$


Compilation
My shell will be compiled this way:



	gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh

Testing

My shell should work like this in interactive mode:



	$ ./hsh

	($) /bin/ls

	hsh main.c shell.c

	($)

	($) exit

	$

	But also in non-interactive mode:



	$ echo "/bin/ls" | ./hsh

	hsh main.c shell.c test_ls_2

	$

	$ cat test_ls_2

	/bin/ls

	/bin/ls

	$

	$ cat test_ls_2 | ./hsh
