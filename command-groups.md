# Command groups

## Subshell

	(list)

	Evaluate list of commands in a subshell, meaning that its environment is distinct
	from the current shell and its parameters are contained.

	> This actually launches a new instance of bash and any variables that are created
	  or stored in the subshell are gone completely once the subshell is finished.

	```
	unset x; (x=hello; echo $x); echo $x
	```

	> If we run this we'll have two lines print to the screen, hello and a new line

	> This is because x was defined in the subshell and when it died, so did x 

	> When we echo x outside the subshell it has no value so prints a new line

## Group command

	{ list; }

	Evaluate list of commands in the current shell, sharing the current shell's 
	environment.

	> The spaces and trailing semicolon are obligatory

	> Without them, bash won't know if you mean group command or brace expansion
	  and by default it will assume brace expansion

	```
	unset x; { x=hello; echo $x; }; echo $x
	```

	> This will echo hello twice because the variable is retained within the current shell

> $$ is a special parameter that returns the pid of your current shell

> Backticks do the same thing as the $() but become very unweildy when trying to nest them

> Special case: 

	```
	echo "$(</etc/os-release)"
	```
	> There is no command inside this subshell

	> This will take the contents of the file we're pointing to and interpolate that directly 
	  on the command line

	> It's sort of a poor man's cat
