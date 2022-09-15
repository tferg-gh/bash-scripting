# Redirection

> Controlling the input, output, error, and other streams

	list > file
	
	Overwrite/create file with output from list

	list >| file

	Force overwrite/create file with output from list (Useful on MacOS)

	list >> file

	Append/create file with output from list

	list < file

	Feed file to list as input

	list1 | list2 

	Use output from list1 as input to list2

> If not specified, fd 1 (STDOUT) is assumed when redirecting output.

> Alternative file descriptors may be specified by prepending the fd number,

  	e.g. 2> file to redirect fd 2 (STDERR).

> To refirect to a file descriptor, append '&' and the fd number,
  
  	e.g. 2>&1 to redirect STDERR to the current target for STDOUT
