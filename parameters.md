# Parameters

## Positional Parameter

	$1 $2 $3 $4 $5 $6 $7 $8 $9 ${10} ...

	Parameters passed to command, encapsulating words on the command line
	as arguments

	> You need to add curly braces around anything above $9 otherwise bash
	  will interpret it as $1 and append 0 on the end.

## Special Parameters

	$* $@ $# $- $$ $0 $! $? $_

	Parameters providing information about positional parameters, the current 
	shell, and the previous command.

## Variables

	name=string

	Parameters which may be assigned values by the user. There are also some
	special shell variables which may provide information, toggle shell options,
	or configure certain features

	> For variable assignment, "=" must not have adjacent spaces.
