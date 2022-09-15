# Command and Process Substitution

## Command substitution

	Replace the command substitution in-line with the output of its subshell

		$(list)

	> Will run the command list and replace itself with the output generated by
	  the commands

## Process substitution

	Replace the process substitution with a file descriptor which is connected
	to the input or output of the subshell

		>(list) <(list)

	> Takes that output and puts that into a named pipe with a file descriptor

	> This is a way to have something act like a file that is actually a command 
	  that you're running.

	> The files contents are the output of that command

	> These do run in subshell but that is often not important because you're not
	  trying to set variables here, rather build input for something else